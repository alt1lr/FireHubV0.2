local Library = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local Window = Library.CreateLib("Fire Hub [2]", "BloodTheme")

local Tab1 = Window:NewTab("SwordMan Simulator")
local Tab1Section = Tab1:NewSection("SwordMan Simulator")

local Tab2 = Window:NewTab("Eating Simulator")
local Tab2Section = Tab2:NewSection("Eating Simulator")

local Tab3 = Window:NewTab("Anime Sword Simulator")
local Tab3Section = Tab3:NewSection("Anime Sword Simulator")

local Tab5 = Window:NewTab("Step Counter")
local Tab5Section = Tab5:NewSection(" Step Counter")

Tab1Section:NewToggle("Kill Farm", "", function(state)
    if state then
while true do wait(1)
    getgenv().autokill = true
 
if getgenv().autokill then
task.spawn(function()
while getgenv().autokill do
for I, V in pairs(game.Players:GetChildren()) do
local NewPlayerCFrame = V.Character.HumanoidRootPart.CFrame
 
if workspace[V.Name]:FindFirstChild("ForceField") then
print("User is in the safe zone/has a force field.")
else
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = NewPlayerCFrame  
wait(0.5)
getgenv().autokill = false
end
end
end
end)
end
end
    else
game:GetService'TeleportService':TeleportToPlaceInstance(game.PlaceId,game.JobId,game:GetService'Players'.LocalPlayer)
    end
end)

Tab1Section:NewButton("Claim All Chest", "", function()
local old = game.Players.LocalPlayer.Character:getChildren()
for i=1,#old do
if old[i].Name == "HumanoidRootPart" then
lastPos = old[i].CFrame
end
end
wait()
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(657, 556, -203)})
tween:Play()
wait(5)
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(706, 554, -753)})
tween:Play()
wait(5)
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(1305, 555, -68)})
tween:Play()
wait(5)
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(1, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(1323, 554, -51)})
tween:Play()
wait(1)
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(382, 555, 953)})
tween:Play()
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(-212, 556, 242)})
tween:Play()
wait(5)
tweenService, tweenInfo = game:GetService("TweenService"), TweenInfo.new(4, Enum.EasingStyle.Linear)
tween = tweenService:Create(game:GetService("Players")["LocalPlayer"].Character.HumanoidRootPart, tweenInfo, {CFrame = CFrame.new(432, 555, 960)})
tween:Play()
wait(5)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = lastPos
end)

Tab1Section:NewButton("Auto Click", "", function()
local range = 1000

local player = game:GetService("Players").LocalPlayer

game:GetService("RunService").RenderStepped:Connect(function()
    local p = game.Players:GetPlayers()
    for i = 2, #p do local v = p[i].Character
        if v and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v:FindFirstChild("HumanoidRootPart") and player:DistanceFromCharacter(v.HumanoidRootPart.Position) <= range then
            local tool = player.Character and player.Character:FindFirstChildOfClass("Tool")
            if tool and tool:FindFirstChild("Handle") then
                tool:Activate()
                for i,v in next, v:GetChildren() do
                    if v:IsA("BasePart") then
                        firetouchinterest(tool.Handle,v,0)
                        firetouchinterest(tool.Handle,v,1)
                    end
                end
            end
        end
    end
end)
end)

local Tab1Section = Tab1:NewSection("Teleport")

Tab1Section:NewButton("Artic Island", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(869, 553, 47)
end)

Tab1Section:NewButton("King Territory", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(545, 570, 211)
end)

Tab1Section:NewButton("Marine Island", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(511, 553, -349)
end)

Tab2Section:NewToggle("Auto Sell", "", function(state)
    if state then
local range = 1000

local player = game:GetService("Players").LocalPlayer

game:GetService("RunService").RenderStepped:Connect(function()
    local p = game.Players:GetPlayers()
    for i = 2, #p do local v = p[i].Character
        if v and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 and v:FindFirstChild("HumanoidRootPart") and player:DistanceFromCharacter(v.HumanoidRootPart.Position) <= range then
            local tool = player.Character and player.Character:FindFirstChildOfClass("Tool")
            if tool and tool:FindFirstChild("Handle") then
                tool:Activate()
                for i,v in next, v:GetChildren() do
                    if v:IsA("BasePart") then
                        firetouchinterest(tool.Handle,v,0)
                        firetouchinterest(tool.Handle,v,1)
                    end
                end
            end
        end
    end
end)
    else
--active loop
getgenv().autosell = true
 
if getgenv().autosell then
task.spawn(function()
while getgenv().autosell do
for I, V in pairs(game.Players:GetChildren()) do
--Save ps
local old = game.Players.LocalPlayer.Character:getChildren()
for i=1,#old do
if old[i].Name == "HumanoidRootPart" then
lastPos = old[i].CFrame
end
end
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-66, 10, 115)
wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = lastPos
wait(10)
end
end
end)
end
    end
end)

Tab1Section:NewToggle("Auto Sell", "", function(state)
    if state then
--active loop
getgenv().autosell = true
 
if getgenv().autosell then
task.spawn(function()
while getgenv().autosell do
for I, V in pairs(game.Players:GetChildren()) do
--Save ps
local old = game.Players.LocalPlayer.Character:getChildren()
for i=1,#old do
if old[i].Name == "HumanoidRootPart" then
lastPos = old[i].CFrame
end
end
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-66, 10, 115)
wait()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = lastPos
wait(10)
end
end
end)
end
    else
getgenv().autosell = false
    end
end)

local Tab2Section = Tab2:NewSection("Teleport")

Tab2Section:NewButton("Candy Island", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-348, 7042, 803)
end)

Tab2Section:NewButton("Soda Island Island", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-121, 2062, 350)
end)

Tab2Section:NewButton("Shop", "", function()
game.Players.LocalPlayer.Character.Humanoid.RootPart.CFrame = CFrame.new(-142, 11, 120)
end)

Tab3Section:NewToggle("Auto Click", "", function(state)
    if state then
-----auto Tap
getgenv().autotap = true
while getgenv().autotap == true do
   task.wait()
local args = {
   [1] = {}
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("combat attack"):FireServer(unpack(args))
end
    else
getgenv().autotraining = false
    end
end)

Tab3Section:NewToggle("Auto Rebrith", "", function(state)
    if state then
getgenv().autorebirth = true -- change to false to stop
while getgenv().autorebirth == true do
   task.wait()
local args = {
   [1] = {
       [1] = 1
   }
}

game:GetService("ReplicatedStorage").Assets.Events.rebirth:FireServer(unpack(args))
end
    else
getgenv().autorebirth = false
    end
end)

Tab3Section:NewToggle("Auto Train", "", function(state)
    if state then
getgenv().autotraining = true
while getgenv().autotraining == true do
   task.wait()
local args = {
   [1] = {
       [1] = workspace.__MAP.Workouts.Training
   }
}

game:GetService("ReplicatedStorage").Assets.Events.training:InvokeServer(unpack(args))
end
    else

    end
end)

Tab3Section:NewButton("Redeem All Codes", "", function()
------Redeem All Codes
local args = {
   [1] = {
       [1] = "levelup"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "energym"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "awaitseason"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "gmarket"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "???"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "clashzone_fc"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "gseller"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
task.wait(1)
local args = {
   [1] = {
       [1] = "release"
   }
}

game:GetService("ReplicatedStorage").Assets.Events:FindFirstChild("redeem twitter code"):InvokeServer(unpack(args))
end)

Tab5Section:NewToggle("Auto Rebirth", "", function(state)
    if state then
getgenv().autoRb = true
while getgenv().autoRb == true do
local args = {
[1] = "rebirthrequest"
}
game:GetService("ReplicatedStorage").rebirthrequest:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv()autoRb = false
    end
end)

Tab5Section:NewToggle("Auto Step", "", function(state)
    if state then
getgenv().autostep = true
while getgenv().autostep == true do
local args = {
[1] = "stepclickrequest"
}
game:GetService("ReplicatedStorage").stepclickrequest:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autostep = false
    end
end)

Tab5Section:NewToggle("Auto Sell", "", function(state)
    if state then
getgenv().autoSell = true
while getgenv().autoSell == true do
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "SellArea" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait()
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "SellArea" then
         	child.CFrame = CFrame.new(-65, 1, 66)
         	wait(10)
		end
  	end
end
    else
getgenv().autoSell = false
    end
end)

Tab5Section:NewToggle("Auto Get Piece", "", function(state)
    if state then
getgenv().autoPiece = true
while getgenv().autoPiece == true do
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "5piece" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "10piece" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "20piece" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
local children = game.Workspace:GetChildren()
	for _, child in pairs(children) do
  		for _, child in pairs(child:GetChildren()) do
       		table.insert(children, child)
  		 end
  		 if child:IsA("BasePart") and child.Name == "50piece" then
         	child.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
		end
  	end
wait(5)
end
    else
getgenv().autoPiece = false
    end
end)

Tab5Section:NewToggle("Auto Upgrade Step", "", function(state)
    if state then
getgenv().autoUpg = true
while getgenv().autoUpg == true do
local args = {
[1] = "upgrademysteps"
}
game:GetService("ReplicatedStorage").upgrademysteps:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autoUpg = false
    end
end)

Tab5Section:NewToggle("Auto Upgrade Max", "", function(state)
    if state then
getgenv().autoUpgm = true
while getgenv().autoUpgm == true do
local args = {
[1] = "upgrademymaxsteps"
}
game:GetService("ReplicatedStorage").upgrademymaxsteps:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autoUpgm = false
    end
end)

local Tab4 = Window:NewTab("Nen Fighting Simulator")
local Tab4Section = Tab4:NewSection("Nen Fighting Simulator")

local Tab6 = Window:NewTab("Tower Of Hell")
local Tab6Section = Tab6:NewSection("Tower Of Hell")

local Tab7 = Window:NewTab("Prison Life")
local Tab7Section = Tab7:NewSection("Prison Life")

local Tab8 = Window:NewTab("Credits")
local Tab8Section = Tab8:NewSection("Ui: Kavo Ui Libary")
local Tab8Section = Tab8:NewSection("Kavo Ui Made By Xheptc")
local Tab8Section = Tab8:NewSection("Discord: alt1lr#9459")
local Tab8Section = Tab8:NewSection("Youtube: Fire")
local Tab8Section = Tab8:NewSection("Password Gui: Red Coat#5495")

Tab4Section:NewToggle("Auto Strenght", "", function(state)
    if state then
------Auto Strength
getgenv().autostr = true
while getgenv().autostr == true do
local args = {
[1] = "str"
}
game:GetService("ReplicatedStorage").Remotes.train:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autostr = false
    end
end)

Tab4Section:NewToggle("Auto Agility", "", function(state)
    if state then
------Auto Agility
getgenv().autoagi = true
while getgenv().autoagi == true do
local args = {
[1] = "agi"
}
game:GetService("ReplicatedStorage").Remotes.train:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autoagi = false
    end
end)

Tab4Section:NewToggle("Auto Nen", "", function(state)
    if state then
-----Auto Nen
getgenv().autonen = true
while getgenv().autonen == true do
local args = {
[1] = "nen"
}
game:GetService("ReplicatedStorage").Remotes.train:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autonen = false
    end
end)

Tab4Section:NewToggle("Auto Durability", "", function(state)
    if state then
------Auto Durability
getgenv().autodura = true
while getgenv().autodura == true do
local args = {
[1] = "dur"
}
game:GetService("ReplicatedStorage").Remotes.train:FireServer(unpack(args))
wait(0.1)
end
    else
getgenv().autodura = false
    end
end)

Tab6Section:NewToggle("Auto Farm 1", "", function(state)
    if state then
while true do wait(0.1)
local endzone = game.Workspace.tower.sections.finish.FinishGlow.CFrame
 
    local player = game.Players.LocalPlayer.Character
    player.HumanoidRootPart.CFrame = endzone
wait(1)
end
    else
game:GetService'TeleportService':TeleportToPlaceInstance(game.PlaceId,game.JobId,game:GetService'Players'.LocalPlayer)
    end
end)

Tab6Section:NewButton("Get Tool", "", function()
    for _,e in pairs(game.Players.LocalPlayer.Backpack:GetDescendants()) do
        if e:IsA("Tool") then
        e:Destroy()
        end
        end
        wait() 
        for _,v in pairs(game.ReplicatedStorage.Gear:GetDescendants()) do
        if v:IsA("Tool") then
        local CloneThings = v:Clone()
        wait()
        CloneThings.Parent = game.Players.LocalPlayer.Backpack
 
        end
        end
end)

Tab6Section:NewButton("God Mode", "", function()
for i,v in pairs(game:GetService("Workspace").tower:GetDescendants()) do
        if v:IsA("BoolValue") and v.Name == "kills" then
            v.Parent:Destroy()
        end
    end
end)

local Tab7Section = Tab7:NewSection("Guns")

Tab7Section:NewDropdown("Give Gun {M4A1 Need Gamepass}", "Gives  Gun", {"M9", "Remington 870", "AK-47", "M4A1"}, function(v)
   local A_1 = game:GetService("Workspace")["Prison_ITEMS"].giver[v].ITEMPICKUP
   local Event = game:GetService("Workspace").Remote.ItemHandler
   Event:InvokeServer(A_1)
end)

Tab7Section:NewDropdown("Gun Mod", "Makes the gun op", {"M9", "Remington 870", "AK-47"}, function(v)
      local module = nil
      if game:GetService("Players").LocalPlayer.Backpack:FindFirstChild(v) then
          module = require(game:GetService("Players").LocalPlayer.Backpack[v].GunStates)
      elseif game:GetService("Players").LocalPlayer.Character:FindFirstChild(v) then
          module = require(game:GetService("Players").LocalPlayer.Character[v].GunStates)
      end
      if module ~= nil then
          module["MaxAmmo"] = math.huge
          module["CurrentAmmo"] = math.huge
          module["StoredAmmo"] = math.huge
          module["FireRate"] = 0.000001
          module["Spread"] = 0
          module["Range"] = math.huge
          module["Bullets"] = 10
          module["ReloadTime"] = 0.000001
          module["AutoFire"] = true
     end
end)

local Tab7Section = Tab7:NewSection("Teleports")

Tab7Section:NewButton("Outside Of Outside Prison", "Teleports You outside of the prison!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(451.6684265136719, 98.0399169921875, 2216.338134765625)
end)
            
Tab7Section:NewButton("Cafeteria", "Teleports you to the Cafeteria!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(918.994873046875, 99.98993682861328, 2325.73095703125)
end)

Tab7Section:NewButton("Prison Yard", "Teleports You to the Prison Yard", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(736.4671630859375, 97.99992370605469, 2517.583740234375)
end)
            
Tab7Section:NewButton("Kitchen", "Teleports You to the Kitchen!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(906.641845703125, 99.98993682861328, 2237.67333984375)
end)
            
Tab7Section:NewButton("Prison Cells", "Teleports You to the Prison Cells!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(919.5551147460938, 99.98998260498047, 2441.700927734375)
end)
            
Tab7Section:NewButton("Surveilance Room", "Teleports You to the Surveilance Room!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(795.251953125, 99.98998260498047, 2327.720703125)
end)
            
Tab7Section:NewButton("Break Room", "Teleports You to the Break Room!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(800.0896606445312, 99.98998260498047, 2266.71630859375)
end)
            
Tab7Section:NewButton("Police Armory", "Teleports You to the Police Armory!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(837.2889404296875, 99.98998260498047, 2270.99658203125)
end)

Tab7Section:NewButton("Police Room", "Teleports to to the Police Room", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(836.5386352539062, 99.98998260498047, 2320.604248046875)
end)
            
Tab7Section:NewButton("Cafeteria", "Teleports you to the Cafeteria!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(918.994873046875, 99.98993682861328, 2325.73095703125)
end)
   
Tab7Section:NewButton("Criminal Base Inside", "Teleports you to the Criminal Base Inside!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-975.8451538085938, 109.32379150390625, 2053.11376953125)
end)

Tab7:NewButton("Prison Cells", "Teleports You to the Prison Cells!", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(919.5551147460938, 99.98998260498047, 2441.700927734375)
end)
