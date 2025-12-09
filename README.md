# Blitz Sweep

A fast-paced Minesweeper-style game with progressive difficulty levels, time limits, and scoring!

## About the Game

Blitz Sweep is an exciting twist on the classic Minesweeper game. Your goal is to clear all safe cells across 5 progressively challenging levels. Each level features:
- **Larger boards** - Starting at 8x8 and growing to 16x16
- **More mines** - From 10 mines in Level 1 to 50 mines in Level 5
- **Tighter time limits** - From 2 minutes down to 70 seconds
- **Increasing difficulty** - Test your skills as you advance!

## How to Play

### Basic Controls
- **Left-click** on a cell to reveal it
- **Right-click** on a cell to place or remove a flag (mark suspected mines)
- Numbers show how many mines are adjacent to that cell
- Clear all safe cells to complete the level

### Game Rules
- **First click is always safe** - The game ensures your first click reveals a safe area
- **Complete 5 levels to win** - Progress through increasingly difficult levels
- **Time limits** - Each level has a countdown timer
- **Game over conditions**:
  - Clicking on a mine resets you to Level 1
  - Running out of time resets you to Level 1
- **Level progression** - Successfully complete a level to advance to the next one

### Scoring System
- **10 points** for each cell you reveal
- **100 × level** bonus points for completing a level (e.g., 500 points for completing Level 5)
- **5 points** per second remaining on the timer when you complete a level

### Game Features
- **Save/Load** - Save your progress and resume later
- **Visual feedback** - Enjoy particle effects and animations
- **Real-time status** - Track your level, score, time, and mine/flag counts

## How to Start the Game

### Prerequisites
- Java 17 or higher
- Maven (for building and running)

### Running the Game

#### Option 1: Using Maven (Recommended)
```bash
mvn exec:java
```

#### Option 2: Using Make
```bash
make run
```

#### Option 3: Compile and Run Manually
```bash
# Compile the project
mvn compile

# Run the game
mvn exec:java
```

The game window will open automatically. Click "New Game" to start playing, or use the "Instructions" button in-game for a quick reference!

### Building from Source
```bash
# Compile the project
mvn compile

# Run tests
mvn test

# Package as JAR
mvn package
```

## Tips for Success
1. **Start with the edges** - Often easier to deduce mine locations
2. **Use flags strategically** - Mark mines you're certain about
3. **Watch the timer** - Plan your moves efficiently
4. **Look for patterns** - Numbers reveal mine locations through logic
5. **Save your progress** - Use the save feature to take breaks between levels

## Running for Evaluation

To run this game, execute the main method in the `Game` class. The game can be started using:

```bash
mvn exec:java
```

or

```bash
make run
```

Good luck, and enjoy Blitz Sweep!
