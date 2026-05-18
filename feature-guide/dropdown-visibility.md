# Dropdown Visibility

Dropdowns do not have a `Function` callback. Use this pattern to show/hide options:

```lua
local function updateVisibility()
    local mode = MyDropdown.Value
    SliderA.Object.Visible = (mode == 'Mode A')
    SliderB.Object.Visible = (mode == 'Mode B')
end

-- Inside CreateModule
Function = function(callback)
    if callback then
        updateVisibility()
        -- ...
    end
end
```
