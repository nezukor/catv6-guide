\# Basic Skeleton



Every feature follows this exact structure:



```lua

run(function()

&#x20;   local MyFeature

&#x20;   local MySlider

&#x20;   local MyToggle

&#x20;   local MyDropdown



&#x20;   MyFeature = vape.Categories.Combat:CreateModule({

&#x20;       Name = 'My Feature',

&#x20;       Tooltip = 'Description shown on hover',

&#x20;       Function = function(callback)

&#x20;           if callback then

&#x20;               -- Setup: runs when the feature is toggled ON

&#x20;               -- Register connections with MyFeature:Clean()

&#x20;           else

&#x20;               -- Teardown: runs when the feature is toggled OFF

&#x20;               -- Restore any changes made (hooks, values, etc.)

&#x20;           end

&#x20;       end

&#x20;   })



&#x20;   -- Create options (sliders, toggles, dropdowns)

&#x20;   MySlider = MyFeature:CreateSlider({

&#x20;       Name = 'Speed',

&#x20;       Min = 0,

&#x20;       Max = 100,

&#x20;       Default = 50,

&#x20;       Suffix = '%',

&#x20;       Decimal = 10,

&#x20;       Tooltip = 'Controls speed',

&#x20;       Function = function(val) end

&#x20;   })



&#x20;   MyToggle = MyFeature:CreateToggle({

&#x20;       Name = 'Extra Option',

&#x20;       Default = false,

&#x20;       Tooltip = 'Does something extra',

&#x20;       Function = function(callback) end

&#x20;   })



&#x20;   MyDropdown = MyFeature:CreateDropdown({

&#x20;       Name = 'Mode',

&#x20;       List = {'Option A', 'Option B', 'Option C'},

&#x20;       Default = 'Option A',

&#x20;       Tooltip = 'Pick a mode'

&#x20;   })

end)

