local LocalUi = Instance.new("ScreenGui")
local FlyButton = Instance.new("TextButton")
local SpeedButton = Instance.new("TextButton")
local JumpButton = Instance.new("TextButton")

LocalUi.Name = "LocalUi"
LocalUi.Parent = game.CoreGui

FlyButton.Name = "FlyButton"
FlyButton.Parent = LocalUi
FlyButton.BackgroundColor3 = Color3.new(1, 1, 1)
FlyButton.Position = UDim2.new(0, 50, 0, 50)
FlyButton.Size = UDim2.new(0, 200, 0, 50)
FlyButton.Text = "Fly"

SpeedButton.Name = "SpeedButton"
SpeedButton.Parent = LocalUi
SpeedButton.BackgroundColor3 = Color3.new(1, 1, 1)
SpeedButton.Position = UDim2.new(0, 50, 0, 110)
SpeedButton.Size = UDim2.new(0, 200, 0, 50)
SpeedButton.Text = "Extra Speed"

JumpButton.Name = "JumpButton"
JumpButton.Parent = LocalUi
JumpButton.BackgroundColor3 = Color3.new(1, 1, 1)
JumpButton.Position = UDim2.new(0, 50, 0, 170)
JumpButton.Size = UDim2.new(0, 200, 0, 50)
JumpButton.Text = "Extra Jump"

FlyButton.MouseButton1Click:Connect(function()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    humanoid.WalkSpeed = humanoid.WalkSpeed * 1.1
end)

SpeedButton.MouseButton1Click:Connect(function()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    humanoid.WalkSpeed = humanoid.WalkSpeed * 1.2
end)

JumpButton.MouseButton1Click:Connect(function()
    local player = game.Players.LocalPlayer
    local character = player.Character or player.CharacterAdded:Wait()
    local humanoid = character:FindFirstChildOfClass("Humanoid")
    humanoid.JumpPower = humanoid.JumpPower * 1.3
end)
