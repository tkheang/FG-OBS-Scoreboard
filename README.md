# FG OBS Scoreboard
This is a simple scoreboard app for OBS (Open Broadcaster Software). Since it's run in the browser, it can be docked in OBS using Custom Browser Docks. Functionality is based on [SBE - ScoreBoard Edit](https://obsproject.com/forum/resources/sbe-scoreboard-edit.83/).

Features:
   * Web UI with options for singles and team tourneys
   * Output names, scores, and match info to text files, which can then be added to OBS using text sources and the "read from file" option

# Requirements
* Windows 10/11 

* [ASP.NET Core Runtime 7 for Windows](https://dotnet.microsoft.com/en-us/download/dotnet/7.0)  
   * Download and install the Hosting Bundle as recommended by Microsoft.
  
     ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/94051270-71e0-4015-a9d4-9564254b4d8c)

# Usage
1. [Download the latest release](https://github.com/tkheang/FG-OBS-Scoreboard/releases) and extract the folder. Run the program "FG-OBS-Scoreboard.exe".
2. A console window should open.
   
   ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/c8d0c7be-2fd7-4861-8ca2-d8e0cbc16e57)

3. In OBS, click "Docks, Custom Browser Docks...".
   
   ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/57658443-4b25-4d42-816f-75e77e590653)

4. Enter the dock name and "http://localhost:5000" for URL and click "Apply".
   
   ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/3b2a5313-36f7-45a9-a30b-c9473302a7be)

5. A dockable browser window should appear. Depending on the width, the sidebar may be on the left or accessed by the top right button. It can be moved and docked within OBS by dragging it between panels. If closed, it can be reopened from the bottom of the "Docks" menu.

   The app doesn't have to be docked in OBS; it can be run in a separate browser if desired.

   <img src="https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/519146f7-9202-4410-b624-ba0e2290eca8" width="300"/>
   <img src="https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/9cd120be-d61e-4fbd-b4dc-0febf38a59c1" width="500"/>

   <img src="https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/d79b781c-bd40-4ed5-a036-8356325c90d0" width="600"/>

6. Open the "Singles Tourney" page from the sidebar or top right button.

7. Add Text (GDI+) sources for Player 1 name, Player 1 score, Player 2 name, Player 2 score, and match info and arrange them as desired in the scene. For each text source, go to Properties and browse for the corresponding .txt file, located in FG-OBS-Scoreboard/Output.
   - Player 1 name: P1.txt
   - Player 1 score: scrP1.txt
   - Player 2 name: P2.txt
   - Player 2 score: scrP2.txt
   - Match info: label.txt

   ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/33fddc90-b8d2-47d6-946d-84944b99f4b4)

8. Enter player names, scores, and match info and click "Update". The text sources in the scene should update based on the contents of the .txt files. "Switch" swaps the player names and scores. "Clear" clears out all text and resets the scores to 0.

   Scores can be incremented/decremented by clicking on the up/down arrows in each score entry box.

   ![image](https://github.com/tkheang/FG-OBS-Scoreboard/assets/15349500/c568320e-a33c-4cbb-bc7c-141a0e6cd1bd)

9. Experiment with "edit transform" options for each text source to make sure it scales and aligns properly within the scene.
