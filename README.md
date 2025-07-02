# Color Match Challenge - Premium Edition

![Color Match Challenge Banner](https://github.com/ericgoh09/Color-Match-Challenge/blob/main/assets/Banner.png)

## Overview

Color Match Challenge is a visually stunning game that tests your ability to match RGB color values to actual colors. With a sleek glass-morphism design, dynamic animations, and challenging gameplay, this premium edition offers an engaging experience for players of all skill levels.

## Features

- 🎨 **Three difficulty levels** (Easy, Medium, Hard)
- ✨ **Stunning glass-morphism UI** with animated background
- 🌌 **Floating particle effects** for immersive experience
- 🔥 **Streak system** with special effects for consecutive wins
- 💡 **Hint system** for when you need assistance
- 📊 **Score tracking** with animated updates
- 📱 **Fully responsive design** for all devices

## How to Play

1. **Match the RGB value** displayed at the top to one of the color boxes
2. Choose your difficulty level:
   - 🟢 **Easy**: 3 colors (1 point per correct answer)
   - 🟠 **Medium**: 6 colors (2 points per correct answer)
   - 🔴 **Hard**: 9 colors (3 points per correct answer)
3. Build your streak by getting consecutive correct answers
4. Use the hint button when you're stuck (costs 1 point)
5. Try to achieve the highest score possible!

## Getting Started

Simply open the `index.html` file in any modern web browser to start playing. No installation required!

## Game Controls

| Button | Description |
|--------|-------------|
| **New Colors** | Generate a new set of colors |
| **Give Me a Hint** | Briefly highlight the correct color (costs 1 point) |
| **Difficulty Buttons** | Switch between Easy, Medium, and Hard modes |

## Bug Fixes in This Version

- 🛑 **Fixed incorrect selection after correct answer**:  
  Players can no longer click on colors after selecting the correct answer
- 🚫 **Prevented clicking on wrong colors**:  
  Once a color is identified as wrong, it remains disabled for the current round
- 🎨 **Updated button colors**:
  - Medium: Orange gradient (#ffa726 to #ff7043)
  - Hard: Red gradient (#ff5252 to #ff4081)
  - Hint: Golden gradient (#ffd740 to #ffab40)

## Technical Implementation

This game is built with:
- **HTML5** for structure
- **CSS3** with advanced animations and glass-morphism effects
- **JavaScript** for game logic and interactivity

```javascript
// Example game logic
function checkAnswer(color, element) {
  if (color === correctColor) {
    // Correct answer handling
    score += points;
    streak++;
    disableAllColors(); // Prevent further clicks
  } else {
    // Wrong answer handling
    element.classList.add('disabled');
    wrongAttempts.add(color);
  }
}
