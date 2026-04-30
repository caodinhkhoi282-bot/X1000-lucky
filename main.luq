--// X1000 Lucky GUI by dinhkhoireal28

local player = game.Players.LocalPlayer
local gui = Instance.new("ScreenGui", player:WaitForChild("PlayerGui"))
gui.Name = "LuckyGUI"

-- Main Frame
local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0, 240, 0, 140)
frame.Position = UDim2.new(0.5, -120, 0.3, 0)
frame.BackgroundColor3 = Color3.fromRGB(30, 0, 60)
frame.BorderSizePixel = 0
frame.Active = true
frame.Draggable = true

-- Gradient nền
local gradient = Instance.new("UIGradient", frame)
gradient.Color = ColorSequence.new{
	ColorSequenceKeypoint.new(0, Color3.fromRGB(140, 0, 255)),
	ColorSequenceKeypoint.new(1, Color3.fromRGB(0, 170, 255))
}

-- Title
local title = Instance.new("TextLabel", frame)
title.Size = UDim2.new(1, 0, 0, 30)
title.BackgroundTransparency = 1
title.Text = "dinhkhoireal28"
title.TextColor3 = Color3.fromRGB(255,255,255)
title.Font = Enum.Font.GothamBold
title.TextSize = 18

-- Credit
local credit = Instance.new("TextLabel", frame)
credit.Size = UDim2.new(1, 0, 0, 20)
credit.Position = UDim2.new(0,0,1,-20)
credit.BackgroundTransparency = 1
credit.Text = "dinhkhoireal28"
credit.TextColor3 = Color3.fromRGB(255,255,255)
credit.Font = Enum.Font.Gotham
credit.TextSize = 12

-- Button
local btn = Instance.new("TextButton", frame)
btn.Size = UDim2.new(0.8, 0, 0, 40)
btn.Position = UDim2.new(0.1, 0, 0.5, -20)
btn.Text = "X1000 Lucky 🍀"
btn.Font = Enum.Font.GothamBold
btn.TextSize = 16
btn.TextColor3 = Color3.fromRGB(255,255,255)
btn.BackgroundColor3 = Color3.fromRGB(100, 0, 200)

local corner = Instance.new("UICorner", btn)
corner.CornerRadius = UDim.new(0, 12)

-- Hover effect
btn.MouseEnter:Connect(function()
	btn.BackgroundColor3 = Color3.fromRGB(150, 50, 255)
end)

btn.MouseLeave:Connect(function()
	btn.BackgroundColor3 = Color3.fromRGB(100, 0, 200)
end)

-- Notification
local function notify(text)
	game.StarterGui:SetCore("SendNotification", {
		Title = "dinhkhoireal28",
		Text = text,
		Duration = 3
	})
end

-- 🌿 Hiệu ứng lá rơi
local function spawnLeaf()
	local leaf = Instance.new("TextLabel", gui)
	leaf.Text = "🍀"
	leaf.TextScaled = true
	leaf.Size = UDim2.new(0, 30, 0, 30)
	leaf.BackgroundTransparency = 1
	leaf.Position = UDim2.new(math.random(), 0, -0.1, 0)

	-- rơi xuống
	local tweenService = game:GetService("TweenService")
	local tween = tweenService:Create(leaf, TweenInfo.new(3, Enum.EasingStyle.Linear), {
		Position = UDim2.new(leaf.Position.X.Scale, 0, 1.1, 0)
	})
	tween:Play()

	tween.Completed:Connect(function()
		leaf:Destroy()
	end)
end

-- Khi bấm
btn.MouseButton1Click:Connect(function()
	notify("Đã bật X1000 Lucky 🍀")

	-- spam lá rơi
	for i = 1, 20 do
		spawnLeaf()
		task.wait(0.1)
	end
end)
