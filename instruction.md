# Copilot Instruction File

## Project Context

This is a Flask-based Sudoku application being modernized from legacy code.

Prioritize preserving existing functionality while making focused, modular improvements.

## Code Style & Structure

- Follow PEP 8 guidelines for Python code.
- Use clear, meaningful names.
- Keep functions and modules focused on a single responsibility.
- Add docstrings for important public functions and classes.
- Prefer simple, maintainable solutions over unnecessary abstraction.
- Comments should explain why a non-obvious decision was made.
- Preserve existing APIs and behavior unless a requirement explicitly requires a change.

Current structure:

- `starter/board.py` → Sudoku board generation, solving, validation, and uniqueness logic.
- `starter/sudoku_logic.py` → puzzle-generation compatibility layer.
- `starter/app.py` → Flask application and API routes.
- `starter/templates/` → HTML templates.
- `starter/static/` → JavaScript and CSS.
- `tests/` → automated tests.

Do not create additional modules such as `game.py`, `routes.py`, or `utils.py` unless they are clearly necessary and approved.

## Testing

- Use pytest for Python tests.
- Add focused tests for new functionality.
- Preserve existing tests when refactoring.
- Test both normal behavior and important edge cases.
- Run the relevant test suite after changes.
- Document useful test commands in `README.md`.

## Sudoku Requirements

- Every generated puzzle must have exactly one valid solution.
- Support Easy, Medium, and Hard difficulty levels.
- Difficulty must affect the number of prefilled cells.
- Easy: 45 clues.
- Medium: 35 clues.
- Hard: 25 clues.
- Prefilled cells must remain locked.
- Invalid Sudoku moves should receive immediate visual feedback.
- The Check button must identify incorrect entries.
- The Hint button must fill one valid empty cell and lock it.
- Completing a puzzle correctly must display a congratulatory message.

## Game Features

- Timer starts after a puzzle successfully loads.
- Timer stops when the puzzle is correctly completed.
- Hint usage must be counted for the current game.
- Dark mode toggle must work correctly.
- Preserve existing game behavior when adding new features.

## Leaderboard

- Maintain a browser-side Top 10 leaderboard using `localStorage`.
- Each completed score must contain:
  - player name
  - completion time
  - difficulty
  - number of hints used
- Lower completion times rank higher.
- Keep only the best 10 scores.
- Handle malformed or unavailable localStorage safely.
- Preserve compatibility with older leaderboard entries where practical.

## Styling & Accessibility

- Use the existing plain CSS approach.
- Make the application responsive on desktop and mobile.
- Prevent horizontal overflow and visible layout shifts.
- The Sudoku 3×3 blocks must use alternating colors.
- Support both light and dark modes.
- Keep text, buttons, inputs, and feedback states readable in both themes.
- Preserve visual distinctions between:
  - prefilled cells
  - editable cells
  - invalid cells
  - incorrect cells
  - hint cells
  - focused cells

## Copilot Workflow

- Inspect the existing implementation before making changes.
- Start with a clear implementation plan for significant changes.
- Make the smallest change that satisfies the requirement.
- Do not modify unrelated files.
- Review Copilot suggestions before accepting them.
- Question or adjust suggestions that conflict with the project requirements.
- Run tests after implementing changes.
- Keep Copilot context focused and reset it when necessary.
- Use screenshots to document required Copilot milestone interactions.