# 🎮 Words Scramble Game

An interactive word scramble puzzle game built with **JavaFX**. Test your skills by unscrambling words across three difficulty levels with progressive challenges and scoring.

## 📋 Table of Contents
- [Features](#features)
- [System Requirements](#system-requirements)
- [Installation & Setup](#installation--setup)
- [How to Play](#how-to-play)
- [Game Levels](#game-levels)
- [Project Structure](#project-structure)
- [Troubleshooting](#troubleshooting)

## ✨ Features

- **Three Difficulty Levels**: Easy, Medium, and Hard modes
- **User Authentication**: Login and registration system
- **Progressive Levels**: Three in-game levels with increasing difficulty
- **Points System**: Earn points for correct answers
- **Sound Effects**: Audio feedback during gameplay
- **Database Integration**: XAMPP MySQL database for user management
- **Responsive UI**: Clean and intuitive JavaFX interface
- **Hints & Answers**: Visual hints provided for each word

## 💻 System Requirements

- **Java 11** or higher
- **JavaFX SDK** (configured in your project)
- **XAMPP** with MySQL server running
- **Windows, macOS, or Linux**

## 🚀 Installation & Setup

### 1. **Initial Database Setup**
Before running the game for the first time, configure your database credentials:

- Start **XAMPP** and ensure MySQL is running
- Edit `password.txt` with your XAMPP username and password
- On first launch, the game will prompt you to enter your XAMPP credentials
- The database will be automatically initialized

### 2. **Building the Project**
```bash
# Using your IDE (Eclipse/IntelliJ)
1. Import the project
2. Configure JavaFX library paths
3. Right-click project → Build
```

Or use the provided build file:
```bash
javafxbuild build.fxbuild
```

### 3. **Running the Game**
```bash
# Run from your IDE
Right-click Main.java → Run As → Java Application

# Or run from command line
java -jar WordsScrambleGame.jar
```

## 🎯 How to Play

### First Time Setup
1. Launch the application
2. Enter your XAMPP MySQL username and password
3. Create a new account with username and password
4. Select difficulty level: **EASY**, **MEDIUM**, or **HARD**

### GamePlay
1. **Unscramble the Word**: Rearrange the scrambled letters shown
2. **Drag & Drop**: Click letter buttons to fill answer fields
3. **Use Hints**: View hints related to each word
4. **Submit Answer**: Click SUBMIT to check your answer
5. **Earn Points**: Gain points for correct answers
6. **Progress Through Levels**: Advance from Level 1 → Level 2 → Level 3

## 📊 Game Levels

| Level | Difficulty | Description |
|-------|-----------|-------------|
| **Level 1** | EASY | Basic words, simple puzzles, good for beginners |
| **Level 2** | MEDIUM | Standard words, moderate challenge |
| **Level 3** | HARD | Complex words, advanced difficulty |

## 📁 Project Structure

```
WordsScrambleGame/
├── src/application/
│   ├── Main.java                    # Entry point
│   ├── LoginPage.java              # User login & registration
│   ├── GameConfiguration.java      # Database configuration
│   ├── LevelOneController.java     # Level 1 game logic
│   ├── LevelTwoController.java     # Level 2 game logic
│   ├── LevelThreeController.java   # Level 3 game logic
│   ├── LevelOneProcessAnswers.java # Answer processing for Level 1
│   ├── LevelTwoProcessAnswers.java # Answer processing for Level 2
│   ├── LevelThreeProcessAnswers.java # Answer processing for Level 3
│   ├── ScrambleWords.java          # Word scrambling logic
│   ├── ProcessPoints.java          # Score calculation
│   ├── DataBaseSetUp.java          # MySQL table setup
│   ├── DataBaseHelper.java         # Database operations
│   ├── USER.java                   # User data model
│   ├── WORD.java                   # Word data model
│   ├── Components.java             # UI components
│   ├── SOUNDS.java                 # Audio management
│   ├── Alert.java                  # Alert dialogs
│   └── application.css             # Styling
├── bin/                            # Compiled classes
├── build.fxbuild                   # Build configuration
├── databasestate.txt               # Database state flag
├── password.txt                    # XAMPP credentials
├── user.txt                        # User data storage
└── README.md                       # This file
```

## 🔧 Database Configuration

### Default Database Credentials
- **Server**: localhost
- **Port**: 3306 (default MySQL port)
- **Username**: Enter your XAMPP username
- **Password**: Enter your XAMPP password

### Database Files Created
- `databasestate.txt` - Tracks if database is configured
- `password.txt` - Stores XAMPP credentials
- `user.txt` - Stores user profile information

## ❓ Troubleshooting

### **Issue**: "Database connection failed"
- ✅ Ensure XAMPP is running
- ✅ Verify MySQL service is started
- ✅ Check `password.txt` has correct XAMPP credentials
- ✅ Confirm port 3306 is accessible

### **Issue**: "JavaFX module not found"
- ✅ Download JavaFX SDK for your OS
- ✅ Configure library path in IDE settings
- ✅ Add `--module-path` to VM options

### **Issue**: "No database tables found"
- ✅ Delete `databasestate.txt` to reinitialize
- ✅ Restart the application
- ✅ Re-enter XAMPP credentials

### **Issue**: "Cannot find login credentials"
- ✅ Ensure `user.txt` exists in project root
- ✅ Register a new account in-game

### **Issue**: "Sound not playing"
- ✅ Ensure audio files are present
- ✅ Check system volume settings
- ✅ Verify file permissions

## 📝 Game Tips

💡 **Hints**: Pay attention to hints provided with each scrambled word  
💡 **Timer**: Work quickly to earn bonus points  
💡 **Practice**: Start with EASY mode to learn the game mechanics  
💡 **Accuracy**: Focus on correct answers rather than speed  

## 🎓 Technical Stack

- **Language**: Java 11+
- **GUI Framework**: JavaFX
- **Database**: MySQL with XAMPP
- **Audio**: JavaFX Media API
- **Build Tool**: JavaFX Build Tools
