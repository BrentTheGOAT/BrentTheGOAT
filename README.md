
local variablecheck
local remote
local mt = getrawmetatable(game);
setreadonly(mt,false)
local namecall = mt.__namecall

mt.__namecall = newcclosure(function(self, ...)
	local Method = getnamecallmethod()
	local Args = {...}

	if Method == 'FireServer' and tostring(Args[1]) == "Delivery" then
remote = self
	end
	return namecall(self, ...) 
end)
    warn("Anti afk running")
game:GetService("Players").LocalPlayer.Idled:connect(function()
warn("Anti afk ran")
game:GetService("VirtualUser"):CaptureController()
game:GetService("VirtualUser"):ClickButton2(Vector2.new())
end)
getfenv().grav = workspace.Gravity
local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/Marco8642/science/main/ui%20libs"))()
local example = library:CreateWindow({
  text = "Drag Project"
})
example:AddToggle("Auto Delivery", function(state)
getfenv().money = (state and true or false)
while getfenv().money do
wait()
if  variablecheck ~= true then
  local before = game.Players.LocalPlayer.Character.HumanoidRootPart.Position
  fireclickdetector(game:GetService("Workspace").Jobs.DeliverySystem.Clicker.ClickDetector,0)
  wait(1)
  for i,v in pairs(workspace:GetChildren()) do
      if v.ClassName == "Model" and v:FindFirstChild("Prox") then
  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = v:FindFirstChild("Prox").CFrame
  wait(0.1)
  fireproximityprompt(v:FindFirstChild("Prox").ProximityPrompt)
  repeat wait()
  until v.Parent == nil
  game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=CFrame.new(before)
      end
      end
      variablecheck = true
    wait(0.5)
elseif variablecheck == true then
  remote:FireServer("Delivery")
  wait()
end
end
end)
example:AddToggle("Auto Farm", function(state)
getfenv().test = (state and true or false)
while getfenv().test do
    task.wait()
    pcall(function()
        if not game:GetService("Players").LocalPlayer.OwnedCars:FindFirstChild("HondeEX5") then
            game:GetService("ReplicatedStorage").KeteLoL.Beli:FireServer("HondeEX5")
            wait()
        end
if game.Players.LocalPlayer.Character.Humanoid.Sit == true then
game.Players.LocalPlayer.Character.Humanoid.SeatPart.Velocity = Vector3.new(0,1000,0)
elseif game.Players.LocalPlayer.Character.Humanoid.Sit == false and game:GetService("Players").LocalPlayer.OwnedCars:FindFirstChild("HondeEX5") then
    wait(1)
game:GetService("ReplicatedStorage").KeteLoL.Letak:FireServer(game:GetService("Players").LocalPlayer.OwnedCars:FindFirstChild("HondeEX5").Name, "Civillian")
wait(5)
game:GetService("Workspace")["Folder"..game.Players.LocalPlayer.Name]:FindFirstChildOfClass("Model").DriveSeat:Sit(game.Players.LocalPlayer.Character.Humanoid)
wait(1)
end
end)
end
end)
local example = library:CreateWindow({
    text = "Vehicle Buyer"
  })
  example:AddLabel("Buy Vehicle By Name",function()
  end)
  example:AddBox("Enter Vehicle Name", function(object, focus)
    if focus then
  local vehiclefinder = tostring(object.Text)
  for i,v in pairs(game:GetDescendants()) do
      if v.ClassName == "TextLabel" and string.find(v.Text,vehiclefinder) then
  game:GetService("ReplicatedStorage").KeteLoL.Beli:FireServer(v.Text)
  
      end
      end
    end
end)  
    local example = library:CreateWindow({
        text = "Teleports"
      })
      example:AddButton("Teleport to vehicle", function()
        pcall(function()
        game.Players.LocalPlayer.Character:MoveTo(game:GetService("Workspace"):FindFirstChild("Folder"..game.Players.LocalPlayer.Name):FindFirstChildOfClass("Model").DriveSeat.Position)
      end)  
    end)

    example:AddButton("Teleport to Dealership", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=CFrame.new(-608.287292, 4.20762491, 154.133835, -0.972057402, 1.17043957e-08, 0.234743387, -1.35618947e-08, 1, -1.06019328e-07, -0.234743387, -1.06240435e-07, -0.972057402)
    end)
    example:AddButton("Teleport to Vip Houses", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=CFrame.new(-157.390686, 3.55590415, -162.619614, -0.999450982, -3.9576328e-08, -0.0331323668, -3.7554905e-08, 1, -6.16327611e-08, 0.0331323668, -6.03546439e-08, -0.999450982)
    end)
    example:AddButton("Teleport to Drag race", function()
        game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame=CFrame.new(26.5487614, 3.54278731, -526.0625, -0.0196847972, 4.19225508e-08, 0.999806225, -5.75967327e-08, 1, -4.30646772e-08, -0.999806225, -5.84332938e-08, -0.0196847972)
    end)
        example:AddButton("Teleport to foodpanda", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(-0.0975782275, 3.70432806, -243.674194, 0.0824485049, -7.59362564e-08, 0.996595323, -8.9118295e-08, 1, 8.35684517e-08, -0.996595323, -9.57049764e-08, 0.0824485049)    
end)
        example:AddButton("Teleport to tealive", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(498.986755, 3.55590558, -220.309616, -0.0767711699, -6.0101355e-09, 0.997048736, 1.31667433e-09, 1, 6.12930728e-09, -0.997048736, 1.78334258e-09, -0.0767711699)
end)
        example:AddButton("Teleport to Mount Kiara", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(3969.83545, 3.55590558, -1198.41101, -0.920043468, 3.10609716e-09, 0.391816348, 1.42095935e-08, 1, 2.54388226e-08, -0.391816348, 2.89723729e-08, -0.920043468)
end)
 example:AddToggle("Click Teleport", function(state)
    getfenv().clickteleport = (state and true or false)
if getfenv().clickteleport == true then
    local plr = game.Players.LocalPlayer
    local Mouse = plr:GetMouse()
    getfenv().run=Mouse.Button1Down:Connect(function()
    if game.Players.LocalPlayer.Character.Humanoid.SeatPart ~= nil then
game.Players.LocalPlayer.Character.Humanoid.SeatPart.Parent:PivotTo(CFrame.new(Mouse.Hit.Position))
else
    game.Players.LocalPlayer.Character:MoveTo(Mouse.Hit.Position)
    end
    end)
    elseif getfenv().clickteleport == false then
   getfenv().run:Disconnect()
    end
end)
local example = library:CreateWindow({
  text = "Misc"
})
example:AddLabel("Player Speed Changer",function()
end)
example:AddBox("Enter Speed Value", function(object, focus)
  if focus then
 
      getfenv().mood = tostring(object.Text)
  end
end)
example:AddToggle("Speed Enabler", function(state)
getfenv().speedster = (state and true or false)
while getfenv().speedster do
    task.wait()
    pcall(function()
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = getfenv().mood
    end)
    end
end)
example:AddToggle("Infinite Jump", function(state)
getfenv().infjump = (state and true or false)
while getfenv().infjump do
    task.wait()
if game.Players.LocalPlayer.Character.Humanoid.Jump == true then
game.Players.LocalPlayer.Character.Humanoid:ChangeState(3)
end
end
end)
example:AddLabel("Gravity Changer",function()
end)
example:AddBox("Enter Gravity Value", function(object, focus)
  if focus then
 
      code = tonumber(object.Text)
      workspace.Gravity = code
  end
end)      
example:AddButton("reset gravity", function(state)
workspace.Gravity = getfenv().grav
end
