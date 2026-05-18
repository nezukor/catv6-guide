# Rules (Never Break These)

1. Always wrap your code in `run(function() ... end)`
2. Declare all locals at the top of the `run()` block
3. Never insert code in the middle of existing features (always append at bottom)
4. Use `MyFeature:Clean()` for **every** connection
5. Always restore hooked functions in the `else` block
6. Never use `task.wait()` inside `PostSimulation` connections
7. Dropdowns have no `Function` callback — read `.Value` directly
8. Always test your feature after adding it

### Breaking these rules commonly causes crashes, memory leaks, features that don't toggle off properly, or CatVape entirely breaking and indefinitely loading
