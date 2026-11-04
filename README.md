# Pong
 
A classic Pong game made in **Godot 4** with GDScript. Play against a CPU opponent and see who reaches the highest score.
 
<img width="960" height="200" alt="Pong gameplay" src="https://github.com/user-attachments/assets/2d809bb2-840f-49f3-831e-ca4f43e9e0e2" />
<img width="347" height="192" alt="Pong screenshot" src="https://github.com/user-attachments/assets/0bef3c5e-0b46-42ba-adea-f3a00321fb01" />

🎮 **Play it on itch.io:**
[shadwdev.itch.io/pong](https://shadwdev.itch.io/pong)
 
## Controls
 
| Key | Action |
| --- | --- |
| ↑ Up arrow | Move paddle up |
| ↓ Down arrow | Move paddle down |
 
## Features
 
- **CPU opponent** that follows the ball at the same speed limit as the player, so it can be beaten
- **The ball speeds up** every time it hits a paddle, so rallies get harder the longer they last
- **The angle changes depending on where the ball hits the paddle**: hit it with the edge for a steeper bounce
- **Random serve**: each new ball starts at a random height and in a random direction
- **Score counter** for the player and the CPU, with a short pause before the next ball
- Pixel-style font and a dark background for a retro look
## Built with
 
- **Godot 4** (2D)
- **GDScript**
  
## How it works
 
| Script | What it does |
| --- | --- |
| `main.gd` | Keeps score, updates the score labels and starts a new ball after a point |
| `player.gd` | Moves the player paddle with the arrow keys and keeps it inside the screen |
| `cpu.gd` | Moves the CPU paddle towards the ball, limited by the paddle speed |
| `ball.gd` | Moves the ball, bounces it off walls and paddles, and speeds it up on each paddle hit |
 
## What I learned
 
I made this by following a tutorial, as my first finished game in Godot. Along the way I learned:
 
- **Godot's node and scene system:** building a game from nodes like `CharacterBody2D`, `StaticBody2D`, `Area2D`, `Timer` and `CanvasLayer`
- **Movement with `delta`:** so the game runs at the same speed no matter the frame rate
- **Collisions:** using `move_and_collide()` and bouncing with `bounce()` and the collision normal
- **Vectors:** controlling the ball's direction with `Vector2` and `normalized()`
- **Signals:** using `body_entered` on score zones and `timeout` on a timer to react to events
- **Simple AI:** making a CPU paddle follow the ball in a fair way
- **UI:** showing the score with labels and a custom font
  
## Run it yourself
 
1. Install [Godot 4](https://godotengine.org/download)
2. Clone the repo:
```bash
   git clone https://github.com/Sh4dwDev/Pong-Godot.git
```
3. Open Godot, click **Import**, and select the `project.godot` file
4. Press **F5** to play
   
## Future ideas
 
- Two-player mode on the same keyboard (W/S and arrow keys)
- Start menu and a "first to 10 wins" end screen
- Sound effects for hits and points
- Difficulty settings for the CPU
  
## Credits
 
- Based on a Pong tutorial for Godot 4
- Font: Public Pixel
 
