import xml.etree.ElementTree as ET
import uuid
import random
import math

# --- Configuration ---
# Input and output file names
input_file = "Mazda787B.xml"
output_file = "regenerated.xml"

# Parameters for pitch curve generation
START_RPM = 1000
END_RPM = 10000
# How many points to generate on each side of the current RPM
NUM_POINTS_AROUND_CURRENT = 3
# How far apart (in RPM) the generated points should be
POINT_DISTANCE = 50


# --- Helper Functions ---

def get_current_rpm(sound_name):
    """
    Derives the 'current RPM' value from a sound file name.
    - "rpm" -> 1000
    - "rpm-001" -> 1100
    - "rpm-080" -> 9000
    """

    if sound_name.startswith("OnLoadRPM-"):
        try:
            # Extracts the number from "rpm-xxx"
            number_part = int(sound_name.split('-')[1])
            return 1000.0 + (number_part * 100.0)
        except (ValueError, IndexError):
            # Fallback for unexpected formats
            print(f"Warning: Could not parse RPM from '{sound_name}'. Defaulting to 1000.")
            return 1000.0
    # Default for any other name format
    return 1000.0

def generate_pitch_points(current_rpm, start_rpm, end_rpm, num_between, distance):
    """
    Generates the XML string for the <PointList> of a pitch curve.
    """
    # Use a set to automatically handle duplicate RPM values
    x_positions = {float(start_rpm), float(end_rpm)}

    # Add the central point (the sound's actual RPM) if it's within the main range
    if start_rpm < current_rpm < end_rpm:
        x_positions.add(float(current_rpm))

    # Generate points around the current RPM
    for i in range(1, num_between + 1):
        # Point to the left (lower RPM)
        left_point = float(current_rpm - (i * distance))
        if left_point > start_rpm:
            x_positions.add(left_point)

        # Point to the right (higher RPM)
        right_point = float(current_rpm + (i * distance))
        if right_point < end_rpm:
            x_positions.add(right_point)

    # Sort points by RPM value
    sorted_x = sorted(list(x_positions))

    point_xml_parts = []
    total_points = len(sorted_x)

    # Create the XML for each point
    for i, x_pos in enumerate(sorted_x):
        # Avoid math errors with log(0) or division by zero
        if x_pos <= 0 or current_rpm <= 0:
            y_pos = 0
        else:
            # Calculate pitch in cents: 1200 * log2(target_freq / base_freq)
            y_pos = round(1200 * math.log2(x_pos / current_rpm))

        # Set flags: 5 for the first point, 37 for the last, 0 for others
        if i == 0:
            flags = 5
        elif i == total_points - 1:
            flags = 37
        else:
            flags = 0

        # Format the XML for a single point with proper indentation
        point_xml = (
            f'{" " * 24}<Point>\n'
            f'{" " * 32}<XPos>{x_pos}</XPos>\n'
            f'{" " * 32}<YPos>{y_pos}</YPos>\n'
            f'{" " * 32}<Flags>{flags}</Flags>\n'
            f'{" " * 24}</Point>'
        )
        point_xml_parts.append(point_xml)

    # Join all point XML blocks into a single string
    return "\n".join(point_xml_parts)


# --- Main Script ---

# Parse XML from file
try:
    tree = ET.parse(input_file)
    root = tree.getroot()
except FileNotFoundError:
    print(f"Error: Input file '{input_file}' not found.")
    exit()
except ET.ParseError:
    print(f"Error: Could not parse XML from '{input_file}'. Check if it's a valid XML file.")
    exit()


# Template for regenerated Sound elements
template = """
  <Sound Name="{sound_name}" ID="{sound_id}" ShortID="{sound_short_id}">
    <PropertyList>
        <Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
    </PropertyList>
    <ReferenceList>
        <Reference Name="Conversion">
            <ObjectRef Name="Default Conversion Settings" ID="{{6D1B890C-9826-4384-BF07-C15223E9FB56}}" WorkUnitID="{{85E5CEB6-E4D7-4003-A9DA-3DE3C4DDB4EE}}"/>
        </Reference>
        <Reference Name="OutputBus">
            <ObjectRef Name="Main Audio Bus" ID="{{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}}" WorkUnitID="{{BB97648F-0961-445F-A6FD-4DC61EA3CC4B}}"/>
        </Reference>
    </ReferenceList>
    <ChildrenList>
        <AudioFileSource Name="{sound_name}" ID="{audio_source_id}">
            <Language>SFX</Language>
            <AudioFile>{audio_file_name}</AudioFile>
            <MediaIDList>
                <MediaID ID="{media_id}"/>
            </MediaIDList>
        </AudioFileSource>
    </ChildrenList>
    <ObjectLists>
        <ObjectList Name="RTPC">
            <RTPC Name="" ID="{rtpc_pitch_id}" ShortID="{rtpc_pitch_short_id}">
                <PropertyList>
                    <Property Name="PropertyName" Type="string" Value="Pitch"/>
                </PropertyList>
                <ReferenceList>
                    <Reference Name="ControlInput">
                        <ObjectRef Name="RPM" ID="{{E5B0C6F5-BD9B-462D-9AFF-9C0CC742CF4B}}" WorkUnitID="{{3C7A61F0-33B5-402E-8074-3C0ADBF36EF3}}"/>
                    </Reference>
                    <Reference Name="Curve">
                        <Custom>
                            <Curve Name="" ID="{curve_pitch_id}">
                                <PropertyList>
                                    <Property Name="Flags" Type="int32" Value="65537"/>
                                </PropertyList>
                                <PointList>
                                {pitch_points}
                                </PointList>
                            </Curve>
                        </Custom>
                    </Reference>
                </ReferenceList>
            </RTPC>
        </ObjectList>
    </ObjectLists>
    <ActiveSourceList>
        <ActiveSource Name="{sound_name}" ID="{audio_source_id}" Platform="Linked"/>
    </ActiveSourceList>
  </Sound>"""

output_sounds = []

# Find ALL <Sound> tags in the document, no matter how deep
for sound in root.findall(".//Sound"):
    sound_name = sound.get("Name")
    if sound_name.startswith("OnLoadRPM-"):
      sound_id = sound.get("ID")
      sound_short_id = sound.get("ShortID")

      # Some <Sound> might not have AudioFileSource, so check before using
      audio_source = sound.find("./ChildrenList/AudioFileSource")
      if audio_source is None:
          continue  # Skip if no audio source found

      audio_source_id = audio_source.get("ID")
      audio_file_name = audio_source.findtext("AudioFile")
      media_id_element = audio_source.find("./MediaIDList/MediaID")
      if media_id_element is None:
          continue # Skip if no MediaID found

      media_id = media_id_element.get("ID")

      # Generate new random IDs for the new elements
      rtpc_pitch_id = f"{{{str(uuid.uuid4()).upper()}}}"
      rtpc_pitch_short_id = random.randint(100_000_000, 999_999_999)
      curve_pitch_id = f"{{{str(uuid.uuid4()).upper()}}}"

      # --- Generate the pitch points ---
      current_rpm = get_current_rpm(sound_name)
      pitch_points = generate_pitch_points(
          current_rpm,
          START_RPM,
          END_RPM,
          NUM_POINTS_AROUND_CURRENT,
          POINT_DISTANCE
      )

      # Populate the template with all the extracted and generated data
      regenerated = template.format(
          sound_name=sound_name,
          sound_id=sound_id,
          sound_short_id=sound_short_id,
          audio_source_id=audio_source_id,
          audio_file_name=audio_file_name,
          media_id=media_id,
          rtpc_pitch_id=rtpc_pitch_id,
          rtpc_pitch_short_id=rtpc_pitch_short_id,
          curve_pitch_id=curve_pitch_id,
          pitch_points=pitch_points
      )

      output_sounds.append(regenerated)


# Write regenerated XML to the output file
with open(output_file, "w", encoding="utf-8") as f:
    f.write("\n\n".join(output_sounds))

print(f" Regenerated XML written to {output_file} with {len(output_sounds)} sounds.")
