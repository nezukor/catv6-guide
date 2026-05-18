# Creating Custom Features
Every custom feature must follow a strict structure and be placed at the very bottom of `main.luau`.

## Key Requirements
- Always wrap your code in `run(function() ... end)`
- Declare all locals at the top of the `run()` block
- Use the module system (`CreateModule`) to register your feature
- Properly handle enable/disable states in the `Function` callback
