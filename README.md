# FG OBS Scoreboard
This is a simple scoreboard app for OBS (Open Broadcaster Software). Since it's run in the browser, it can be docked in OBS using Custom Browser Docks. Functionality is based on [SBE - ScoreBoard Edit](https://obsproject.com/forum/resources/sbe-scoreboard-edit.83/).

Features:
   * Web UI with options for singles and team tourneys
   * Output names, scores, and match info to text files, which can then be added to OBS using text sources and the "read from file" option

# Requirements
* Windows 10/11 

# Usage
1. [Download the latest release](https://github.com/tkheang/FG-OBS-Scoreboard/releases) and extract the folder. Run the program "FG-OBS-Scoreboard.exe". A console window should open.
2. In OBS, click "Docks, Custom Browser Docks...".
3. Enter the dock name and "http://localhost:5000" for URL and click "Apply".
4. A dockable browser window should appear. Depending on the width, the sidebar may be on the left or accessed by the top right button. It can be moved and docked within OBS by dragging it between panels. If closed, it can be reopened from the bottom of the "Docks" menu. The app doesn't have to be docked in OBS; it can be run in a separate browser if desired.
5. Open the "Singles Tourney" page from the sidebar or top right button.
6. Add Text (GDI+) sources for Player 1 name, Player 1 score, Player 2 name, Player 2 score, and match info and arrange them as desired in the scene. For each text source, go to Properties and browse for the corresponding .txt file, located in FG-OBS-Scoreboard/Output.
   - Player 1 name: P1.txt
   - Player 1 score: scrP1.txt
   - Player 2 name: P2.txt
   - Player 2 score: scrP2.txt
   - Match info: label.txt
7. Enter player names, scores, and match info and click "Update". The text sources in the scene should update based on the contents of the .txt files. "Switch" swaps the player names and scores. "Clear" clears out all text and resets the scores to 0. Scores can be incremented/decremented by clicking on the up/down arrows in each score entry box.
8. Experiment with "edit transform" options for each text source to make sure it scales and aligns properly within the scene.
