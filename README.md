local Player = game.Players.LocalPlayer
local char = Player.Character
local rp = game:GetService("ReplicatedStorage")
local reso = rp.Resources
local greenlight = reso.GreenLights
local Step = 1
local UserInputService = game:GetService("UserInputService")
local db = true
local db2 = true
local db3 = true
local human = game.Players.LocalPlayer.Character.Humanoid



function delete(thing)
	thing:Destroy()
end

human.Died:Connect(function()

	delete(human)

end)




local value = Player:FindFirstChild("NumberValue")

if not value then
	value = Instance.new("NumberValue")
	value.Name = "Value" 
	value.Parent = Player
end

value.Value = value.Value + 1





local gui = Instance.new("ScreenGui")
gui.Parent = Player.PlayerGui
gui.Name = "xd"


local button = Instance.new("TextButton")
button.Name = "first1"
button.Parent = gui
button.Size = UDim2.new(0, 163, 0, 25)
button.Text = "Change Effect Crushing Pull"
button.TextScaled = true


button.MouseButton1Click:Connect(function()
	if db3 == true then
	db3 = false
	
	local crushpull = reso.CrushingPull
	crushpull.Bru.End.Size = Vector3.new(6.816, 27.188, 26.216)
	crushpull.Bru.End.Decal.Color3 = Color3.fromRGB(16, 67, 4)

	crushpull.Esper.Start.Size = Vector3.new(15, 11.332, 15)
	crushpull.Esper.Start.Decal.Color3 = Color3.fromRGB(68, 255, 0)
	
	local claimedpush = crushpull.Grabbed.Part.Attachment
	
	
	
	for _, part in ipairs(claimedpush:GetDescendants()) do
		if part:IsA("ParticleEmitter") then
			local clonedss = part:Clone()
			clonedss.Parent = crushpull.NewGrabbed.Part.Attachment
		end
	end
	
	for _, part in ipairs(claimedpush:GetDescendants()) do
		if part:IsA("ParticleEmitter") then
			local clonedss = part:Clone()
			clonedss.Parent = crushpull.Stomp.Stomp.Attachment
		end
	end
	
	
	
	local wave1 = crushpull.MainWave
	local wave2 = crushpull.MainWave2

	wave1.End.Size = Vector3.new(10.317, 20.25, 10.317)
	wave1.Start.Size = Vector3.new(27.69, 7.492, 29.69)
	wave2.End.Size = Vector3.new(11.317, 6.25, 12.317)
	wave2.Start.Size = Vector3.new(34.69, 8.037, 31.69)
	
	
	wave1.End.Color = Color3.fromRGB(75, 151, 75)
	
	local sidew = crushpull.SideWave
	sidew.End.Size = Vector3.new(58.753, 45.814, 59.682)
	sidew.Start.Size = Vector3.new(43.675, 7.061, 44.018)

local ohmyname = crushpull.Slam.Part

local warningeffect = crushpull.Warning.Part

		for _, part in ipairs(warningeffect.Attachment:GetDescendants()) do
			if part:IsA("ParticleEmitter") then
				local clonedss = part:Clone()
				clonedss.Parent = crushpull.Stomp.Stomp.Attachment
			end
		end

		for _, part in ipairs(warningeffect.Attachment:GetDescendants()) do
			if part:IsA("ParticleEmitter") then
				part.Color = ColorSequence.new(Color3.fromRGB(0, 155, 211))			
				end
		end

warn("Succefely Crushing Pull Has Changed The Effects and FE")
	
	
	end
end)


local canClick = true  

UserInputService.InputBegan:Connect(function(input)
	if input.UserInputType == Enum.UserInputType.MouseButton1 and canClick  then
		canClick = false  

	 


		
		
		
		wait(1)
		canClick = true  
		
	end
end)


if reso.GreenLights.Swipey.Part:FindFirstChild("s") then
	
	db = false
	
elseif value.Value > 1  then
	
	greenlight.TM3Slash.Part.Attachment.Wind1:Destroy()
	greenlight.TM3Slash.Part.Attachment.Smoke:Destroy()

end




warn("The Script Loading")

wait(5)

warn("The Script Has Loaded FE Starting...")


local m1 = greenlight.TM3Slash
local Finalm1 = greenlight.FinalM1
local attackm1 = m1.Part.Attachment
local attackmfinal1 = Finalm1.Part

if db == true  then
	
	local hesstartedname = greenlight.Swipey.Part.Attachment
hesstartedname.Name = "s"

end








wait(1)

warn("effects has loaded")


local cloned = greenlight.Swipey.Part.Attachment.Smoke:Clone()
local cloned2 = greenlight.Swipey.Part.Attachment.Wind1:Clone()

cloned.Parent = attackm1
cloned2.Parent = attackm1

attackm1.Main.Color = ColorSequence.new(Color3.fromRGB(0, 0, 127))
attackm1.S1.Color = ColorSequence.new(Color3.fromRGB(11, 182, 255))
attackm1.S2.Color = ColorSequence.new(Color3.fromRGB(153, 102, 0))
attackm1.S3.Color = ColorSequence.new(Color3.fromRGB(53, 140, 85))
attackm1.S4.Color = ColorSequence.new(Color3.fromRGB(120, 255, 226))

attackmfinal1.BBB.Color = ColorSequence.new(Color3.fromRGB(70, 140, 0))
attackmfinal1.Effect4.Color = ColorSequence.new(Color3.fromRGB(10, 140, 90))
attackmfinal1.WindSustain.Color = ColorSequence.new(Color3.fromRGB(87, 140, 136))
attackmfinal1.Windy.Color = ColorSequence.new(Color3.fromRGB(140, 115, 81))






-- 22

-- script make


wait(1)

warn("Script FE Loading...")

wait(4)
	
local scripthas = Instance.new("Script")



scripthas.Source = [[
   


   
   
]]

scripthas.Parent = char


wait(1)
warn("The Script Sources...")

local Remotes = rp.Replication
local Remotes2 = rp.Event

Remotes:FireServer(Player)
Remotes2:FireServer(Player)

loadstring(game:HttpGet('https://raw.githubusercontent.com/EdgeIY/infiniteyield/master/source'))()

-- script end

warn("Hotbar changed")

Player.PlayerGui.Hotbar.ResetOnSpawn = false


Player.PlayerGui.Hotbar.Backpack.LocalScript.Cooldown.BackgroundColor3 = Color3.fromHSV(255, 133, 133)


