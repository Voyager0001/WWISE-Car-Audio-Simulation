import xml.etree.ElementTree as ET
import uuid
import random
import math

# The XML data provided by the user, containing the source sounds.
INPUT_XML_DATA = """
<ChildrenList>
				<Sound Name="rpm" ID="{AF92B137-69E9-4650-BED0-6A10667E448F}" ShortID="542335721">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm" ID="{EAABF85B-C0B1-491D-AE77-E2043E867032}">
							<Language>SFX</Language>
							<AudioFile>rpm.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="5737802"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm" ID="{EAABF85B-C0B1-491D-AE77-E2043E867032}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-001" ID="{EBA18633-66F2-4AA6-BE8D-19309CAC2CE6}" ShortID="103374469">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-001" ID="{FC3AA124-3710-4797-8766-BCF5F0A1AA5B}">
							<Language>SFX</Language>
							<AudioFile>rpm-001.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="583303974"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-001" ID="{FC3AA124-3710-4797-8766-BCF5F0A1AA5B}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-002" ID="{95BBD46A-C122-4771-BA3E-3042214422AD}" ShortID="646318240">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-002" ID="{57C1BDE8-C59D-42C4-8176-0BAC5E760629}">
							<Language>SFX</Language>
							<AudioFile>rpm-002.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="336925111"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-002" ID="{57C1BDE8-C59D-42C4-8176-0BAC5E760629}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-026" ID="{838BE6C5-C2A6-4367-89F1-47A3DCBD337D}" ShortID="466925093">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-026" ID="{A51B6FCC-A2AD-4E80-B565-B118F746FF29}">
							<Language>SFX</Language>
							<AudioFile>rpm-026.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="230369285"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-026" ID="{A51B6FCC-A2AD-4E80-B565-B118F746FF29}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-020" ID="{D26EC0A9-E996-453B-8111-A303C9EBF38E}" ShortID="69754028">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-020" ID="{611DCD04-F630-4C1C-81CF-1791B61BC0ED}">
							<Language>SFX</Language>
							<AudioFile>rpm-020.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="156222088"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-020" ID="{611DCD04-F630-4C1C-81CF-1791B61BC0ED}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-014" ID="{D112FF9A-A247-4A0A-8E5B-36463744F55B}" ShortID="750956782">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-014" ID="{09856511-CE7A-4AC2-83CA-DDC4C8162804}">
							<Language>SFX</Language>
							<AudioFile>rpm-014.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="280302856"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-014" ID="{09856511-CE7A-4AC2-83CA-DDC4C8162804}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-027" ID="{A5144BEF-D8D0-4266-AB83-263E9643A8A0}" ShortID="653050624">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-027" ID="{84B44A4A-BD21-4DF8-8662-C588162FAED9}">
							<Language>SFX</Language>
							<AudioFile>rpm-027.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="370295657"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-027" ID="{84B44A4A-BD21-4DF8-8662-C588162FAED9}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-015" ID="{AF3EFB21-27B1-44FB-9389-60A5C0D4F4A1}" ShortID="419701574">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-015" ID="{FED80F67-33A3-4D60-8A90-F4BF78A1AC80}">
							<Language>SFX</Language>
							<AudioFile>rpm-015.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="206613516"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-015" ID="{FED80F67-33A3-4D60-8A90-F4BF78A1AC80}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-028" ID="{97DC12D1-79A1-4418-8B6A-0A1E3FCD6653}" ShortID="498802547">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-028" ID="{57EEDAE9-E0FD-493F-8196-B88BD5A4BE83}">
							<Language>SFX</Language>
							<AudioFile>rpm-028.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1007248752"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-028" ID="{57EEDAE9-E0FD-493F-8196-B88BD5A4BE83}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-011" ID="{97999658-4C0E-414C-9A23-424D3DAAACC9}" ShortID="487900095">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-011" ID="{5238C377-DAB3-410B-9EB9-63C28C86AB66}">
							<Language>SFX</Language>
							<AudioFile>rpm-011.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="835146160"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-011" ID="{5238C377-DAB3-410B-9EB9-63C28C86AB66}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-029" ID="{5FADE491-F60D-40CD-8B46-612FE7224058}" ShortID="769255139">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-029" ID="{C1847CB5-1725-4F56-965F-EB60C2BFFDB6}">
							<Language>SFX</Language>
							<AudioFile>rpm-029.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="368364421"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-029" ID="{C1847CB5-1725-4F56-965F-EB60C2BFFDB6}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-007" ID="{CE0DCA09-67E1-4708-8F5A-93EF596B6EF2}" ShortID="223509375">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-007" ID="{68AD6E98-49B9-43D5-90D3-17F2535B9120}">
							<Language>SFX</Language>
							<AudioFile>rpm-007.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="743283975"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-007" ID="{68AD6E98-49B9-43D5-90D3-17F2535B9120}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-005" ID="{BA6F9F32-F0C2-4183-9A52-9C4FF074D652}" ShortID="637637219">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-005" ID="{46028708-2D29-42C2-B624-6FE6FC8FC794}">
							<Language>SFX</Language>
							<AudioFile>rpm-005.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="252219714"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-005" ID="{46028708-2D29-42C2-B624-6FE6FC8FC794}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-006" ID="{F137AB19-A12B-46BB-8519-16BB7FBDFD9E}" ShortID="800824135">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-006" ID="{7D2F0468-2E51-4813-A4E7-9C1FD9F1831E}">
							<Language>SFX</Language>
							<AudioFile>rpm-006.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="861853621"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-006" ID="{7D2F0468-2E51-4813-A4E7-9C1FD9F1831E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-021" ID="{E1B6E0AC-A4E1-42A1-94DB-04043362101E}" ShortID="969051807">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-021" ID="{FC481D19-A466-4B86-97D5-328832D68B1A}">
							<Language>SFX</Language>
							<AudioFile>rpm-021.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="787137485"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-021" ID="{FC481D19-A466-4B86-97D5-328832D68B1A}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-022" ID="{8201E95F-6996-457F-AC00-6ACAB544D3AD}" ShortID="52987641">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-022" ID="{9E4B92C9-F978-4E93-94B9-685B985627CB}">
							<Language>SFX</Language>
							<AudioFile>rpm-022.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="278344994"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-022" ID="{9E4B92C9-F978-4E93-94B9-685B985627CB}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-008" ID="{6490FC09-748C-406D-9D06-A75367DD4D29}" ShortID="279342535">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-008" ID="{173CFD6D-B96A-4501-83BB-CA797E52A544}">
							<Language>SFX</Language>
							<AudioFile>rpm-008.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="916171091"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-008" ID="{173CFD6D-B96A-4501-83BB-CA797E52A544}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-025" ID="{BA37161E-0EBC-40D6-9510-629B483DA0AD}" ShortID="523718083">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-025" ID="{78B2FE5A-3901-420A-8C2F-3D73E6A88EE2}">
							<Language>SFX</Language>
							<AudioFile>rpm-025.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="442953090"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-025" ID="{78B2FE5A-3901-420A-8C2F-3D73E6A88EE2}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-019" ID="{B40DA2E6-6246-4123-8187-77EA1D122523}" ShortID="877160471">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-019" ID="{98BE4402-06D8-4288-BB2A-0C46652583C6}">
							<Language>SFX</Language>
							<AudioFile>rpm-019.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="358918977"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-019" ID="{98BE4402-06D8-4288-BB2A-0C46652583C6}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-003" ID="{4224D65E-AD0E-4340-A33C-E090EE08B936}" ShortID="595156196">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-003" ID="{E22193A9-47D4-44B3-A934-97E48298980D}">
							<Language>SFX</Language>
							<AudioFile>rpm-003.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="913501607"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-003" ID="{E22193A9-47D4-44B3-A934-97E48298980D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-046" ID="{7628467D-685E-4F00-BA51-577D4457E4EC}" ShortID="944163449">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-046" ID="{1608A057-F1FA-45EF-9D2B-EF7760B1DE03}">
							<Language>SFX</Language>
							<AudioFile>rpm-046.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="659661881"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-046" ID="{1608A057-F1FA-45EF-9D2B-EF7760B1DE03}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-004" ID="{3CE82E56-F800-49FD-9417-4E2F4CDBAD53}" ShortID="697053450">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-004" ID="{52232EDE-3F07-4FCB-8E7F-C85C7FD5DBBA}">
							<Language>SFX</Language>
							<AudioFile>rpm-004.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="190039620"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-004" ID="{52232EDE-3F07-4FCB-8E7F-C85C7FD5DBBA}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-049" ID="{0798C4FA-6CCC-43F1-88D0-C27CEDF53DA1}" ShortID="19669412">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-049" ID="{85EF1B3F-48AA-47C8-82A5-FF0B7397709C}">
							<Language>SFX</Language>
							<AudioFile>rpm-049.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1021930761"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-049" ID="{85EF1B3F-48AA-47C8-82A5-FF0B7397709C}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-052" ID="{6D61FAF7-E44E-480C-8CC2-79C8C8C9389A}" ShortID="1001379079">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-052" ID="{DC9ED1E5-3C66-4D2C-B866-935EDD4AF2D1}">
							<Language>SFX</Language>
							<AudioFile>rpm-052.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="843453814"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-052" ID="{DC9ED1E5-3C66-4D2C-B866-935EDD4AF2D1}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-012" ID="{605D4ED5-2F1F-4325-A130-2757F54E7C84}" ShortID="278772576">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-012" ID="{42BE642D-47F6-40AF-BECF-23581B04C9BD}">
							<Language>SFX</Language>
							<AudioFile>rpm-012.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1009259306"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-012" ID="{42BE642D-47F6-40AF-BECF-23581B04C9BD}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-061" ID="{C1D97577-1721-4B86-AE5A-84313854C0E8}" ShortID="1022746336">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-061" ID="{588AAF46-5DAD-41F0-9326-C49FA7D771C6}">
							<Language>SFX</Language>
							<AudioFile>rpm-061.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="247417775"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-061" ID="{588AAF46-5DAD-41F0-9326-C49FA7D771C6}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-009" ID="{2D791FE7-8EA4-42A7-89D0-E7524557BDF8}" ShortID="514546812">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-009" ID="{66F33B44-C1ED-48FE-A1F2-45F09FF77B2E}">
							<Language>SFX</Language>
							<AudioFile>rpm-009.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="617848349"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-009" ID="{66F33B44-C1ED-48FE-A1F2-45F09FF77B2E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-058" ID="{AF9FB7E7-37E9-4F19-BF78-AC2AC3745EA6}" ShortID="476692011">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-058" ID="{408B5F8D-4456-43AE-BA11-615EB34C7640}">
							<Language>SFX</Language>
							<AudioFile>rpm-058.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="712604724"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-058" ID="{408B5F8D-4456-43AE-BA11-615EB34C7640}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-017" ID="{CD2D951A-9E81-42A6-AC11-65B15C0283EE}" ShortID="751511039">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-017" ID="{04FA3E5D-4990-476F-9CA4-567074096609}">
							<Language>SFX</Language>
							<AudioFile>rpm-017.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="179238437"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-017" ID="{04FA3E5D-4990-476F-9CA4-567074096609}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-010" ID="{A58F2530-0841-42A4-989A-4774E3A6781B}" ShortID="873276162">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-010" ID="{7798B0E0-E8D7-43A7-B8C2-D259AF16C676}">
							<Language>SFX</Language>
							<AudioFile>rpm-010.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1012736931"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-010" ID="{7798B0E0-E8D7-43A7-B8C2-D259AF16C676}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-023" ID="{D07BD3D8-D8EA-4660-8203-DC4FC50B4A0D}" ShortID="868190656">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-023" ID="{1C236610-43FE-4467-89CE-6BA5DBAC2444}">
							<Language>SFX</Language>
							<AudioFile>rpm-023.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1017486157"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-023" ID="{1C236610-43FE-4467-89CE-6BA5DBAC2444}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-018" ID="{1C25546E-6510-412C-98F9-9E83866EFB71}" ShortID="976816943">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-018" ID="{E6D8C873-2AAF-4872-A00A-09253B23FBE9}">
							<Language>SFX</Language>
							<AudioFile>rpm-018.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="978110182"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-018" ID="{E6D8C873-2AAF-4872-A00A-09253B23FBE9}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-013" ID="{834ED9E4-8994-41CA-86EB-8F90165A571D}" ShortID="551446606">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-013" ID="{F7123091-343B-4B90-BC46-C9859795EE55}">
							<Language>SFX</Language>
							<AudioFile>rpm-013.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1041748189"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-013" ID="{F7123091-343B-4B90-BC46-C9859795EE55}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-024" ID="{3FB21BB2-FB45-4668-8EAE-7BAF6F105531}" ShortID="275837553">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-024" ID="{9A02F989-B446-41BA-A20D-A6CA6B1D5F44}">
							<Language>SFX</Language>
							<AudioFile>rpm-024.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="830578961"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-024" ID="{9A02F989-B446-41BA-A20D-A6CA6B1D5F44}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-016" ID="{EBA1C438-2B3A-4173-A520-1AE8795BA841}" ShortID="852610252">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-016" ID="{977DAFA9-3D9C-4D25-B8F5-52A33290E20F}">
							<Language>SFX</Language>
							<AudioFile>rpm-016.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="277487563"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-016" ID="{977DAFA9-3D9C-4D25-B8F5-52A33290E20F}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-039" ID="{16CD22B5-C911-4C8F-AB8B-236AD2AB9FCA}" ShortID="788046345">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-039" ID="{2CD41D18-58E5-4480-8171-4C5E39BEC9A4}">
							<Language>SFX</Language>
							<AudioFile>rpm-039.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="509717476"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-039" ID="{2CD41D18-58E5-4480-8171-4C5E39BEC9A4}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-034" ID="{807B166F-C7F4-4DD4-BD71-1548B169CBC2}" ShortID="741173177">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-034" ID="{F6F115DA-86A8-494E-BFB0-8E64707764F5}">
							<Language>SFX</Language>
							<AudioFile>rpm-034.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="271458725"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-034" ID="{F6F115DA-86A8-494E-BFB0-8E64707764F5}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-036" ID="{199E0B2B-6088-4751-BBB5-3D339874B7F3}" ShortID="127394799">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-036" ID="{E9E65558-8B57-43AE-ABAF-60F86D63AC48}">
							<Language>SFX</Language>
							<AudioFile>rpm-036.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="651656111"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-036" ID="{E9E65558-8B57-43AE-ABAF-60F86D63AC48}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-043" ID="{D876B5CF-04B1-4F80-AC10-7A4C01F89769}" ShortID="953121574">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-043" ID="{05D03CDE-F076-4DE5-BF29-C8EF391EA567}">
							<Language>SFX</Language>
							<AudioFile>rpm-043.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="154375524"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-043" ID="{05D03CDE-F076-4DE5-BF29-C8EF391EA567}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-070" ID="{4AA820FE-B16E-4834-A281-CBDC5C34DAFD}" ShortID="347913704">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-070" ID="{A7729CA0-40DF-4E3A-A3B7-13EF07E52BCB}">
							<Language>SFX</Language>
							<AudioFile>rpm-070.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="563752448"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-070" ID="{A7729CA0-40DF-4E3A-A3B7-13EF07E52BCB}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-076" ID="{2FAEB8CC-4D80-4AA9-988A-907E93488588}" ShortID="541031621">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-076" ID="{850A2CC5-2E6B-49C6-83F2-455A858C0855}">
							<Language>SFX</Language>
							<AudioFile>rpm-076.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="529344362"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-076" ID="{850A2CC5-2E6B-49C6-83F2-455A858C0855}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-068" ID="{764CE4B0-36E5-46CB-A2E9-C4BDFD1BFAF1}" ShortID="721427757">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-068" ID="{B997D0CF-DE7D-43CA-88EA-45D00F7919A3}">
							<Language>SFX</Language>
							<AudioFile>rpm-068.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="804459662"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-068" ID="{B997D0CF-DE7D-43CA-88EA-45D00F7919A3}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-030" ID="{6414AC9E-4FCB-4A9D-8940-4FC66FD3E728}" ShortID="758642076">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-030" ID="{998B1D04-72B9-477D-A014-9C229C6C38F9}">
							<Language>SFX</Language>
							<AudioFile>rpm-030.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="791681056"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-030" ID="{998B1D04-72B9-477D-A014-9C229C6C38F9}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-074" ID="{928B2705-4E4F-4884-924E-033210F14496}" ShortID="2074103">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-074" ID="{5D5E55EB-C289-4801-A63E-099B1E53E3E3}">
							<Language>SFX</Language>
							<AudioFile>rpm-074.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="389180162"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-074" ID="{5D5E55EB-C289-4801-A63E-099B1E53E3E3}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-035" ID="{A890842B-7AC5-4CFC-A711-1E8E9B247C9D}" ShortID="809447940">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-035" ID="{6C2F7D1F-FBA0-47EB-99D6-CA86D98F56CE}">
							<Language>SFX</Language>
							<AudioFile>rpm-035.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="396126685"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-035" ID="{6C2F7D1F-FBA0-47EB-99D6-CA86D98F56CE}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-078" ID="{29ADD91F-ABF9-4577-9A99-7929FF0CE437}" ShortID="918189328">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-078" ID="{F84989DC-A6F4-45BD-AB1E-147CA9C8A8E3}">
							<Language>SFX</Language>
							<AudioFile>rpm-078.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="758085116"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-078" ID="{F84989DC-A6F4-45BD-AB1E-147CA9C8A8E3}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-080" ID="{82D57F42-EE9B-424E-A20D-C0D769351575}" ShortID="1030884094">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-080" ID="{137CF056-078A-48A7-B426-D9EB1CCB1901}">
							<Language>SFX</Language>
							<AudioFile>rpm-080.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="540903749"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-080" ID="{137CF056-078A-48A7-B426-D9EB1CCB1901}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-033" ID="{EF033DE1-7055-4739-ADD5-4F8083181A01}" ShortID="231729706">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-033" ID="{31CE9AE7-CB0F-48D6-BB84-EFD2923CFC5D}">
							<Language>SFX</Language>
							<AudioFile>rpm-033.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="387607565"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-033" ID="{31CE9AE7-CB0F-48D6-BB84-EFD2923CFC5D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-073" ID="{AE1C4317-12AE-4BC8-8227-ADA772D52B86}" ShortID="480173261">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-073" ID="{A3ADBEBF-553E-4FD8-B72B-CBBF4DD2AC0D}">
							<Language>SFX</Language>
							<AudioFile>rpm-073.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="210310706"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-073" ID="{A3ADBEBF-553E-4FD8-B72B-CBBF4DD2AC0D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-054" ID="{9D40D242-E107-42A6-87A4-C105F34C5644}" ShortID="519953233">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-054" ID="{A1A53D0D-E7EE-4DF2-94D4-E21F8BAECEE7}">
							<Language>SFX</Language>
							<AudioFile>rpm-054.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="709480232"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-054" ID="{A1A53D0D-E7EE-4DF2-94D4-E21F8BAECEE7}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-075" ID="{4C98F2E4-7104-430B-BD5A-229373C8596C}" ShortID="760829986">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-075" ID="{292480A5-B883-4A25-B06B-0F4E7917DD03}">
							<Language>SFX</Language>
							<AudioFile>rpm-075.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="461099252"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-075" ID="{292480A5-B883-4A25-B06B-0F4E7917DD03}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-063" ID="{E3F527E2-9CCF-4AEC-A728-C6829E6864AA}" ShortID="767100765">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-063" ID="{0F268D6A-9BBC-43A9-805B-21792581FFC5}">
							<Language>SFX</Language>
							<AudioFile>rpm-063.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="87663228"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-063" ID="{0F268D6A-9BBC-43A9-805B-21792581FFC5}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-031" ID="{204AACA5-B716-4443-B4F0-1BDC5C933668}" ShortID="493909225">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-031" ID="{CDE780BE-E3D3-4298-86F0-BF2C6CB72B9B}">
							<Language>SFX</Language>
							<AudioFile>rpm-031.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="858495985"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-031" ID="{CDE780BE-E3D3-4298-86F0-BF2C6CB72B9B}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-048" ID="{0B673A64-50E7-4084-8F44-4091D1C54268}" ShortID="961377088">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-048" ID="{328AB6CF-AA4C-4AAC-96AF-1A59F43AE1FF}">
							<Language>SFX</Language>
							<AudioFile>rpm-048.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1029410210"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-048" ID="{328AB6CF-AA4C-4AAC-96AF-1A59F43AE1FF}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-069" ID="{0DF0C753-66DD-4556-8CFC-DFB5110F5491}" ShortID="240186546">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-069" ID="{BCF80EAB-08CB-4987-ABA2-55E8BA0A2C6E}">
							<Language>SFX</Language>
							<AudioFile>rpm-069.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="494910499"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-069" ID="{BCF80EAB-08CB-4987-ABA2-55E8BA0A2C6E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-055" ID="{05D5A1BA-E5ED-4FD3-8EE3-0EB8FFF89328}" ShortID="492082131">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-055" ID="{9B8896D5-0C28-4C9C-B144-AB3BC14ECCEB}">
							<Language>SFX</Language>
							<AudioFile>rpm-055.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="396352686"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-055" ID="{9B8896D5-0C28-4C9C-B144-AB3BC14ECCEB}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-066" ID="{87CEFE27-74E1-44E3-922D-26E623930C4D}" ShortID="1054145109">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-066" ID="{22B37465-7F76-4EF5-B145-7E94CD2BA6D8}">
							<Language>SFX</Language>
							<AudioFile>rpm-066.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="647484161"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-066" ID="{22B37465-7F76-4EF5-B145-7E94CD2BA6D8}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-050" ID="{EE7C453C-BDBF-4425-85E0-34397928BC9C}" ShortID="511358819">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-050" ID="{6F93B48B-1EE1-4E89-81C2-6D55139E3F3F}">
							<Language>SFX</Language>
							<AudioFile>rpm-050.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="13803639"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-050" ID="{6F93B48B-1EE1-4E89-81C2-6D55139E3F3F}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-042" ID="{65F4B998-00E4-4E47-8573-3A1282FBBF68}" ShortID="613389368">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-042" ID="{462C0B2D-B26D-47C0-9DDA-8AB34D54865E}">
							<Language>SFX</Language>
							<AudioFile>rpm-042.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="516985786"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-042" ID="{462C0B2D-B26D-47C0-9DDA-8AB34D54865E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-051" ID="{6734AB44-5B85-4473-8697-DAEE8F937723}" ShortID="962170433">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-051" ID="{702A5B80-0216-4985-8BEE-D527B229C6E6}">
							<Language>SFX</Language>
							<AudioFile>rpm-051.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="289314735"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-051" ID="{702A5B80-0216-4985-8BEE-D527B229C6E6}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-064" ID="{2271C857-3D63-4FE4-A6DE-0DB232457FE5}" ShortID="682371406">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-064" ID="{78378982-D346-4AF6-A800-DF102FEA5E18}">
							<Language>SFX</Language>
							<AudioFile>rpm-064.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="524562688"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-064" ID="{78378982-D346-4AF6-A800-DF102FEA5E18}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-062" ID="{3326EC83-D0A0-48DC-9B49-DCFC4B0D5FC5}" ShortID="207338416">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-062" ID="{B4817B3C-A898-4E85-B31C-8B1DE12B4C07}">
							<Language>SFX</Language>
							<AudioFile>rpm-062.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="245802808"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-062" ID="{B4817B3C-A898-4E85-B31C-8B1DE12B4C07}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-032" ID="{0C143D48-44DC-431E-9981-25EA68CEC9FC}" ShortID="168438915">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-032" ID="{FB69F5AD-2743-4C27-B0A9-1D415AAB5E20}">
							<Language>SFX</Language>
							<AudioFile>rpm-032.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="92110185"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-032" ID="{FB69F5AD-2743-4C27-B0A9-1D415AAB5E20}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-040" ID="{AEF59DB1-2834-469A-AEAE-09EAB07AD232}" ShortID="215841144">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-040" ID="{8132DD22-492F-4B06-97CE-BFE1A13C7A41}">
							<Language>SFX</Language>
							<AudioFile>rpm-040.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="599076247"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-040" ID="{8132DD22-492F-4B06-97CE-BFE1A13C7A41}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-045" ID="{7525CEC4-AACE-425B-B37D-6EEC0DC8CCEC}" ShortID="889093443">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-045" ID="{5BE37D54-BF52-42D0-9843-6A366D2E194E}">
							<Language>SFX</Language>
							<AudioFile>rpm-045.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="955170639"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-045" ID="{5BE37D54-BF52-42D0-9843-6A366D2E194E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-057" ID="{F0613897-856E-4C3C-ABFF-6803F3551B7C}" ShortID="283468845">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-057" ID="{E62E5381-F420-4033-B7C8-1070A3A37403}">
							<Language>SFX</Language>
							<AudioFile>rpm-057.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="36563204"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-057" ID="{E62E5381-F420-4033-B7C8-1070A3A37403}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-079" ID="{15C36EAE-8CAF-4092-A6CB-159EF5424D26}" ShortID="966870551">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-079" ID="{E54EBD0C-0900-4554-96F8-782FCD0B815D}">
							<Language>SFX</Language>
							<AudioFile>rpm-079.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="4540841"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-079" ID="{E54EBD0C-0900-4554-96F8-782FCD0B815D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-071" ID="{7775BDCB-B1CE-44B4-AF5D-29BF00B4D806}" ShortID="635616469">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-071" ID="{68D42EE1-1B39-49D9-9850-1CD09AB71A2D}">
							<Language>SFX</Language>
							<AudioFile>rpm-071.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="907320155"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-071" ID="{68D42EE1-1B39-49D9-9850-1CD09AB71A2D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-059" ID="{C9A8CA57-3B73-45B4-8FE3-7F176F509C91}" ShortID="809258965">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-059" ID="{263039A0-8EA6-436F-B5E3-AF993C198E2E}">
							<Language>SFX</Language>
							<AudioFile>rpm-059.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="885851331"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-059" ID="{263039A0-8EA6-436F-B5E3-AF993C198E2E}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-072" ID="{38DD4339-740B-4C32-873C-0BEA5813E393}" ShortID="615582524">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-072" ID="{33F303C3-40E3-46AA-82F5-3492016F1281}">
							<Language>SFX</Language>
							<AudioFile>rpm-072.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="454857164"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-072" ID="{33F303C3-40E3-46AA-82F5-3492016F1281}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-053" ID="{02C1A823-1F71-4B4F-B083-A5B79CD3017D}" ShortID="39996321">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-053" ID="{585876F7-D638-4B6C-ABB3-7456166DA645}">
							<Language>SFX</Language>
							<AudioFile>rpm-053.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="761943461"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-053" ID="{585876F7-D638-4B6C-ABB3-7456166DA645}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-037" ID="{58B3D47A-E8AC-40AD-B425-984C4EA6C1B4}" ShortID="634151325">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-037" ID="{6D5EAB2B-0145-491C-996A-41BF9519C795}">
							<Language>SFX</Language>
							<AudioFile>rpm-037.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="256523876"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-037" ID="{6D5EAB2B-0145-491C-996A-41BF9519C795}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-056" ID="{938B4FA3-2316-4C27-ABB5-646452056BFE}" ShortID="276397146">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-056" ID="{07713FAB-1AC0-4F2F-B081-799A2D08A918}">
							<Language>SFX</Language>
							<AudioFile>rpm-056.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1063510791"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-056" ID="{07713FAB-1AC0-4F2F-B081-799A2D08A918}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-060" ID="{442D986D-1809-4419-8FC8-F40ED4C741A9}" ShortID="613229044">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-060" ID="{2ECA206A-FBF7-49F2-94CB-16DACEAA56D9}">
							<Language>SFX</Language>
							<AudioFile>rpm-060.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="442234865"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-060" ID="{2ECA206A-FBF7-49F2-94CB-16DACEAA56D9}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-077" ID="{50AB7907-3151-4662-BFCA-CABF552DEC6D}" ShortID="195101911">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-077" ID="{3FEA9CC8-3EC2-43D6-9D43-ED4D90E30116}">
							<Language>SFX</Language>
							<AudioFile>rpm-077.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="1059669207"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-077" ID="{3FEA9CC8-3EC2-43D6-9D43-ED4D90E30116}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-038" ID="{F6220E2C-EE84-4CB5-A54F-83A0E84BFFFA}" ShortID="915648731">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-038" ID="{38C398F4-A53B-4637-9F42-C864EFCD00EB}">
							<Language>SFX</Language>
							<AudioFile>rpm-038.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="155918875"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-038" ID="{38C398F4-A53B-4637-9F42-C864EFCD00EB}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-065" ID="{EC68CBA7-5FAC-4F46-B2A7-7B68507CC3D7}" ShortID="888927782">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-065" ID="{4132BEDB-BE65-4ECA-A573-5C2247E923DB}">
							<Language>SFX</Language>
							<AudioFile>rpm-065.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="426337631"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-065" ID="{4132BEDB-BE65-4ECA-A573-5C2247E923DB}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-047" ID="{FCBF053E-A837-49C1-ACF8-1B744C02AB9E}" ShortID="362190328">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-047" ID="{802F69D2-1CD7-43C8-9D87-D6F334AF957B}">
							<Language>SFX</Language>
							<AudioFile>rpm-047.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="380270276"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-047" ID="{802F69D2-1CD7-43C8-9D87-D6F334AF957B}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-041" ID="{CC901D64-1DD2-48E3-A1B4-BA3424C85C8B}" ShortID="774544259">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-041" ID="{89088275-A578-4134-B261-ED8159DEA4B6}">
							<Language>SFX</Language>
							<AudioFile>rpm-041.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="250115528"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-041" ID="{89088275-A578-4134-B261-ED8159DEA4B6}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-044" ID="{F1B72C7C-F79D-451C-B773-E4BA31C62C9F}" ShortID="928003552">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-044" ID="{C4CA4992-CBB7-481A-AA79-002EEA6647A4}">
							<Language>SFX</Language>
							<AudioFile>rpm-044.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="185946088"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-044" ID="{C4CA4992-CBB7-481A-AA79-002EEA6647A4}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
				<Sound Name="rpm-067" ID="{CB27E97F-CA9D-4814-965B-E39DC5528FDD}" ShortID="181569997">
					<PropertyList>
						<Property Name="IsLoopingEnabled" Type="bool" Value="True"/>
					</PropertyList>
					<ReferenceList>
						<Reference Name="Conversion">
							<ObjectRef Name="Default Conversion Settings" ID="{6D1B890C-9826-4384-BF07-C15223E9FB56}" WorkUnitID="{4E542F91-11B5-49AA-B157-426F63A391A9}"/>
						</Reference>
						<Reference Name="OutputBus">
							<ObjectRef Name="Main Audio Bus" ID="{1514A4D8-1DA6-412A-A17E-75CA0C2149F3}" WorkUnitID="{CEB3814E-FD24-49BE-80A9-5125DBA050FA}"/>
						</Reference>
					</ReferenceList>
					<ChildrenList>
						<AudioFileSource Name="rpm-067" ID="{7B751E9D-5045-41CE-8218-7B26BE1E819D}">
							<Language>SFX</Language>
							<AudioFile>rpm-067.wav</AudioFile>
							<MediaIDList>
								<MediaID ID="919136368"/>
							</MediaIDList>
						</AudioFileSource>
					</ChildrenList>
					<ActiveSourceList>
						<ActiveSource Name="rpm-067" ID="{7B751E9D-5045-41CE-8218-7B26BE1E819D}" Platform="Linked"/>
					</ActiveSourceList>
				</Sound>
</ChildrenList>
"""

def parse_sound_ids(xml_data):
    """
    Parses an XML string to find all <Sound> elements and extracts their
    Name and ID attributes.

    Args:
        xml_data (str): A string containing the XML structure.

    Returns:
        dict: A dictionary mapping sound names to their corresponding IDs.
              Example: {'rpm': '{...}', 'rpm-001': '{...}'}
    """
    sound_id_map = {}
    # The root element in the provided text is <ChildrenList>, so we start there.
    root = ET.fromstring(xml_data)

    # Use .//Sound to find all Sound tags at any depth below the current element.
    for sound_element in root.findall('.//Sound'):
        name = sound_element.get('Name')
        sound_id = sound_element.get('ID')
        if name and sound_id:
            sound_id_map[name] = sound_id

    return sound_id_map

# --- Function to calculate pitch shift in cents from RPM values ---
def rpm_to_cents(RPM_of_Current_Track, RPM_to_Shift_to):
    """
    Calculates the pitch difference in cents between two RPM values.
    1200 cents = 1 octave (double the frequency).
    """
    if RPM_of_Current_Track <= 0 or RPM_to_Shift_to <= 0:
        raise ValueError("RPM values must be greater than zero.")

    # The core formula for converting a frequency ratio to cents.
    cents = 1200 * math.log2(RPM_to_Shift_to / RPM_of_Current_Track)
    return cents

def generate_blend_track_xml(rpm, sound_name, sound_id):
    """
    Generates a single <BlendTrack> XML block based on a specific RPM value,
    using a mathematical function to calculate pitch values.

    Args:
        rpm (int): The central RPM value for this track (e.g., 1100, 1200).
        sound_name (str): The name of the sound to reference (e.g., "rpm-001").
        sound_id (str): The GUID of the sound to reference.
    """

    # --- Generate unique IDs for every new element ---
    blend_track_id = f"{{{str(uuid.uuid4()).upper()}}}"
    blend_track_short_id = random.randint(100_000_000, 999_999_999)
    rtpc_pitch_id = f"{{{str(uuid.uuid4()).upper()}}}"
    rtpc_pitch_short_id = random.randint(100_000_000, 999_999_999)
    curve_pitch_id = f"{{{str(uuid.uuid4()).upper()}}}"
    rtpc_vol_rpm_id = f"{{{str(uuid.uuid4()).upper()}}}"
    rtpc_vol_rpm_short_id = random.randint(100_000_000, 999_999_999)
    curve_vol_rpm_id = f"{{{str(uuid.uuid4()).upper()}}}"
    rtpc_vol_throttle_id = f"{{{str(uuid.uuid4()).upper()}}}"
    rtpc_vol_throttle_short_id = random.randint(100_000_000, 999_999_999)
    curve_vol_throttle_id = f"{{{str(uuid.uuid4()).upper()}}}"

    # --- Calculate dynamic positions based on the pattern ---
    left_edge_pos = rpm - 50
    right_edge_pos = rpm + 100

    # --- Calculate Pitch Curve points using the provided function ---
    pitch_points = []
    # The X-axis offsets for the pitch curve points remain the same as the original pattern.
    x_offsets = [-50, -30, -10, 0, 20, 40, 60, 80, 100]
    for offset in x_offsets:
        x_pos = rpm + offset
        # Calculate Y-Position (cents) using the function and round to the nearest integer.
        y_pos = round(rpm_to_cents(rpm, x_pos))
        pitch_points.append({'x': x_pos, 'y': y_pos})

    # NOTE: The ObjectRef IDs for "RPM", "Throttle", and their "WorkUnitID" are kept
    # constant, as they refer to the same global game parameters in the audio engine.
    xml_template = f"""
     <BlendTrack Name="{rpm}" ID="{blend_track_id}" ShortID="{blend_track_short_id}">
       <PropertyList>
         <Property Name="EnableCrossFading" Type="bool" Value="True"/>
       </PropertyList>
       <ReferenceList>
         <Reference Name="LayerCrossFadeControlInput">
           <ObjectRef Name="RPM" ID="{{7A793AE3-B8C6-4F7E-9967-671BE62D90C5}}" WorkUnitID="{{2AD4B559-C66F-4D92-94D4-E08C1FB8FC54}}"/>
         </Reference>
       </ReferenceList>
       <ObjectLists>
         <ObjectList Name="RTPC">
           <RTPC Name="" ID="{rtpc_pitch_id}" ShortID="{rtpc_pitch_short_id}">
             <PropertyList>
               <Property Name="PropertyName" Type="string" Value="Pitch"/>
             </PropertyList>
             <ReferenceList>
               <Reference Name="ControlInput">
                 <ObjectRef Name="RPM" ID="{{7A793AE3-B8C6-4F7E-9967-671BE62D90C5}}" WorkUnitID="{{2AD4B559-C66F-4D92-94D4-E08C1FB8FC54}}"/>
               </Reference>
               <Reference Name="Curve">
                 <Custom>
                   <Curve Name="" ID="{curve_pitch_id}">
                     <PropertyList>
                       <Property Name="Flags" Type="int32" Value="65537"/>
                     </PropertyList>
                     <PointList>
                       <Point>
                         <XPos>1000</XPos>
                         <YPos>0</YPos>
                         <Flags>5</Flags>
                         <SegmentShape>Constant</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[0]['x']}</XPos>
                         <YPos>{pitch_points[0]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[1]['x']}</XPos>
                         <YPos>{pitch_points[1]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[2]['x']}</XPos>
                         <YPos>{pitch_points[2]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[3]['x']}</XPos>
                         <YPos>{pitch_points[3]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[4]['x']}</XPos>
                         <YPos>{pitch_points[4]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[5]['x']}</XPos>
                         <YPos>{pitch_points[5]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[6]['x']}</XPos>
                         <YPos>{pitch_points[6]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[7]['x']}</XPos>
                         <YPos>{pitch_points[7]['y']}</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{pitch_points[8]['x']}</XPos>
                         <YPos>{pitch_points[8]['y']}</YPos>
                         <Flags>0</Flags>
                         <SegmentShape>Constant</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>9000</XPos>
                         <YPos>0</YPos>
                         <Flags>37</Flags>
                       </Point>
                     </PointList>
                   </Curve>
                 </Custom>
               </Reference>
             </ReferenceList>
           </RTPC>
           <RTPC Name="" ID="{rtpc_vol_rpm_id}" ShortID="{rtpc_vol_rpm_short_id}">
             <PropertyList>
               <Property Name="PropertyName" Type="string" Value="Volume"/>
             </PropertyList>
             <ReferenceList>
               <Reference Name="ControlInput">
                 <ObjectRef Name="RPM" ID="{{7A793AE3-B8C6-4F7E-9967-671BE62D90C5}}" WorkUnitID="{{2AD4B559-C66F-4D92-94D4-E08C1FB8FC54}}"/>
               </Reference>
               <Reference Name="Curve">
                 <Custom>
                   <Curve Name="" ID="{curve_vol_rpm_id}">
                     <PropertyList>
                       <Property Name="Flags" Type="int32" Value="3"/>
                     </PropertyList>
                     <PointList>
                       <Point>
                         <XPos>1000</XPos>
                         <YPos>0</YPos>
                         <Flags>5</Flags>
                         <SegmentShape>Constant</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>1000.001</XPos>
                         <YPos>-200</YPos>
                         <Flags>0</Flags>
                         <SegmentShape>Constant</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>{rpm - 50}</XPos>
                         <YPos>-200</YPos>
                         <Flags>0</Flags>
                         <SegmentShape>Log2</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>{rpm}</XPos>
                         <YPos>0</YPos>
                         <Flags>0</Flags>
                       </Point>
                       <Point>
                         <XPos>{rpm + 50}</XPos>
                         <YPos>0</YPos>
                         <Flags>0</Flags>
                         <SegmentShape>Exp2</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>{rpm + 100}</XPos>
                         <YPos>-200</YPos>
                         <Flags>0</Flags>
                         <SegmentShape>Constant</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>9000</XPos>
                         <YPos>0</YPos>
                         <Flags>37</Flags>
                       </Point>
                     </PointList>
                   </Curve>
                 </Custom>
               </Reference>
             </ReferenceList>
           </RTPC>
           <RTPC Name="" ID="{rtpc_vol_throttle_id}" ShortID="{rtpc_vol_throttle_short_id}">
             <PropertyList>
               <Property Name="PropertyName" Type="string" Value="Volume"/>
             </PropertyList>
             <ReferenceList>
               <Reference Name="ControlInput">
                 <ObjectRef Name="Throttle" ID="{{250EB65B-767F-4B2E-A1E8-0BC405EC66BD}}" WorkUnitID="{{2AD4B559-C66F-4D92-94D4-E08C1FB8FC54}}"/>
               </Reference>
               <Reference Name="Curve">
                 <Custom>
                   <Curve Name="" ID="{curve_vol_throttle_id}">
                     <PropertyList>
                       <Property Name="Flags" Type="int32" Value="3"/>
                     </PropertyList>
                     <PointList>
                       <Point>
                         <XPos>0</XPos>
                         <YPos>0</YPos>
                         <Flags>5</Flags>
                         <SegmentShape>Exp2</SegmentShape>
                       </Point>
                       <Point>
                         <XPos>1</XPos>
                         <YPos>-200</YPos>
                         <Flags>37</Flags>
                       </Point>
                     </PointList>
                   </Curve>
                 </Custom>
               </Reference>
             </ReferenceList>
           </RTPC>
         </ObjectList>
       </ObjectLists>
       <BlendTrackAssocList>
         <BlendTrackAssoc>
           <ItemRef Name="{sound_name}" ID="{sound_id}"/>
           <CrossfadingInfo>
             <LeftEdgePos>{left_edge_pos}</LeftEdgePos>
             <LeftFadingMode>Automatic</LeftFadingMode>
             <RightEdgePos>{right_edge_pos}</RightEdgePos>
             <RightFadingMode>Automatic</RightFadingMode>
           </CrossfadingInfo>
         </BlendTrackAssoc>
       </BlendTrackAssocList>
     </BlendTrack>"""
    return xml_template

# --- Main Generation Loop ---
if __name__ == "__main__":
    # 1. Parse the input XML to get a map of sound names to their IDs
    sound_data_map = parse_sound_ids(INPUT_XML_DATA)

    # Sort the items by name to ensure a consistent processing order
    # This gives a list of (name, id) tuples, e.g., [('rpm', '{...}'), ('rpm-001', '{...}')]
    sorted_sound_items = sorted(sound_data_map.items())

    # 2. Define the RPM generation parameters
    start_rpm = 1100
    end_rpm = 9000
    increment = 100

    # 3. Loop through the *parsed sounds* instead of a generic range
    # The loop will only run as many times as there are sounds available.
    for i, (sound_name, sound_id) in enumerate(sorted_sound_items):
        # Calculate the RPM for the current track based on its index
        current_rpm = start_rpm + ((i-1) * increment)

        # Optional: Stop if the calculated RPM exceeds the defined maximum
        if current_rpm > end_rpm:
            print(f"--- INFO: Reached max RPM of {end_rpm}. Stopping generation. ---")
            break

        # Generate the XML block using the calculated RPM and the parsed sound info
        xml_output = generate_blend_track_xml(current_rpm, sound_name, sound_id)
        print(xml_output)

        # Print a blank line between entries for readability
        if i < len(sorted_sound_items) - 1:
            print()
