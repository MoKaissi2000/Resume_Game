# Game_Project
What's Included in this repository:

Included in this submission is the folders containing the scripts, prefabs, scenes, and sprites.

 How to play game yourself:

* Access the google share drive https://drive.google.com/drive/folders/1A6nmqfXZpyXhraC8qmFeMau13l3AXKUw?usp=drive_link where there are two separate folders '4410_final_unity_package' and '4410_final_executable'.
* To directly start playing, you can download the entire folder '4410_final_executable' and run 'cse4410_final.exe'. Note: it is necessary to download entire folder or the executable will not run.
* Alternatively, you can navigate to '4410_final_unity_package' and download the latest unity package 'CSE4410FinalProjpt3_ChrisD.unitypackage' and import this into Unity to make any personal changes, additions, or play game within Unity hub.

Gameplay overview:

* The game is a simple 2D platformer where the objective is to shoot spawning enemies and remain alive as long as possible. The player (stickman) is equipped with projectiles (detergent) and can run and jump on different platforms. It faces three types of opponents which are jerseys, pants, and hats. The jeans and jerseys continuously spawn in different areas and follow predetermined paths either North-South or East-West. The hats are spawned in only once at the beginning of the game and these know the player location and follow it around. Enemies have a health of 1 and once they are hit with detergent they vanish and The score is increased. The player has a health of 5 and loses 1 health each time it makes contact with an enemy. Once health reaches 0 the player is destroyed and there is a prompt asking for user to start game all over.

How it works. Brief description of each script file:

* BoxController - Updates the 3 text boxes in the game for score, health, and game over.
* CloseButton - After the popup window has been opened, when we click close this script is called. Closes popup and resumes time which resumes game.
* DetergentMovement - When we instantiate a new projectile (detergent) this script uses RigidBody for movement and also detects collisions, performs calls accordingly.
* EnemyHealth - This is called to destroy enemy gameObject when it collides with projectile. Also calls for an update to the score.
* EnemyMovement - Attached to the hats, this script allows these enemies to know the current player location and move towards it.
* EnemySpawn - We pass in prefabs and this spawns enemies at a preset spawnRate.
* GearController - This opens settings menu if it is not opened yet. It also pauses time which in effect pauses the game in the background.
* JeansAI - Attached to the jeans, this script continuously moves jean enemies up and down within the camera.
* LoadMainMenu - Within the popup menu if we click on the main menu button this script is called and loads scene 'MainMenu'.
* MovingPlatform - In the game background there is a ladder, this script moves an invisible one-way platform up and down to allow player to "use" ladder.
* PauseManager - This pauses time in order to pause game when the menu is opened.
* PlatformPlayer - Performs player movement, animations, detects collisions with enemies, and destroys player if health is 0.
* PlayerShoot - If we receive a mouse click, shoot detergent projectile in the correct direction.
* QuitGame - When a user clicks the 'quit game' button this script is called to quit application.
* SettingsPopup - This opens or closes the popup settings window whenever called. Also has a boolean method to return state of popup.
* ShirtAI - Attached to the jerseys, this script continuously moves jersey enemies left and right within the camera.
* StartButton - Re-loads the Sample Scene when a user clicks the Start button
* StartScreenManager - This simply loads 'SampleScene' when we click the start button. SampleScene is where the game is played.
