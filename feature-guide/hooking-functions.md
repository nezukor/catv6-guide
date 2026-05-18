# Hooking Functions

### Hooking Lua Functions

```lua
local old
old = bedwars.SomeUtil.someMethod

bedwars.SomeUtil.someMethod = function(...)
    -- your logic here
    return old(...) -- always call original unless blocking
end
```

## Important: Always restore the original function in the else (teardown) block.

# For C Functions / Remotes
`hookfunction` does not work on C methods like `RemoteEvent:FireServer.`
Use `oth.hook` (if your executor supports it) instead.