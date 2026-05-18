# Common Patterns

### Per-Frame Loop
```lua
MyFeature:Clean(runService.PostSimulation:Connect(function()
    if not entitylib.isAlive then return end
    -- your logic
end))
```

### React to Damage
```lua
MyFeature:Clean(vapeEvents.EntityDamageEvent.Event:Connect(function(damageTable)
    if damageTable.entityInstance ~= lplr.Character then return end
    -- handle damage
end))
```

### Get Best Tools
```lua
local sword, slot = getSword()
local bow, slot = getBow()
local tool, slot = getTool('wood')
```

### Switch Hotbar Slot
```lua
local slot = getHotbar(sword.tool)
hotbarSwitch(slot)
```

### Iterate Enemies
```lua
for _, ent in entitylib.List do
    if not ent.Targetable then continue end
    local dist = (ent.RootPart.Position - entitylib.character.RootPart.Position).Magnitude
end
```