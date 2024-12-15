local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()
--//

local Window = Fluent:CreateWindow({
    Title = "Kamui x hub", --Título do seu Hub
    SubTitle = "by Junior",--sub título do seu Hub
    TabWidth = 160,
    Size = UDim2.fromOffset(560, 350),--Largura e Estatura do seu hub / Tamanho.
    Acrylic = true, --Blur
    Theme = "Darker",--Temas da cor: [ Dark, Darker, White, Rose, Aqua, Amethyst.
    MinimizeKey = Enum.KeyCode.LeftControl --Key para minimizar o seu hub
})
--//

local Tabs = {
   Main = Window:AddTab({ Title = "teste", Icon = "cloud" }),
   Settings = Window:AddTab({ Title = "Settings", Icon = "settings" })
}

local Toggle = Tabs.Main:AddToggle("MyToggle", {Title = "Toggle", Default = false })

    Toggle:OnChanged(function()
    --função do toggle
        print("Toggle changed:", Options.MyToggle.Value)
    end)

    Options.MyToggle:SetValue(false)
--[[
Title = "Toggle", -- Título do botão
Default = false }) -- Valor booleano ( true / false) 
]]
