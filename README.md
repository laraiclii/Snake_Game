# Snake Game

The goal of Snake is to grow the snake as long as possible by guiding it to apples. The snake moves automatically and dies if it collides with itself. The snake grows by **3 cells per apple**, and the board wraps around at the edges. The head shows its current direction.

---

## Features

- Snake starts with **length 3** at the top-left
- Wrap-around board edges (no death on borders)
- Head shows direction
- Reverse mode available (assignment 2.3)
- Apples placed deterministically for testing

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
