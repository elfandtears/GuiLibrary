# GuiLibrary
Simple Gui library

Usage examples:

For example you want create screen gui, for this you need:

1: load gui library

GuiLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/elfandtears/GuiLibrary/main/source.lua"))()

2:

If you want create ScreenGui first you need create table with properties:

ScreenGuiProperties = {Name = "ScreenGUI", ResetOnSpawn = false, Parent = game.CoreGui}

3:

After that call function with properties table in args:

GuiLibrary.ScreenGUI(ScreenGuiProperties)

Done! now you created ScreenGui

GuiLibrary function return you gui instance so you can use them:

ScreenGUIMain = GuiLibrary.ScreenGUI(ScreenGuiProperties)

ScreenGUIMain.Name = "ScreenGUI2"

ScreenGUIMain:Destroy()

GuiLibrary functions:

GuiLibrary.ScreenGUI, GuiLibrary.TextLabel, GuiLibrary.TextButton, GuiLibrary.ImageLabel, GuiLibrary.ImageButton, GuiLibrary.Frame, GuiLibrary.ViewportFrame, GuiLibrary.UICorner

Also you can make gui draggable or attach gui to other gui:

GuiLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/elfandtears/GuiLibrary/main/source.lua"))()

ScreenGuiProperties = {Name = "ScreenGUI", ResetOnSpawn = false, Parent = game.CoreGui}

ScreenGUIMain = GuiLibrary.ScreenGUI(ScreenGuiProperties)

FrameProperties = {Name = "Draggable", AnchorPoint = Vector2.new(0.5, 0.5), Position = UDim2.new(0.5, 0, 0.5, 0), Size = UDim2.new(0, 300, 0, 300), Parent = ScreenGUIMain, Draggable_ = true} -- <-- Draggable_ allow you to drag gui

Frame = GuiLibrary.Frame(FrameProperties)

Done! now you can drag your frame

attach useful when you want make borders with UICorner:

GuiLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/elfandtears/GuiLibrary/main/source.lua"))()

ScreenGuiProperties = {Name = "ScreenGUI", ResetOnSpawn = false, Parent = game.CoreGui}

ScreenGUIMain = GuiLibrary.ScreenGUI(ScreenGuiProperties)

FrameProperties = {Name = "Draggable", AnchorPoint = Vector2.new(0.5, 0.5), ZIndex = 2, Position = UDim2.new(0.5, 0, 0.5, 0), Size = UDim2.new(0, 300, 0, 300), Parent = ScreenGUIMain, Draggable_ = true}

Frame = GuiLibrary.Frame(FrameProperties)

FrameProperties2 = {Name = "DraggableBorder", AnchorPoint = Vector2.new(0.5, 0.5), Position = UDim2.new(0.5, 0, 0.5, 0), Size = UDim2.new(0, 330, 0, 330), Parent = ScreenGUIMain, attach = Frame} <-- 'attach' attach your gui to other gui

FrameBorders = GuiLibrary.Frame(FrameProperties2)

UICornerProperties1 = {Name = "UICorner", CornerRadius = UDim.new(0, 8), Parent = Frame}

UICornerProperties2 = {Name = "UICorner", CornerRadius = UDim.new(0, 8), Parent = FrameBorders}

GuiLibrary.UICorner(UICornerProperties1)

GuiLibrary.UICorner(UICornerProperties2)

Done! now you can drag your Frame with UICorner and borders!
