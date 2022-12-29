# Visual Command Bar UI

### README
This document is made for a ScriptHub im making so feel free to use it

## creating the Library
```lua
local Library = loadstring(game:HttpGet('https://raw.githubusercontent.com/Duhscriptposter/visual/main/Source1.lua', true))()
```

## Creating a Command Bar
```lua
local Window = Library:CreateWindow({
    Name = 'Visual Command UI Library', -- Ui Title
    IntroText = 'Visual Command UI Library',
    IntroIcon = 'rbxassetid://10618644218',
    IntroBlur = true,
    IntroBlurIntensity = 15,
    Theme = Library.Themes.dark,
    Position = 'bottom',
    Draggable = true,
    Prefix = ';'
})
```

## Creating a Command
```lua
Window:AddCommand('Name', {}, 'Description'.', function(Arguments, Speaker)
    print('Hello World')
end)
```

## Creating a Argument Command
```lua
Window:AddCommand('Name', {'Argument'}, 'Description', function(Arguments, Speaker)
    print(Arguments[1])
end)
```

## Creating a SetPrefix Command
```lua
Window:AddCommand('SetPrefix', {'New Prefix'}, 'Changes The Prefix.', function(Arguments, Speaker)
    Window:ChangePrefix(Arguments[1])
end)
```

## Creating a SetTheme Command
```lua
Window:AddCommand('SetPrefix', {'New Prefix'}, 'Changes The Prefix.', function(Arguments, Speaker)
    Window:ChangePrefix(Arguments[1])
end)
```

## Creating a Notification Command
```lua
Window:AddCommand('Name', {}, 'Description', function(Arguments, Speaker)
    Window:CreateNotification('Visual Command UI Library', 'Notification', 5)
end)
```

## Adding a Theme (used for SetTheme Command)
```lua
Window:AddTheme('Name', {
    BackgroundColor = Color3.fromRGB(0, 0, 0), -- changes background colour
    SecondaryColor = Color3.fromRGB(0, 0, 0), -- changes Secondary colour
    AccentColor = Color3.fromRGB(0, 0, 0), -- changes Accent colour
    PrimaryTextColor = Color3.fromRGB(0, 0, 0), -- changes PrimartyText colour
    SecondaryTextColor = Color3.fromRGB(0, 0, 0) -- changes SecondaryText colour
})
end)
```
