# Basic Skeleton

```lua
run(function()
    local MyFeature
    local MySlider
    local MyToggle
    local MyDropdown

    MyFeature = vape.Categories.Combat:CreateModule({
        Name = 'My Feature',
        Tooltip = 'Description shown on hover',
        Function = function(callback)
            if callback then
                -- Setup: runs when toggled ON
            else
                -- Teardown: runs when toggled OFF
            end
        end
    })

    MySlider = MyFeature:CreateSlider({
        Name = 'Speed',
        Min = 0,
        Max = 100,
        Default = 50,
        Suffix = '%',
        Tooltip = 'Controls speed'
    })

    MyToggle = MyFeature:CreateToggle({
        Name = 'Extra Option',
        Default = false,
        Tooltip = 'Does something extra'
    })

    MyDropdown = MyFeature:CreateDropdown({
        Name = 'Mode',
        List = {'Option A', 'Option B', 'Option C'},
        Default = 'Option A',
        Tooltip = 'Pick a mode'
    })
end)
