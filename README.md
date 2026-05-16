# Doraemon's Treat Hunt

**Doraemon's Treat Hunt** is a 2D interactive Computer Graphics game developed using **C++**, **OpenGL**, **GLUT**, and **Code::Blocks**. The game presents a side-scrolling adventure where the player controls a Doraemon-inspired character, collects doracakes, avoids hazards, survives obstacles, and completes five different levels with changing environments.

This project was developed as part of a **Computer Graphics** course to demonstrate practical use of OpenGL drawing, animation, keyboard interaction, collision detection, score handling, level design, sound, and file-based high-score storage.

---

## Project Information

| Item | Details |
|---|---|
| Project Title | Doraemon's Treat Hunt |
| Project Type | 2D OpenGL Interactive Graphics Game |
| Course | Computer Graphics |
| Language | C++ |
| Graphics Library | OpenGL and GLUT |
| IDE | Code::Blocks |
| Platform | Windows |
| Repository | https://github.com/Abid3R/Doraemon-Hunt |

---

## Group Members and Contribution

| Sl. No. | Name | Student ID | Role | Contribution |
|---|---|---|---|---|
| 1 | Shafayat Jamil | 23-55457-7 | Gameplay Logic & Integration Developer | Implemented and integrated the main gameplay flow, player movement, level selection, score updates, level-completion return-to-menu logic, and final testing/debugging. |
| 2 | Abrar Kabir | 23-55095-3 | Graphics & Scene Designer | Designed and refined OpenGL-based visual scenes, backgrounds, character/environment drawing support, level atmosphere, scenery planning, and screenshot preparation guidance. |
| 3 | Md. Towhidul Islam | 23-55036-3 | Collision & Obstacle System Developer | Worked on randomized obstacle behaviour, hazard placement, obstacle movement, collision consistency, hitbox/cooldown improvement, and gameplay balancing across levels. |
| 4 | Aditya Roy | 23-55077-3 | Audio, File Handling & Documentation Support | Handled custom background music setup, `music_config.txt` use, high-score text-file saving, Code::Blocks setup instructions, documentation organization, and report preparation support. |

Each group member contributed **25%** to the project.

---

## Game Scenario

The game follows a simple adventure-style scenario. The player controls a Doraemon-inspired character who travels through different environments to collect doracakes. Each level contains collectible doracakes, hearts, and several hazards. The player must collect all required doracakes while avoiding fire, stones, falling rocks, ghost enemies, lightning, and other moving obstacles.

The game begins with a home menu where the player can select any of the five available levels. Each level has a different visual mood and challenge style, such as bright day, evening/sunset, night, rainy dawn, and storm night.

---

## Key Features

- Five selectable levels from the home menu
- Side-scrolling 2D gameplay
- Keyboard-controlled player movement and jumping
- Doraemon-inspired character drawn using OpenGL primitives
- Doracake collection system
- Score increment for collected items
- Heart/life system for player survival
- Randomized obstacle placement and movement
- Level-specific hazards such as fire, stones, falling rocks, ghost enemies, and lightning
- Per-level high-score saving using `highscore.txt`
- Custom background music using `music_config.txt`
- Sound effects for item collection, damage, level completion, game over, and final win
- Pause and resume feature using the **P** key
- Return-to-main-menu flow after completing a level

---

## Technologies Used

| Technology | Use in Project |
|---|---|
| C++ | Main programming language for variables, arrays, functions, loops, conditions, input handling, and file handling. |
| OpenGL | Used for rendering all 2D graphics such as the character, backgrounds, clouds, buildings, obstacles, collectibles, stars, and HUD elements. |
| GLUT | Used for window creation, keyboard input, mouse input, display callback, and timer-based animation. |
| Code::Blocks | Development environment used to compile and run the project. |
| MinGW/GCC | Compiler used with Code::Blocks. |
| Windows Multimedia / winmm | Used for MP3/WAV playback through `mciSendString`. |
| Text File I/O | Used to read custom music path and store high scores. |
| Random Number Generation | Used for randomized collectibles, hearts, obstacles, and movement behaviour. |

---

## Controls

| Key / Input | Action |
|---|---|
| Left Arrow | Move left |
| Right Arrow | Move right |
| Up Arrow | Jump |
| P | Pause / Resume game |
| Mouse Click | Select level or menu option |

---

## Level Overview

| Level | Environment | Main Challenge |
|---|---|---|
| Level 1 | Bright Day / Home Environment | Basic movement, doracake collection, and simple hazards |
| Level 2 | Evening or Sunset Environment | More collectible interaction and obstacle placement |
| Level 3 | Night Environment | Darker visual atmosphere and night-based obstacle navigation |
| Level 4 | Rainy Dawn / Falling Rock Environment | Falling rock-style hazards and stronger challenge |
| Level 5 | Storm Night / Ghost and Lightning Environment | Ghost enemy, lightning, and storm-night hazards |

---

## Important Functions / Modules

| Function / Module | Purpose |
|---|---|
| `main()` | Initializes the game, loads music preference and high scores, creates the GLUT window, and registers callback functions. |
| `init()` | Sets the OpenGL projection, coordinate range, and display settings. |
| `display()` | Controls whether the home screen or selected level is drawn. |
| `homeScreen()` | Draws the title screen and level selection buttons. |
| `mouseClick()` | Detects mouse clicks on level buttons and menu options. |
| `specialKeyPress()` / `specialKeyRelease()` | Handles arrow-key movement and jump control. |
| `keyPress()` | Controls pause and resume using the P key. |
| `update()` | Main timer loop for movement, jumping, clouds, obstacles, hazards, and redraw timing. |
| `Level1()` to `Level5()` | Draw and control each level scene. |
| `placeCollectibles()` | Randomly places doracakes and hearts. |
| `checkCollectibles()` | Detects item collection, updates score, level score, and lives. |
| `placeObstacles()` / `placeObstaclesAdvanced()` | Places obstacles with random positions and behaviour. |
| `respawnObstacle()` | Respawns obstacles in new random positions. |
| `updateObstacles()` | Animates obstacle movement and rotation. |
| `checkObstacles()` / `damagePlayer()` | Detects player-obstacle collision and reduces lives. |
| `loadHiScore()` | Loads saved level scores from `highscore.txt`. |
| `saveHiScore()` | Saves per-level high scores into `highscore.txt`. |
| `updateHiScoreForCurrentLevel()` | Updates the best score for the current level. |
| `loadMusicPreference()` | Reads the preferred music path from `music_config.txt`. |
| `playBGM()` / `stopBGM()` | Starts and stops background music. |
| `playSound()` / `playSoundForce()` | Plays one-shot sound effects for game events. |
| `drawHUD()` | Displays collected cakes, lives, score, and level best score. |
| `completeLevelAndReturnHome()` | Saves the current level result and returns to the main menu. |

---

## Required Files

The project should include the following files:

```text
Doraemon-Hunt/
│
├── main.cpp
├── dora.cbp
├── dora.depend
├── dora.layout
├── README.md
├── music_config.txt
├── highscore.txt                # Generated automatically after running the game
└── sounds/
    ├── bgm.mp3
    └── optional sound effects
```

> Note: `highscore.txt` is generated automatically when the game saves a score. If custom music is used, the music file path should be set correctly in `music_config.txt`.

---

## Build Requirements

Before running the project, make sure the following are installed and configured:

- Code::Blocks IDE
- MinGW/GCC compiler
- OpenGL library
- GLUT library
- Windows multimedia library support (`winmm`)

Required linker options:

```bash
-lopengl32 -lglu32 -lglut32 -lwinmm
```

---

## How to Run the Project

1. Download or clone the repository.

```bash
git clone https://github.com/Abid3R/Doraemon-Hunt.git
```

2. Open the project folder in **Code::Blocks**.

3. Open the Code::Blocks project file:

```text
dora.cbp
```

4. Make sure the required linker libraries are added:

```bash
-lopengl32 -lglu32 -lglut32 -lwinmm
```

5. Rebuild the project.

6. Run the project.

7. Select a level from the home menu and start playing.

---

## Music Setup

The game supports custom background music.

1. Place the background music file inside the `sounds` folder.
2. Use an MP3 file such as:

```text
sounds/bgm.mp3
```

3. Make sure `music_config.txt` contains the correct music path.
4. Run the game again to play the selected background music.

---

## High-Score System

The game saves the best score separately for each level. The high-score data is stored in a text file named:

```text
highscore.txt
```

Example format:

```text
Level 1 500
Level 2 700
Level 3 900
Level 4 600
Level 5 1000
```

This allows the player to close the game and later view the previous best score for each level.

---

## Screenshots

Add project screenshots in this section after uploading images to the repository.

Recommended screenshots:

- Home menu
- Level 1 gameplay
- Level 2 gameplay
- Level 3 gameplay
- Level 4 gameplay
- Level 5 gameplay
- Level completion screen
- Game over screen

Example Markdown format:

```markdown
![Home Menu](screenshots/home-menu.png)
![Level 1](screenshots/level-1.png)
![Level 5](screenshots/level-5.png)
```

---

## Future Improvements

- Add sprite images and texture mapping instead of drawing all objects only with primitives
- Add an in-game settings menu for music, sound volume, and difficulty
- Add a player profile system for separate high-score records
- Add more levels with progressive difficulty
- Improve collision detection using more precise hitboxes or pixel-level collision
- Add enemy AI with patrol, chase, and attack behaviour
- Add a pause menu with restart, resume, main menu, and sound settings
- Add a level editor or external level file system
- Use cross-platform audio libraries for Windows, Linux, and macOS support
- Add smoother animation using frame-rate independent movement
- Add a scoreboard screen showing best scores for all five levels
- Upload a release package with screenshots, instructions, and compiled executable

---

## Limitations

- The project uses direct OpenGL primitive drawing instead of sprite or texture-based rendering.
- The audio system is Windows-specific because it uses `mciSendString` and `winmm`.
- Some visual elements and level data are hard-coded inside the source file.
- Collision detection uses simplified hitbox logic rather than detailed shape-based collision.
- The project currently focuses on educational Computer Graphics implementation rather than full commercial game-engine design.

---

## Conclusion

Doraemon's Treat Hunt demonstrates how OpenGL and GLUT can be used to build an interactive 2D graphics game with animation, input handling, collision detection, sound, scoring, and file-based storage. The project connects core Computer Graphics concepts with practical gameplay mechanics and presents a complete educational game structure suitable for academic submission.

---

## License

This project was developed for academic purposes as part of a Computer Graphics course. Use or modification should follow the rules of the course, institution, and project contributors.
