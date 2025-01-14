### **MVP Scope**

1. **Goal**:
    - Complete a single mission to steal data from a secure room and exit safely.
2. **Features**:
    - Player movement and stealth (vision cones and hiding mechanics).
    - A single enemy with basic patrol AI.
    - Interactive elements: one door to unlock and one objective to collect.
    - Isometric grid-based map.
3. **Environment**:
    - One small level (e.g., 10x10 grid).
    - Walls, obstacles, a locked door, and the objective room.

---

### **Technical Overview**

1. **Platform**: Web-based (HTML5, JavaScript, and WebGL or Canvas).
2. **Libraries/Tools**:
    - **Rendering**: Three.js or Babylon.js for isometric rendering.
    - **Game Logic**: Custom or lightweight library like Phaser.js.
    - **Grid System**: Basic array to represent tiles and their states.

---
### **Game Flow**

1. **Start**:
    - The player spawns at the bottom left of the map.
    - The objective is marked at the top right.
2. **Gameplay**:
    - Use arrow keys or WASD for movement (or click to specific tiles).
    - Avoid the enemy’s vision cone.
    - Interact with the door (e.g., press “E” to unlock).
    - Reach the objective and exit safely.
    - Steps and interactions create an radius of "noise".
1. **Win/Loss Conditions**:
    - **Win**: Collect the objective and reach the exit.
    - **Lose**: Enter the enemy’s vision cone.

---

### **Development Plan**

#### **1. Grid-Based Map**

- Represent the map as a 2D array.
- Tile types:
    - Empty (`0`)
    - Wall (`1`)
    - Door (`2`)
    - Objective (`3`)
    - Player (`P`)
    - Enemy (`E`)

#### **2. Player Mechanics**
- Movement: Grid-based, snapping to tiles.
- Visibility: Show a small radius of tiles around the player.

#### **3. Enemy AI**
- Patrol: Move in a loop between predefined points.
- Vision cone: Triangular or cone-shaped overlay originating from the enemy’s position.

#### **4. Interaction**
- Door: Player must stand adjacent and press a key to unlock.
- Objective: Player collects it by stepping on the tile.

#### **5. Simple UI**
- Display win/loss messages.
- Basic start and end screens.

---

### **MVP Development Timeline**

1. **Day 1-2**:
    - Set up the grid-based map and rendering.
    - Implement player movement.
2. **Day 3-4**:
    - Add basic enemy patrol logic.
    - Create the vision cone mechanic.
3. **Day 5-6**:
    - Implement interactive elements (door and objective).
    - Add win/loss conditions.
4. **Day 7**:
    - Polish the visuals and test the game.

---