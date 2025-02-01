-- Banana Hub Script for Blox Fruits (Xeno 1.1.4)
repeat wait() until game:IsLoaded()

local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Banana Hub - Blox Fruits", "DarkTheme")

-- Auto Farm Tab
local AutoFarmTab = Window:NewTab("Auto Farm")
local AutoFarmSection = AutoFarmTab:NewSection("Auto Farm Settings")

AutoFarmSection:NewToggle("Auto Farm Level", "Tự động farm quái theo level", function(state)
    _G.AutoFarm = state
    while _G.AutoFarm do
        wait()
        -- Auto Farm Code Here
    end
end)

AutoFarmSection:NewButton("Auto Quest", "Tự động nhận nhiệm vụ", function()
    -- Auto Quest Code Here
end)

-- Teleport Tab
local TeleportTab = Window:NewTab("Teleport")
local TeleportSection = TeleportTab:NewSection("Teleport Settings")

TeleportSection:NewButton("Teleport To Second Sea", "Di chuyển đến Second Sea", function()
    game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(0, 100, 0) -- Change to correct coordinates
end)

-- ESP Tab
local ESPTab = Window:NewTab("ESP")
local ESPSection = ESPTab:NewSection("ESP Features")

ESPSection:NewToggle("ESP Players", "Hiển thị vị trí người chơi", function(state)
    _G.ESPPlayers = state
    while _G.ESPPlayers do
        wait()
        -- ESP Players Code Here
    end
end)

ESPSection:NewToggle("ESP Devil Fruits", "Hiển thị trái ác quỷ", function(state)
    _G.ESPDevilFruits = state
    while _G.ESPDevilFruits do
        wait()
        -- ESP Devil Fruits Code Here
    end
end)

-- Misc Tab
local MiscTab = Window:NewTab("Misc")
local MiscSection = MiscTab:NewSection("Other Features")

MiscSection:NewButton("Infinite Energy", "Năng lượng vô hạn", function()
    game.Players.LocalPlayer.Character.Energy.Value = 999999
end)

Library:Init()

