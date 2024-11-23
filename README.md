This program is a game called "Flappy Oinc", inspired by the mechanics of Flappy Bird. It is implemented in C using the Raylib library for graphics and sound management. Below is an overview of the project:

**Features**

Gameplay: 

  A player controls a pig character ("Oinc") that must navigate through obstacles by "jumping" to avoid colliding with pipes.
  
  Points are earned as the pig successfully passes through pipe gaps, and difficulty increases over time.

Game Modes:

  Difficulty Settings: Players can choose between "Easy", "Normal", or "Hard", each with unique obstacle speeds and configurations.

  Power-ups: Occasionally, the game provides power-ups that make the pig temporarily invincible.

  Ranking System: The game maintains a leaderboard of the top 5 scores, stored in a binary file.

Graphics and Sounds: 

  The game uses sprite-based textures for pipes, backgrounds, and the pig. 
  
  Sounds are triggered for specific events like jumping, game over, and collecting power-ups.

Menu System: 

  Includes menus for starting the game, selecting difficulty, viewing the ranking, and displaying a "Game Over" screen.

**Code Structure**

Constants and Enums: 

  Defined for screen dimensions, difficulty levels, and menu states.

Structs: 

  Represent game elements like the player, pig, pipes, power-ups, and scoring.

Global Variables: 

  Hold textures, sounds, and game state data such as difficulty settings, score, and menu state.

Functions:

  Modularized into specific tasks:
  
    Rendering different screens (DesenharTudo, Inicio, Gameover, etc.).
    
    Gameplay logic (Gameplay, MudarDificuldade, PowerUp).
    
    File handling for rankings (CarregarRanking, AtualizarRanking).
    
    Handling user input and animations.
    
    Main Loop:

        Initializes the window, loads resources, and enters the main menu.

        Manages state transitions through a switch statement, calling relevant functions for gameplay, menus, and rankings.

**Key Highlights
**

Collision Detection: 
  
  Checks for collisions between the pig and pipes or power-ups to determine game state transitions.

Dynamic Difficulty: 
  
  Gradually increases the challenge based on the score by modifying gap sizes and pipe movement speed.

File I/O: 
  
  Implements file reading and writing to manage ranking persistence.

**Dependencies**

Raylib Library: 

  Required for rendering, input management, and sound effects.
  
Image and Sound Files: 
  The game relies on specific assets such as textures for pipes and backgrounds, and sound files for jumps and power-ups.
  
