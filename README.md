# 🎮 Number Guessing Game

[![Java](https://img.shields.io/badge/Java-14%2B-orange?style=for-the-badge&logo=java)](https://www.oracle.com/java/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)
[![Roadmap.sh](https://img.shields.io/badge/Roadmap.sh-Project-green?style=for-the-badge)](https://roadmap.sh/projects/number-guessing-game)

> A feature-rich command-line number guessing game built with Java, featuring multiple difficulty levels, intelligent hints, and persistent high score tracking.

**Solution for the [Number Guessing Game](https://roadmap.sh/projects/number-guessing-game) backend project from [roadmap.sh](https://roadmap.sh/)** [![](https://avatars.githubusercontent.com/u/120650344?s=40&v=4)](https://roadmap.sh/)

---

## 📋 Table of Contents

- [About](#-about)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation & Usage](#-installation--usage)
- [Game Rules](#-game-rules)
- [Example Gameplay](#-example-gameplay)
- [Contributing](#-contributing)
- [License](#-license)
- [Author](#-author)

---

## 🎯 About

This is an interactive command-line number guessing game where the computer randomly selects a number between 1 and 100, and the player attempts to guess it. The game features multiple difficulty levels, an intelligent hint system, and tracks high scores across sessions.

**Key Highlights:**
- 🎲 Random number generation (1-100)
- 🏆 Persistent high score tracking per difficulty level
- 💡 Smart proximity-based hint system
- ⏱️ Time tracking for each game session
- 🔄 Unlimited replay capability

---

## ✨ Features

### 🎮 **Multiple Difficulty Levels**
Choose from three challenging difficulty modes:
- **Easy**: 10 attempts to guess the number
- **Medium**: 5 attempts to guess the number
- **Hard**: 3 attempts to guess the number

### 🏅 **High Score System**
- Tracks the best performance (fewest attempts) for each difficulty level
- Persistent across game sessions
- Displays all high scores on demand

### 💡 **Intelligent Hint System**
After 3 attempts, receive proximity-based hints:
- **"Quite close"**: Within 25% of the range
- **"Close"**: Within 50% of the range
- **"Far off"**: Beyond 50% of the range

### 🔄 **Multiple Rounds**
- Play unlimited rounds without restarting the application
- Seamless replay functionality
- Clean menu-driven interface

### ⏱️ **Time Tracking**
- Measures how long it takes to guess the correct number
- Displays completion time in seconds

---

## 🛠️ Tech Stack

This project demonstrates core Java programming concepts:

| Technology | Purpose |
|------------|---------|
| **Java 14+** | Core language (uses modern switch expressions) |
| **Enums** | Type-safe difficulty level management |
| **HashMap** | High score data storage |
| **Scanner** | User input handling |
| **OOP Principles** | Clean separation of concerns across classes |

**Java Features Used:**
- Modern switch expressions (Java 14+)
- Enum with methods and properties
- Static methods and fields
- Exception handling
- Time measurement with `System.currentTimeMillis()`

---

## 📁 Project Structure

```
number-guessing-game/
├── src/
│   ├── Main.java              # Entry point and main menu
│   ├── Game.java              # Core game logic and loop
│   ├── Difficulty.java        # Enum for difficulty levels
│   ├── HighScoreManager.java  # High score tracking
│   └── InputHandler.java      # User input validation
├── LICENSE                     # MIT License
├── README.md                   # This file
└── NumberGuessingGame.iml     # IntelliJ IDEA module file
```

### Class Responsibilities

| Class | Responsibility |
|-------|----------------|
| `Main` | Application entry point, main menu display and navigation |
| `Game` | Random number generation, game loop, hint system, time tracking |
| `Difficulty` | Enum defining difficulty levels and attempt limits |
| `HighScoreManager` | Stores and retrieves high scores using HashMap |
| `InputHandler` | Validates and processes user input for difficulty selection |

---

## 🚀 Installation & Usage

### Prerequisites
- Java Development Kit (JDK) 14 or higher
- Terminal/Command Prompt

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/himanshugupta91/number-guessing-game.git
   ```

2. **Navigate to the source directory**
   ```bash
   cd number-guessing-game/src
   ```

3. **Compile all Java files**
   ```bash
   javac Difficulty.java Game.java HighScoreManager.java InputHandler.java Main.java
   ```

4. **Run the application**
   ```bash
   java Main
   ```

5. **Start playing!**
   ```
   Guessing Game:
   1. Play
   2. See scores
   3. Exit Game
   Enter option:
   ```

---

## 🎲 Game Rules

### How to Play

1. **Select an option** from the main menu:
   - `1` - Start a new game
   - `2` - View high scores
   - `3` - Exit the application

2. **Choose difficulty level**:
   - `1` - Easy (10 attempts)
   - `2` - Medium (5 attempts)
   - `3` - Hard (3 attempts)

3. **Make your guesses**:
   - Enter a number between 1 and 100
   - Receive feedback: "Too high" or "Too low"
   - Get proximity hints after 3 attempts

4. **Win or lose**:
   - **Win**: Guess correctly within the attempt limit
   - **Lose**: Run out of attempts
   - View your completion time and attempt count

5. **High scores**:
   - Automatically saved if you beat the current record
   - Tracked separately for each difficulty level

### Scoring System

- **Best score** = Fewest attempts to guess correctly
- High scores are persistent across game sessions
- Each difficulty level maintains its own high score

---

## 📸 Example Gameplay

```bash
$ java Main

Guessing Game:
1. Play
2. See scores
3. Exit Game
Enter option: 1

Select difficulty level:
1 for Easy
2 for Medium
3 for Hard:
1

Enter your guess: 50
Too high! Try again.
You have 9 chances to guess the number.

Enter your guess: 25
Too low! Try again.
You have 8 chances to guess the number.

Enter your guess: 35
Too high! Try again.
You have 7 chances to guess the number.

Enter your guess: 30
Too low! Try again.
Hint: quite close
You have 6 chances to guess the number.

Enter your guess: 32
Too low! Try again.
Hint: quite close
You have 5 chances to guess the number.

Enter your guess: 33
Congratulations! You guessed the correct number in 6 attempts and 18 seconds.
The number was 33
New high scores for easy difficulty: 6 attempts.

Do you want to play again? (yes/no): no

Guessing Game:
1. Play
2. See scores
3. Exit Game
Enter option: 2

High scores
medium: No high score yet.
hard: No high score yet.
easy: 6 attempts.

Guessing Game:
1. Play
2. See scores
3. Exit Game
Enter option: 3

Exiting Guessing Game.
```

---

**⭐ Star this repository if you found it helpful!**

Made with ❤️ as part of the [Roadmap.sh](https://roadmap.sh/) backend projects

</div>
