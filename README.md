# Qwirkle Game

## Introduction
Qwirkle is a tile-based game where players create lines of matching colors and shapes, either vertically or horizontally, with the aim of achieving the highest score. The game allows both human players and AI opponents to compete, with customizable difficulty levels for AI.

## Game Rules

### Objective
The main goal of Qwirkle is to score the most points by forming lines of matching shapes or colors on the board.

### Tile Placement Rules
- A player can place a tile in a position that:
  - Is adjacent to a previously placed tile
  - Shares either the same color or shape as the adjacent tile
- A line (horizontal or vertical) must consist of tiles that all share either:
  - The same color, or
  - The same shape (but not both)
- Players score points based on the number of tiles they add to a line
- The game ends when the board is full or when no player can make a valid move

## Game Logic Implementation

### Board Representation
- 2D grid of hexagonal cells
- Each cell can be empty or contain a tile
- Uses axial coordinates for row and column positions
- Tiles are represented by color and shape combinations

### Power-ups
| Power-up | Effect |
|----------|--------|
| UNDO | Reverts the last move made by the opponent |
| DOUBLE | Doubles the score for the current move |
| WILD | Allows placing a tile in any position without matching rules |

### Tile Placement and Scoring
- **Tile Placement**: Board checks validity based on adjacency and shape/color rules
- **Scoring**: Points earned based on tiles added (doubled if placed on DOUBLE power-up)

## AI Implementation
| Difficulty | Algorithm | Behavior |
|------------|-----------|----------|
| Easy | Uninformed Search | Places first available valid tile |
| Medium | Informed Search | Evaluates immediate moves, prioritizes power-ups |
| Hard | Minimax with Alpha-Beta Pruning | Simulates future moves, strategic power-up use |

## Tiles Description
**Colors (6):**  
Red, Yellow, Green, Cyan, Magenta, Blue  

**Shapes (6):**  
Triangle, Diamond, Square, Circle, Star, Spiral  

- 72 tiles total (2 of each shape/color combination)

## How to Play
1. **Setup**: Board initialized, each player gets 6 tiles
2. **Turns**: Players alternate placing valid tiles
3. **Power-ups**: Activate when landing on their cells
4. **Game End**: When no valid moves remain or board is full

## Conclusion
Qwirkle combines strategy, tile placement, and power-ups for an engaging experience with multiple AI difficulty levels.
