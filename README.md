MASS-CASUALTY INCIDENT COMMANDER SIMULATOR
Installation and Startup Guide — Windows 64-bit

Current language: Hebrew. An English version will be released soon.

1. SET UP GODOT 3.5.1
Extract the supplied ZIP package to a folder on your computer. It contains
four main folders:
- Godot: the supplied Godot 3.5.1 engine.
- MCISimulationWithResources: the simulator project and its resources.
- ParticipantsData: the working folder where simulation data is saved.
- ParticipantsData_Clean: a clean backup of the data-folder structure.
Open the Godot folder and launch the included Godot_v3.5.1-stable_win64
executable. Godot can run directly from this folder; a separate installation wizard is not required. Use this supplied
version and do not convert the project to Godot 4.

2. IMPORT THE SIMULATOR PROJECT
Launch Godot from the Godot folder. In the Project Manager, select Import
and choose MCISimulationWithResources/project.godot inside the extracted package. Import and open the project. Keep the
project's files and subfolders together, and allow Godot to finish importing
its resources before continuing.

3. CONFIGURE THE PARTICIPANT OUTPUT FOLDERS
Use ParticipantsData as the active output folder. Preserve its supplied
subfolders for FirstPhase, SecondPhase and ThirdPhase.

ParticipantsData_Clean is the clean backup version. Keep it unchanged and do
not point any saving paths to it. To start again with a clean data folder,
first close the simulator and archive your existing ParticipantsData folder.
Then copy ParticipantsData_Clean and name the new working copy ParticipantsData.

The examples below assume you extracted the package into C:/MCI_Simulator.
Replace C:/MCI_Simulator with the ACTUAL absolute path on your computer.
Your active data folder would then be C:/MCI_Simulator/ParticipantsData.

Most original paths already contain ParticipantsData: replace their old prefix
with the full path to your working ParticipantsData folder, keeping the rest.
Five references instead use TestData or CasualtiesData. To keep their outputs
under ParticipantsData too, create these additional subfolders if absent:
- ParticipantsData/TestData
- ParticipantsData/CasualtiesData
These two subfolders are proposed destinations for the legacy paths; they are
not confirmed contents of the supplied clean folder.

All script filenames are
relative to MCISimulationWithResources, the project folder containing
project.godot. For example, FirstPhasePanel.gd is located at
MCISimulationWithResources/FirstPhasePanel.gd, and Ambulances/AmbulanceBLS.gd
is located at MCISimulationWithResources/Ambulances/AmbulanceBLS.gd.

Line numbers refer to the supplied source and may shift after editing.
Search for "Omer Perry" if the line numbers in your copy differ.
Each entry below shows the ORIGINAL code line and an UPDATED EXAMPLE.
Use your own extraction path in place of C:/MCI_Simulator in every example.
Keep output filenames and dynamic expressions (such as + sava_name or + time)
unchanged. Ensure all destination folders exist and are writable.

Ambulances/AmbulanceBLS.gd — line 401
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/TestData/AMB_" + str(self.ambulance_id) + time + "_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/TestData/AMB_" + str(self.ambulance_id) + time + "_Results.csv"

ArrivalCasualties.gd — line 603
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/TestData/Casualties" + time + "_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/TestData/Casualties" + time + "_Results.csv"

Casualties/StoredData.gd — line 23
    f.open("C:/Users/Omer Perry/Desktop/CasualtiesData/casualtyone.csv", f.WRITE)
    Updated example:
    f.open("C:/MCI_Simulator/ParticipantsData/CasualtiesData/casualtyone.csv", f.WRITE)

DualProcessModelEvacuationNode2D.gd — line 61
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/ThirdPhase/DualProcess/Dual_Process_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/ThirdPhase/DualProcess/Dual_Process_Results.csv"

DualProcessModelNode2D.gd — line 59
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/FirstPhase/DualProcess/Dual_Process_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/FirstPhase/DualProcess/Dual_Process_Results.csv"

DualProcessModelTreatmentNode2D.gd — line 59
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/SecondPhase/DualProcess/Dual_Process_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/SecondPhase/DualProcess/Dual_Process_Results.csv"

EvacuationCasualties.gd — line 604
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/TestData/Casualties" + time + "_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/TestData/Casualties" + time + "_Results.csv"

EvacuationMain.gd — line 1121
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/ThirdPhase/Casualties_Data.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/ThirdPhase/Casualties_Data.csv"

FirstPhasePanel.gd — line 164
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/FirstPhase/Indicators/first_phase_indicators.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/FirstPhase/Indicators/first_phase_indicators.csv"

FirstPhasePanel.gd — line 228
    var save_file = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/FirstPhase/Recordings/" + sava_name
    Updated example:
    var save_file = "C:/MCI_Simulator/ParticipantsData/FirstPhase/Recordings/" + sava_name

FirstPhasePanel.gd — line 301
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/FirstPhase/Casualties/Reported_Casualties_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/FirstPhase/Casualties/Reported_Casualties_Results.csv"

FirstPhasePanelData.gd — line 101
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/FirstPhase/Casualties/Reported_Casualties_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/FirstPhase/Casualties/Reported_Casualties_Results.csv"

ProtocolSecondPhasePanel.gd — line 192
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/SecondPhase/Indicators/second_phase_indicators.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/SecondPhase/Indicators/second_phase_indicators.csv"

ProtocolSecondPhasePanel.gd — line 255
    var save_file = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/SecondPhase/Recordings/" + sava_name
    Updated example:
    var save_file = "C:/MCI_Simulator/ParticipantsData/SecondPhase/Recordings/" + sava_name

ProtocolSecondPhasePanel.gd — line 307
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/SecondPhase/Casualties/Reported_Casualties_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/SecondPhase/Casualties/Reported_Casualties_Results.csv"

ProtocolThirdPhasePanel.gd — line 365
    var save_file = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/ThirdPhase/Recordings/" + sava_name
    Updated example:
    var save_file = "C:/MCI_Simulator/ParticipantsData/ThirdPhase/Recordings/" + sava_name

ProtocolThirdPhasePanel.gd — line 423
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/ThirdPhase/Casualties/Reported_Casualties_Results.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/ThirdPhase/Casualties/Reported_Casualties_Results.csv"

StoredData.gd — line 22
    f.open("C:/Users/Omer Perry/Desktop/CasualtiesData/casualtyone.csv", f.WRITE)
    Updated example:
    f.open("C:/MCI_Simulator/ParticipantsData/CasualtiesData/casualtyone.csv", f.WRITE)

global.gd — line 140
    var file_path = "C:/Users/Omer Perry/Desktop/GameDevelopment/ParticipantsData/Phase_Transition.csv"
    Updated example:
    var file_path = "C:/MCI_Simulator/ParticipantsData/Phase_Transition.csv"

Some scripts target the same output file. This list identifies all 19 references
in 14 scripts; it does not imply every save function runs in the current scenario.

4. USE THE PROVIDED CASUALTY SET
This release is configured to work with one predefined casualty set. Use the
provided set and keep its casualty IDs, descriptions, and associated resources
unchanged. No selection of an alternative casualty set is required for the
current setup.

5. START THE SIMULATOR AND GET SUPPORT
In Godot, open the imported MCISimulationWithResources project. The startup
script is MCISimulationWithResources/Driving.gd, attached to
MCISimulationWithResources/Driving.tscn.
Open Driving.tscn and click Run Current Scene (F6). Alternatively, run the
project (F5); its configured main scene is Driving.tscn. Run the scene/project,
not the .gd script as a standalone file.

The current simulator interface is in Hebrew. An English version will be
released soon.

If you encounter installation, startup, or saving problems, contact Omer at:
Omerpe@post.bgu.ac.il
Include the error message or a screenshot and a brief description of the issue.
