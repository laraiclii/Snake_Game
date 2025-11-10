# Snake Game

In Snake, your goal is to grow the snake as long as possible by chasing apples. Each apple adds 3 cells, hitting yourself ends the game, and the board wraps around the edges. The snake’s head shows which way it’s moving.

---

## Framework

- `SnakeGame.scala` handles rendering and input.
- `GameLogic.scala` contains the game mechanics.
- Additional files should go in `src/snake/logic/`.

`SnakeGame` interacts with `GameLogic`:

- Draws the board based on `CellType`:
  - `Empty()`
  - `Apple()`
  - `SnakeHead(direction: Direction)` (North, East, South, West)
  - `SnakeBody(distanceToHead: Float)` (optional color gradient)
- Arrow keys call `changeDir(direction: Direction)`
- `"R"` key toggles reverse mode via `setReverse(true/false)`
- `step()` advances the game; called automatically 5 times/sec (adjust via `FramesPerSecond`)

## Testing

- ./gradlew test2_1 # Basic Snake (no reverse) 
- ./gradlew test2_3 # Snake with reverse mode

---

## Run

### IntelliJ
- Open `src/snake/game/SnakeGame.scala`
-  Click **Run**

### Terminal
- ./gradlew run
