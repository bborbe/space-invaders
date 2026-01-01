# Space Invaders

**Play online:** https://bborbe.github.io/space-invaders/

A classic Space Invaders arcade game built with vanilla JavaScript, HTML5 Canvas, and CSS. Defend Earth from waves of alien invaders!

## Features

- **Classic Arcade Gameplay**: Shoot aliens before they reach the ground
- **5 Alien Types**: Different shapes, colors, and point values
- **Progressive Waves**: 10 waves with increasing difficulty and speed
- **UFO Bonus Targets**: Random mystery ships for extra points (50-300)
- **Destructible Shields**: 4 shields that protect you from alien bombs
- **Lives System**: 3 lives to survive all waves
- **Enemy AI**: Aliens drop bombs randomly and speed up as numbers decrease
- **Score Tracking**: Leaderboard with localStorage persistence
- **Pause/Restart**: Pause gameplay and restart anytime
- **Victory Detection**: Beat all 10 waves to win
- **Retro CRT Aesthetic**: Classic green terminal styling

## How to Play

1. Open `index.html` in a web browser
2. Use **arrow keys** to move your ship
3. Press **Space** to shoot
4. Destroy all aliens before they reach the bottom
5. Survive all 10 waves to achieve victory

## Controls

- **← →**: Move ship left/right
- **Space**: Shoot
- **P** or **Esc**: Pause/unpause game
- **R**: Restart game

## Gameplay Rules

- You start with **3 lives**
- Aliens move side-to-side and descend when hitting screen edges
- Aliens randomly drop bombs
- Shields absorb damage from both bullets and bombs
- Lose a life if hit by alien bomb
- Game over if aliens reach the ground or you lose all lives
- Victory after completing wave 10

## Scoring System

Aliens award different points based on row type:
- **Row 1 (Top)**: 30 points (Red - Octopus)
- **Row 2**: 20 points (Orange - Crab)
- **Row 3**: 20 points (Yellow - Crab)
- **Row 4**: 10 points (Green - Squid)
- **Row 5 (Bottom)**: 10 points (Cyan - Squid)

**UFO Bonus**: 50, 100, 150, or 300 points (random)

**Total possible score per wave**: 880 points (55 aliens)

## Technical Details

- **Canvas Size**: 800x600 pixels
- **Player Ship**: 50x30 pixels
- **Aliens**: 40x30 pixels, 5 rows × 11 columns
- **Bullet Speed**: 8 pixels per frame
- **Alien Bomb Speed**: 4 pixels per frame
- **Wave Progression**: Speed increases 20% per wave, move interval decreases 3 frames
- **No Dependencies**: Pure vanilla JavaScript

## Game Architecture

The game follows a modular architecture pattern:

- **Game State Module**: Manages state, collision detection, wave progression, scoring
- **Renderer Module**: Handles all canvas drawing (aliens, player, bullets, shields, UFO)
- **Input Handler Module**: Processes keyboard input
- **Game Loop**: Uses requestAnimationFrame for smooth 60fps gameplay

## Browser Compatibility

Works in all modern browsers supporting:
- HTML5 Canvas
- ES6 JavaScript
- localStorage API

## Development

Built following the same architectural patterns as the companion Tetris, Snake, Breakout, and Pacman games.

## License

Free to use and modify.
