# Connections & Cleanup

## Proper Connection Handling

Use `MyFeature:Clean(connection)` for **every** connection created while the feature is enabled.

```lua
-- Correct
MyFeature:Clean(runService.PostSimulation:Connect(function()
    -- per-frame logic
end))

MyFeature:Clean(vapeEvents.EntityDamageEvent.Event:Connect(function() end))

-- Wrong (never do this)
runService.PostSimulation:Connect(function() end)

-- Manual Cleanup
For things that :Clean() cannot handle (hooks, created objects, etc.), restore them manually in the else block:
LuaFunction = function(callback)
    if callback then
        oldFunc = bedwars.SomeUtil.someMethod
        bedwars.SomeUtil.someMethod = function(...) 
            -- your code 
        end
    else
        bedwars.SomeUtil.someMethod = oldFunc  -- restore
    end
end
```
