-- BASEPLATE GAME SCRIPT
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("EscapeHead - Made by @c.o.u.r.t.l.a.n.d on YT", "BloodTheme")

if game.PlaceId == 5194438573 then
    -- MAIN
    local Main = Window:NewTab("Main")
    local MainSection = Main:NewSection("Main")


    MainSection:NewButton("Become The Boss", "ONLY DO THIS ON THE BOSS ROUND", function()
        game:GetService("Players").LocalPlayer.GamePasses.BecameBoss.Value = true
    end)

    MainSection:NewToggle("Double Jump", "tehehehehe", function(state)
        game:GetService("Players").LocalPlayer.GamePasses.DoubleJump.Value = true
    end)

    MainSection:NewButton("Skip Stage", "idk what to put here tbh", function()
        game:GetService("Players").LocalPlayer.GamePasses.SkipStage.Value = true
    end)


    --LOCAL PLAYER
    local Player = Window:NewTab("Player")
    local PlayerSection = Player:NewSection("Player")

    PlayerSection:NewSlider("Walkspeed", "SPEED!!", 500, 16, function(s)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = s
    end)

    PlayerSection:NewSlider("Jumppower", "JUMP HIGH!!", 350, 50, function(s)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = s
    end)

    PlayerSection:NewButton("Reset WS/JP", "Resets to all defaults", function()
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
    end)


    --Other
    local Other = Window:NewTab("Other")
    local OtherSection = Other:NewSection("Other")

    OtherSection:NewButton("Chat Spoofer", "Lets you chat for other people", function()
        loadstring(game:HttpGet(('https://pastebin.com/raw/djBfk8Li'),true))()
    end)

    OtherSection:NewButton("Bypassed Fly", "bird mode", function()
        loadstring(game:HttpGet("https://raw.githubusercontent.com/Nicuse/RobloxScripts/main/BypassedFly.lua"))() 
    end)
