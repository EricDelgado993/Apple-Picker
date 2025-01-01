# Apple Picker Game

## Overview
Apple Picker is an engaging Unity game where players control a basket to catch falling apples. Avoid missing apples to maintain your baskets and achieve the highest score. The game combines quick reflexes and strategic movement, with increasing difficulty as the apple tree continues to drop apples.

---

## Gameplay Features

### Core Gameplay
- **Catch Apples:**
  - Move the basket horizontally using your mouse to catch falling apples.
  - Each caught apple adds +100 points to your score.

- **Avoid Misses:**
  - Missing an apple removes one basket.
  - Lose all baskets, and the game resets.

### Dynamic Elements
- **Apple Tree:**
  - Moves horizontally, dropping apples at regular intervals.
  - Randomly changes direction, adding unpredictability to the gameplay.

- **Baskets:**
  - Players start with three baskets, positioned vertically on the screen.
  - Each missed apple destroys one basket.

- **High Score Tracker:**
  - Records the highest score across sessions using Unity's `PlayerPrefs`.

---

## 🛠️ Key Features from the Code

### Scripts and Mechanics

#### `ApplePicker.cs`
- **Basket Management:**
  - Dynamically spawns three baskets at the start of the game.
  - Removes a basket when an apple is missed.
  - Restarts the game if all baskets are lost.

- **Apple Cleanup:**
  - Destroys all falling apples when a basket is lost.

#### `Apple.cs`
- **Apple Lifecycle:**
  - Apples are destroyed when they fall below a certain point (`-20f`).
  - Triggers `ApplePicker.AppleDestroyed()` to manage game state.

#### `AppleTree.cs`
- **Apple Tree Behavior:**
  - Moves left and right across the screen.
  - Randomly changes direction.
  - Drops apples at regular intervals (`secondsBetweenAppleDrops`).

#### `Basket.cs`
- **Basket Movement:**
  - Follows the horizontal position of the mouse.
  - Catches apples when they collide with the basket.

- **Score System:**
  - Increases score by +100 for each caught apple.
  - Updates the score display in real-time.
  - Tracks the high score and updates it dynamically.

#### `HighScore.cs`
- **Persistent High Score:**
  - Uses `PlayerPrefs` to save and load the highest score across sessions.
  - Displays the current high score on the screen.

---

## Visual and UI Features
- **Score Display:**
  - Real-time score updates shown at the top of the screen.

- **High Score Display:**
  - Persistent high score shown during gameplay.

- **Basket and Apple Prefabs:**
  - Customizable visuals for baskets and apples for a polished look.
