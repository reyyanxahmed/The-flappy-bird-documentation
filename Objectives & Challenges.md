# Objectives & Challenges

## Project Development Phases

### 1. Storyboard Design
Develop a detailed storyboard outlining the flow of the project. This will serve as a roadmap for the development process, ensuring a clear understanding of the game's structure and functionality.

### 2. Resource Gathering
Gather all the necessary resources for the project, including graphics for the bird, pipes, background, and any other elements needed for the game. This step ensures that all required assets are available before proceeding with development.

### 3. Game Mechanics Implementation
Implement the core game mechanics, including the movement of the bird and collision detection with obstacles such as pipes. This phase focuses on bringing the game to life by coding its fundamental functionalities.

### 4. User Input Handling
Develop functionality to capture user input, such as keyboard presses to control the bird's movement. This step enables players to interact with the game and control the bird's actions effectively.

### 5. Scoring System
Create a scoring system that increases with each successful passage through a set of pipes. This adds an element of challenge and progression to the game, motivating players to achieve higher scores.

### 6. Animation Integration
Integrate animations seamlessly with the HTML canvas. This final phase enhances the visual appeal of the game by adding fluid animations to the bird, pipes, and other elements, creating a more immersive gaming experience.


## Challenges

### Challenge 1: The game did't have a clear way to restart

**Situation:**
After the bird crashes, there was no way for the user to restart the game without refreshing the page. This disrupted the flow of the game.

**Task:**
To implement a mechanism for the user to restart the game after a collision.

**Action:**
In the `moveBird` function within the `flappybird.js` file, we included a conditional statement that checks if the user presses the spacebar, up arrow key, or "X" key. If any of these keys are pressed and the game is over (`gameOver` is true), the function resets several variables:
- `bird.y` is set back to its original position.
- The `pipeArray` is emptied, removing all pipes from the screen.
- The score is reset to 0.
- The `gameOver` flag is set to false, allowing the game to resume.

**Result:**
Now the user can restart the game by detecting specific key presses when the game is over. This enhances the user experience by allowing them to resume playing without needing to refresh the page.


### Challenge 2: Collision Detection between Bird and Pipes
**Situation:**
The game did not have a clear way for the user to restart after the bird crashes, which disrupted the flow of the game. Accurate collision detection between the bird and pipes was also crucial for determining the game's outcome.

**Task:**
- Implement a mechanism for the user to restart the game after a collision and improve collision detection between the bird and pipes.

**Action:**
- **For the restart mechanism:**
  - In the `moveBird` function within the `flappybird.js` file, added a conditional statement to check if the user presses specific keys (spacebar, up arrow key, or "X" key) when the game is over (`gameOver` is true).
  - If any of these keys are pressed, reset several variables:
    - Set `bird.y` back to its original position.
    - Empty the `pipeArray`, removing all pipes from the screen.
    - Reset the score to 0.
    - Set the `gameOver` flag to false, allowing the game to resume.
- **For collision detection:**
  - Added a collision detection function to the `flappybird.js` file.
  - This function checks whether the bounding boxes of the bird and pipes intersect or not by comparing their positions and sizes.
  - If a collision is detected, trigger the game over conditions to end the game.

**Result:**
- The user can now restart the game by pressing specific keys when the game is over, enhancing the user experience by allowing them to resume playing without refreshing the page.
- With the implementation of the collision detection function, the game now accurately detects collisions between the bird and pipes, providing a more realistic and engaging gameplay experience.
- Overall, by addressing the challenges of implementing a restart mechanism and accurate collision detection, the team has successfully improved the game's functionality and user experience.
