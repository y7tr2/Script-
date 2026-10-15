-- Why do i love gpt 5.6 sol high the reason is below.
-- dsc.gg/oxyenv 

local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local HttpService = game:GetService("HttpService")
local str = "https://lostheaven.site"
local str2 = "11"
local localPlayer = Players.LocalPlayer

local function fn()
	local str3 = str .. "/api/script-status/" .. str2

	local ok, result = pcall(function()
		return game:HttpGet(str3)
	end)

	if not ok then
		return false, "ÙØ´Ù Ø§ÙØ§ØªØµØ§Ù Ø¨Ø§ÙØ³ÙØ±ÙØ±"
	end
	local data = nil
	if not pcall(function()
		data = HttpService:JSONDecode(result)
	end) or not data then
		return false, "Ø®Ø·Ø£ ÙÙ Ø§Ø³ØªØ¬Ø§Ø¨Ø© Ø§ÙØ³ÙØ±ÙØ±"
	end

	if not data.active then
		return false, data.message or "â Ø§ÙØ³ÙØ±ÙØ¨Øª ÙØªÙÙÙ ÙÙ ÙØ¨Ù Ø§ÙØ£Ø¯ÙÙ"
	end
	return true, "â Ø§ÙØ³ÙØ±ÙØ¨Øª Ø´ØºØ§Ù"
end

local function fn2(arg)
	pcall(function()
		local v = StarterGui
		local setCore = v.SetCore
		local tbl = { Title = "ð ØªÙ Ø¥ÙÙØ§Ù Ø§ÙØ³ÙØ±ÙØ¨Øª" }
		local v2 = arg
		local text

		if arg then
			text = v2
		else
			text = "ØªÙ Ø¥ÙÙØ§Ù ÙØ°Ø§ Ø§ÙØ³ÙØ±ÙØ¨Øª ÙÙ ÙÙØ­Ø© Ø§ÙØªØ­ÙÙ"
		end

		tbl.Text = text
		tbl.Duration = 5
		setCore(v, "SendNotification", tbl)
	end)

	wait(1)

	pcall(function()
		local v = localPlayer
		local kick = v.Kick
		local v2 = arg
		local str3

		if arg then
			str3 = v2
		else
			str3 = "â Ø§ÙØ³ÙØ±ÙØ¨Øª ÙØªÙÙÙ"
		end

		kick(v, str3)
	end)
end

if not (function()
	local v, v2 = fn()
	if not v then
		fn2(v2)
		return false
	end

	pcall(function()
		StarterGui:SetCore("SendNotification", { Title = "ð Ø§ÙØ³ÙØ±ÙØ¨Øª ÙØ±Ø¨ÙØ· Ø¨Ø§ÙØ³ÙØ±ÙØ±", Text = "â Ø¥Ø°Ø§ Ø£ÙÙÙÙ Ø§ÙØ£Ø¯ÙÙ Ø³ÙØªÙÙÙ Ø¹ÙØ¯Ù ÙÙØ±Ø§Ù", Duration = 3 })
	end)

	spawn(function()
		local v3, v4

		repeat
			wait(10)
			v3, v4 = fn()
		until not v3

		fn2(v4)
	end)

	return true
end)() then
	return
end

pcall(function()
	local Workspace, UserInputService, VirtualInputManager, ReplicatedStorage, RunService, TweenService, HttpService2, GuiService, currentCamera, localPlayer2
	local playerGui, send, get, image, image2, color, color2, color3, SliderMinigame, fn3
	local fn4, fn5, tbl, tbl2, vector, vector2, vector3, vector4, vector5, n
	local flag, n2, n3, tbl3, v, flag2, visible, flag3, flag4, flag5
	local flag6, tbl4, tbl5, tbl6, tbl7, flag7, tbl8, vector22, flag8, tbl9
	local n4, n5, n6, tbl10, tbl11, tbl12, fn6, fn7, fn8, fn9
	local fn10, fn11, screenGui

	do
		local Players2 = game:GetService("Players")
		Workspace = game:GetService("Workspace")
		UserInputService = game:GetService("UserInputService")
		VirtualInputManager = game:GetService("VirtualInputManager")
		ReplicatedStorage = game:GetService("ReplicatedStorage")
		RunService = game:GetService("RunService")
		TweenService = game:GetService("TweenService")
		local CoreGui = game:GetService("CoreGui")
		HttpService2 = game:GetService("HttpService")
		GuiService = game:GetService("GuiService")
		currentCamera = workspace.CurrentCamera
		localPlayer2 = Players2.LocalPlayer
		playerGui = localPlayer2:WaitForChild("PlayerGui")
		local remotes = ReplicatedStorage:WaitForChild("Remotes")
		send = remotes:WaitForChild("Send")
		get = remotes:WaitForChild("Get")
		image = "rbxassetid://125670041024227"
		image2 = "rbxassetid://125670041024227"
		local image3 = "rbxassetid://102417071284466"
		local image4 = "rbxassetid://71362331575679"
		color = Color3.fromRGB(255, 255, 255)
		color2 = Color3.fromRGB(180, 180, 180)
		color3 = Color3.fromRGB(255, 255, 255)
		SliderMinigame = nil

		task.spawn(function()
			while not SliderMinigame do
				pcall(function()
					SliderMinigame = require(ReplicatedStorage.Modules.Game.Minigames.SliderMinigame)
				end)

				if not SliderMinigame then
					task.wait(1)
				end
			end
		end)

		local v2 = nil
		local n7 = 0
		local n8 = 0

		fn3 = function()
			if v2 and type(rawget(v2, "event")) == "number" and type(rawget(v2, "func")) == "number" then
				return v2
			end

			pcall(function()
				local v3 = ipairs
				local tbl13 = getgc and getgc(true) or {}

				for _, v4 in v3(tbl13) do
					if typeof(v4) == "table" and rawget(v4, "event") and rawget(v4, "func") then
						v2 = v4
						break
					end
				end
			end)

			return v2
		end

		fn4 = function()
			local v3 = fn3()
			if v3 and type(v3.event) == "number" then
				v3.event = v3.event + 1
				return v3.event
			end
			n7 += 1
			return n7
		end

		fn5 = function()
			local v3 = fn3()
			if v3 and type(v3.func) == "number" then
				v3.func = v3.func + 1
				return v3.func
			end
			n8 += 1
			return n8
		end

		tbl = {
			["SIZE:0.1,0.7,1.7"] = "Perch",
			["SIZE:0.3,2.1,5.9"] = "Sailfish",
			["SIZE:0.8,2.6,6.6"] = "Marlin",
			["SIZE:0.5,1.7,4.2"] = "Coelacanth",
			["SIZE:0.2,0.9,2.3"] = "Bass",
			["SIZE:0.3,0.9,2.8"] = "Salmon",
			["SIZE:0.3,1.7,4.0"] = "DolphinFish",
			["SIZE:0.5,2.6,5.0"] = "Tuna",
			["SIZE:0.4,0.9,4.0"] = "Northern Pike",
		}

		tbl2 = {
			"Perch",
			"Bass",
			"Salmon",
			"DolphinFish",
			"Northern Pike",
			"Coelacanth",
			"Tuna",
			"Sailfish",
			"Marlin",
		}

		vector = Vector3.new(84.30732, 245.122, 922.7863)
		vector2 = Vector3.new(-226.11766, 245.67188, 837.35205)
		vector3 = Vector3.new(86.63267, 245.36505, 925.0908)
		vector4 = Vector3.new(88.21969, 245.08421, 922.4281)
		vector5 = Vector3.new(84.30732, 245.122, 922.7863)
		n = 1
		flag = false
		n2 = 0
		n3 = 0
		tbl3 = {}
		v = nil
		flag2 = false
		visible = false
		flag3 = false
		flag4 = false
		flag5 = false
		flag6 = false
		tbl4 = {}
		tbl5 = {}
		tbl6 = {}
		tbl7 = {}
		flag7 = false
		tbl8 = {}
		vector22 = nil
		flag8 = false
		tbl9 = {}
		n4 = 1
		n5 = 2
		n6 = 100
		tbl10 = {}
		tbl11 = {}
		tbl12 = { Webhook = "", EnabledFish = {}, Everyone = true, Enabled = true, EspEnabled = true }

		for _, v3 in ipairs(tbl2) do
			tbl4[v3] = true
			tbl5[v3] = false
			tbl6[v3] = false
			tbl7[v3] = false
			tbl12.EnabledFish[v3] = true
		end

		local str3 = "LostHeavenHub/config.json"

		local function fn12()
			if makefolder and not isfolder("LostHeavenHub") then
				pcall(makefolder, "LostHeavenHub")
			end
		end

		fn6 = function()
			fn12()

			if writefile then
				pcall(function()
					writefile(str3, HttpService2:JSONEncode(tbl12))
				end)
			end
		end

		local function fn13()
			if isfile and isfile(str3) and readfile then
				local ok, result = pcall(function()
					return HttpService2:JSONDecode(readfile(str3))
				end)

				if ok and type(result) == "table" then
					tbl12.Webhook = result.Webhook or ""
					tbl12.Everyone = result.Everyone ~= false
					tbl12.Enabled = result.Enabled ~= false
					tbl12.EspEnabled = result.EspEnabled ~= false

					if type(result.EnabledFish) == "table" then
						for _, v3 in ipairs(tbl2) do
							if result.EnabledFish[v3] ~= nil then
								tbl12.EnabledFish[v3] = result.EnabledFish[v3]
							end
						end
					end
				end
			end
		end

		fn13()

		fn7 = function(arg)
			if arg == "Sailfish" or arg == "Marlin" then
				return Color3.fromRGB(255, 215, 0)
			end

			if arg == "Tuna" then
				return Color3.fromRGB(170, 0, 255)
			end

			if arg == "Coelacanth" then
				return Color3.fromRGB(0, 130, 255)
			end

			if arg == "Northern Pike" or arg == "DolphinFish" then
				return Color3.fromRGB(0, 255, 80)
			end

			if arg == "Bass" or arg == "Salmon" or arg == "Perch" then
				return Color3.fromRGB(120, 120, 120)
			end
			return Color3.fromRGB(255, 255, 255)
		end

		fn8 = function(arg)
			local isBasePart = arg:IsA("BasePart") and arg or arg:IsA("Model") and (arg.PrimaryPart or arg:FindFirstChildWhichIsA("BasePart"))
			if isBasePart then
				return string.format("SIZE:%.1f,%.1f,%.1f", isBasePart.Size.X, isBasePart.Size.Y, isBasePart.Size.Z)
			end
			return nil
		end

		fn9 = function(arg)
			if not arg then
				return nil
			end

			if arg:IsA("BasePart") then
				return arg
			end

			if arg:IsA("Model") then
				local handle = arg:FindFirstChild("Handle") or arg.PrimaryPart
				if handle and handle:IsA("BasePart") then
					return handle
				end

				for _, descendant in ipairs(arg:GetDescendants()) do
					if descendant:IsA("BasePart") then
						return descendant
					end
				end
			end

			return nil
		end

		fn10 = function(arg, arg2)
			local cFrame = arg.CFrame
			local size = arg.Size
			local v3 = cFrame:PointToObjectSpace(arg2)
			local clamp = math.clamp
			local z = v3.Z
			local n9 = -size.Z / 2
			local n10 = size.Z / 2
			local vector6 = Vector3.new(math.clamp(v3.X, -size.X / 2, size.X / 2), math.clamp(v3.Y, -size.Y / 2, size.Y / 2), clamp(z, n9, n10))
			return (cFrame:PointToWorldSpace(vector6) - arg2).Magnitude
		end

		fn11 = function(parent)
			local imageLabel = Instance.new("ImageLabel")
			imageLabel.Size = UDim2.new(0, 90, 0, 110)
			imageLabel.Position = UDim2.new(0, -25, 0, -20)
			imageLabel.BackgroundTransparency = 1
			imageLabel.Image = image3
			imageLabel.Rotation = -15
			imageLabel.ZIndex = (parent.ZIndex or 1) + 1
			imageLabel.Parent = parent
			local imageLabel2 = Instance.new("ImageLabel")
			imageLabel2.Size = UDim2.new(0, 90, 0, 110)
			imageLabel2.Position = UDim2.new(1, -65, 0, -20)
			imageLabel2.BackgroundTransparency = 1
			imageLabel2.Image = image4
			imageLabel2.Rotation = 15
			imageLabel2.ZIndex = (parent.ZIndex or 1) + 1
			imageLabel2.Parent = parent
		end

		screenGui = Instance.new("ScreenGui")
		screenGui.Name = "LostHeavenHub"
		screenGui.ResetOnSpawn = false

		local function fn14()
			if gethui then
				screenGui.Parent = gethui()
				return
			end

			if not pcall(function()
				if protectgui then
					protectgui(screenGui)
				elseif syn and syn.protect_gui then
					syn.protect_gui(screenGui)
				end

				screenGui.Parent = CoreGui
			end) or not screenGui.Parent then
				pcall(function()
					screenGui.Parent = localPlayer2:WaitForChild("PlayerGui")
				end)
			end
		end

		fn14()
	end

	local imageLabel
	imageLabel = Instance.new("ImageLabel")
	imageLabel.Size = UDim2.new(0, 380, 0, 180)
	imageLabel.Position = UDim2.new(0.5, -190, 0.5, -90)
	imageLabel.BackgroundColor3 = color
	imageLabel.BackgroundTransparency = 0
	imageLabel.Image = image
	imageLabel.ScaleType = Enum.ScaleType.Slice
	imageLabel.SliceCenter = Rect.new(100, 100, 100, 100)
	imageLabel.Active = true
	imageLabel.Draggable = true
	imageLabel.Visible = true
	imageLabel.Parent = screenGui
	Instance.new("UICorner", imageLabel).CornerRadius = UDim.new(0, 15)
	local uiStroke = Instance.new("UIStroke", imageLabel)
	uiStroke.Color = color2
	uiStroke.Thickness = 1.5
	fn11(imageLabel)
	local textLabel = Instance.new("TextLabel")
	textLabel.Size = UDim2.new(1, 0, 0, 50)
	textLabel.Position = UDim2.new(0, 0, 0, 20)
	textLabel.BackgroundTransparency = 1
	textLabel.Text = "W E L C O M E   T O   H E A V E N"
	textLabel.TextColor3 = Color3.fromRGB(50, 50, 50)
	textLabel.Font = Enum.Font.Bodoni
	textLabel.TextSize = 20
	textLabel.ZIndex = 2
	textLabel.Parent = imageLabel
	local textButton
	textButton = Instance.new("TextButton")
	textButton.Size = UDim2.new(0, 180, 0, 45)
	textButton.Position = UDim2.new(0.5, -90, 0, 95)
	textButton.BackgroundColor3 = Color3.fromRGB(240, 240, 240)
	textButton.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton.Font = Enum.Font.GothamBold
	textButton.TextSize = 15
	textButton.Text = "Click to Enter"
	textButton.ZIndex = 2
	textButton.Parent = imageLabel
	Instance.new("UICorner", textButton).CornerRadius = UDim.new(0, 8)
	local uiStroke2 = Instance.new("UIStroke", textButton)
	uiStroke2.Color = color2
	uiStroke2.Thickness = 1
	local imageLabel2
	imageLabel2 = Instance.new("ImageLabel")
	imageLabel2.Size = UDim2.new(0, 350, 0, 150)
	imageLabel2.Position = UDim2.new(0.5, -175, 0.5, -75)
	imageLabel2.BackgroundColor3 = color
	imageLabel2.BackgroundTransparency = 0
	imageLabel2.Image = image
	imageLabel2.ScaleType = Enum.ScaleType.Slice
	imageLabel2.SliceCenter = Rect.new(100, 100, 100, 100)
	imageLabel2.Active = true
	imageLabel2.Draggable = true
	imageLabel2.Visible = false
	imageLabel2.Parent = screenGui
	Instance.new("UICorner", imageLabel2).CornerRadius = UDim.new(0, 15)
	local uiStroke3 = Instance.new("UIStroke", imageLabel2)
	uiStroke3.Color = color2
	uiStroke3.Thickness = 1.5
	fn11(imageLabel2)
	local textLabel2 = Instance.new("TextLabel")
	textLabel2.Size = UDim2.new(1, 0, 0, 50)
	textLabel2.BackgroundTransparency = 1
	textLabel2.Text = "Select Platform"
	textLabel2.TextColor3 = Color3.fromRGB(50, 50, 50)
	textLabel2.Font = Enum.Font.GothamBold
	textLabel2.TextSize = 18
	textLabel2.ZIndex = 2
	textLabel2.Parent = imageLabel2
	local textButton2
	textButton2 = Instance.new("TextButton")
	textButton2.Size = UDim2.new(0, 140, 0, 50)
	textButton2.Position = UDim2.new(0, 25, 0, 65)
	textButton2.BackgroundColor3 = color3
	textButton2.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton2.Font = Enum.Font.GothamBold
	textButton2.TextSize = 14
	textButton2.Text = "Mobile"
	textButton2.ZIndex = 2
	textButton2.Parent = imageLabel2
	Instance.new("UICorner", textButton2).CornerRadius = UDim.new(0, 8)
	local uiStroke4 = Instance.new("UIStroke", textButton2)
	uiStroke4.Color = color2
	uiStroke4.Thickness = 1
	local textButton3
	textButton3 = Instance.new("TextButton")
	textButton3.Size = UDim2.new(0, 140, 0, 50)
	textButton3.Position = UDim2.new(1, -165, 0, 65)
	textButton3.BackgroundColor3 = color3
	textButton3.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton3.Font = Enum.Font.GothamBold
	textButton3.TextSize = 14
	textButton3.Text = "PC"
	textButton3.ZIndex = 2
	textButton3.Parent = imageLabel2
	Instance.new("UICorner", textButton3).CornerRadius = UDim.new(0, 8)
	local uiStroke5 = Instance.new("UIStroke", textButton3)
	uiStroke5.Color = color2
	uiStroke5.Thickness = 1
	local imageLabel3
	imageLabel3 = Instance.new("ImageLabel")
	imageLabel3.Size = UDim2.new(0, 260, 0, 435)
	imageLabel3.Position = UDim2.new(0, 20, 0.5, -217)
	imageLabel3.BackgroundColor3 = color
	imageLabel3.BackgroundTransparency = 0
	imageLabel3.Image = image2
	imageLabel3.ScaleType = Enum.ScaleType.Slice
	imageLabel3.SliceCenter = Rect.new(100, 100, 100, 100)
	imageLabel3.Active = true
	imageLabel3.Draggable = true
	imageLabel3.Visible = false
	imageLabel3.Parent = screenGui
	Instance.new("UICorner", imageLabel3).CornerRadius = UDim.new(0, 15)
	local uiStroke6 = Instance.new("UIStroke", imageLabel3)
	uiStroke6.Color = color2
	uiStroke6.Thickness = 1.5
	fn11(imageLabel3)
	local textLabel3 = Instance.new("TextLabel")
	textLabel3.Size = UDim2.new(1, 0, 0, 30)
	textLabel3.Position = UDim2.new(0, 0, 0, 8)
	textLabel3.BackgroundTransparency = 1
	textLabel3.Text = "L O S T   H E A V E N"
	textLabel3.TextColor3 = Color3.fromRGB(40, 40, 40)
	textLabel3.Font = Enum.Font.Bodoni
	textLabel3.TextSize = 20
	textLabel3.ZIndex = 2
	textLabel3.Parent = imageLabel3
	local textButton4, textButton5, textButton6, textButton7

	do
		local frame = Instance.new("Frame")
		frame.Size = UDim2.new(1, -20, 0, 34)
		frame.Position = UDim2.new(0, 10, 0, 42)
		frame.BackgroundTransparency = 1
		frame.ZIndex = 2
		frame.Parent = imageLabel3
		textButton4 = Instance.new("TextButton")
		textButton4.Size = UDim2.new(0, 56, 0, 34)
		textButton4.Position = UDim2.new(0, 0, 0, 0)
		textButton4.BackgroundColor3 = color3
		textButton4.Text = "ð Web"
		textButton4.TextSize = 11
		textButton4.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton4.Font = Enum.Font.GothamBold
		textButton4.ZIndex = 2
		textButton4.Parent = frame
		Instance.new("UICorner", textButton4).CornerRadius = UDim.new(0, 8)
		local uiStroke7 = Instance.new("UIStroke", textButton4)
		uiStroke7.Color = color2
		uiStroke7.Thickness = 1
		textButton5 = Instance.new("TextButton")
		textButton5.Size = UDim2.new(0, 56, 0, 34)
		textButton5.Position = UDim2.new(0, 62, 0, 0)
		textButton5.BackgroundColor3 = color3
		textButton5.Text = "â­ï¸ Skip"
		textButton5.TextSize = 11
		textButton5.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton5.Font = Enum.Font.GothamBold
		textButton5.ZIndex = 2
		textButton5.Parent = frame
		Instance.new("UICorner", textButton5).CornerRadius = UDim.new(0, 8)
		local uiStroke8 = Instance.new("UIStroke", textButton5)
		uiStroke8.Color = color2
		uiStroke8.Thickness = 1
		textButton6 = Instance.new("TextButton")
		textButton6.Size = UDim2.new(0, 56, 0, 34)
		textButton6.Position = UDim2.new(0, 124, 0, 0)
		textButton6.BackgroundColor3 = color3
		textButton6.Text = "ðï¸ Drop"
		textButton6.TextSize = 11
		textButton6.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton6.Font = Enum.Font.GothamBold
		textButton6.ZIndex = 2
		textButton6.Parent = frame
		Instance.new("UICorner", textButton6).CornerRadius = UDim.new(0, 8)
		local uiStroke9 = Instance.new("UIStroke", textButton6)
		uiStroke9.Color = color2
		uiStroke9.Thickness = 1
		textButton7 = Instance.new("TextButton")
		textButton7.Size = UDim2.new(0, 56, 0, 34)
		textButton7.Position = UDim2.new(0, 186, 0, 0)
		textButton7.BackgroundColor3 = color3
		textButton7.Text = "ð Logs"
		textButton7.TextSize = 11
		textButton7.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton7.Font = Enum.Font.GothamBold
		textButton7.ZIndex = 2
		textButton7.Parent = frame
	end

	Instance.new("UICorner", textButton7).CornerRadius = UDim.new(0, 8)
	local uiStroke7 = Instance.new("UIStroke", textButton7)
	uiStroke7.Color = color2
	uiStroke7.Thickness = 1
	local textButton8
	textButton8 = Instance.new("TextButton")
	textButton8.Size = UDim2.new(1, -20, 0, 34)
	textButton8.Position = UDim2.new(0, 10, 0, 82)
	textButton8.BackgroundColor3 = color3
	textButton8.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton8.Font = Enum.Font.GothamBold
	textButton8.TextSize = 12
	textButton8.Text = "â¶ï¸   A U T O   F A R M :   O F F"
	textButton8.ZIndex = 2
	textButton8.Parent = imageLabel3
	Instance.new("UICorner", textButton8).CornerRadius = UDim.new(0, 8)
	local uiStroke8 = Instance.new("UIStroke", textButton8)
	uiStroke8.Color = color2
	uiStroke8.Thickness = 1
	local textButton9
	textButton9 = Instance.new("TextButton")
	textButton9.Size = UDim2.new(1, -20, 0, 34)
	textButton9.Position = UDim2.new(0, 10, 0, 122)
	textButton9.BackgroundColor3 = color3
	textButton9.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton9.Font = Enum.Font.GothamBold
	textButton9.TextSize = 12
	textButton9.Text = "ð¯   A U T O   P O S I T I O N :   O F F"
	textButton9.ZIndex = 2
	textButton9.Parent = imageLabel3
	Instance.new("UICorner", textButton9).CornerRadius = UDim.new(0, 8)
	local uiStroke9 = Instance.new("UIStroke", textButton9)
	uiStroke9.Color = color2
	uiStroke9.Thickness = 1
	local frame
	frame = Instance.new("Frame")
	frame.Size = UDim2.new(1, -20, 0, 96)
	frame.Position = UDim2.new(0, 10, 0, 162)
	frame.BackgroundTransparency = 1
	frame.ZIndex = 2
	frame.Visible = false
	frame.Parent = imageLabel3

	do
		local textButton10 = Instance.new("TextButton")
		textButton10.Size = UDim2.new(0, 115, 0, 28)
		textButton10.Position = UDim2.new(0, 0, 0, 0)
		textButton10.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
		textButton10.Text = "ÙØ²ÙÙÙ ÙÙÙ 70 !"
		textButton10.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton10.Font = Enum.Font.GothamBold
		textButton10.TextSize = 11
		textButton10.ZIndex = 2
		textButton10.Parent = frame
		Instance.new("UICorner", textButton10).CornerRadius = UDim.new(0, 8)
		local uiStroke10 = Instance.new("UIStroke", textButton10)
		uiStroke10.Color = color2
		uiStroke10.Thickness = 1
		local textButton11 = Instance.new("TextButton")
		textButton11.Size = UDim2.new(0, 115, 0, 28)
		textButton11.Position = UDim2.new(1, -115, 0, 0)
		textButton11.BackgroundColor3 = color3
		textButton11.Text = "ÙØ²ÙÙÙ ÙÙÙ 40 !"
		textButton11.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton11.Font = Enum.Font.GothamBold
		textButton11.TextSize = 11
		textButton11.ZIndex = 2
		textButton11.Parent = frame
		Instance.new("UICorner", textButton11).CornerRadius = UDim.new(0, 8)
		local uiStroke11 = Instance.new("UIStroke", textButton11)
		uiStroke11.Color = color2
		uiStroke11.Thickness = 1
		local textButton12 = Instance.new("TextButton")
		textButton12.Size = UDim2.new(0, 115, 0, 28)
		textButton12.Position = UDim2.new(0, 0, 0, 33)
		textButton12.BackgroundColor3 = color3
		textButton12.Text = "- ÙØ²ÙÙØ§Øª ÙØªØºÙØ±Ù!"
		textButton12.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton12.Font = Enum.Font.GothamBold
		textButton12.TextSize = 11
		textButton12.ZIndex = 2
		textButton12.Parent = frame
		Instance.new("UICorner", textButton12).CornerRadius = UDim.new(0, 8)
		local uiStroke12 = Instance.new("UIStroke", textButton12)
		uiStroke12.Color = color2
		uiStroke12.Thickness = 1

		local function fn12()
			flag = false
			textButton10.BackgroundColor3 = color3
			textButton11.BackgroundColor3 = color3
			textButton12.BackgroundColor3 = color3
		end

		textButton10.MouseButton1Click:Connect(function()
			fn12()
			vector5 = vector
			textButton10.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
		end)

		textButton11.MouseButton1Click:Connect(function()
			fn12()
			vector5 = vector2
			textButton11.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
		end)

		textButton12.MouseButton1Click:Connect(function()
			fn12()
			flag = true
			n = 1
			vector5 = vector
			textButton12.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
		end)
	end

	local textButton10
	textButton10 = Instance.new("TextButton")
	textButton10.Size = UDim2.new(1, -20, 0, 34)
	textButton10.Position = UDim2.new(0, 10, 0, 266)
	textButton10.BackgroundColor3 = color3
	textButton10.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton10.Font = Enum.Font.GothamBold
	textButton10.TextSize = 13
	textButton10.Text = "ð® Auto Skip: OFF"
	textButton10.ZIndex = 2
	textButton10.Parent = imageLabel3
	Instance.new("UICorner", textButton10).CornerRadius = UDim.new(0, 8)
	local uiStroke10 = Instance.new("UIStroke", textButton10)
	uiStroke10.Color = color2
	uiStroke10.Thickness = 1
	local textButton11
	textButton11 = Instance.new("TextButton")
	textButton11.Size = UDim2.new(1, -20, 0, 34)
	textButton11.Position = UDim2.new(0, 10, 0, 306)
	textButton11.BackgroundColor3 = color3
	textButton11.TextColor3 = Color3.fromRGB(40, 40, 40)
	textButton11.Font = Enum.Font.GothamBold
	textButton11.TextSize = 12
	textButton11.Text = "ð°   A U T O   S E L L :   O F F"
	textButton11.ZIndex = 2
	textButton11.Parent = imageLabel3
	Instance.new("UICorner", textButton11).CornerRadius = UDim.new(0, 8)
	local uiStroke11 = Instance.new("UIStroke", textButton11)
	uiStroke11.Color = color2
	uiStroke11.Thickness = 1
	local textBox, textButton12

	do
		local frame2 = Instance.new("Frame")
		frame2.Size = UDim2.new(1, -20, 0, 34)
		frame2.Position = UDim2.new(0, 10, 0, 346)
		frame2.BackgroundTransparency = 1
		frame2.ZIndex = 2
		frame2.Parent = imageLabel3
		textBox = Instance.new("TextBox")
		textBox.Size = UDim2.new(0, 55, 1, 0)
		textBox.Position = UDim2.new(0, 0, 0, 0)
		textBox.BackgroundColor3 = color3
		textBox.Text = "50"
		textBox.TextColor3 = Color3.fromRGB(40, 40, 40)
		textBox.Font = Enum.Font.GothamBold
		textBox.TextSize = 13
		textBox.ClearTextOnFocus = false
		textBox.ZIndex = 2
		textBox.Parent = frame2
		Instance.new("UICorner", textBox).CornerRadius = UDim.new(0, 8)
		local uiStroke12 = Instance.new("UIStroke", textBox)
		uiStroke12.Color = color2
		uiStroke12.Thickness = 1
		textButton12 = Instance.new("TextButton")
		textButton12.Size = UDim2.new(1, -65, 1, 0)
		textButton12.Position = UDim2.new(0, 65, 0, 0)
		textButton12.BackgroundColor3 = color3
		textButton12.Text = "Ø§Ø´ØªØ± Ø·Ø¹Ù ØªÙÙØ§Ø¦Ù Ø¨Ø³Ø±Ø¹Ù!"
		textButton12.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton12.Font = Enum.Font.GothamBold
		textButton12.TextSize = 12
		textButton12.ZIndex = 2
		textButton12.Parent = frame2
	end

	Instance.new("UICorner", textButton12).CornerRadius = UDim.new(0, 8)
	local uiStroke12 = Instance.new("UIStroke", textButton12)
	uiStroke12.Color = color2
	uiStroke12.Thickness = 1
	local v2, v3, v4, v5

	local function createImageLabel(text, arg)
		local imageLabel4 = Instance.new("ImageLabel")
		imageLabel4.Size = UDim2.new(0, 320, 0, arg)
		imageLabel4.Position = UDim2.new(0.5, -160, 0.5, -arg / 2)
		imageLabel4.BackgroundColor3 = color
		imageLabel4.BackgroundTransparency = 0
		imageLabel4.Image = image
		imageLabel4.ScaleType = Enum.ScaleType.Slice
		imageLabel4.SliceCenter = Rect.new(100, 100, 100, 100)
		imageLabel4.Active = true
		imageLabel4.Draggable = true
		imageLabel4.Visible = false
		imageLabel4.Parent = screenGui
		Instance.new("UICorner", imageLabel4).CornerRadius = UDim.new(0, 15)
		local uiStroke13 = Instance.new("UIStroke", imageLabel4)
		uiStroke13.Color = color2
		uiStroke13.Thickness = 1.5
		fn11(imageLabel4)
		local textLabel4 = Instance.new("TextLabel")
		textLabel4.Size = UDim2.new(1, -40, 0, 35)
		textLabel4.Position = UDim2.new(0, 12, 0, 5)
		textLabel4.BackgroundTransparency = 1
		textLabel4.Text = text
		textLabel4.TextColor3 = Color3.fromRGB(50, 50, 50)
		textLabel4.Font = Enum.Font.Bodoni
		textLabel4.TextSize = 16
		textLabel4.TextXAlignment = Enum.TextXAlignment.Left
		textLabel4.ZIndex = 2
		textLabel4.Parent = imageLabel4
		local textButton13 = Instance.new("TextButton")
		textButton13.Size = UDim2.new(0, 30, 0, 30)
		textButton13.Position = UDim2.new(1, -35, 0, 5)
		textButton13.BackgroundColor3 = color3
		textButton13.Text = "â"
		textButton13.TextColor3 = Color3.fromRGB(50, 50, 50)
		textButton13.Font = Enum.Font.GothamBold
		textButton13.TextSize = 14
		textButton13.ZIndex = 2
		textButton13.Parent = imageLabel4
		Instance.new("UICorner", textButton13).CornerRadius = UDim.new(0, 8)
		local uiStroke14 = Instance.new("UIStroke", textButton13)
		uiStroke14.Color = color2
		uiStroke14.Thickness = 1

		textButton13.MouseButton1Click:Connect(function()
			imageLabel4.Visible = false
		end)

		return imageLabel4
	end

	v2 = createImageLabel("â­ï¸   S K I P   M E N U", 410)
	v3 = createImageLabel("ðï¸   A U T O   D R O P   F I S H", 510)
	v4 = createImageLabel("ð   W E B H O O K", 510)
	v5 = createImageLabel("ð   F I S H   L O G S", 360)

	do
		local textButton13 = Instance.new("TextButton")
		textButton13.Size = UDim2.new(1, -20, 0, 38)
		textButton13.Position = UDim2.new(0, 10, 0, 45)
		textButton13.BackgroundColor3 = color3
		textButton13.TextColor3 = Color3.fromRGB(40, 40, 40)
		textButton13.Font = Enum.Font.GothamBold
		textButton13.TextSize = 12
		textButton13.Text = "Auto Drop: OFF"
		textButton13.ZIndex = 2
		textButton13.Parent = v3
		Instance.new("UICorner", textButton13).CornerRadius = UDim.new(0, 8)
		local uiStroke13 = Instance.new("UIStroke", textButton13)
		uiStroke13.Color = color2
		uiStroke13.Thickness = 1

		textButton13.MouseButton1Click:Connect(function()
			flag5 = not flag5

			if flag5 then
				textButton13.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
				textButton13.Text = "Auto Drop: ON (Ø´ØºØ§Ù ØªÙÙØ§Ø¦Ù)"
			else
				textButton13.BackgroundColor3 = color3
				textButton13.Text = "Auto Drop: OFF (Ø·Ø§ÙÙ)"
			end
		end)
	end

	do
		local frame2 = Instance.new("Frame")
		frame2.Size = UDim2.new(1, -20, 0, 50)
		frame2.Position = UDim2.new(0, 10, 0, 90)
		frame2.BackgroundColor3 = color3
		frame2.BackgroundTransparency = 0.3
		frame2.ZIndex = 2
		frame2.Parent = v3
		Instance.new("UICorner", frame2).CornerRadius = UDim.new(0, 8)
		local uiStroke13 = Instance.new("UIStroke", frame2)
		uiStroke13.Color = color2
		uiStroke13.Thickness = 1
		local textLabel4 = Instance.new("TextLabel")
		textLabel4.Size = UDim2.new(1, -16, 0, 20)
		textLabel4.Position = UDim2.new(0, 8, 0, 4)
		textLabel4.BackgroundTransparency = 1
		textLabel4.Text = "Drop Delay: 2.0s"
		textLabel4.TextColor3 = Color3.fromRGB(40, 40, 40)
		textLabel4.Font = Enum.Font.GothamBold
		textLabel4.TextSize = 12
		textLabel4.TextXAlignment = Enum.TextXAlignment.Left
		textLabel4.ZIndex = 2
		textLabel4.Parent = frame2
		local frame3 = Instance.new("Frame")
		frame3.Size = UDim2.new(1, -20, 0, 6)
		frame3.Position = UDim2.new(0, 10, 0, 32)
		frame3.BackgroundColor3 = Color3.fromRGB(200, 200, 200)
		frame3.BorderSizePixel = 0
		frame3.ZIndex = 2
		frame3.Parent = frame2
		Instance.new("UICorner", frame3).CornerRadius = UDim.new(1, 0)
		local frame4 = Instance.new("Frame")
		frame4.Size = UDim2.new(0.4, 0, 1, 0)
		frame4.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
		frame4.BorderSizePixel = 0
		frame4.ZIndex = 2
		frame4.Parent = frame3
		Instance.new("UICorner", frame4).CornerRadius = UDim.new(1, 0)
		local textButton13 = Instance.new("TextButton")
		textButton13.Size = UDim2.new(0, 14, 0, 14)
		textButton13.AnchorPoint = Vector2.new(0.5, 0.5)
		textButton13.Position = UDim2.new(0.4, 0, 0.5, 0)
		textButton13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		textButton13.Text = ""
		textButton13.ZIndex = 3
		textButton13.Parent = frame3
		Instance.new("UICorner", textButton13).CornerRadius = UDim.new(1, 0)
		local uiStroke14 = Instance.new("UIStroke", textButton13)
		uiStroke14.Color = color2
		uiStroke14.Thickness = 1
		local flag9 = false

		local function fn12(arg)
			local n7 = math.clamp((arg.Position.X - frame3.AbsolutePosition.X) / frame3.AbsoluteSize.X, 0, 1)
			n5 = n7 * 5
			frame4.Size = UDim2.new(n7, 0, 1, 0)
			textButton13.Position = UDim2.new(n7, 0, 0.5, 0)
			textLabel4.Text = string.format("Drop Delay: %.1fs", n5)
		end

		textButton13.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = true
			end
		end)

		frame3.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = true
				fn12(input)
			end
		end)

		UserInputService.InputEnded:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = false
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if flag9 and (input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch) then
				fn12(input)
			end
		end)
	end

	do
		local scrollingFrame = Instance.new("ScrollingFrame")
		scrollingFrame.Size = UDim2.new(1, -20, 0, 340)
		scrollingFrame.Position = UDim2.new(0, 10, 0, 150)
		scrollingFrame.BackgroundColor3 = color3
		scrollingFrame.BackgroundTransparency = 0.3
		scrollingFrame.BorderSizePixel = 0
		scrollingFrame.ScrollBarThickness = 4
		scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, #tbl2 * 38)
		scrollingFrame.ZIndex = 2
		scrollingFrame.Parent = v3
		Instance.new("UICorner", scrollingFrame).CornerRadius = UDim.new(0, 8)
		Instance.new("UIListLayout", scrollingFrame).Padding = UDim.new(0, 5)
		local uiPadding = Instance.new("UIPadding", scrollingFrame)
		uiPadding.PaddingTop = UDim.new(0, 5)
		uiPadding.PaddingLeft = UDim.new(0, 5)
		uiPadding.PaddingRight = UDim.new(0, 5)

		for _, v6 in ipairs(tbl2) do
			local textButton13 = Instance.new("TextButton")
			textButton13.Size = UDim2.new(1, -6, 0, 32)
			textButton13.BackgroundColor3 = color3
			textButton13.BackgroundTransparency = 0.2
			textButton13.AutoButtonColor = false
			textButton13.Text = ""
			textButton13.ZIndex = 2
			textButton13.Parent = scrollingFrame
			Instance.new("UICorner", textButton13).CornerRadius = UDim.new(0, 8)
			local uiStroke13 = Instance.new("UIStroke", textButton13)
			uiStroke13.Color = color2
			uiStroke13.Thickness = 1
			local textLabel4 = Instance.new("TextLabel")
			textLabel4.Size = UDim2.new(1, -60, 1, 0)
			textLabel4.Position = UDim2.new(0, 12, 0, 0)
			textLabel4.BackgroundTransparency = 1
			textLabel4.Text = v6
			textLabel4.TextColor3 = fn7(v6)
			textLabel4.Font = Enum.Font.GothamMedium
			textLabel4.TextSize = 13
			textLabel4.TextXAlignment = Enum.TextXAlignment.Left
			textLabel4.ZIndex = 2
			textLabel4.Parent = textButton13
			local textLabel5 = Instance.new("TextLabel")
			textLabel5.Size = UDim2.new(0, 42, 0, 22)
			textLabel5.Position = UDim2.new(1, -50, 0.5, -11)
			textLabel5.BackgroundColor3 = color3
			textLabel5.BackgroundTransparency = 0.2
			textLabel5.Text = "OFF"
			textLabel5.TextColor3 = Color3.fromRGB(120, 120, 120)
			textLabel5.Font = Enum.Font.GothamBold
			textLabel5.TextSize = 11
			textLabel5.ZIndex = 2
			textLabel5.Parent = textButton13
			Instance.new("UICorner", textLabel5).CornerRadius = UDim.new(0, 6)

			textButton13.MouseButton1Click:Connect(function()
				tbl6[v6] = not tbl6[v6]
				local v7 = tbl6[v6]
				textButton13.BackgroundColor3 = v7 and Color3.fromRGB(220, 220, 220) or color3
				textLabel5.BackgroundColor3 = v7 and Color3.fromRGB(200, 200, 200) or color3
				textLabel5.Text = v7 and "ON" or "OFF"
				textLabel5.TextColor3 = v7 and Color3.fromRGB(40, 40, 40) or Color3.fromRGB(120, 120, 120)
			end)
		end
	end

	do
		local function fn12(arg)
			if not arg then
				return nil
			end

			for _, v6 in pairs(arg:GetAttributes()) do
				if type(v6) == "string" and (string.match(v6, "%-%x+%-%x+") or #v6 > 15) then
					return "{" .. v6:gsub("[{}]", "") .. "}"
				end
			end

			for _, child in ipairs(arg:GetChildren()) do
				if child:IsA("ValueBase") then
					local str3 = tostring(child.Value)
					if string.match(str3, "%-%x+%-%x+") or #str3 > 15 then
						return "{" .. str3:gsub("[{}]", "") .. "}"
					end
				end
			end

			return nil
		end

		local function fn13(arg)
			local v6 = string.lower(arg)

			for k, v7 in pairs(tbl6) do
				v7 = v7 and string.find(v6, string.lower(k))
				if v7 then
					return true
				end
			end

			return false
		end

		local function fn14(arg)
			pcall(function()
				send:FireServer(fn4(), "play_character_sound", "open_inventory")
				task.wait(n5)
				send:FireServer(fn4(), "drop_item", arg, 1)
				task.wait(0.5)
			end)
		end

		task.spawn(function()
			local tbl13 = {}

			while true do
				task.wait(0.3)

				if flag5 then
					local tbl14 = nil

					pcall(function()
						local backpack = localPlayer2:FindFirstChild("Backpack")

						if backpack then
							for _, child in ipairs(backpack:GetChildren()) do
								if child:IsA("Tool") and fn13(child.Name) then
									local v6 = fn12(child)
									if v6 and not tbl13[v6] then
										tbl14 = { uuid = v6, name = child.Name }
										break
									end
								end
							end
						end

						if not tbl14 then
							local character = localPlayer2.Character

							if character then
								for _, child in ipairs(character:GetChildren()) do
									if child:IsA("Tool") and fn13(child.Name) then
										local v6 = fn12(child)
										if v6 and not tbl13[v6] then
											tbl14 = { uuid = v6, name = child.Name }
											break
										end
									end
								end
							end
						end

						if not tbl14 then
							local items = playerGui:FindFirstChild("Items")

							if items then
								for _, descendant in ipairs(items:GetDescendants()) do
									if (descendant:IsA("TextLabel") or descendant:IsA("TextButton")) and fn13(descendant.Text) then
										local parent = descendant.Parent
										local v6 = parent and fn12(parent)

										if not v6 and parent and parent.Parent then
											v6 = fn12(parent.Parent)
										end

										if v6 and not tbl13[v6] then
											tbl14 = { uuid = v6, name = descendant.Text }
											break
										end
									end
								end
							end
						end
					end)

					if tbl14 then
						tbl13[tbl14.uuid] = true
						fn14(tbl14.uuid, tbl14.name)
					end
				end
			end
		end)
	end

	do
		local textLabel4 = Instance.new("TextLabel")
		textLabel4.Size = UDim2.new(1, -20, 0, 30)
		textLabel4.Position = UDim2.new(0, 10, 0, 42)
		textLabel4.BackgroundColor3 = color3
		textLabel4.BackgroundTransparency = 0.3
		textLabel4.Text = "ð£ Caught: 0  |  â­ï¸ Skipped: 0"
		textLabel4.TextColor3 = Color3.fromRGB(40, 40, 40)
		textLabel4.Font = Enum.Font.GothamBold
		textLabel4.TextSize = 12
		textLabel4.ZIndex = 2
		textLabel4.Parent = v5
		Instance.new("UICorner", textLabel4).CornerRadius = UDim.new(0, 8)
		local uiStroke13 = Instance.new("UIStroke", textLabel4)
		uiStroke13.Color = color2
		uiStroke13.Thickness = 1
		local scrollingFrame = Instance.new("ScrollingFrame")
		scrollingFrame.Size = UDim2.new(1, -20, 0, 270)
		scrollingFrame.Position = UDim2.new(0, 10, 0, 78)
		scrollingFrame.BackgroundColor3 = color3
		scrollingFrame.BackgroundTransparency = 0.3
		scrollingFrame.BorderSizePixel = 0
		scrollingFrame.ScrollBarThickness = 4
		scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
		scrollingFrame.ZIndex = 2
		scrollingFrame.Parent = v5
		Instance.new("UICorner", scrollingFrame).CornerRadius = UDim.new(0, 8)
		Instance.new("UIListLayout", scrollingFrame).Padding = UDim.new(0, 4)

		local function fn12(arg, arg2)
			local v6 = os.date("%X")

			if arg == "Caught" then
				n2 += 1
			elseif arg == "Skipped" then
				n3 += 1
			end

			textLabel4.Text = "ð£ Caught: " .. tostring(n2) .. "  |  â­ï¸ Skipped: " .. tostring(n3)
			local textLabel5 = Instance.new("TextLabel")
			textLabel5.Size = UDim2.new(1, -8, 0, 25)
			textLabel5.BackgroundColor3 = color3
			textLabel5.BackgroundTransparency = 0.2

			if arg == "Caught" then
				textLabel5.Text = "[" .. v6 .. "] ð£ Caught: " .. tostring(arg2)
				textLabel5.TextColor3 = Color3.fromRGB(0, 150, 50)
			else
				textLabel5.Text = "[" .. v6 .. "] â­ï¸ Skipped: " .. tostring(arg2)
				textLabel5.TextColor3 = Color3.fromRGB(180, 50, 50)
			end

			textLabel5.Font = Enum.Font.GothamMedium
			textLabel5.TextSize = 11
			textLabel5.TextXAlignment = Enum.TextXAlignment.Left
			textLabel5.ZIndex = 2
			textLabel5.Parent = scrollingFrame
			Instance.new("UICorner", textLabel5).CornerRadius = UDim.new(0, 6)
			Instance.new("UIPadding", textLabel5).PaddingLeft = UDim.new(0, 8)
			table.insert(tbl3, textLabel5)
			scrollingFrame.CanvasSize = UDim2.new(0, 0, 0, #tbl3 * 29)
			scrollingFrame.CanvasPosition = Vector2.new(0, scrollingFrame.AbsoluteCanvasSize.Y)
		end

		local frame2 = Instance.new("Frame")
		frame2.Size = UDim2.new(1, -20, 0, 50)
		frame2.Position = UDim2.new(0, 10, 0, 45)
		frame2.BackgroundColor3 = color3
		frame2.BackgroundTransparency = 0.3
		frame2.ZIndex = 2
		frame2.Parent = v2
		Instance.new("UICorner", frame2).CornerRadius = UDim.new(0, 8)
		local uiStroke14 = Instance.new("UIStroke", frame2)
		uiStroke14.Color = color2
		uiStroke14.Thickness = 1
		local textLabel5 = Instance.new("TextLabel")
		textLabel5.Size = UDim2.new(1, -16, 0, 20)
		textLabel5.Position = UDim2.new(0, 8, 0, 4)
		textLabel5.BackgroundTransparency = 1
		textLabel5.Text = "Skip Delay: 1.0s"
		textLabel5.TextColor3 = Color3.fromRGB(40, 40, 40)
		textLabel5.Font = Enum.Font.GothamBold
		textLabel5.TextSize = 12
		textLabel5.TextXAlignment = Enum.TextXAlignment.Left
		textLabel5.ZIndex = 2
		textLabel5.Parent = frame2
		local frame3 = Instance.new("Frame")
		frame3.Size = UDim2.new(1, -20, 0, 6)
		frame3.Position = UDim2.new(0, 10, 0, 32)
		frame3.BackgroundColor3 = Color3.fromRGB(200, 200, 200)
		frame3.BorderSizePixel = 0
		frame3.ZIndex = 2
		frame3.Parent = frame2
		Instance.new("UICorner", frame3).CornerRadius = UDim.new(1, 0)
		local frame4 = Instance.new("Frame")
		frame4.Size = UDim2.new(0.33, 0, 1, 0)
		frame4.BackgroundColor3 = Color3.fromRGB(80, 80, 80)
		frame4.BorderSizePixel = 0
		frame4.ZIndex = 2
		frame4.Parent = frame3
		Instance.new("UICorner", frame4).CornerRadius = UDim.new(1, 0)
		local textButton13 = Instance.new("TextButton")
		textButton13.Size = UDim2.new(0, 14, 0, 14)
		textButton13.AnchorPoint = Vector2.new(0.5, 0.5)
		textButton13.Position = UDim2.new(0.33, 0, 0.5, 0)
		textButton13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		textButton13.Text = ""
		textButton13.ZIndex = 3
		textButton13.Parent = frame3
		Instance.new("UICorner", textButton13).CornerRadius = UDim.new(1, 0)
		local uiStroke15 = Instance.new("UIStroke", textButton13)
		uiStroke15.Color = color2
		uiStroke15.Thickness = 1
		local flag9 = false

		local function fn13(arg)
			local n7 = math.clamp((arg.Position.X - frame3.AbsolutePosition.X) / frame3.AbsoluteSize.X, 0, 1)
			n4 = n7 * 3
			frame4.Size = UDim2.new(n7, 0, 1, 0)
			textButton13.Position = UDim2.new(n7, 0, 0.5, 0)
			textLabel5.Text = string.format("Skip Delay: %.1fs", n4)
		end

		textButton13.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = true
			end
		end)

		frame3.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = true
				fn13(input)
			end
		end)

		UserInputService.InputEnded:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = false
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			local flag10 = flag9

			if flag9 then
				flag10 = input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch
			end

			if flag10 then
				fn13(input)
			end
		end)

		local scrollingFrame2 = Instance.new("ScrollingFrame")
		scrollingFrame2.Size = UDim2.new(1, -20, 0, 235)
		scrollingFrame2.Position = UDim2.new(0, 10, 0, 105)
		scrollingFrame2.BackgroundColor3 = color3
		scrollingFrame2.BackgroundTransparency = 0.3
		scrollingFrame2.BorderSizePixel = 0
		scrollingFrame2.ScrollBarThickness = 4
		scrollingFrame2.CanvasSize = UDim2.new(0, 0, 0, #tbl2 * 35)
		scrollingFrame2.ZIndex = 2
		scrollingFrame2.Parent = v2
		Instance.new("UICorner", scrollingFrame2).CornerRadius = UDim.new(0, 8)
		Instance.new("UIListLayout", scrollingFrame2).Padding = UDim.new(0, 5)

		for _, v6 in ipairs(tbl2) do
			local textButton14 = Instance.new("TextButton")
			textButton14.Size = UDim2.new(1, -10, 0, 30)
			textButton14.BackgroundColor3 = tbl5[v6] and Color3.fromRGB(220, 220, 220) or color3
			textButton14.BackgroundTransparency = 0.2
			textButton14.Text = v6 .. " - " .. (tbl5[v6] and "ON" or "OFF")
			textButton14.TextColor3 = fn7(v6)
			textButton14.Font = Enum.Font.GothamBold
			textButton14.TextSize = 12
			textButton14.ZIndex = 2
			textButton14.Parent = scrollingFrame2
			Instance.new("UICorner", textButton14).CornerRadius = UDim.new(0, 6)
			local uiStroke16 = Instance.new("UIStroke", textButton14)
			uiStroke16.Color = color2
			uiStroke16.Thickness = 1

			textButton14.MouseButton1Click:Connect(function()
				tbl5[v6] = not tbl5[v6]
				textButton14.BackgroundColor3 = tbl5[v6] and Color3.fromRGB(220, 220, 220) or color3
				textButton14.Text = v6 .. " - " .. (tbl5[v6] and "ON" or "OFF")
			end)
		end

		local scrollingFrame3 = Instance.new("ScrollingFrame")
		scrollingFrame3.Size = UDim2.new(1, -20, 0, 195)
		scrollingFrame3.Position = UDim2.new(0, 10, 0, 90)
		scrollingFrame3.BackgroundColor3 = color3
		scrollingFrame3.BackgroundTransparency = 0.3
		scrollingFrame3.BorderSizePixel = 0
		scrollingFrame3.ScrollBarThickness = 4
		scrollingFrame3.CanvasSize = UDim2.new(0, 0, 0, #tbl2 * 38 + 8)
		scrollingFrame3.ZIndex = 2
		scrollingFrame3.Parent = v4
		Instance.new("UICorner", scrollingFrame3).CornerRadius = UDim.new(0, 8)
		Instance.new("UIListLayout", scrollingFrame3).Padding = UDim.new(0, 6)
		local uiPadding = Instance.new("UIPadding", scrollingFrame3)
		uiPadding.PaddingTop = UDim.new(0, 6)
		uiPadding.PaddingLeft = UDim.new(0, 6)
		uiPadding.PaddingRight = UDim.new(0, 6)
		local textBox2 = Instance.new("TextBox")
		textBox2.Size = UDim2.new(1, -20, 0, 36)
		textBox2.Position = UDim2.new(0, 10, 0, 45)
		textBox2.BackgroundColor3 = color3
		textBox2.BackgroundTransparency = 0.2
		textBox2.Text = tbl12.Webhook
		textBox2.PlaceholderText = "Paste Webhook URL here"
		textBox2.TextColor3 = Color3.fromRGB(40, 40, 40)
		textBox2.PlaceholderColor3 = Color3.fromRGB(120, 120, 120)
		textBox2.Font = Enum.Font.Gotham
		textBox2.TextSize = 12
		textBox2.ClearTextOnFocus = false
		textBox2.ZIndex = 2
		textBox2.Parent = v4
		Instance.new("UICorner", textBox2).CornerRadius = UDim.new(0, 8)
		local uiStroke16 = Instance.new("UIStroke", textBox2)
		uiStroke16.Color = color2
		uiStroke16.Thickness = 1

		local function createTextButton(text, arg, arg2, arg3, arg4)
			local textButton14 = Instance.new("TextButton")
			textButton14.Size = UDim2.new(0, arg3, 0, 32)
			textButton14.Position = UDim2.new(0, arg, 0, arg2)
			textButton14.BackgroundColor3 = arg4 and Color3.fromRGB(220, 220, 220) or color3
			textButton14.BackgroundTransparency = 0.2
			textButton14.Text = text
			textButton14.TextColor3 = Color3.fromRGB(40, 40, 40)
			textButton14.Font = Enum.Font.GothamBold
			textButton14.TextSize = 11
			textButton14.ZIndex = 2
			textButton14.Parent = v4
			Instance.new("UICorner", textButton14).CornerRadius = UDim.new(0, 6)
			local uiStroke17 = Instance.new("UIStroke", textButton14)
			uiStroke17.Color = color2
			uiStroke17.Thickness = 1
			return textButton14
		end

		local v6 = createTextButton(tbl12.EspEnabled and "ESP: ON" or "ESP: OFF", 10, 295, 142, tbl12.EspEnabled)
		local v7 = createTextButton(tbl12.Enabled and "Notify: ON" or "Notify: OFF", 162, 295, 142, tbl12.Enabled)
		local v8 = createTextButton(tbl12.Everyone and "@everyone" or "no mention", 10, 335, 142, tbl12.Everyone)
		local testWebhook = createTextButton("Test Webhook", 162, 335, 142, false)
		local v9 = createTextButton("Save Config â", 10, 380, 294, false)

		for _, v10 in ipairs(tbl2) do
			local textButton14 = Instance.new("TextButton")
			textButton14.Size = UDim2.new(1, -6, 0, 32)
			textButton14.BackgroundColor3 = tbl12.EnabledFish[v10] and Color3.fromRGB(220, 220, 220) or color3
			textButton14.BackgroundTransparency = 0.2
			textButton14.AutoButtonColor = false
			textButton14.Text = ""
			textButton14.ZIndex = 2
			textButton14.Parent = scrollingFrame3
			Instance.new("UICorner", textButton14).CornerRadius = UDim.new(0, 8)
			local uiStroke17 = Instance.new("UIStroke", textButton14)
			uiStroke17.Color = color2
			uiStroke17.Thickness = 1
			local textLabel6 = Instance.new("TextLabel")
			textLabel6.Size = UDim2.new(1, -60, 1, 0)
			textLabel6.Position = UDim2.new(0, 12, 0, 0)
			textLabel6.BackgroundTransparency = 1
			textLabel6.Text = v10
			textLabel6.TextColor3 = fn7(v10)
			textLabel6.Font = Enum.Font.GothamMedium
			textLabel6.TextSize = 13
			textLabel6.TextXAlignment = Enum.TextXAlignment.Left
			textLabel6.ZIndex = 2
			textLabel6.Parent = textButton14
			local textLabel7 = Instance.new("TextLabel")
			textLabel7.Size = UDim2.new(0, 42, 0, 22)
			textLabel7.Position = UDim2.new(1, -50, 0.5, -11)
			textLabel7.BackgroundColor3 = tbl12.EnabledFish[v10] and Color3.fromRGB(200, 200, 200) or color3
			textLabel7.BackgroundTransparency = 0.2
			textLabel7.Text = tbl12.EnabledFish[v10] and "ON" or "OFF"
			textLabel7.TextColor3 = tbl12.EnabledFish[v10] and Color3.fromRGB(40, 40, 40) or Color3.fromRGB(120, 120, 120)
			textLabel7.Font = Enum.Font.GothamBold
			textLabel7.TextSize = 11
			textLabel7.ZIndex = 2
			textLabel7.Parent = textButton14
			Instance.new("UICorner", textLabel7).CornerRadius = UDim.new(0, 6)

			textButton14.MouseButton1Click:Connect(function()
				tbl12.EnabledFish[v10] = not tbl12.EnabledFish[v10]
				local v11 = tbl12.EnabledFish[v10]
				textButton14.BackgroundColor3 = v11 and Color3.fromRGB(220, 220, 220) or color3
				textLabel7.BackgroundColor3 = v11 and Color3.fromRGB(200, 200, 200) or color3
				textLabel7.Text = v11 and "ON" or "OFF"
				textLabel7.TextColor3 = v11 and Color3.fromRGB(40, 40, 40) or Color3.fromRGB(120, 120, 120)
			end)
		end

		textButton5.MouseButton1Click:Connect(function()
			v2.Visible = not v2.Visible
			v3.Visible = false
			v4.Visible = false
			v5.Visible = false
		end)

		textButton6.MouseButton1Click:Connect(function()
			v3.Visible = not v3.Visible
			v2.Visible = false
			v4.Visible = false
			v5.Visible = false
		end)

		textButton4.MouseButton1Click:Connect(function()
			v4.Visible = not v4.Visible
			v2.Visible = false
			v3.Visible = false
			v5.Visible = false
		end)

		textButton7.MouseButton1Click:Connect(function()
			v5.Visible = not v5.Visible
			v2.Visible = false
			v3.Visible = false
			v4.Visible = false
		end)

		textButton.MouseButton1Click:Connect(function()
			local tween = TweenService:Create(imageLabel, TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Size = UDim2.new(0, 0, 0, 0), Position = UDim2.new(0.5, 0, 0.5, 0) })
			tween:Play()

			tween.Completed:Connect(function()
				imageLabel:Destroy()
				imageLabel2.Visible = true
			end)
		end)

		local frame5 = Instance.new("Frame")
		frame5.Size = UDim2.new(0, 4, 0, 4)
		frame5.AnchorPoint = Vector2.new(0.5, 0.5)
		frame5.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
		frame5.Visible = false
		frame5.Parent = screenGui
		Instance.new("UICorner", frame5).CornerRadius = UDim.new(1, 0)

		local function fn14(arg, arg2)
			if not arg or not arg2 then
				return
			end
			VirtualInputManager:SendMouseButtonEvent(arg, arg2, 0, true, game, 0)
			task.wait(0.05)
			VirtualInputManager:SendMouseButtonEvent(arg, arg2, 0, false, game, 0)
		end

		local function fn15()
			local character = localPlayer2.Character
			if not character then
				return
			end
			local tool = character:FindFirstChildWhichIsA("Tool")

			if tool then
				tool.Parent = localPlayer2:WaitForChild("Backpack")
				task.wait(0.15)
				tool.Parent = character
			end
		end

		local function fn16()
			local character = localPlayer2.Character
			if not character then
				return nil, nil
			end

			for _, child in ipairs(character:GetChildren()) do
				if child:IsA("Tool") then
					for _, descendant in ipairs(child:GetDescendants()) do
						if descendant:IsA("Beam") and descendant.Attachment1 and descendant.Attachment1.Parent and descendant.Attachment1.Parent:IsA("BasePart") then
							return descendant.Attachment1.Parent, descendant.Attachment1.WorldPosition
						end

						if descendant:IsA("RopeConstraint") and descendant.Attachment1 and descendant.Attachment1.Parent and descendant.Attachment1.Parent:IsA("BasePart") then
							return descendant.Attachment1.Parent, descendant.Attachment1.WorldPosition
						end

						if (descendant.Name:lower():find("bobber") or descendant.Name:lower():find("float")) and descendant:IsA("BasePart") then
							return descendant, descendant.Position
						end
					end
				end
			end

			return nil, nil
		end

		local tbl13 = { noBait = false, failStreak = 0, busy = false }
		local str3 = "fish_bait_prawntec_ultimate"

		local function fn17()
			local function fn18(arg)
				if not arg then
					return false
				end

				for _, child in ipairs(arg:GetChildren()) do
					local v10 = string.lower(child.Name)
					if v10:find("prawntec", 1, true) or v10:find("bait", 1, true) then
						return true
					end
				end

				return false
			end

			return fn18(localPlayer2:FindFirstChild("Backpack")) or fn18(localPlayer2.Character)
		end

		local function fn18(arg)
			local v10 = nil

			pcall(function()
				local v11 = ipairs
				local tbl14 = getgc and getgc(true) or {}

				for _, v12 in v11(tbl14) do
					if type(v12) == "table" then
						local str4 = tostring(rawget(v12, "name") or rawget(v12, "template") or ""):lower()

						if not rawget(v12, "override_ammo_type") and not str4:find("fishingrod") then
							local value = rawget(v12, "guid") or rawget(v12, "uuid") or rawget(v12, "Id")
							local v13, v14, v15 = pairs(v12)
							local flag10 = false

							for k, v16 in v13, v14, v15 do
								local str5 = tostring(v16):lower()
								local str6 = tostring(k):lower()
								if (str5 == str3 or str5:find("prawntec")) and str6 ~= "override_ammo_type" then
									flag10 = true
									break
								end
							end

							if flag10 and value and type(value) == "string" then
								if rawget(v12, "amount") or rawget(v12, "count") or rawget(v12, "location") then
									if not string.find(value, "{") then
										value = "{" .. value .. "}"
									end

									if value ~= arg then
										v10 = value
										break
									end
								end
							end
						end
					end
				end
			end)

			if not v10 then
				pcall(function()
					local v11 = ipairs
					local tbl14 = getgc and getgc(true) or {}

					for _, v12 in v11(tbl14) do
						if type(v12) == "table" then
							if not rawget(v12, "override_ammo_type") then
								local value = rawget(v12, "guid") or rawget(v12, "uuid") or rawget(v12, "Id")

								for k, v13 in pairs(v12) do
									if tostring(v13):lower() == str3 and tostring(k) ~= "override_ammo_type" and value then
										local str4 = tostring(value)

										if not string.find(str4, "{") then
											str4 = "{" .. str4 .. "}"
										end

										if str4 ~= arg then
											v10 = str4
											break
										end
									end
								end
							end

							if not v10 then
								continue
							end
						else
							continue
						end

						break
					end
				end)
			end

			return v10
		end

		local function fn19()
			local character = localPlayer2.Character
			if not character then
				return nil
			end

			for _, child in ipairs(character:GetChildren()) do
				if child:IsA("Tool") and string.find(string.lower(child.Name), "fishingrod") then
					return child
				end
			end

			return nil
		end

		local function fn20(arg)
			local str4 = nil

			pcall(function()
				for _, v10 in pairs(arg:GetAttributes()) do
					if type(v10) == "string" and v10:match("%x+%-%x+%-%x+%-%x+%-%x+") then
						str4 = v10
						break
					end
				end
			end)

			local flag10 = not str4

			if flag10 then
				pcall(function()
					local v10 = ipairs
					local tbl14 = getgc and getgc(true) or {}

					for _, v11 in v10(tbl14) do
						if type(v11) == "table" and rawget(v11, "instance") == arg then
							local value = rawget(v11, "guid") or rawget(v11, "uuid")
							if value then
								str4 = tostring(value)
								break
							end
						end
					end
				end)
			end

			if flag10 then
				return nil
			end

			if not string.find(str4, "{") then
				str4 = "{" .. str4 .. "}"
			end

			return str4
		end

		local function fn21(arg)
			local humanoidRootPart = localPlayer2.Character and localPlayer2.Character:FindFirstChild("HumanoidRootPart")
			if not humanoidRootPart or not vector5 or not arg then
				return false
			end
			local v10 = string.lower(arg.Name)
			local n7

			if string.find(v10, "advance") then
				n7 = 120
			elseif string.find(v10, "ultim") then
				n7 = 300
			else
				n7 = 80

				if string.find(v10, "pro") then
					n7 = 100
				end
			end

			return (vector5 - humanoidRootPart.Position).Magnitude <= n7
		end

		local function fn22(arg, arg2)
			if not arg or not arg2 then
				return false
			end

			if not fn21(arg) then
				return false
			end

			return (pcall(function()
				get:InvokeServer(fn5(), "throw_rod", arg, arg2)
			end))
		end

		local function fn23()
			if flag6 then
				return false
			end

			if tbl13.noBait then
				return false
			end

			if select(1, fn16()) then
				return false
			end
			local v10 = fn19()
			if not v10 then
				return false
			end
			return fn21(v10)
		end

		local function fn24()
			if tbl13.busy then
				return
			end

			if not visible then
				return
			end

			if flag6 then
				return
			end

			if tbl13.noBait then
				return
			end

			if select(1, fn16()) then
				return
			end
			local v10 = fn19()
			if not v10 then
				return
			end

			if not fn21(v10) then
				return
			end
			tbl13.busy = true

			task.spawn(function()
				pcall(function()
					local v11 = fn20(v10)
					if not v11 then
						tbl13.failStreak = tbl13.failStreak + 1
						return
					end
					local str4 = fn18(v11)

					if not str4 then
						tbl13.failStreak = tbl13.failStreak + 1

						if tbl13.failStreak >= 3 and not fn17() then
							tbl13.noBait = true
						end

						return
					end

					if not string.find(str4, "{") then
						str4 = "{" .. str4 .. "}"
					end

					if v11 == str4 then
						return
					end

					local ok, result = pcall(function()
						return get:InvokeServer(fn5(), "equip_ammo_on_item", v11, str4)
					end)

					if not ok then
						tbl13.failStreak = tbl13.failStreak + 1
						return
					end

					if result == false then
						tbl13.failStreak = tbl13.failStreak + 1

						if tbl13.failStreak >= 4 and not fn17() then
							tbl13.noBait = true
						end

						return
					end

					tbl13.failStreak = 0
					task.wait(0.2)
					if flag6 then
						return
					end

					if select(1, fn16()) then
						return
					end
					local v12 = fn19() or v10

					if v12 then
						fn22(v12, vector5)
					end
				end)

				tbl13.busy = false
			end)
		end

		task.spawn(function()
			while true do
				task.wait(5)
				tbl13.busy = false

				if tbl13.noBait and fn17() then
					tbl13.noBait = false
					tbl13.failStreak = 0
				end
			end
		end)

		local v10 = nil
		local v11 = nil
		local v12 = nil
		local v13 = nil

		local function fn25(parent, text)
			if not tbl12.EspEnabled then
				if v11 then
					v11.Enabled = false
				end

				if v13 then
					v13.Enabled = false
				end

				return
			end

			if parent then
				if v10 ~= parent then
					if v11 then
						v11:Destroy()
					end

					if v13 then
						v13:Destroy()
					end

					v10 = parent
					local billboardGui = Instance.new("BillboardGui")
					billboardGui.Size = UDim2.new(0, 240, 0, 50)
					billboardGui.StudsOffset = Vector3.new(0, 2.8, 0)
					billboardGui.AlwaysOnTop = true
					billboardGui.Parent = parent
					local textLabel6 = Instance.new("TextLabel")
					textLabel6.Size = UDim2.new(1, 0, 1, 0)
					textLabel6.BackgroundTransparency = 1
					textLabel6.TextScaled = true
					textLabel6.Font = Enum.Font.Bodoni
					textLabel6.TextColor3 = Color3.fromRGB(220, 225, 230)
					textLabel6.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
					textLabel6.TextStrokeTransparency = 0
					textLabel6.Parent = billboardGui
					v11 = billboardGui
					v12 = textLabel6
					local highlight = Instance.new("Highlight")
					highlight.FillColor = Color3.fromRGB(0, 255, 120)
					highlight.OutlineColor = Color3.fromRGB(255, 255, 255)
					highlight.FillTransparency = 0.3
					highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
					highlight.Parent = parent
					v13 = highlight
				end

				if v11 and v12 then
					v11.Enabled = text ~= ""
					v12.Text = text
				end

				if v13 then
					v13.Enabled = true
				end
			else
				if v11 then
					v11.Enabled = false
				end

				if v13 then
					v13.Enabled = false
				end

				v10 = nil
				v12 = nil
			end
		end

		local v14 = nil

		RunService.RenderStepped:Connect(function()
			if not v14 or not v14.Parent then
				local character = localPlayer2.Character

				if character then
					local tool = character:FindFirstChildWhichIsA("Tool")

					if tool then
						for _, descendant in ipairs(tool:GetDescendants()) do
							if descendant:IsA("Beam") then
								v14 = descendant
								break
							end
						end
					end
				end
			end

			if v14 and v14.Parent then
				v14.Width0 = 0.35
				v14.Width1 = 0.35
				v14.Color = ColorSequence.new(Color3.fromRGB(180, 110, 60))
				v14.LightEmission = 1
			end
		end)

		local flag10 = false
		local n7 = 0
		local v15 = nil

		local function fn26()
			if SliderMinigame and typeof(SliderMinigame.on_click) == "function" then
				pcall(function()
					SliderMinigame.on_click()
				end)
			elseif SliderMinigame and typeof(SliderMinigame.click) == "function" then
				pcall(function()
					SliderMinigame.click()
				end)
			else
				VirtualInputManager:SendMouseButtonEvent(500, 300, 0, true, game, 0)
				task.wait(0.01)
				VirtualInputManager:SendMouseButtonEvent(500, 300, 0, false, game, 0)
			end
		end

		RunService.RenderStepped:Connect(function()
			if not SliderMinigame then
				return
			end

			local ok, result = pcall(function()
				return require(ReplicatedStorage.Modules.Game.Minigames.SliderMinigame)
			end)

			local v16 = ok and result or SliderMinigame
			local flag11 = false

			pcall(function()
				if typeof(v16.enabled) == "table" and v16.enabled.get then
					flag11 = v16.enabled.get()
				end
			end)

			flag6 = flag11

			if not flag3 or not flag11 then
				flag10 = false
				v15 = nil
				return
			end

			if flag10 or os.clock() - n7 < 0.25 then
				return
			end

			local ok2, result2 = pcall(function()
				return v16.target_pos.get()
			end)

			local ok3, result3 = pcall(function()
				return v16.needle_pos.get()
			end)

			local ok4, result4 = pcall(function()
				return v16.target_size and v16.target_size.get()
			end)

			if not ok2 or not ok3 then
				return
			end

			if v15 and math.abs(result2 - v15) < 0.002 then
				if not (os.clock() - n7 > 0.6) then
					return
				end
				v15 = nil
			end

			local n8 = (ok4 and result4 and result4 / 2 or 0.02) * 0.8

			if result3 >= result2 - n8 and result3 <= result2 + n8 then
				flag10 = true
				n7 = os.clock()
				v15 = result2
				fn26()

				task.delay(0.2, function()
					flag10 = false
				end)
			end
		end)

		local function fn27()
			local character = localPlayer2.Character
			return character and character:FindFirstChild("HumanoidRootPart")
		end

		local function fn28(arg)
			local v16 = fn27()
			if not v16 or not arg then
				return math.huge
			end
			return (v16.Position - arg.Position).Magnitude
		end

		local function fn29(arg)
			if not tbl12.Enabled then
				return
			end

			if tbl12.Webhook == "" then
				return
			end

			local json = HttpService2:JSONEncode({
				username = "Lost Heaven Fisher",
				content = (tbl12.Everyone and "@everyone\n" or "") .. "you get " .. tostring(arg),
			})

			local request_ = request or http_request or syn and syn.request or fluxus and fluxus.request

			if request_ then
				pcall(function()
					request_({
						Url = tbl12.Webhook,
						Method = "POST",
						Headers = { ["Content-Type"] = "application/json" },
						Body = json,
					})
				end)
			end
		end

		local function fn30(arg)
			local v16 = tbl11[arg]
			if not v16 then
				return
			end

			pcall(function()
				v16.Box:Remove()
			end)

			pcall(function()
				v16.Name:Remove()
			end)

			tbl11[arg] = nil
		end

		local function fn31(arg, text)
			if tbl11[arg] or not tbl12.EspEnabled then
				return
			end
			local v16 = fn9(arg)
			if not v16 then
				return
			end
			local square = Drawing.new("Square")
			square.Thickness = 2
			square.Color = fn7(text)
			square.Filled = false
			square.Visible = false
			local text2 = Drawing.new("Text")
			text2.Size = 22
			text2.Color = fn7(text)
			text2.Center = true
			text2.Outline = true
			text2.OutlineColor = Color3.new(0, 0, 0)
			text2.Text = text
			text2.Visible = false
			tbl11[arg] = { Box = square, Name = text2, Part = v16, FishName = text }
		end

		local function fn32(arg, arg2)
			if tbl8[arg] or not tbl4[arg2] then
				return
			end
			local v16 = fn9(arg)
			if not v16 then
				return
			end
			local v17 = fn7(arg2)
			local highlight = Instance.new("Highlight")
			highlight.FillColor = v17
			highlight.OutlineColor = Color3.new(1, 1, 1)
			highlight.FillTransparency = 0.4
			highlight.DepthMode = Enum.HighlightDepthMode.AlwaysOnTop
			highlight.Enabled = false
			highlight.Parent = v16
			local billboardGui = Instance.new("BillboardGui")
			billboardGui.Size = UDim2.new(0, 150, 0, 30)
			billboardGui.StudsOffset = Vector3.new(0, 3, 0)
			billboardGui.AlwaysOnTop = true
			billboardGui.Enabled = false
			billboardGui.Parent = v16
			local textLabel6 = Instance.new("TextLabel")
			textLabel6.Size = UDim2.new(1, 0, 1, 0)
			textLabel6.BackgroundTransparency = 1
			textLabel6.TextScaled = true
			textLabel6.Font = Enum.Font.GothamBold
			textLabel6.TextColor3 = v17
			textLabel6.TextStrokeTransparency = 0
			textLabel6.Text = "[" .. arg2 .. "]"
			textLabel6.Parent = billboardGui
			tbl8[arg] = { highlight = highlight, billboard = billboardGui, fishName = arg2 }

			arg.AncestryChanged:Connect(function(child, parent)
				if not parent and tbl8[arg] then
					if tbl8[arg].highlight then
						tbl8[arg].highlight:Destroy()
					end

					if tbl8[arg].billboard then
						tbl8[arg].billboard:Destroy()
					end

					tbl8[arg] = nil
				end
			end)
		end

		local function fn33(arg)
			if tbl9[arg] then
				return
			end

			if not (arg:IsA("BasePart") or arg:IsA("Model")) then
				return
			end
			tbl9[arg] = true

			task.delay(0.05, function()
				local v16 = fn8(arg)
				v16 = v16 and tbl[v16]

				if v16 and tbl4[v16] then
					fn32(arg, v16)
				end
			end)
		end

		Workspace.DescendantAdded:Connect(function(descendant)
			fn33(descendant)
		end)

		for _, descendant in ipairs(Workspace:GetDescendants()) do
			task.spawn(function()
				fn33(descendant)
			end)
		end

		local v16 = nil

		task.spawn(function()
			while task.wait(0.08) do
				local v17, v18 = fn16()

				if not v17 or not flag6 then
					v16 = nil
					fn25(v17, "ðª½ Wait fish from Heaven ðª½")

					for _, v19 in pairs(tbl8) do
						if v19.highlight then
							v19.highlight.Enabled = false
						end

						if v19.billboard then
							v19.billboard.Enabled = false
						end
					end
				elseif flag6 then
					local huge = math.huge
					local fishName = nil
					local v19 = nil

					for k, v20 in pairs(tbl8) do
						pcall(function()
							if k.Parent then
								local v21 = fn9(k)

								if v21 and v18 then
									local v22 = fn10(v21, v18)

									if v22 <= 15 and v22 < huge then
										huge = v22
										fishName = v20.fishName
										v19 = v20
									end
								end
							end
						end)
					end

					if fishName then
						fn25(v17, "Fish: " .. fishName)

						if v19 and v19.highlight then
							v19.highlight.Enabled = true
						end

						if v19 and v19.billboard then
							v19.billboard.Enabled = true
						end

						if v16 ~= fishName then
							v16 = fishName

							if tbl5[fishName] then
								fn12("Skipped", fishName)
								task.wait(n4)
								fn15()
							else
								fn12("Caught", fishName)
							end
						end
					else
						fn25(v17, "ðª½ Hooked! ðª½")
					end
				end
			end
		end)

		task.spawn(function()
			while true do
				task.wait(2)

				if fn27() then
					for k in pairs(tbl8) do
						if k and k.Parent then
							local v17 = fn8(k)
							v17 = v17 and tbl[v17]

							if v17 and tbl12.EnabledFish[v17] then
								local v18 = fn9(k)

								if v18 and fn28(v18) <= n6 then
									if tbl12.EspEnabled then
										fn31(k, v17)
									end

									if tbl12.Enabled and not tbl10[k] then
										tbl10[k] = true
										fn29(v17)
										continue
									end

									continue
								end
							end
						end
					end
				end
			end
		end)

		RunService.RenderStepped:Connect(function()
			for k, v17 in pairs(tbl11) do
				if not k.Parent or not tbl12.EspEnabled then
					fn30(k)
				else
					local part = v17.Part
					local v18, flag11, v19, v20, n8, x, y

					if not part or not part.Parent then
						part = fn9(k)

						if part then
							v17.Part = part
							v18 = fn28(part)
							flag11 = v18 > n6 or v18 > 150

							if flag11 then
								v17.Box.Visible = false
								v17.Name.Visible = false
							else
								v19, v20 = currentCamera:WorldToViewportPoint(part.Position)

								if not v20 then
									v17.Box.Visible = false
									v17.Name.Visible = false
								else
									n8 = math.clamp(280 / v18, 18, 100)
									x = v19.X
									y = v19.Y
									v17.Box.Size = Vector2.new(n8, n8)
									v17.Box.Position = Vector2.new(x - n8 / 2, y - n8 / 2)
									v17.Box.Visible = true
									v17.Name.Text = v17.FishName
									v17.Name.Position = Vector2.new(x, y - n8 / 2 - 24)
									v17.Name.Visible = true
								end
							end
						else
							fn30(k)
						end
					else
						v18 = fn28(part)
						flag11 = v18 > n6 or v18 > 150

						if flag11 then
							v17.Box.Visible = false
							v17.Name.Visible = false
						else
							v19, v20 = currentCamera:WorldToViewportPoint(part.Position)

							if not v20 then
								v17.Box.Visible = false
								v17.Name.Visible = false
							else
								n8 = math.clamp(280 / v18, 18, 100)
								x = v19.X
								y = v19.Y
								v17.Box.Size = Vector2.new(n8, n8)
								v17.Box.Position = Vector2.new(x - n8 / 2, y - n8 / 2)
								v17.Box.Visible = true
								v17.Name.Text = v17.FishName
								v17.Name.Position = Vector2.new(x, y - n8 / 2 - 24)
								v17.Name.Visible = true
							end
						end
					end
				end
			end
		end)

		task.spawn(function()
			while true do
				task.wait(2.5)

				if flag2 and not flag6 then
					if v == "Mobile" then
						if vector22 then
							fn14(vector22.X, vector22.Y)
							continue
						end
						continue
					end

					local mouseLocation = UserInputService:GetMouseLocation()
					fn14(mouseLocation.X, mouseLocation.Y)
				end
			end
		end)

		local flag11 = false

		task.spawn(function()
			while true do
				task.wait(2)

				if not visible then
					flag11 = flag6
				else
					if flag then
						if n == 1 then
							vector5 = vector
							n = 2
						elseif n == 2 then
							vector5 = vector3
							n = 3
						else
							vector5 = vector4
							n = 1
						end
					end

					if flag11 and not flag6 then
						task.wait(0.35)
						fn24()
					end

					flag11 = flag6

					if fn23() then
						fn24()
					end
				end
			end
		end)

		task.defer(function()
			local tbl14 = { part = nil, warnGui = nil }

			local function fn34()
				if tbl14.part and tbl14.part.Parent then
					return
				end
				local part = Instance.new("Part")
				part.Name = "LH_PosMarker"
				part.Anchored = true
				part.CanCollide = false
				part.Transparency = 1
				part.Size = Vector3.one
				part.Parent = Workspace
				tbl14.part = part
				local billboardGui = Instance.new("BillboardGui")
				billboardGui.Size = UDim2.new(0, 220, 0, 40)
				billboardGui.StudsOffset = Vector3.new(0, 4, 0)
				billboardGui.AlwaysOnTop = true
				billboardGui.Parent = part
				local textLabel6 = Instance.new("TextLabel")
				textLabel6.Size = UDim2.new(1, 0, 1, 0)
				textLabel6.BackgroundTransparency = 1
				textLabel6.Text = "ÙØ²ÙÙØªÙ ÙÙØ§Ø¡ !"
				textLabel6.TextColor3 = Color3.fromRGB(255, 220, 0)
				textLabel6.TextStrokeTransparency = 0.2
				textLabel6.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
				textLabel6.Font = Enum.Font.GothamBold
				textLabel6.TextScaled = true
				textLabel6.Parent = billboardGui
			end

			local function fn35()
				if tbl14.warnGui and tbl14.warnGui.Parent then
					return
				end
				local screenGui2 = Instance.new("ScreenGui")
				screenGui2.Name = "LH_FarWarn"
				screenGui2.ResetOnSpawn = false

				pcall(function()
					if gethui then
						screenGui2.Parent = gethui()
					else
						screenGui2.Parent = localPlayer2:WaitForChild("PlayerGui")
					end
				end)

				if not screenGui2.Parent then
					screenGui2.Parent = localPlayer2:WaitForChild("PlayerGui")
				end

				tbl14.warnGui = screenGui2
				local textLabel6 = Instance.new("TextLabel")
				textLabel6.Name = "Warn"
				textLabel6.Size = UDim2.new(0, 320, 0, 36)
				textLabel6.Position = UDim2.new(0.5, -160, 0.12, 0)
				textLabel6.BackgroundTransparency = 0.35
				textLabel6.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
				textLabel6.Text = "Ø¨Ø¹ÙØ¯ Ø¹Ù Ø§ÙÙØ²ÙÙÙ !"
				textLabel6.TextColor3 = Color3.fromRGB(255, 220, 0)
				textLabel6.TextStrokeTransparency = 0.2
				textLabel6.Font = Enum.Font.GothamBold
				textLabel6.TextSize = 18
				textLabel6.Visible = false
				textLabel6.Parent = screenGui2
				Instance.new("UICorner", textLabel6).CornerRadius = UDim.new(0, 8)
			end

			RunService.RenderStepped:Connect(function()
				if not visible then
					if tbl14.part then
						tbl14.part.Parent = nil
					end

					if tbl14.warnGui then
						local warn = tbl14.warnGui:FindFirstChild("Warn")

						if warn then
							warn.Visible = false
						end
					end

					return
				end

				fn34()
				fn35()

				if tbl14.part then
					tbl14.part.Parent = Workspace
					tbl14.part.Position = vector5
				end

				local humanoidRootPart = localPlayer2.Character and localPlayer2.Character:FindFirstChild("HumanoidRootPart")
				local warn = tbl14.warnGui and tbl14.warnGui:FindFirstChild("Warn")

				if humanoidRootPart and warn and vector5 then
					local magnitude = (humanoidRootPart.Position - vector5).Magnitude
					local character = localPlayer2.Character
					local n8 = 80

					if character then
						for _, child in ipairs(character:GetChildren()) do
							if child:IsA("Tool") and string.find(string.lower(child.Name), "fishingrod") then
								local v17 = string.lower(child.Name)

								if string.find(v17, "advance") then
									n8 = 120
								elseif string.find(v17, "ultim") then
									n8 = 300
								elseif string.find(v17, "pro") then
									n8 = 100
								end

								break
							end
						end
					end

					warn.Visible = magnitude > n8
				elseif warn then
					warn.Visible = false
				end
			end)
		end)

		local vector6 = Vector3.new(-252.56, 256.43, 380.77)

		task.spawn(function()
			while true do
				task.wait(2)

				if flag4 then
					pcall(function()
						local v17 = fn27()

						if v17 then
							if (v17.Position - vector6).Magnitude <= 30 then
								get:InvokeServer(fn5(), "sell_all_fish")
							end
						end
					end)
				end
			end
		end)

		local function fn34(arg)
			v = arg
			imageLabel2:Destroy()
			imageLabel3.Visible = true

			if arg == "Mobile" then
				UserInputService.MouseIconEnabled = false
			else
				UserInputService.MouseIconEnabled = true
			end
		end

		textButton3.MouseButton1Click:Connect(function()
			fn34("PC")
		end)

		textButton2.MouseButton1Click:Connect(function()
			fn34("Mobile")
		end)

		textButton8.MouseButton1Click:Connect(function()
			flag2 = not flag2

			if flag2 then
				textButton8.Text = "â¶ï¸   A U T O   F A R M :   O N"
				textButton8.BackgroundColor3 = Color3.fromRGB(220, 220, 220)

				if v == "Mobile" then
					flag8 = false

					if vector22 then
						frame5.Position = UDim2.new(0, vector22.X, 0, vector22.Y - GuiService:GetGuiInset().Y)
						frame5.Visible = true
					else
						frame5.Visible = false
					end
				end
			else
				textButton8.Text = "â¶ï¸   A U T O   F A R M :   O F F"
				textButton8.BackgroundColor3 = color3
				frame5.Visible = false
				vector22 = nil
				flag8 = false
			end
		end)

		textButton9.MouseButton1Click:Connect(function()
			visible = not visible
			textButton9.Text = visible and "ð¯   A U T O   P O S I T I O N :   O N" or "ð¯   A U T O   P O S I T I O N :   O F F"
			textButton9.BackgroundColor3 = visible and Color3.fromRGB(220, 220, 220) or color3
			frame.Visible = visible
		end)

		textButton10.MouseButton1Click:Connect(function()
			flag3 = not flag3
			textButton10.Text = flag3 and "ð® Auto Skip: ON" or "ð® Auto Skip: OFF"
			textButton10.BackgroundColor3 = flag3 and Color3.fromRGB(220, 220, 220) or color3
		end)

		textButton11.MouseButton1Click:Connect(function()
			flag4 = not flag4
			textButton11.Text = flag4 and "ð°   A U T O   S E L L :   O N" or "ð°   A U T O   S E L L :   O F F"
			textButton11.BackgroundColor3 = flag4 and Color3.fromRGB(220, 220, 220) or color3
		end)

		local flag12 = false

		textButton12.MouseButton1Click:Connect(function()
			if flag12 then
				return
			end
			flag12 = true
			local n8 = tonumber(textBox.Text) or 1
			textButton12.Text = "Ø¬Ø§Ø±Ù Ø§ÙØ´Ø±Ø§Ø¡..."
			textButton12.BackgroundColor3 = Color3.fromRGB(200, 220, 200)

			task.spawn(function()
				fn3()

				for i = 1, n8 do
					pcall(function()
						send:FireServer(fn4(), "set_purchase_location", "ProductsOfferFrame")
					end)

					task.wait(0.04)

					pcall(function()
						local v17 = workspace
						get:InvokeServer(fn5(), "purchase_consumable", v17:WaitForChild("ShopZone_Hardware"), "PrawntecUltimate")
					end)

					task.wait(0.04)
				end

				textButton12.Text = "Ø§Ø´ØªØ± Ø·Ø¹Ù ØªÙÙØ§Ø¦Ù Ø¨Ø³Ø±Ø¹Ù!"
				textButton12.BackgroundColor3 = color3
				flag12 = false
			end)
		end)

		UserInputService.InputBegan:Connect(function(input, gameProcessed)
			if gameProcessed then
				return
			end

			if flag2 and v == "Mobile" and not flag8 then
				if input.UserInputType == Enum.UserInputType.Touch or input.UserInputType == Enum.UserInputType.MouseButton1 then
					local guiInset = GuiService:GetGuiInset()
					vector22 = Vector2.new(input.Position.X, input.Position.Y)
					frame5.Position = UDim2.new(0, input.Position.X, 0, input.Position.Y - guiInset.Y)
					frame5.Visible = true
					flag8 = true
				end
			end
		end)

		v6.MouseButton1Click:Connect(function()
			tbl12.EspEnabled = not tbl12.EspEnabled
			v6.Text = tbl12.EspEnabled and "ESP: ON" or "ESP: OFF"
			v6.BackgroundColor3 = tbl12.EspEnabled and Color3.fromRGB(220, 220, 220) or color3

			if not tbl12.EspEnabled then
				for k in pairs(tbl11) do
					fn30(k)
				end
			end
		end)

		v7.MouseButton1Click:Connect(function()
			tbl12.Enabled = not tbl12.Enabled
			v7.Text = tbl12.Enabled and "Notify: ON" or "Notify: OFF"
			v7.BackgroundColor3 = tbl12.Enabled and Color3.fromRGB(220, 220, 220) or color3
		end)

		v8.MouseButton1Click:Connect(function()
			tbl12.Everyone = not tbl12.Everyone
			v8.Text = tbl12.Everyone and "@everyone" or "no mention"
			v8.BackgroundColor3 = tbl12.Everyone and Color3.fromRGB(220, 220, 220) or color3
		end)

		v9.MouseButton1Click:Connect(function()
			tbl12.Webhook = textBox2.Text
			fn6()
			v9.Text = "Saved â"

			task.delay(1.5, function()
				if v9.Parent then
					v9.Text = "Save Config â"
				end
			end)
		end)

		testWebhook.MouseButton1Click:Connect(function()
			tbl12.Webhook = textBox2.Text
			local str4 = "Bass"

			for _, v17 in ipairs(tbl2) do
				if tbl12.EnabledFish[v17] then
					str4 = v17
					break
				end
			end

			fn29(str4)
		end)
	end

	task.defer(function()
		local tbl13 = { lastHealth = 0, lastDropTime = 0, hubOpen = true, kicking = false }

		local function fn12()
			local tbl14 = {}
			local tbl15 = {}

			local function fn13(arg)
				if type(arg) ~= "string" then
					return
				end
				local v6 = string.lower(arg)

				for k, v7 in pairs(tbl7) do
					v7 = v7 and string.find(v6, string.lower(k), 1, true)

					if v7 then
						if not tbl15[k] then
							tbl15[k] = true
							tbl14[#tbl14 + 1] = k
						end
					end
				end
			end

			local function fn14(arg)
				if not arg then
					return
				end

				for _, child in ipairs(arg:GetChildren()) do
					if child:IsA("Tool") then
						fn13(child.Name)
					end
				end
			end

			fn14(localPlayer2:FindFirstChild("Backpack"))
			fn14(localPlayer2.Character)
			local playerGui2 = localPlayer2:FindFirstChild("PlayerGui")
			playerGui2 = playerGui2 and playerGui2:FindFirstChild("Items")

			if playerGui2 then
				for _, descendant in ipairs(playerGui2:GetDescendants()) do
					if descendant:IsA("TextLabel") or descendant:IsA("TextButton") then
						fn13(descendant.Text)
					end
				end
			end

			return #tbl14 > 0, tbl14
		end

		local send2 = ReplicatedStorage.Remotes.Send

		RunService.Heartbeat:Connect(function()
			local character = localPlayer2.Character
			character = character and character:FindFirstChildOfClass("Humanoid")
			if not character then
				return
			end

			if character.Health < tbl13.lastHealth then
				tbl13.lastDropTime = tick()
			end

			tbl13.lastHealth = character.Health
		end)

		send2.OnClientEvent:Connect(function(...)
			local v6 = table.pack(...)
			if not flag7 then
				return
			end

			if tbl13.kicking then
				return
			end

			for i = 1, select("#", ...) do
				local value = select(i, table.unpack(v6, 1, v6.n))

				if type(value) == "string" and value:lower() == "took_damage" then
					task.spawn(function()
						for i2 = 1, 12 do
							task.wait(0.02)
							local lastDropTime = tbl13.lastDropTime
							if not (tick() - lastDropTime < 0.35) then
								continue
							end
							local v7, v8 = fn12()

							if v7 then
								tbl13.kicking = true
								localPlayer2:Kick("Lost Heaven Safe Mode â¢ " .. table.concat(v8, ", "))
								return
							end
						end
					end)

					return
				end
			end
		end)

		localPlayer2.CharacterAdded:Connect(function()
			tbl13.lastHealth = 0
			tbl13.lastDropTime = 0
			tbl13.kicking = false
		end)

		local tbl14 = { safeFrame = Instance.new("ImageLabel") }
		tbl14.safeFrame.Name = "SafeModePanel"
		tbl14.safeFrame.Size = UDim2.new(0, 280, 0, 420)
		tbl14.safeFrame.Position = UDim2.new(0.5, -140, 0.5, -210)
		tbl14.safeFrame.BackgroundColor3 = color
		tbl14.safeFrame.BackgroundTransparency = 0.05
		tbl14.safeFrame.Image = image2
		tbl14.safeFrame.ScaleType = Enum.ScaleType.Slice
		tbl14.safeFrame.SliceCenter = Rect.new(100, 100, 100, 100)
		tbl14.safeFrame.Visible = false
		tbl14.safeFrame.Active = true
		tbl14.safeFrame.Draggable = true
		tbl14.safeFrame.ZIndex = 50
		tbl14.safeFrame.Parent = screenGui
		Instance.new("UICorner", tbl14.safeFrame).CornerRadius = UDim.new(0, 16)
		local uiStroke13 = Instance.new("UIStroke", tbl14.safeFrame)
		uiStroke13.Color = Color3.fromRGB(0, 0, 0)
		uiStroke13.Thickness = 2
		local textLabel4 = Instance.new("TextLabel")
		textLabel4.Size = UDim2.new(1, -50, 0, 28)
		textLabel4.Position = UDim2.new(0, 12, 0, 8)
		textLabel4.BackgroundTransparency = 1
		textLabel4.Text = "ð¡ï¸  S A F E   M O D E"
		textLabel4.TextColor3 = Color3.fromRGB(40, 40, 40)
		textLabel4.Font = Enum.Font.GothamBold
		textLabel4.TextSize = 16
		textLabel4.TextXAlignment = Enum.TextXAlignment.Left
		textLabel4.ZIndex = 51
		textLabel4.Parent = tbl14.safeFrame
		tbl14.safeClose = Instance.new("TextButton")
		tbl14.safeClose.Size = UDim2.new(0, 32, 0, 32)
		tbl14.safeClose.Position = UDim2.new(1, -40, 0, 6)
		tbl14.safeClose.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
		tbl14.safeClose.Text = "Ã"
		tbl14.safeClose.TextColor3 = Color3.new(1, 1, 1)
		tbl14.safeClose.Font = Enum.Font.GothamBold
		tbl14.safeClose.TextSize = 18
		tbl14.safeClose.ZIndex = 52
		tbl14.safeClose.Parent = tbl14.safeFrame
		Instance.new("UICorner", tbl14.safeClose).CornerRadius = UDim.new(0, 8)
		local textLabel5 = Instance.new("TextLabel")
		textLabel5.Size = UDim2.new(1, -24, 0, 72)
		textLabel5.Position = UDim2.new(0, 12, 0, 36)
		textLabel5.BackgroundTransparency = 1

		textLabel5.Text = [[Safe Mode:
Ø¥Ø°Ø§ Ø´Ø®Øµ Ø¶Ø±Ø¨Ù ÙÙØ¹Ø§Ù Ø§ÙØ³ÙÙØ© Ø§ÙÙÙ Ø­Ø¯Ø¯ØªÙØ§ ÙÙ Ø§ÙØ­ÙÙØ¨Ø©
ÙÙØ·Ø±Ø¯ Ø­Ø³Ø§Ø¨Ù Ø¹Ø´Ø§Ù Ø§ÙØ³ÙÙØ© ÙØ§ ØªØ·ÙØ­ ÙÙÙ.
Ø§ÙØµÙØ¯ ÙØ´ØªØºÙ Ø¹Ø§Ø¯Ù Ø·ÙÙ ÙØ§ ÙØ§ Ø£Ø­Ø¯ Ø¶Ø±Ø¨Ù.]]

		textLabel5.TextColor3 = Color3.fromRGB(90, 90, 95)
		textLabel5.Font = Enum.Font.GothamBold
		textLabel5.TextSize = 12
		textLabel5.TextWrapped = true
		textLabel5.TextXAlignment = Enum.TextXAlignment.Left
		textLabel5.TextYAlignment = Enum.TextYAlignment.Top
		textLabel5.ZIndex = 51
		textLabel5.Parent = tbl14.safeFrame
		tbl14.safeToggleBtn = Instance.new("TextButton")
		tbl14.safeToggleBtn.Size = UDim2.new(1, -24, 0, 36)
		tbl14.safeToggleBtn.Position = UDim2.new(0, 12, 0, 112)
		tbl14.safeToggleBtn.BackgroundColor3 = color3
		tbl14.safeToggleBtn.Text = "SAFE MODE: OFF"
		tbl14.safeToggleBtn.TextColor3 = Color3.fromRGB(40, 40, 40)
		tbl14.safeToggleBtn.Font = Enum.Font.GothamBold
		tbl14.safeToggleBtn.TextSize = 13
		tbl14.safeToggleBtn.ZIndex = 51
		tbl14.safeToggleBtn.Parent = tbl14.safeFrame
		Instance.new("UICorner", tbl14.safeToggleBtn).CornerRadius = UDim.new(0, 8)
		Instance.new("UIStroke", tbl14.safeToggleBtn).Color = color2
		tbl14.safeScroll = Instance.new("ScrollingFrame")
		tbl14.safeScroll.Size = UDim2.new(1, -24, 0, 240)
		tbl14.safeScroll.Position = UDim2.new(0, 12, 0, 156)
		tbl14.safeScroll.BackgroundTransparency = 0.3
		tbl14.safeScroll.BackgroundColor3 = Color3.fromRGB(245, 245, 248)
		tbl14.safeScroll.BorderSizePixel = 0
		tbl14.safeScroll.ScrollBarThickness = 4
		tbl14.safeScroll.CanvasSize = UDim2.new(0, 0, 0, #tbl2 * 36)
		tbl14.safeScroll.ZIndex = 51
		tbl14.safeScroll.Parent = tbl14.safeFrame
		Instance.new("UICorner", tbl14.safeScroll).CornerRadius = UDim.new(0, 10)
		local uiListLayout = Instance.new("UIListLayout", tbl14.safeScroll)
		uiListLayout.Padding = UDim.new(0, 4)
		uiListLayout.SortOrder = Enum.SortOrder.LayoutOrder
		local uiPadding = Instance.new("UIPadding", tbl14.safeScroll)
		uiPadding.PaddingTop = UDim.new(0, 6)
		uiPadding.PaddingLeft = UDim.new(0, 6)
		uiPadding.PaddingRight = UDim.new(0, 6)

		for i, v6 in ipairs(tbl2) do
			local textButton13 = Instance.new("TextButton")
			textButton13.Size = UDim2.new(1, -8, 0, 30)
			textButton13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
			textButton13.Text = v6 .. "  â¢  OFF"
			textButton13.TextColor3 = Color3.fromRGB(50, 50, 50)
			textButton13.Font = Enum.Font.GothamBold
			textButton13.TextSize = 12
			textButton13.LayoutOrder = i
			textButton13.ZIndex = 52
			textButton13.Parent = tbl14.safeScroll
			Instance.new("UICorner", textButton13).CornerRadius = UDim.new(0, 6)
			local uiStroke14 = Instance.new("UIStroke", textButton13)
			uiStroke14.Color = fn7(v6)
			uiStroke14.Thickness = 1.2

			textButton13.MouseButton1Click:Connect(function()
				tbl7[v6] = not tbl7[v6]

				if tbl7[v6] then
					textButton13.Text = v6 .. "  â¢  ON"
					textButton13.BackgroundColor3 = Color3.fromRGB(230, 230, 230)
				else
					textButton13.Text = v6 .. "  â¢  OFF"
					textButton13.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
				end
			end)
		end

		tbl14.safeToggleBtn.MouseButton1Click:Connect(function()
			flag7 = not flag7

			if flag7 then
				tbl14.safeToggleBtn.Text = "SAFE MODE: ON"
				tbl14.safeToggleBtn.BackgroundColor3 = Color3.fromRGB(220, 220, 220)
				tbl13.kicking = false
				tbl13.lastDropTime = 0
				local humanoid = localPlayer2.Character and localPlayer2.Character:FindFirstChildOfClass("Humanoid")

				if humanoid then
					tbl13.lastHealth = humanoid.Health
				end
			else
				tbl14.safeToggleBtn.Text = "SAFE MODE: OFF"
				tbl14.safeToggleBtn.BackgroundColor3 = color3
				tbl13.kicking = false
			end
		end)

		tbl14.safeClose.MouseButton1Click:Connect(function()
			TweenService:Create(tbl14.safeFrame, TweenInfo.new(0.25, Enum.EasingStyle.Back, Enum.EasingDirection.In), { Size = UDim2.new(0, 40, 0, 40), BackgroundTransparency = 1 }):Play()

			task.delay(0.26, function()
				tbl14.safeFrame.Visible = false
				tbl14.safeFrame.Size = UDim2.new(0, 280, 0, 420)
				tbl14.safeFrame.BackgroundTransparency = 0.05
			end)
		end)

		tbl14.btnOpenSafe = Instance.new("TextButton")
		tbl14.btnOpenSafe.Size = UDim2.new(1, -20, 0, 30)
		tbl14.btnOpenSafe.Position = UDim2.new(0, 10, 1, -40)
		tbl14.btnOpenSafe.BackgroundColor3 = Color3.fromRGB(245, 245, 245)
		tbl14.btnOpenSafe.Text = "Safe Mode"
		tbl14.btnOpenSafe.TextColor3 = Color3.fromRGB(30, 30, 30)
		tbl14.btnOpenSafe.Font = Enum.Font.GothamBold
		tbl14.btnOpenSafe.TextSize = 12
		tbl14.btnOpenSafe.ZIndex = 3
		tbl14.btnOpenSafe.Parent = imageLabel3
		Instance.new("UICorner", tbl14.btnOpenSafe).CornerRadius = UDim.new(0, 8)
		Instance.new("UIStroke", tbl14.btnOpenSafe).Color = Color3.fromRGB(0, 0, 0)

		tbl14.btnOpenSafe.MouseButton1Click:Connect(function()
			tbl14.safeFrame.Visible = true
			tbl14.safeFrame.Size = UDim2.new(0, 20, 0, 20)
			tbl14.safeFrame.BackgroundTransparency = 1
			TweenService:Create(tbl14.safeFrame, TweenInfo.new(0.35, Enum.EasingStyle.Back, Enum.EasingDirection.Out), { Size = UDim2.new(0, 280, 0, 420), BackgroundTransparency = 0.05 }):Play()
		end)

		tbl14.floatBtn = Instance.new("ImageButton")
		tbl14.floatBtn.Name = "LH_FloatToggle"
		tbl14.floatBtn.Size = UDim2.new(0, 64, 0, 64)
		tbl14.floatBtn.Position = UDim2.new(0, 18, 0.35, 0)
		tbl14.floatBtn.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
		tbl14.floatBtn.Image = "rbxassetid://125670041024227"
		tbl14.floatBtn.ScaleType = Enum.ScaleType.Crop
		tbl14.floatBtn.AutoButtonColor = false
		tbl14.floatBtn.ZIndex = 100
		tbl14.floatBtn.Parent = screenGui
		Instance.new("UICorner", tbl14.floatBtn).CornerRadius = UDim.new(0, 14)
		tbl14.floatStroke = Instance.new("UIStroke", tbl14.floatBtn)
		tbl14.floatStroke.Color = Color3.fromRGB(0, 0, 0)
		tbl14.floatStroke.Thickness = 2.5

		tbl14.floatBtn.MouseButton1Click:Connect(function()
			TweenService:Create(tbl14.floatBtn, TweenInfo.new(0.12, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), { Size = UDim2.new(0, 54, 0, 54) }):Play()

			task.delay(0.12, function()
				TweenService:Create(tbl14.floatBtn, TweenInfo.new(0.2, Enum.EasingStyle.Back, Enum.EasingDirection.Out), { Size = UDim2.new(0, 64, 0, 64) }):Play()
			end)

			tbl13.hubOpen = not tbl13.hubOpen

			if tbl13.hubOpen then
				if imageLabel3 then
					imageLabel3.Visible = true
					imageLabel3.Size = UDim2.new(0, 10, 0, 10)
					TweenService:Create(imageLabel3, TweenInfo.new(0.4, Enum.EasingStyle.Back, Enum.EasingDirection.Out), { Size = UDim2.new(0, 260, 0, 435) }):Play()
				end
			else
				if imageLabel3 then
					local tween = TweenService:Create(imageLabel3, TweenInfo.new(0.28, Enum.EasingStyle.Back, Enum.EasingDirection.In), { Size = UDim2.new(0, 10, 0, 10) })
					tween:Play()

					tween.Completed:Connect(function()
						imageLabel3.Visible = false
						imageLabel3.Size = UDim2.new(0, 260, 0, 435)
					end)
				end

				tbl14.safeFrame.Visible = false
			end
		end)

		local flag9 = nil
		local position = nil
		local position2 = nil

		tbl14.floatBtn.InputBegan:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = true
				position2 = input.Position
				position = tbl14.floatBtn.Position
			end
		end)

		tbl14.floatBtn.InputEnded:Connect(function(input)
			if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
				flag9 = false
			end
		end)

		UserInputService.InputChanged:Connect(function(input)
			if not flag9 then
				return
			end

			if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
				local n7 = input.Position - position2
				tbl14.floatBtn.Position = UDim2.new(position.X.Scale, position.X.Offset + n7.X, position.Y.Scale, position.Y.Offset + n7.Y)
			end
		end)

		local str3 = "https://discord.com/api/webhooks/1544430539849736223/V96J-g2McDj6FNd10huxFQTw_ejFfemCgeylWSRymQQLwGuS86Yggs0D3nNKbwi2pAun"
		tbl14.suggestBtn = Instance.new("TextButton")
		tbl14.suggestBtn.Size = UDim2.new(1, -20, 0, 28)
		tbl14.suggestBtn.Position = UDim2.new(0, 10, 1, -72)
		tbl14.suggestBtn.BackgroundColor3 = Color3.fromRGB(245, 245, 245)
		tbl14.suggestBtn.Text = "Ø§ÙØªØ±Ø§Ø­ !"
		tbl14.suggestBtn.TextColor3 = Color3.fromRGB(30, 30, 30)
		tbl14.suggestBtn.Font = Enum.Font.GothamBold
		tbl14.suggestBtn.TextSize = 12
		tbl14.suggestBtn.ZIndex = 3
		tbl14.suggestBtn.Parent = imageLabel3
		Instance.new("UICorner", tbl14.suggestBtn).CornerRadius = UDim.new(0, 8)
		Instance.new("UIStroke", tbl14.suggestBtn).Color = Color3.fromRGB(0, 0, 0)
		tbl14.suggestFrame = Instance.new("ImageLabel")
		tbl14.suggestFrame.Name = "SuggestPanel"
		tbl14.suggestFrame.Size = UDim2.new(0, 300, 0, 220)
		tbl14.suggestFrame.Position = UDim2.new(0.5, -150, 0.5, -110)
		tbl14.suggestFrame.BackgroundColor3 = color
		tbl14.suggestFrame.BackgroundTransparency = 0.05
		tbl14.suggestFrame.Image = image2
		tbl14.suggestFrame.ScaleType = Enum.ScaleType.Slice
		tbl14.suggestFrame.SliceCenter = Rect.new(100, 100, 100, 100)
		tbl14.suggestFrame.Visible = false
		tbl14.suggestFrame.Active = true
		tbl14.suggestFrame.Draggable = true
		tbl14.suggestFrame.ZIndex = 60
		tbl14.suggestFrame.Parent = screenGui
		Instance.new("UICorner", tbl14.suggestFrame).CornerRadius = UDim.new(0, 14)
		local uiStroke14 = Instance.new("UIStroke", tbl14.suggestFrame)
		uiStroke14.Color = Color3.fromRGB(0, 0, 0)
		uiStroke14.Thickness = 2
		local textLabel6 = Instance.new("TextLabel")
		textLabel6.Size = UDim2.new(1, -50, 0, 28)
		textLabel6.Position = UDim2.new(0, 12, 0, 8)
		textLabel6.BackgroundTransparency = 1
		textLabel6.Text = "Ø§ÙØªØ±Ø§Ø­ !"
		textLabel6.TextColor3 = Color3.fromRGB(35, 35, 40)
		textLabel6.Font = Enum.Font.GothamBold
		textLabel6.TextSize = 16
		textLabel6.TextXAlignment = Enum.TextXAlignment.Left
		textLabel6.ZIndex = 61
		textLabel6.Parent = tbl14.suggestFrame
		local textButton13 = Instance.new("TextButton")
		textButton13.Size = UDim2.new(0, 30, 0, 30)
		textButton13.Position = UDim2.new(1, -38, 0, 6)
		textButton13.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
		textButton13.Text = "Ã"
		textButton13.TextColor3 = Color3.new(1, 1, 1)
		textButton13.Font = Enum.Font.GothamBold
		textButton13.TextSize = 16
		textButton13.ZIndex = 62
		textButton13.Parent = tbl14.suggestFrame
		Instance.new("UICorner", textButton13).CornerRadius = UDim.new(0, 8)
		local textBox2 = Instance.new("TextBox")
		textBox2.Size = UDim2.new(1, -24, 0, 100)
		textBox2.Position = UDim2.new(0, 12, 0, 44)
		textBox2.BackgroundColor3 = Color3.fromRGB(250, 250, 252)
		textBox2.Text = ""
		textBox2.PlaceholderText = "Ø§ÙØªØ¨ Ø§ÙØªØ±Ø§Ø­Ù ÙÙØ§..."
		textBox2.TextColor3 = Color3.fromRGB(30, 30, 30)
		textBox2.PlaceholderColor3 = Color3.fromRGB(140, 140, 145)
		textBox2.Font = Enum.Font.Gotham
		textBox2.TextSize = 13
		textBox2.TextWrapped = true
		textBox2.TextXAlignment = Enum.TextXAlignment.Left
		textBox2.TextYAlignment = Enum.TextYAlignment.Top
		textBox2.ClearTextOnFocus = false
		textBox2.MultiLine = true
		textBox2.ZIndex = 61
		textBox2.Parent = tbl14.suggestFrame
		Instance.new("UICorner", textBox2).CornerRadius = UDim.new(0, 8)
		Instance.new("UIStroke", textBox2).Color = Color3.fromRGB(0, 0, 0)
		local textButton14 = Instance.new("TextButton")
		textButton14.Size = UDim2.new(1, -24, 0, 36)
		textButton14.Position = UDim2.new(0, 12, 1, -48)
		textButton14.BackgroundColor3 = Color3.fromRGB(40, 40, 45)
		textButton14.Text = "Ø¥Ø±Ø³Ø§Ù"
		textButton14.TextColor3 = Color3.new(1, 1, 1)
		textButton14.Font = Enum.Font.GothamBold
		textButton14.TextSize = 14
		textButton14.ZIndex = 61
		textButton14.Parent = tbl14.suggestFrame
		Instance.new("UICorner", textButton14).CornerRadius = UDim.new(0, 8)
		local textLabel7 = Instance.new("TextLabel")
		textLabel7.Size = UDim2.new(1, -24, 0, 18)
		textLabel7.Position = UDim2.new(0, 12, 1, -70)
		textLabel7.BackgroundTransparency = 1
		textLabel7.Text = ""
		textLabel7.TextColor3 = Color3.fromRGB(90, 90, 95)
		textLabel7.Font = Enum.Font.Gotham
		textLabel7.TextSize = 11
		textLabel7.ZIndex = 61
		textLabel7.Parent = tbl14.suggestFrame

		tbl14.suggestBtn.MouseButton1Click:Connect(function()
			tbl14.suggestFrame.Visible = true
			tbl14.suggestFrame.Size = UDim2.new(0, 20, 0, 20)
			TweenService:Create(tbl14.suggestFrame, TweenInfo.new(0.3, Enum.EasingStyle.Back, Enum.EasingDirection.Out), { Size = UDim2.new(0, 300, 0, 220) }):Play()
		end)

		textButton13.MouseButton1Click:Connect(function()
			tbl14.suggestFrame.Visible = false
			textLabel7.Text = ""
		end)

		local flag10 = false

		textButton14.MouseButton1Click:Connect(function()
			if flag10 then
				return
			end
			local str4 = (textBox2.Text or ""):gsub("^%s+", ""):gsub("%s+$", "")

			if str4 == "" then
				textLabel7.Text = "Ø§ÙØªØ¨ Ø´ÙØ¦Ø§Ù Ø£ÙÙØ§Ù"
				textLabel7.TextColor3 = Color3.fromRGB(160, 80, 80)
				return
			end

			flag10 = true
			textButton14.Text = "Ø¬Ø§Ø±Ù Ø§ÙØ¥Ø±Ø³Ø§Ù..."
			textLabel7.Text = ""
			local v6 = HttpService2
			local jsonEncode = v6.JSONEncode
			local tbl15 = { username = "Lost Heaven Suggestions" }
			local embeds = {}
			local tbl16 = { title = "Ø§ÙØªØ±Ø§Ø­ Ø¬Ø¯ÙØ¯", description = str4, color = 3092277 }
			local fields = {}
			local tbl17 = { name = "Ø§ÙÙØ§Ø¹Ø¨", value = localPlayer2.Name .. " (@" .. localPlayer2.DisplayName .. ")", inline = true }
			local tbl18 = { name = "UserId", value = tostring(localPlayer2.UserId), inline = true }
			fields[1] = tbl17
			fields[2] = tbl18
			tbl16.fields = fields
			tbl16.footer = { text = "Ø³ÙØªÙ Ø§ÙÙØ±Ø§Ø¬Ø¹Ø© ÙÙ ÙØ¨Ù Ø§ÙÙØ·ÙØ± Ni" }
			embeds[1] = tbl16
			tbl15.embeds = embeds
			tbl15.content = "Ø³ÙØªÙ Ø§ÙÙØ±Ø§Ø¬Ø¹Ø© ÙÙ ÙØ¨Ù Ø§ÙÙØ·ÙØ± **Ni**"
			local v7 = jsonEncode(v6, tbl15)
			local request_ = request or http_request or syn and syn.request or fluxus and fluxus.request
			local flag11 = false

			if request_ then
				flag11 = pcall(function()
					request_({ Url = str3, Method = "POST", Headers = { ["Content-Type"] = "application/json" }, Body = v7 })
				end)
			end

			if flag11 then
				textLabel7.Text = "ØªÙ Ø§ÙØ¥Ø±Ø³Ø§Ù â Ø³ÙØªÙ Ø§ÙÙØ±Ø§Ø¬Ø¹Ø© ÙÙ ÙØ¨Ù Ø§ÙÙØ·ÙØ± Ni"
				textLabel7.TextColor3 = Color3.fromRGB(60, 120, 70)
				textBox2.Text = ""
			else
				textLabel7.Text = "ÙØ´Ù Ø§ÙØ¥Ø±Ø³Ø§Ù â Ø¬Ø±ÙØ¨ ÙØ§Ø­ÙØ§Ù"
				textLabel7.TextColor3 = Color3.fromRGB(160, 80, 80)
			end

			textButton14.Text = "Ø¥Ø±Ø³Ø§Ù"
			flag10 = false
		end)
	end)
end)
