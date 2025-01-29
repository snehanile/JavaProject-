# JavaProject - Design Snake Game

### **1. Overview**  
- The code represents a **Snake Game** implementation.  
- It consists of two main objects:  
  - **Snake Object** → Stores information about the snake.  
  - **Board Object** → Stores information about the game board.  

### **2. Direction Handling**  
- The `direction` variable keeps track of the snake’s movement:  
  - `0` → Left  
  - `1` → Right  
  - `2` → Up  
  - `-2` → Down  

- The `getDirection()` method returns the current direction of the player.  

### **3. Game Over Handling**  
- The `isGameOver()` method checks if a game-over condition has occurred.  
- If **game over** occurs, `setGameOver()` sets the `gameOver` flag to **true**, stopping the game.  
- `gameOver` is set to **true** if the player loses.  
- `isGameOver` is set to **false** if the game continues.  


### **4. Game Properties**  
- **Snake Object**  
  - Stores details about the **snake**, including `direction`, `board`, and `gameOver` status.  
- **Board Object**  
  - Represents the **game surface** and tracks player movement.  

### **5. Game Execution Flow**  
- The code starts by printing:  
  **"Going to update the game."**  
- It checks if `gameOver` is **true**.  
  - If `gameOver == false`, it sets the `direction = DIRECTION_NONE` and marks `gameOver = true`.  

### **6. Determining Snake Movement**  
- The `getNextCell()` method determines the next cell of the snake’s head:  
  - Uses `row` and `col` variables to calculate the next position.  
  - Returns the corresponding **Cell Object**.  

### **7. Handling User Input (Keyboard Events)**  
- The program checks for **keyboard inputs** to move the snake.  
- If the player presses a direction key:  
  - The snake moves in that direction.  
  - If the new cell is a **food item**, the snake grows.  
  - If the new cell is an **obstacle**, the game ends.  


### **8. Snake Growth and Food Generation**  
- If the snake **eats food**, it grows in size.  
- The `generateFood()` method generates new food on the board.  


### **9. Game Initialization**  
- The program starts by creating:  
  - **A new `Snake` object** (player’s snake).  
  - **A new `Board` object** (game area of size **10×10**).  
- The `initPos` variable stores the **initial position** of the snake.  


### **10. Game Object Creation**  
- A `Game` object is created to manage:  
  - The **game state**.  
  - The **snake's movement**.  
- `gameOver = false` to ensure the game is playable.  
- `direction = DIRECTION_RIGHT` to start movement towards the right.  


### **11. Handling User Keystrokes**  
- The program detects **keyboard events** and updates the game accordingly.  
- Example:  
  - If the **Left Arrow key** is pressed → **"Press left arrow to move left"** is printed.  


### **12. Game Update Mechanism**  
- The game updates at **regular intervals** using a timer.  
- The game continues running until:  
  - The player **loses** (`gameOver = true`).  
  - The player **wins** (if applicable).  
