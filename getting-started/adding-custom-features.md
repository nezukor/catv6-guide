# Adding Custom Features

## Where to paste your code

1. Open your executor's **Workspace** folder.
2. Go into the `catrewrite` folder.
3. Navigate to `games`.
4. Open the file **`6872274481.lua`** in any text editor
5. Scroll all the way to the **bottom** of the file.
6. Press **Enter** twice to create some clean space.
7. Paste your custom feature code.
8. Save the file (`Ctrl + S`).

----

## Important Rules for Adding Code

- Always append your code **at the very bottom** of `6872274481.lua`.
- Never insert code in the middle of existing `run()` blocks (unless you are modifying/rewriting an existing feature).
- Every custom feature **must** be wrapped inside `run(function() ... end)`.
- Declare all your local variables at the top of the `run()` block.

> **Tip:** Use a good code editor like **VSCode** with Lua syntax highlighting for a much better experience, Notepad and Notepad++ Also work but VSCode is better.

----

> **Make sure to backup your changes because catvape updates will remove the features**
