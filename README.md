# Milodex-- إنشاء الواجهة (Milodex Hub V2)
local ScreenGui = Instance.new("ScreenGui")
local MainFrame = Instance.new("Frame")
local Title = Instance.new("TextLabel")
local SpeedBtn = Instance.new("TextButton")
local JumpBtn = Instance.new("TextButton")
local CloseBtn = Instance.new("TextButton")

-- إعدادات الشاشة
ScreenGui.Parent = game.CoreGui

-- إعدادات الإطار الرئيسي
MainFrame.Name = "MilodexMain"
MainFrame.Parent = ScreenGui
MainFrame.BackgroundColor3 = Color3.fromRGB(20, 20, 20)
MainFrame.BorderSizePixel = 2
MainFrame.BorderColor3 = Color3.fromRGB(0, 255, 127) -- لون أخضر نيون
MainFrame.Position = UDim2.new(0.5, -100, 0.4, -100)
MainFrame.Size = UDim2.new(0, 220, 0, 250)
MainFrame.Active = true
MainFrame.Draggable = true

-- العنوان
Title.Parent = MainFrame
Title.Text = "MILODEX HUB V2"
Title.Size = UDim2.new(1, 0, 0, 40)
Title.BackgroundColor3 = Color3.fromRGB(30, 30, 30)
Title.TextColor3 = Color3.fromRGB(0, 255, 127)
Title.TextSize = 18
Title.Font = Enum.Font.GothamBold

-- زر السرعة (Speed)
SpeedBtn.Parent = MainFrame
SpeedBtn.Text = "Super Speed (100)"
SpeedBtn.Position = UDim2.new(0.1, 0, 0.25, 0)
SpeedBtn.Size = UDim2.new(0.8, 0, 0, 40)
SpeedBtn.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
SpeedBtn.TextColor3 = Color3.fromRGB(255, 255, 255)

SpeedBtn.MouseButton1Click:Connect(function()
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 100
    print("Milodex: Speed set to 100")
end)

-- زر القفز (Jump)
JumpBtn.Parent = MainFrame
JumpBtn.Text = "Mega Jump (150)"
JumpBtn.Position = UDim2.new(0.1, 0, 0.5, 0)
JumpBtn.Size = UDim2.new(0.8, 0, 0, 40)
JumpBtn.BackgroundColor3 = Color3.fromRGB(40, 40, 40)
JumpBtn.TextColor3 = Color3.fromRGB(255, 255, 255)

JumpBtn.MouseButton1Click:Connect(function()
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = 150
    print("Milodex: Jump set to 150")
end)

-- زر الإغلاق
CloseBtn.Parent = MainFrame
CloseBtn.Text = "Close"
CloseBtn.Position = UDim2.new(0.1, 0, 0.75, 0)
CloseBtn.Size = UDim2.new(0.8, 0, 0, 40)
CloseBtn.BackgroundColor3 = Color3.fromRGB(150, 0, 0)
CloseBtn.TextColor3 = Color3.fromRGB(255, 255, 255)

CloseBtn.MouseButton1Click:Connect(function()
    ScreenGui:Destroy()
end)
