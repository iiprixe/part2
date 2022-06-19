
local console = Instance.new("ScreenGui")
local console_2 = Instance.new("Frame")
local UICorner = Instance.new("UICorner")
local Frame = Instance.new("Frame")
local ImageButton = Instance.new("ImageButton")
local TextLabel = Instance.new("TextLabel")
local BackGround = Instance.new("Frame")
local Holder = Instance.new("Frame")
local BackGroundBottom = Instance.new("Frame")
local UICorner_2 = Instance.new("UICorner")
local ImageLabel = Instance.new("ImageLabel")
local UICorner_3 = Instance.new("UICorner")
local OutputFrame = Instance.new("Frame")
local console_3 = Instance.new("ScrollingFrame")
local output = Instance.new("TextLabel")

--Properties:

console.Name = "console"
console.Parent = game.CoreGui
console.ResetOnSpawn = false

console_2.Name = "console"
console_2.Parent = console
console_2.Active = true
console_2.BackgroundColor3 = Color3.fromRGB(36, 77, 113)
console_2.Position = UDim2.new(0.472429216, 0, 0.13966158, 0)
console_2.Size = UDim2.new(0, 551, 0, 27)
console_2.Active = true
console_2.Draggable = true

UICorner.CornerRadius = UDim.new(0, 9)
UICorner.Parent = console_2

Frame.Parent = console_2
Frame.BackgroundColor3 = Color3.fromRGB(36, 77, 113)
Frame.BorderColor3 = Color3.fromRGB(27, 42, 53)
Frame.BorderSizePixel = 0
Frame.Position = UDim2.new(0, 0, 0.581612468, 0)
Frame.Size = UDim2.new(0, 551, 0, 13)

ImageButton.Parent = console_2
ImageButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
ImageButton.BackgroundTransparency = 1.000
ImageButton.Position = UDim2.new(0, 0, 0.0357142873, 0)
ImageButton.Size = UDim2.new(0, 26, 0, 28)
ImageButton.Image = "rbxassetid://4430382116"

TextLabel.Parent = console_2
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Position = UDim2.new(0.0470871255, 0, 0.129992455, 0)
TextLabel.Size = UDim2.new(0, 309, 0, 23)
TextLabel.Font = Enum.Font.GothamBold
TextLabel.Text = "Dev Console"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 12.000
TextLabel.TextXAlignment = Enum.TextXAlignment.Left

BackGround.Name = "BackGround"
BackGround.Parent = console_2
BackGround.BackgroundColor3 = Color3.fromRGB(33, 33, 33)
BackGround.BackgroundTransparency = 1.000
BackGround.BorderColor3 = Color3.fromRGB(27, 42, 53)
BackGround.BorderSizePixel = 0
BackGround.ClipsDescendants = true
BackGround.Position = UDim2.new(0, 0, 1, 0)
BackGround.Size = UDim2.new(0, 758, 0, 463)

Holder.Name = "Holder"
Holder.Parent = BackGround
Holder.BackgroundColor3 = Color3.fromRGB(33, 33, 33)
Holder.BorderColor3 = Color3.fromRGB(27, 42, 53)
Holder.BorderSizePixel = 0
Holder.Position = UDim2.new(0, 0, 0.00215982716, 0)
Holder.Size = UDim2.new(0, 551, 0, 420)

BackGroundBottom.Name = "BackGroundBottom"
BackGroundBottom.Parent = Holder
BackGroundBottom.BackgroundColor3 = Color3.fromRGB(33, 33, 33)
BackGroundBottom.BorderColor3 = Color3.fromRGB(27, 42, 53)
BackGroundBottom.Position = UDim2.new(0, 0, 0.980369031, 0)
BackGroundBottom.Size = UDim2.new(0, 551, 0, 37)

UICorner_2.CornerRadius = UDim.new(0, 9)
UICorner_2.Parent = BackGroundBottom

ImageLabel.Parent = Holder
ImageLabel.BackgroundColor3 = Color3.fromRGB(50, 50, 50)
ImageLabel.BorderSizePixel = 0
ImageLabel.Position = UDim2.new(0.0132137239, 0, -0.0372529514, 27)
ImageLabel.Size = UDim2.new(0, 537, 0, 425)

UICorner_3.Parent = ImageLabel

OutputFrame.Name = "OutputFrame"
OutputFrame.Parent = ImageLabel
OutputFrame.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
OutputFrame.BackgroundTransparency = 1.000
OutputFrame.Position = UDim2.new(0, 0, 0.0448568203, 0)
OutputFrame.Size = UDim2.new(0, 538, 0, 395)

console_3.Name = "console"
console_3.Parent = OutputFrame
console_3.BackgroundColor3 = Color3.fromRGB(76, 76, 76)
console_3.BackgroundTransparency = 1.000
console_3.BorderColor3 = Color3.fromRGB(36, 77, 113)
console_3.BorderSizePixel = 2
console_3.Position = UDim2.new(1.02973974, -554, 0.684633434, -278)
console_3.Size = UDim2.new(0, 537, 0, 404)
console_3.CanvasSize = UDim2.new(4, 5, 9999999, 9999999)

output.Name = "output"
output.Parent = console_3
output.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
output.BackgroundTransparency = 1.000
output.Size = UDim2.new(0, 517, 0, 11)
output.Font = Enum.Font.Code
output.Text = ""
output.TextColor3 = Color3.fromRGB(59, 255, 0)
output.TextSize = 14.000
output.TextStrokeColor3 = Color3.fromRGB(255, 255, 255)
output.TextXAlignment = Enum.TextXAlignment.Left
output.TextYAlignment = Enum.TextYAlignment.Top

-- Scripts:

local function JWDDU_fake_script() -- ImageButton.LocalScript 
	local script = Instance.new('LocalScript', ImageButton)

	local D = true
	
	script.Parent.MouseButton1Click:Connect(function()
		if D == true then
			script.Parent.Parent.BackGround.Holder:TweenPosition(UDim2.new(0, 0,-1.06, 0),nil, nil, 0.5)
			D = false
		else
			D = true
			script.Parent.Parent.BackGround.Holder:TweenPosition(UDim2.new(0, 0,0, 0),nil, nil, 0.5)
		end
	end)
end
coroutine.wrap(JWDDU_fake_script)()
local function DBSRQ_fake_script() -- console_3.console 
	local script = Instance.new('LocalScript', console_3)

	--in play mode the console only shows output from localscripts.
	--made by pyccknnxakep
	local player = game.Players.LocalPlayer
	local ls = game:GetService('LogService')
	local colors = {[0] = Color3.new(1, 1, 1), Color3.new(0/255,98/255,255/255), Color3.new(1, 1, 0), Color3.new(1, 0, 0)}
	local num = 0
	ls.MessageOut:Connect(function(msg,type)
		num = num + 1
		local t = tick()
		local l = script.Parent.output:Clone()
		l.Position = UDim2.new(0, 0, 0, num*24)
		l.Text = ('>[%02i:%02i:%02i] - %s'):format((t/3600)%24, (t/60)%60, t%60, msg)
		l.TextColor3 = colors[type.Value]
		l.Parent = script.Parent
	end)
	script.Parent.Parent.button.MouseButton1Click:Connect(function()
		script.Parent.Visible = not script.Parent.Visible
	end)
end
coroutine.wrap(DBSRQ_fake_script)()
local function GQIFGKV_fake_script() -- console_2.LocalScript 
	local script = Instance.new('LocalScript', console_2)

	local UserInputService = game:GetService("UserInputService")
	
	function onKeyPress(inputObject, gameProcessedEvent)
		if not gameProcessedEvent then
	    if inputObject.KeyCode == Enum.KeyCode.RightControl then 
				if script.Parent.Visible == false then
					script.Parent.Visible = true
				else
					script.Parent.Visible = false
				end
			end
		end
	end
	
	UserInputService.InputBegan:connect(onKeyPress)
end
coroutine.wrap(GQIFGKV_fake_script)()
local function PLOAI_fake_script() -- console_2.Dragify 
	local script = Instance.new('LocalScript', console_2)

	script.Parent.Parent.console.Active = true
	script.Parent.Parent.console.Draggable = true
end
coroutine.wrap(PLOAI_fake_script)()
local function SBBUE_fake_script() -- console_2.Dragify 
	local script = Instance.new('LocalScript', console_2)

	local UserInputService = game:GetService("UserInputService")
	
	local gui = script.Parent
	
	local dragging
	local dragInput
	local dragStart
	local startPos
	
	local function update(input)
		local delta = input.Position - dragStart
		gui.Position = UDim2.new(startPos.X.Scale, startPos.X.Offset + delta.X, startPos.Y.Scale, startPos.Y.Offset + delta.Y)
	end
	
	gui.InputBegan:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseButton1 or input.UserInputType == Enum.UserInputType.Touch then
			dragging = true
			dragStart = input.Position
			startPos = gui.Position
	
			input.Changed:Connect(function()
				if input.UserInputState == Enum.UserInputState.End then
					dragging = false
				end
			end)
		end
	end)
	
	gui.InputChanged:Connect(function(input)
		if input.UserInputType == Enum.UserInputType.MouseMovement or input.UserInputType == Enum.UserInputType.Touch then
			dragInput = input
		end
	end)
	
	UserInputService.InputChanged:Connect(function(input)
		if input == dragInput and dragging then
			update(input)
		end
	end)
end
coroutine.wrap(SBBUE_fake_script)()
