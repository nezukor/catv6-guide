\# Dropdown Visibility



Dropdowns do \*\*not\*\* have a `Function` callback. To show/hide other options based on dropdown value:



```lua

local function updateVisibility()

&#x20;   local mode = MyDropdown.Value

&#x20;   

&#x20;   SliderA.Object.Visible = (mode == 'Mode A')

&#x20;   SliderB.Object.Visible = (mode == 'Mode B')

end



\-- Inside your module

MyFeature = vape.Categories.Blatant:CreateModule({

&#x20;   Name = 'My Feature',

&#x20;   Function = function(callback)

&#x20;       if callback then

&#x20;           updateVisibility()

&#x20;           -- other setup

&#x20;       end

&#x20;   end

})



```



Call `updateVisibility()` whenever the dropdown changes if needed (by connecting to the dropdown’s internal events if desired).

