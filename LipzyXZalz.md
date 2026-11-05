-- ==========================================================
-- SCRIPT DELTA EXECUTOR - STEAL AN EGG (SCROLLABLE & FIXED)
-- ==========================================================

local Players = game:GetService("Players")
local TweenService = game:GetService("TweenService")
local SoundService = game:GetService("SoundService")
local RunService = game:GetService("RunService")
local Lighting = game:GetService("Lighting")
local player = Players.LocalPlayer

-- Remove old UI if exists
if player.PlayerGui:FindFirstChild("StealAnEggCustomUI") then
    player.PlayerGui.StealAnEggCustomUI:Destroy()
end

local screenGui = Instance.new("ScreenGui")
screenGui.Name = "StealAnEggCustomUI"
screenGui.ResetOnSpawn = false
screenGui.Parent = player.PlayerGui

-- ==========================================================
-- 1. MAIN MENU CREATION (FIXED HEIGHT: 400)
-- ==========================================================
local mainFrame = Instance.new("Frame")
mainFrame.Size = UDim2.new(0, 400, 0, 400)
mainFrame.Position = UDim2.new(0.5, -200, 0.5, -200)
mainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 45)
mainFrame.BorderSizePixel = 0
mainFrame.Active = true
mainFrame.Draggable = true
mainFrame.ClipsDescendants = true
mainFrame.Parent = screenGui

local uiCorner = Instance.new("UICorner")
uiCorner.CornerRadius = UDim.new(0, 12)
uiCorner.Parent = mainFrame

-- Menu Title (Fixed at the top)
local titleLabel = Instance.new("TextLabel")
titleLabel.Size = UDim2.new(1, 0, 0, 40)
titleLabel.Position = UDim2.new(0, 0, 0, 0)
titleLabel.BackgroundTransparency = 1
titleLabel.Text = "Steal An Egg - Panel"
titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
titleLabel.TextSize = 16
titleLabel.Font = Enum.Font.GothamBold
titleLabel.Parent = mainFrame

-- Title Separator Line
local titleLine = Instance.new("Frame")
titleLine.Size = UDim2.new(0.9, 0, 0, 1)
titleLine.Position = UDim2.new(0.05, 0, 0, 40)
titleLine.BackgroundColor3 = Color3.fromRGB(55, 55, 75)
titleLine.BorderSizePixel = 0
titleLine.Parent = mainFrame

-- ==========================================================
-- SCROLLING FRAME FOR UI CONTENT
-- ==========================================================
local scrollFrame = Instance.new("ScrollingFrame")
scrollFrame.Size = UDim2.new(1, 0, 1, -45)
scrollFrame.Position = UDim2.new(0, 0, 0, 45)
scrollFrame.BackgroundTransparency = 1
scrollFrame.BorderSizePixel = 0
scrollFrame.ScrollBarThickness = 5
scrollFrame.ScrollBarImageColor3 = Color3.fromRGB(0, 162, 255)
scrollFrame.CanvasSize = UDim2.new(0, 0, 0, 0)
scrollFrame.AutomaticCanvasSize = Enum.AutomaticSize.Y
scrollFrame.Parent = mainFrame

local scrollPadding = Instance.new("UIPadding")
scrollPadding.PaddingTop = UDim.new(0, 5)
scrollPadding.PaddingBottom = UDim.new(0, 15)
scrollPadding.PaddingLeft = UDim.new(0, 15)
scrollPadding.PaddingRight = UDim.new(0, 15)
scrollPadding.Parent = scrollFrame

local scrollLayout = Instance.new("UIListLayout")
scrollLayout.SortOrder = Enum.SortOrder.LayoutOrder
scrollLayout.Padding = UDim.new(0, 8)
scrollLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
scrollLayout.Parent = scrollFrame

-- Text Box [ WRITE MESSAGE ]
local textBox = Instance.new("TextBox")
textBox.Size = UDim2.new(1, 0, 0, 35)
textBox.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
textBox.TextColor3 = Color3.fromRGB(255, 255, 255)
textBox.PlaceholderText = "Type message here..."
textBox.Text = ""
textBox.TextSize = 13
textBox.Font = Enum.Font.Gotham
textBox.ClearTextOnFocus = false
textBox.LayoutOrder = 1
textBox.Parent = scrollFrame

local boxCorner = Instance.new("UICorner")
boxCorner.CornerRadius = UDim.new(0, 8)
boxCorner.Parent = textBox

-- Button [ SEND MESSAGE ]
local sendButton = Instance.new("TextButton")
sendButton.Size = UDim2.new(1, 0, 0, 32)
sendButton.BackgroundColor3 = Color3.fromRGB(0, 162, 255)
sendButton.TextColor3 = Color3.fromRGB(255, 255, 255)
sendButton.Text = "SEND MESSAGE"
sendButton.TextSize = 13
sendButton.Font = Enum.Font.GothamBold
sendButton.LayoutOrder = 2
sendButton.Parent = scrollFrame

local btnCorner = Instance.new("UICorner")
btnCorner.CornerRadius = UDim.new(0, 8)
btnCorner.Parent = sendButton

-- Text Box [ WRITE SERVER TEXT ]
local textBoxServer = Instance.new("TextBox")
textBoxServer.Size = UDim2.new(1, 0, 0, 35)
textBoxServer.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
textBoxServer.TextColor3 = Color3.fromRGB(255, 255, 255)
textBoxServer.PlaceholderText = "Type server announcement..."
textBoxServer.Text = ""
textBoxServer.TextSize = 13
textBoxServer.Font = Enum.Font.Gotham
textBoxServer.ClearTextOnFocus = false
textBoxServer.LayoutOrder = 3
textBoxServer.Parent = scrollFrame

local boxServerCorner = Instance.new("UICorner")
boxServerCorner.CornerRadius = UDim.new(0, 8)
boxServerCorner.Parent = textBoxServer

-- Button [ SEND SERVER ]
local sendServerButton = Instance.new("TextButton")
sendServerButton.Size = UDim2.new(1, 0, 0, 32)
sendServerButton.BackgroundColor3 = Color3.fromRGB(255, 80, 0)
sendServerButton.TextColor3 = Color3.fromRGB(255, 255, 255)
sendServerButton.Text = "SEND SERVER"
sendServerButton.TextSize = 13
sendServerButton.Font = Enum.Font.GothamBold
sendServerButton.LayoutOrder = 4
sendServerButton.Parent = scrollFrame

local btnServerCorner = Instance.new("UICorner")
btnServerCorner.CornerRadius = UDim.new(0, 8)
btnServerCorner.Parent = sendServerButton

-- ==========================================================
-- TEXT BOX & START BUTTON (OVERHEAD TEXT)
-- ==========================================================
local textBoxHead = Instance.new("TextBox")
textBoxHead.Size = UDim2.new(1, 0, 0, 35)
textBoxHead.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
textBoxHead.TextColor3 = Color3.fromRGB(255, 255, 255)
textBoxHead.PlaceholderText = "Type text above head..."
textBoxHead.Text = ""
textBoxHead.TextSize = 13
textBoxHead.Font = Enum.Font.Gotham
textBoxHead.ClearTextOnFocus = false
textBoxHead.LayoutOrder = 5
textBoxHead.Parent = scrollFrame

local boxHeadCorner = Instance.new("UICorner")
boxHeadCorner.CornerRadius = UDim.new(0, 8)
boxHeadCorner.Parent = textBoxHead

local startHeadButton = Instance.new("TextButton")
startHeadButton.Size = UDim2.new(1, 0, 0, 32)
startHeadButton.BackgroundColor3 = Color3.fromRGB(0, 200, 100)
startHeadButton.TextColor3 = Color3.fromRGB(255, 255, 255)
startHeadButton.Text = "START OVERHEAD"
startHeadButton.TextSize = 13
startHeadButton.Font = Enum.Font.GothamBold
startHeadButton.LayoutOrder = 6
startHeadButton.Parent = scrollFrame

local btnHeadCorner = Instance.new("UICorner")
btnHeadCorner.CornerRadius = UDim.new(0, 8)
btnHeadCorner.Parent = startHeadButton

-- Grid Container for Feature Buttons (2 Columns - Admin, Banner & Spawns)
local gridContainer = Instance.new("Frame")
gridContainer.Size = UDim2.new(1, 0, 0, 0)
gridContainer.BackgroundTransparency = 1
gridContainer.AutomaticSize = Enum.AutomaticSize.Y
gridContainer.LayoutOrder = 7
gridContainer.Parent = scrollFrame

local gridLayout = Instance.new("UIGridLayout")
gridLayout.CellSize = UDim2.new(0.48, 0, 0, 35)
gridLayout.CellPadding = UDim2.new(0.04, 0, 0, 8)
gridLayout.SortOrder = Enum.SortOrder.LayoutOrder
gridLayout.Parent = gridContainer

local function createFeatureButton(name, color, order)
    local btn = Instance.new("TextButton")
    btn.BackgroundColor3 = color
    btn.TextColor3 = Color3.fromRGB(255, 255, 255)
    btn.Text = name
    btn.TextSize = 11
    btn.Font = Enum.Font.GothamBold
    btn.LayoutOrder = order
    btn.Parent = gridContainer
    
    local c = Instance.new("UICorner")
    c.CornerRadius = UDim.new(0, 8)
    c.Parent = btn
    return btn
end

local btnAdmin = createFeatureButton("[ ADMIN NOTIF ]", Color3.fromRGB(200, 50, 50), 1)
local btnLuckEggs = createFeatureButton("[ LUCK EGGS ]", Color3.fromRGB(255, 170, 0), 2)
local btnCustomBanner = createFeatureButton("[ LUCK MEGA FISH ]", Color3.fromRGB(138, 43, 226), 3)
local btnOwnerGeme = createFeatureButton("[ GAME OWNER ]", Color3.fromRGB(46, 139, 87), 4)
local btnSpawnUnicorn = createFeatureButton("[ SPAWN UNICORN ]", Color3.fromRGB(199, 21, 133), 5)
local btnSpawnKitsune = createFeatureButton("[ SPAWN KITSUNE ]", Color3.fromRGB(255, 105, 180), 6)
local btnSpawnNigflame = createFeatureButton("[ SPAWN NIGFLAME ]", Color3.fromRGB(180, 0, 0), 7)
local btnSpawnArchangel = createFeatureButton("[ SPAWN ARCHANGEL ]", Color3.fromRGB(255, 127, 127), 8)
local btnSpawnSkyywhale = createFeatureButton("[ SPAWN SKYWHALE ]", Color3.fromRGB(147, 112, 219), 9)
local btnSpawnWorldBurner = createFeatureButton("[ SPAWN WORLDBURNER ]", Color3.fromRGB(220, 20, 100), 10)

-- ==========================================================
-- FULL-WIDTH SPECIAL FEATURE BUTTONS (LayoutOrder 8, 9, 10)
-- ==========================================================
local function createFullWidthButton(name, color, order)
    local btn = Instance.new("TextButton")
    btn.Size = UDim2.new(1, 0, 0, 32)
    btn.BackgroundColor3 = color
    btn.TextColor3 = Color3.fromRGB(255, 255, 255)
    btn.Text = name
    btn.TextSize = 12
    btn.Font = Enum.Font.GothamBold
    btn.LayoutOrder = order
    btn.Parent = scrollFrame
    
    local c = Instance.new("UICorner")
    c.CornerRadius = UDim.new(0, 8)
    c.Parent = btn
    return btn
end

local btnChaosSky = createFullWidthButton("[ CHAOS OF THE SKY ]", Color3.fromRGB(0, 220, 140), 8)
local btnPlayerStatus = createFullWidthButton("[ PLAYER STATUS ]", Color3.fromRGB(0, 150, 255), 9)
local btnEggPrediction = createFullWidthButton("[ EGG PREDICTION ]", Color3.fromRGB(255, 100, 0), 10)

-- ==========================================================
-- 2. MAIN CONTAINER FOR CHAT NOTIFICATION LAYOUT
-- ==========================================================
local containerFrame = Instance.new("Frame")
containerFrame.Size = UDim2.new(0, 700, 0, 450)
containerFrame.Position = UDim2.new(0.5, 0, 0.02, 0)
containerFrame.AnchorPoint = Vector2.new(0.5, 0)
containerFrame.BackgroundTransparency = 1
containerFrame.Parent = screenGui

local uiListLayout = Instance.new("UIListLayout")
uiListLayout.FillDirection = Enum.FillDirection.Vertical
uiListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
uiListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
uiListLayout.SortOrder = Enum.SortOrder.LayoutOrder
uiListLayout.Padding = UDim.new(0, 6)
uiListLayout.Parent = containerFrame

local globalOrder = 0

local function playCustomSound()
    pcall(function()
        local sound = Instance.new("Sound")
        sound.SoundId = "rbxassetid://130017098772572"
        sound.Volume = 1
        sound.Parent = SoundService
        sound:Play()
        game:GetService("Debris"):AddItem(sound, 5)
    end)
end

local function spawnNotificationRow(senderName, messageText, isPlayer, customAvatar, isGlowingAdmin)
    globalOrder = globalOrder + 1

    local avatarContent = customAvatar

    if isPlayer then
        local userId = player.UserId
        local thumbType = Enum.ThumbnailType.HeadShot
        local thumbSize = Enum.ThumbnailSize.Size420x420
        avatarContent = Players:GetUserThumbnailAsync(userId, thumbType, thumbSize)
    end

    local notifRow = Instance.new("Frame")
    notifRow.Size = UDim2.new(0, 0, 0, 40)
    notifRow.BackgroundTransparency = 1
    notifRow.AnchorPoint = Vector2.new(0.5, 0.5)
    notifRow.AutomaticSize = Enum.AutomaticSize.X
    notifRow.ClipsDescendants = true
    notifRow.LayoutOrder = globalOrder
    notifRow.Parent = containerFrame

    local rowLayout = Instance.new("UIListLayout")
    rowLayout.FillDirection = Enum.FillDirection.Horizontal
    rowLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    rowLayout.VerticalAlignment = Enum.VerticalAlignment.Center
    rowLayout.SortOrder = Enum.SortOrder.LayoutOrder
    rowLayout.Padding = UDim.new(0, 6)
    rowLayout.Parent = notifRow

    if isPlayer and avatarContent and avatarContent ~= "" then
        local avatarImg = Instance.new("ImageLabel")
        avatarImg.Name = "AvatarImg"
        avatarImg.Size = UDim2.new(0, 26, 0, 26)
        avatarImg.BackgroundTransparency = 1
        avatarImg.Image = avatarContent
        avatarImg.LayoutOrder = 0
        avatarImg.Parent = notifRow

        local avatarCorner = Instance.new("UICorner")
        avatarCorner.CornerRadius = UDim.new(0, 6)
        avatarCorner.Parent = avatarImg
    else
        local spacer = Instance.new("Frame")
        spacer.Name = "Spacer"
        spacer.Size = UDim2.new(0, 26, 0, 26)
        spacer.BackgroundTransparency = 1
        spacer.LayoutOrder = 0
        spacer.Parent = notifRow
    end

    local nameLabel = Instance.new("TextLabel")
    nameLabel.Name = "NameLabel"
    nameLabel.Size = UDim2.new(0, 0, 1, 0)
    nameLabel.BackgroundTransparency = 1
    nameLabel.AutomaticSize = Enum.AutomaticSize.X
    nameLabel.Text = senderName
    nameLabel.TextColor3 = isGlowingAdmin and Color3.fromRGB(255, 40, 40) or Color3.fromRGB(0, 162, 255)
    nameLabel.TextSize = 20
    nameLabel.Font = Enum.Font.GothamBlack
    nameLabel.LayoutOrder = 1
    nameLabel.Parent = notifRow

    local strokeName = Instance.new("UIStroke")
    strokeName.Thickness = 2.5
    strokeName.Color = Color3.fromRGB(0, 0, 0)
    strokeName.Parent = nameLabel

    if isGlowingAdmin then
        local gradient = Instance.new("UIGradient")
        gradient.Color = ColorSequence.new({
            ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 80, 80)),
            ColorSequenceKeypoint.new(0.3, Color3.fromRGB(255, 255, 255)),
            ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 220, 220)),
            ColorSequenceKeypoint.new(0.7, Color3.fromRGB(255, 255, 255)),
            ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 80, 80))
        })
        gradient.Rotation = 25
        gradient.Parent = nameLabel

        task.spawn(function()
            local conn
            conn = RunService.RenderStepped:Connect(function()
                if not nameLabel or not nameLabel.Parent then
                    if conn then conn:Disconnect() end
                    return
                end
                gradient.Offset = Vector2.new((tick() * 2.2) % 3 - 1.5, 0)
            end)
        end)
    end

    local verifyImage = Instance.new("ImageLabel")
    verifyImage.Name = "VerifyImage"
    verifyImage.Size = UDim2.new(0, 18, 0, 18)
    verifyImage.BackgroundTransparency = 1
    verifyImage.Image = "rbxassetid://80290718584748"
    verifyImage.LayoutOrder = 2
    verifyImage.Parent = notifRow

    local msgLabel = Instance.new("TextLabel")
    msgLabel.Name = "MsgLabel"
    msgLabel.Size = UDim2.new(0, 0, 1, 0)
    msgLabel.BackgroundTransparency = 1
    msgLabel.AutomaticSize = Enum.AutomaticSize.X
    msgLabel.Text = ": " .. messageText
    msgLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
    msgLabel.TextSize = 20
    msgLabel.Font = Enum.Font.FredokaOne
    msgLabel.LayoutOrder = 3
    msgLabel.Parent = notifRow

    local strokeMsg = Instance.new("UIStroke")
    strokeMsg.Thickness = 2
    strokeMsg.Color = Color3.fromRGB(0, 0, 0)
    strokeMsg.Parent = msgLabel

    playCustomSound()

    notifRow.Size = UDim2.new(0, 0, 0, 0)
    local appearTween = TweenService:Create(
        notifRow, 
        TweenInfo.new(0.25, Enum.EasingStyle.Back, Enum.EasingDirection.Out, 0, false, 0), 
        {Size = UDim2.new(0, 500, 0, 42)}
    )
    appearTween:Play()
    
    appearTween.Completed:Connect(function()
        local settleTween = TweenService:Create(
            notifRow,
            TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
            {Size = UDim2.new(0, 460, 0, 36)}
        )
        settleTween:Play()
    end)

    task.delay(4, function()
        if notifRow and notifRow.Parent then
            local disappearTween = TweenService:Create(
                notifRow, 
                TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.In), 
                {Size = UDim2.new(0, 0, 0, 0)}
            )
            disappearTween:Play()
            disappearTween.Completed:Connect(function()
                notifRow:Destroy()
            end)
        end
    end)
end

-- ==========================================================
-- HELPER FUNCTION FOR USER THUMBNAIL
-- ==========================================================
local function getUserThumbnail()
    local success, result = pcall(function()
        return Players:GetUserThumbnailAsync(player.UserId, Enum.ThumbnailType.HeadShot, Enum.ThumbnailSize.Size420x420)
    end)
    if success then
        return result
    end
    return ""
end

-- ==========================================================
-- CUSTOM SPAWN NOTIFICATION TEMPLATE
-- ==========================================================
local function spawnCustomTemplate(petName, zoneName, petColor, zoneColor)
    playCustomSound()
    globalOrder = globalOrder + 1

    local notifRow = Instance.new("Frame")
    notifRow.Name = "CustomSpawnNotifRow"
    notifRow.Size = UDim2.new(0, 0, 0, 0)
    notifRow.BackgroundTransparency = 1
    notifRow.AnchorPoint = Vector2.new(0.5, 0.5)
    notifRow.AutomaticSize = Enum.AutomaticSize.X
    notifRow.ClipsDescendants = true
    notifRow.LayoutOrder = globalOrder
    notifRow.Parent = containerFrame  -- <-- PERBAIKAN DI SINI (Hanya sekali, tidak dobel)

    local colLayout = Instance.new("UIListLayout")
    colLayout.FillDirection = Enum.FillDirection.Vertical
    colLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    colLayout.VerticalAlignment = Enum.VerticalAlignment.Center
    colLayout.SortOrder = Enum.SortOrder.LayoutOrder
    colLayout.Padding = UDim.new(0, -4)
    colLayout.Parent = notifRow

    -- FIRST LINE
    local line1 = Instance.new("Frame")
    line1.Size = UDim2.new(0, 0, 0, 28)
    line1.BackgroundTransparency = 1
    line1.AutomaticSize = Enum.AutomaticSize.X
    line1.LayoutOrder = 1
    line1.Parent = notifRow

    local l1Layout = Instance.new("UIListLayout")
    l1Layout.FillDirection = Enum.FillDirection.Horizontal
    l1Layout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    l1Layout.VerticalAlignment = Enum.VerticalAlignment.Center
    l1Layout.SortOrder = Enum.SortOrder.LayoutOrder
    l1Layout.Padding = UDim.new(0, 6)
    l1Layout.Parent = line1

    local thumbUrl = getUserThumbnail()
    if thumbUrl ~= "" then
        local avatarImg = Instance.new("ImageLabel")
        avatarImg.Name = "AvatarImg"
        avatarImg.Size = UDim2.new(0, 26, 0, 26)
        avatarImg.BackgroundTransparency = 1
        avatarImg.Image = thumbUrl
        avatarImg.LayoutOrder = 0
        avatarImg.Parent = line1

        local avatarCorner = Instance.new("UICorner")
        avatarCorner.CornerRadius = UDim.new(0, 6)
        avatarCorner.Parent = avatarImg
    end

    local nameLbl = Instance.new("TextLabel")
    nameLbl.Size = UDim2.new(0, 0, 1, 0)
    nameLbl.BackgroundTransparency = 1
    nameLbl.AutomaticSize = Enum.AutomaticSize.X
    nameLbl.Text = "Lifzy"
    nameLbl.TextColor3 = Color3.fromRGB(0, 162, 255)
    nameLbl.TextSize = 17
    nameLbl.Font = Enum.Font.GothamBlack
    nameLbl.LayoutOrder = 1
    nameLbl.Parent = line1

    local s1 = Instance.new("UIStroke")
    s1.Thickness = 2
    s1.Color = Color3.fromRGB(0, 0, 0)
    s1.Parent = nameLbl

    local verImg = Instance.new("ImageLabel")
    verImg.Size = UDim2.new(0, 15, 0, 15)
    verImg.BackgroundTransparency = 1
    verImg.Image = "rbxassetid://80290718584748"
    verImg.LayoutOrder = 2
    verImg.Parent = line1

    local textLbl1 = Instance.new("TextLabel")
    textLbl1.Size = UDim2.new(0, 0, 1, 0)
    textLbl1.BackgroundTransparency = 1
    textLbl1.AutomaticSize = Enum.AutomaticSize.X
    textLbl1.Text = " spawned a "
    textLbl1.TextColor3 = Color3.fromRGB(255, 255, 255)
    textLbl1.TextSize = 16
    textLbl1.Font = Enum.Font.FredokaOne
    textLbl1.LayoutOrder = 3
    textLbl1.Parent = line1

    local s2 = Instance.new("UIStroke")
    s2.Thickness = 1.8
    s2.Color = Color3.fromRGB(0, 0, 0)
    s2.Parent = textLbl1

    local rareEggLbl = Instance.new("TextLabel")
    rareEggLbl.Size = UDim2.new(0, 0, 1, 0)
    rareEggLbl.BackgroundTransparency = 1
    rareEggLbl.AutomaticSize = Enum.AutomaticSize.X
    rareEggLbl.Text = "RARE EGG"
    rareEggLbl.TextColor3 = Color3.fromRGB(255, 170, 0)
    rareEggLbl.TextSize = 17
    rareEggLbl.Font = Enum.Font.GothamBlack
    rareEggLbl.LayoutOrder = 4
    rareEggLbl.Parent = line1

    local s3 = Instance.new("UIStroke")
    s3.Thickness = 2
    s3.Color = Color3.fromRGB(0, 0, 0)
    s3.Parent = rareEggLbl

    local exclam1 = Instance.new("TextLabel")
    exclam1.Size = UDim2.new(0, 0, 1, 0)
    exclam1.BackgroundTransparency = 1
    exclam1.AutomaticSize = Enum.AutomaticSize.X
    exclam1.Text = "!"
    exclam1.TextColor3 = Color3.fromRGB(255, 255, 255)
    exclam1.TextSize = 16
    exclam1.Font = Enum.Font.FredokaOne
    exclam1.LayoutOrder = 5
    exclam1.Parent = line1

    local s4 = Instance.new("UIStroke")
    s4.Thickness = 1.8
    s4.Color = Color3.fromRGB(0, 0, 0)
    s4.Parent = exclam1

    -- SECOND LINE
    local line2 = Instance.new("Frame")
    line2.Size = UDim2.new(0, 0, 0, 28)
    line2.Position = UDim2.new(0, 0, 0, -3)
    line2.BackgroundTransparency = 1
    line2.AutomaticSize = Enum.AutomaticSize.X
    line2.LayoutOrder = 2
    line2.Parent = notifRow

    local l2Layout = Instance.new("UIListLayout")
    l2Layout.FillDirection = Enum.FillDirection.Horizontal
    l2Layout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    l2Layout.VerticalAlignment = Enum.VerticalAlignment.Center
    l2Layout.SortOrder = Enum.SortOrder.LayoutOrder
    l2Layout.Padding = UDim.new(0, 5)
    l2Layout.Parent = line2

    local spacer2 = Instance.new("Frame")
    spacer2.Size = UDim2.new(0, 26, 0, 26)
    spacer2.BackgroundTransparency = 1
    spacer2.LayoutOrder = 0
    spacer2.Parent = line2

    local aLbl = Instance.new("TextLabel")
    aLbl.Size = UDim2.new(0, 0, 1, 0)
    aLbl.BackgroundTransparency = 1
    aLbl.AutomaticSize = Enum.AutomaticSize.X
    aLbl.Text = "A"
    aLbl.TextColor3 = Color3.fromRGB(255, 255, 255)
    aLbl.TextSize = 17
    aLbl.Font = Enum.Font.GothamBlack
    aLbl.LayoutOrder = 1
    aLbl.Parent = line2

    local sa = Instance.new("UIStroke")
    sa.Thickness = 2
    sa.Color = Color3.fromRGB(0, 0, 0)
    sa.Parent = aLbl

    local petLbl = Instance.new("TextLabel")
    petLbl.Size = UDim2.new(0, 0, 1, 0)
    petLbl.BackgroundTransparency = 1
    petLbl.AutomaticSize = Enum.AutomaticSize.X
    petLbl.Text = " Divine " .. petName
    petLbl.TextColor3 = petColor
    petLbl.TextSize = 17
    petLbl.Font = Enum.Font.GothamBlack
    petLbl.LayoutOrder = 2
    petLbl.Parent = line2

    local s5 = Instance.new("UIStroke")
    s5.Thickness = 2
    s5.Color = Color3.fromRGB(0, 0, 0)
    s5.Parent = petLbl

    local textLbl2 = Instance.new("TextLabel")
    textLbl2.Size = UDim2.new(0, 0, 1, 0)
    textLbl2.BackgroundTransparency = 1
    textLbl2.AutomaticSize = Enum.AutomaticSize.X
    textLbl2.Text = " spawned in "
    textLbl2.TextColor3 = Color3.fromRGB(255, 255, 255)
    textLbl2.TextSize = 16
    textLbl2.Font = Enum.Font.FredokaOne
    textLbl2.LayoutOrder = 3
    textLbl2.Parent = line2

    local s6 = Instance.new("UIStroke")
    s6.Thickness = 1.8
    s6.Color = Color3.fromRGB(0, 0, 0)
    s6.Parent = textLbl2

    local zoneLbl = Instance.new("TextLabel")
    zoneLbl.Size = UDim2.new(0, 0, 1, 0)
    zoneLbl.BackgroundTransparency = 1
    zoneLbl.AutomaticSize = Enum.AutomaticSize.X
    zoneLbl.Text = zoneName
    zoneLbl.TextColor3 = zoneColor
    zoneLbl.TextSize = 17
    zoneLbl.Font = Enum.Font.GothamBlack
    zoneLbl.LayoutOrder = 4
    zoneLbl.Parent = line2

    local s7 = Instance.new("UIStroke")
    s7.Thickness = 2
    s7.Color = Color3.fromRGB(0, 0, 0)
    s7.Parent = zoneLbl

    local exclam = Instance.new("TextLabel")
    exclam.Size = UDim2.new(0, 0, 1, 0)
    exclam.BackgroundTransparency = 1
    exclam.AutomaticSize = Enum.AutomaticSize.X
    exclam.Text = "!"
    exclam.TextColor3 = Color3.fromRGB(255, 255, 255)
    exclam.TextSize = 16
    exclam.Font = Enum.Font.FredokaOne
    exclam.LayoutOrder = 5
    exclam.Parent = line2

    local s8 = Instance.new("UIStroke")
    s8.Thickness = 1.8
    s8.Color = Color3.fromRGB(0, 0, 0)
    s8.Parent = exclam

    local appearTween = TweenService:Create(
        notifRow, 
        TweenInfo.new(0.3, Enum.EasingStyle.Back, Enum.EasingDirection.Out, 0, false, 0), 
        {Size = UDim2.new(0, 480, 0, 56)}
    )
    appearTween:Play()

    task.delay(4, function()
        if notifRow and notifRow.Parent then
            local disappearTween = TweenService:Create(
                notifRow, 
                TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.In), 
                {Size = UDim2.new(0, 0, 0, 0)}
            )
            disappearTween:Play()
            disappearTween.Completed:Connect(function()
                notifRow:Destroy()
            end)
        end
    end)
end

-- ==========================================================
-- SPAWN FEATURES
-- ==========================================================
local function spawnUnicornNotification()
    spawnCustomTemplate("Unicorn", "Cosmic 👹", Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 0, 127))
end

local function spawnKitsuneNotification()
    spawnCustomTemplate("Kitsune", "Cherry blossom🌸", Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 255, 0))
end

local function spawnNigflameNotification()
    spawnCustomTemplate("Nigflame", "Titan Temple🦖", Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 0, 0))
end

local function spawnArchangelNotification()
    spawnCustomTemplate("ArchAnggel", "Angels & Demons☯️", Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 140, 160))
end

local function spawnSkyywhaleNotification()
    spawnCustomTemplate("Royal Skywhale", "Enchanted Forest🦋", Color3.fromRGB(255, 255, 0), Color3.fromRGB(170, 0, 255))
end

local function spawnWorldBurnerNotification()
    spawnCustomTemplate("World Burner", "Angels & Demons☯️", Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 140, 160))
end

-- ==========================================================
-- OVERHEAD TEXT FEATURE
-- ==========================================================
local headBillboard = nil

local function triggerHeadText(textInput)
    if headBillboard and headBillboard.Parent then
        headBillboard:Destroy()
        headBillboard = nil
    end

    local character = player.Character or player.CharacterAdded:Wait()
    local head = character:FindFirstChild("Head") or character:WaitForChild("Head", 3)
    if not head then return end

    headBillboard = Instance.new("BillboardGui")
    headBillboard.Name = "CustomHeadTextBillboard"
    headBillboard.Size = UDim2.new(0, 300, 0, 50)
    headBillboard.StudsOffset = Vector3.new(0, 2.5, 0)
    headBillboard.AlwaysOnTop = true
    headBillboard.Parent = head

    local innerRow = Instance.new("Frame")
    innerRow.Size = UDim2.new(1, 0, 1, 0)
    innerRow.BackgroundTransparency = 1
    innerRow.AnchorPoint = Vector2.new(0.5, 0.5)
    innerRow.Position = UDim2.new(0.5, 0, 0.5, 0)
    innerRow.AutomaticSize = Enum.AutomaticSize.X
    innerRow.Parent = headBillboard

    local rowLayout = Instance.new("UIListLayout")
    rowLayout.FillDirection = Enum.FillDirection.Horizontal
    rowLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    rowLayout.VerticalAlignment = Enum.VerticalAlignment.Center
    rowLayout.SortOrder = Enum.SortOrder.LayoutOrder
    rowLayout.Padding = UDim.new(0, 6)
    rowLayout.Parent = innerRow

    local customTextLbl = Instance.new("TextLabel")
    customTextLbl.Size = UDim2.new(0, 0, 1, 0)
    customTextLbl.BackgroundTransparency = 1
    customTextLbl.AutomaticSize = Enum.AutomaticSize.X
    customTextLbl.Text = textInput
    customTextLbl.TextColor3 = Color3.fromRGB(255, 255, 255)
    customTextLbl.TextSize = 19
    customTextLbl.Font = Enum.Font.SourceSans
    customTextLbl.LayoutOrder = 1
    customTextLbl.Parent = innerRow

    local strokeText = Instance.new("UIStroke")
    strokeText.Thickness = 1.5
    strokeText.Color = Color3.fromRGB(0, 0, 0)
    strokeText.Parent = customTextLbl

    local badgeImg = Instance.new("ImageLabel")
    badgeImg.Size = UDim2.new(0, 18, 0, 18)
    badgeImg.BackgroundTransparency = 1
    badgeImg.Image = "rbxassetid://80290718584748"
    badgeImg.LayoutOrder = 2
    badgeImg.Parent = innerRow
end

-- ==========================================================
-- LIVE PLAYER STATUS PANEL
-- ==========================================================
local playerStatusGui = nil

local function togglePlayerStatusPanel()
    if playerStatusGui and playerStatusGui.Parent then
        playerStatusGui:Destroy()
        playerStatusGui = nil
        return
    end

    playerStatusGui = Instance.new("Frame")
    playerStatusGui.Name = "PlayerStatusWindow"
    playerStatusGui.Size = UDim2.new(0, 420, 0, 480)
    playerStatusGui.Position = UDim2.new(0.5, -210, 0.5, -240)
    playerStatusGui.BackgroundColor3 = Color3.fromRGB(25, 25, 38)
    playerStatusGui.BorderSizePixel = 0
    playerStatusGui.Active = true
    playerStatusGui.Draggable = true
    playerStatusGui.ClipsDescendants = true
    playerStatusGui.Parent = screenGui

    local psCorner = Instance.new("UICorner")
    psCorner.CornerRadius = UDim.new(0, 14)
    psCorner.Parent = playerStatusGui

    local psTitle = Instance.new("TextLabel")
    psTitle.Size = UDim2.new(1, -50, 0, 45)
    psTitle.Position = UDim2.new(0, 15, 0, 0)
    psTitle.BackgroundTransparency = 1
    psTitle.Text = "🎮 LIVE PLAYER STATUS HUB"
    psTitle.TextColor3 = Color3.fromRGB(0, 162, 255)
    psTitle.TextSize = 15
    psTitle.Font = Enum.Font.GothamBold
    psTitle.TextXAlignment = Enum.TextXAlignment.Left
    psTitle.Parent = playerStatusGui

    local closeBtn = Instance.new("TextButton")
    closeBtn.Size = UDim2.new(0, 30, 0, 30)
    closeBtn.Position = UDim2.new(1, -38, 0, 8)
    closeBtn.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
    closeBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
    closeBtn.Text = "X"
    closeBtn.TextSize = 14
    closeBtn.Font = Enum.Font.GothamBold
    closeBtn.Parent = playerStatusGui

    local closeCorner = Instance.new("UICorner")
    closeCorner.CornerRadius = UDim.new(0, 8)
    closeCorner.Parent = closeBtn

    closeBtn.MouseButton1Click:Connect(function()
        if playerStatusGui and playerStatusGui.Parent then
            playerStatusGui:Destroy()
            playerStatusGui = nil
        end
    end)

    local psLine = Instance.new("Frame")
    psLine.Size = UDim2.new(0.92, 0, 0, 1)
    psLine.Position = UDim2.new(0.04, 0, 0, 45)
    psLine.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
    psLine.BorderSizePixel = 0
    psLine.Parent = playerStatusGui

    local psScroll = Instance.new("ScrollingFrame")
    psScroll.Size = UDim2.new(1, 0, 1, -55)
    psScroll.Position = UDim2.new(0, 0, 0, 52)
    psScroll.BackgroundTransparency = 1
    psScroll.BorderSizePixel = 0
    psScroll.ScrollBarThickness = 5
    psScroll.ScrollBarImageColor3 = Color3.fromRGB(0, 162, 255)
    psScroll.CanvasSize = UDim2.new(0, 0, 0, 0)
    psScroll.AutomaticCanvasSize = Enum.AutomaticSize.Y
    psScroll.Parent = playerStatusGui

    local psPadding = Instance.new("UIPadding")
    psPadding.PaddingTop = UDim.new(0, 5)
    psPadding.PaddingBottom = UDim.new(0, 15)
    psPadding.PaddingLeft = UDim.new(0, 15)
    psPadding.PaddingRight = UDim.new(0, 15)
    psPadding.Parent = psScroll

    local psLayout = Instance.new("UIListLayout")
    psLayout.SortOrder = Enum.SortOrder.LayoutOrder
    psLayout.Padding = UDim.new(0, 8)
    psLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    psLayout.Parent = psScroll

    task.spawn(function()
        while playerStatusGui and playerStatusGui.Parent do
            local currentPlayers = Players:GetPlayers()
            local activeUserIds = {}

            for index, p in ipairs(currentPlayers) do
                activeUserIds[p.UserId] = true
                local rowName = "PlayerRow_" .. p.UserId
                local row = psScroll:FindFirstChild(rowName)

                if not row then
                    row = Instance.new("Frame")
                    row.Name = rowName
                    row.Size = UDim2.new(1, 0, 0, 55)
                    row.BackgroundColor3 = Color3.fromRGB(38, 38, 55)
                    row.BorderSizePixel = 0
                    row.LayoutOrder = index
                    row.Parent = psScroll

                    local rCorner = Instance.new("UICorner")
                    rCorner.CornerRadius = UDim.new(0, 8)
                    rCorner.Parent = row

                    local pAvatar = Instance.new("ImageLabel")
                    pAvatar.Name = "PAvatar"
                    pAvatar.Size = UDim2.new(0, 40, 0, 40)
                    pAvatar.Position = UDim2.new(0, 8, 0.5, -20)
                    pAvatar.BackgroundTransparency = 1
                    pAvatar.Parent = row

                    local avCorner = Instance.new("UICorner")
                    avCorner.CornerRadius = UDim.new(0, 6)
                    avCorner.Parent = pAvatar

                    pcall(function()
                        pAvatar.Image = Players:GetUserThumbnailAsync(p.UserId, Enum.ThumbnailType.HeadShot, Enum.ThumbnailSize.Size420x420)
                    end)

                    local nameText = Instance.new("TextLabel")
                    nameText.Name = "PName"
                    nameText.Size = UDim2.new(0.55, 0, 0, 22)
                    nameText.Position = UDim2.new(0, 55, 0, 7)
                    nameText.BackgroundTransparency = 1
                    nameText.Text = p.DisplayName .. " (@" .. p.Name .. ")"
                    nameText.TextColor3 = Color3.fromRGB(255, 255, 255)
                    nameText.TextSize = 12
                    nameText.Font = Enum.Font.GothamBold
                    nameText.TextXAlignment = Enum.TextXAlignment.Left
                    nameText.Parent = row

                    local distLabel = Instance.new("TextLabel")
                    distLabel.Name = "PDist"
                    distLabel.Size = UDim2.new(0.55, 0, 0, 18)
                    distLabel.Position = UDim2.new(0, 55, 0, 30)
                    distLabel.BackgroundTransparency = 1
                    distLabel.TextColor3 = Color3.fromRGB(180, 180, 200)
                    distLabel.TextSize = 11
                    distLabel.Font = Enum.Font.Gotham
                    distLabel.TextXAlignment = Enum.TextXAlignment.Left
                    distLabel.Parent = row

                    local statLabel = Instance.new("TextLabel")
                    statLabel.Name = "PStat"
                    statLabel.Size = UDim2.new(0.4, 0, 1, 0)
                    statLabel.Position = UDim2.new(0.58, 0, 0, 0)
                    statLabel.BackgroundTransparency = 1
                    statLabel.TextSize = 11
                    statLabel.Font = Enum.Font.GothamBold
                    statLabel.TextXAlignment = Enum.TextXAlignment.Right
                    statLabel.Parent = row
                end

                local distLabel = row:FindFirstChild("PDist")
                local statLabel = row:FindFirstChild("PStat")

                local distanceStr = "Dist: N/A"
                local statusStr = "Status: Idle"
                local statusColor = Color3.fromRGB(150, 150, 150)

                local myChar = player.Character
                local pChar = p.Character
                if myChar and myChar:FindFirstChild("HumanoidRootPart") and pChar and pChar:FindFirstChild("HumanoidRootPart") then
                    local dist = (myChar.HumanoidRootPart.Position - pChar.HumanoidRootPart.Position).Magnitude
                    distanceStr = string.format("Dist: %.1f studs", dist)

                    local humanoid = pChar:FindFirstChildOfClass("Humanoid")
                    if humanoid then
                        local velocity = pChar.HumanoidRootPart.Velocity.Magnitude
                        if humanoid.Sit then
                            statusStr = "Status: 🪑 Sitting / Equipment"
                            statusColor = Color3.fromRGB(255, 170, 0)
                        elseif velocity > 18 then
                            statusStr = string.format("Status: 🏃 Running (Spd: %.0f)", velocity)
                            statusColor = Color3.fromRGB(0, 255, 120)
                        elseif velocity > 2 then
                            statusStr = "Status: 🚶 Walking"
                            statusColor = Color3.fromRGB(0, 200, 255)
                        else
                            statusStr = "Status: 💤 Standing / Resting"
                            statusColor = Color3.fromRGB(200, 100, 255)
                        end
                    end
                end

                if distLabel then distLabel.Text = distanceStr end
                if statLabel then
                    statLabel.Text = statusStr
                    statLabel.TextColor3 = statusColor
                end
            end

            for _, child in ipairs(psScroll:GetChildren()) do
                if child:IsA("Frame") and string.sub(child.Name, 1, 10) == "PlayerRow_" then
                    local pId = tonumber(string.sub(child.Name, 11))
                    if pId and not activeUserIds[pId] then
                        child:Destroy()
                    end
                end
            end

            task.wait(0.3)
        end
    end)
end

-- ==========================================================
-- EGG SPAWN PREDICTION PANEL (DIMENSIONS: W:390, H:200 + MIN/MAX STATS)
-- ==========================================================
local eggPredictionGui = nil

local function formatTimeDetailed(totalSeconds)
    local days = math.floor(totalSeconds / 86400)
    local hours = math.floor((totalSeconds % 86400) / 3600)
    local minutes = math.floor((totalSeconds % 3600) / 60)
    local seconds = math.floor(totalSeconds % 60)

    local parts = {}
    if days > 0 then table.insert(parts, days .. " days") end
    if hours > 0 then table.insert(parts, hours .. " hours") end
    if minutes > 0 then table.insert(parts, minutes .. " minutes") end
    table.insert(parts, seconds .. " seconds")

    return table.concat(parts, " ")
end

local function getRandomEggTime()
    return math.random(3600, 259200)
end

local function toggleEggPredictionPanel()
    if eggPredictionGui and eggPredictionGui.Parent then
        eggPredictionGui:Destroy()
        eggPredictionGui = nil
        return
    end

    eggPredictionGui = Instance.new("Frame")
    eggPredictionGui.Name = "EggPredictionWindow"
    eggPredictionGui.Size = UDim2.new(0, 390, 0, 200)
    eggPredictionGui.Position = UDim2.new(0.5, -195, 0.5, -100)
    eggPredictionGui.BackgroundColor3 = Color3.fromRGB(25, 25, 38)
    eggPredictionGui.BorderSizePixel = 0
    eggPredictionGui.Active = true
    eggPredictionGui.Draggable = true
    eggPredictionGui.ClipsDescendants = true
    eggPredictionGui.Parent = screenGui

    local epCorner = Instance.new("UICorner")
    epCorner.CornerRadius = UDim.new(0, 12)
    epCorner.Parent = eggPredictionGui

    local epTitle = Instance.new("TextLabel")
    epTitle.Size = UDim2.new(1, -40, 0, 30)
    epTitle.Position = UDim2.new(0, 12, 0, 0)
    epTitle.BackgroundTransparency = 1
    epTitle.Text = "🔮 ROYAL EGG PREDICTION"
    epTitle.TextColor3 = Color3.fromRGB(255, 170, 0)
    epTitle.TextSize = 13
    epTitle.Font = Enum.Font.GothamBold
    epTitle.TextXAlignment = Enum.TextXAlignment.Left
    epTitle.Parent = eggPredictionGui

    local closeBtn = Instance.new("TextButton")
    closeBtn.Size = UDim2.new(0, 22, 0, 22)
    closeBtn.Position = UDim2.new(1, -28, 0, 4)
    closeBtn.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
    closeBtn.TextColor3 = Color3.fromRGB(255, 255, 255)
    closeBtn.Text = "X"
    closeBtn.TextSize = 12
    closeBtn.Font = Enum.Font.GothamBold
    closeBtn.Parent = eggPredictionGui

    local closeCorner = Instance.new("UICorner")
    closeCorner.CornerRadius = UDim.new(0, 6)
    closeCorner.Parent = closeBtn

    closeBtn.MouseButton1Click:Connect(function()
        if eggPredictionGui and eggPredictionGui.Parent then
            eggPredictionGui:Destroy()
            eggPredictionGui = nil
        end
    end)

    local epLine = Instance.new("Frame")
    epLine.Size = UDim2.new(0.94, 0, 0, 1)
    epLine.Position = UDim2.new(0.03, 0, 0, 30)
    epLine.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
    epLine.BorderSizePixel = 0
    epLine.Parent = eggPredictionGui

    local epScroll = Instance.new("ScrollingFrame")
    epScroll.Size = UDim2.new(1, 0, 0, 135)
    epScroll.Position = UDim2.new(0, 0, 0, 33)
    epScroll.BackgroundTransparency = 1
    epScroll.BorderSizePixel = 0
    epScroll.ScrollBarThickness = 4
    epScroll.ScrollBarImageColor3 = Color3.fromRGB(255, 170, 0)
    epScroll.CanvasSize = UDim2.new(0, 0, 0, 0)
    epScroll.AutomaticCanvasSize = Enum.AutomaticSize.Y
    epScroll.Parent = eggPredictionGui

    local epPadding = Instance.new("UIPadding")
    epPadding.PaddingTop = UDim.new(0, 4)
    epPadding.PaddingBottom = UDim.new(0, 6)
    epPadding.PaddingLeft = UDim.new(0, 10)
    epPadding.PaddingRight = UDim.new(0, 10)
    epPadding.Parent = epScroll

    local epLayout = Instance.new("UIListLayout")
    epLayout.SortOrder = Enum.SortOrder.LayoutOrder
    epLayout.Padding = UDim.new(0, 5)
    epLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
    epLayout.Parent = epScroll

    local statsFooter = Instance.new("Frame")
    statsFooter.Size = UDim2.new(1, 0, 0, 30)
    statsFooter.Position = UDim2.new(0, 0, 1, -30)
    statsFooter.BackgroundColor3 = Color3.fromRGB(18, 18, 28)
    statsFooter.BorderSizePixel = 0
    statsFooter.Parent = eggPredictionGui

    local footerLine = Instance.new("Frame")
    footerLine.Size = UDim2.new(1, 0, 0, 1)
    footerLine.Position = UDim2.new(0, 0, 0, 0)
    footerLine.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
    footerLine.BorderSizePixel = 0
    footerLine.Parent = statsFooter

    local statsLabel = Instance.new("TextLabel")
    statsLabel.Size = UDim2.new(1, -20, 1, 0)
    statsLabel.Position = UDim2.new(0, 10, 0, 0)
    statsLabel.BackgroundTransparency = 1
    statsLabel.Text = "Est. Min/Max Spawn: 1 to 5 Eggs | Pets Rate: 50 to 250"
    statsLabel.TextColor3 = Color3.fromRGB(0, 220, 140)
    statsLabel.TextSize = 10
    statsLabel.Font = Enum.Font.GothamBold
    statsLabel.TextXAlignment = Enum.TextXAlignment.Center
    statsLabel.Parent = statsFooter

    local eggDataList = {
        { name = "Unicorn Egg", id = "125379833514592" },
        { name = "Kitsune Egg", id = "123193531109219" },
        { name = "Nigflame Egg", id = "134338256117362" },
        { name = "ArchAngel Egg", id = "94498866817720" },
        { name = "World Burner Egg", id = "127263885560222" },
        { name = "Royal Skywhale Egg", id = "101480954663721" },
    }

    if not _G.EggPredictionTimers then
        _G.EggPredictionTimers = {}
        math.randomseed(os.time())
        for _, egg in ipairs(eggDataList) do
            _G.EggPredictionTimers[egg.id] = getRandomEggTime()
        end
    end

    task.spawn(function()
        while eggPredictionGui and eggPredictionGui.Parent do
            for index, egg in ipairs(eggDataList) do
                local rowName = "EggRow_" .. egg.id
                local row = epScroll:FindFirstChild(rowName)

                if not row then
                    row = Instance.new("Frame")
                    row.Name = rowName
                    row.Size = UDim2.new(1, 0, 0, 36)
                    row.BackgroundColor3 = Color3.fromRGB(35, 35, 50)
                    row.BorderSizePixel = 0
                    row.LayoutOrder = index
                    row.Parent = epScroll

                    local rCorner = Instance.new("UICorner")
                    rCorner.CornerRadius = UDim.new(0, 6)
                    rCorner.Parent = row

                    local iconImg = Instance.new("ImageLabel")
                    iconImg.Name = "EggIcon"
                    iconImg.Size = UDim2.new(0, 26, 0, 26)
                    iconImg.Position = UDim2.new(0, 6, 0.5, -13)
                    iconImg.BackgroundTransparency = 1
                    iconImg.Image = "rbxassetid://" .. egg.id
                    iconImg.Parent = row

                    local icCorner = Instance.new("UICorner")
                    icCorner.CornerRadius = UDim.new(0, 4)
                    icCorner.Parent = iconImg

                    local nameText = Instance.new("TextLabel")
                    nameText.Name = "EggName"
                    nameText.Size = UDim2.new(0.38, 0, 1, 0)
                    nameText.Position = UDim2.new(0, 38, 0, 0)
                    nameText.BackgroundTransparency = 1
                    nameText.Text = egg.name
                    nameText.TextColor3 = Color3.fromRGB(255, 255, 255)
                    nameText.TextSize = 10
                    nameText.Font = Enum.Font.GothamBold
                    nameText.TextXAlignment = Enum.TextXAlignment.Left
                    nameText.Parent = row

                    local countdownText = Instance.new("TextLabel")
                    countdownText.Name = "EggCountdown"
                    countdownText.Size = UDim2.new(0.58, 0, 1, 0)
                    countdownText.Position = UDim2.new(0.40, 0, 0, 0)
                    countdownText.BackgroundTransparency = 1
                    countdownText.TextColor3 = Color3.fromRGB(255, 200, 0)
                    countdownText.TextSize = 9
                    countdownText.Font = Enum.Font.GothamBold
                    countdownText.TextXAlignment = Enum.TextXAlignment.Right
                    countdownText.Parent = row
                end

                local timeLeft = _G.EggPredictionTimers[egg.id] or getRandomEggTime()
                if timeLeft > 0 then
                    timeLeft = timeLeft - 1
                    _G.EggPredictionTimers[egg.id] = timeLeft
                else
                    _G.EggPredictionTimers[egg.id] = getRandomEggTime()
                end

                local countdownLabel = row:FindFirstChild("EggCountdown")
                if countdownLabel then
                    countdownLabel.Text = formatTimeDetailed(timeLeft)
                end
            end

            task.wait(1)
        end
    end)
end

-- ==========================================================
-- CHAOS OF THE SKY FEATURE
-- ==========================================================
local isChaosActive = false
local chaosFolder = nil

local function toggleChaosOfTheSky()
    isChaosActive = not isChaosActive
    
    if isChaosActive then
        spawnNotificationRow("SYSTEM", "MEGA AURORA BOREALIS ACTIVATED!", false, nil, true)
        
        chaosFolder = Instance.new("Folder")
        chaosFolder.Name = "ChaosSkyEffects"
        chaosFolder.Parent = workspace
        
        Lighting.ClockTime = 0
        Lighting.Brightness = 0.9
        Lighting.OutdoorAmbient = Color3.fromRGB(15, 35, 60)
        
        local atmos = Instance.new("Atmosphere")
        atmos.Name = "ChaosAtmosphere"
        atmos.Density = 0.4
        atmos.Offset = 0.2
        atmos.Color = Color3.fromRGB(0, 255, 170)
        atmos.Decay = Color3.fromRGB(50, 10, 140)
        atmos.Glare = 0.8
        atmos.Haze = 2.0
        atmos.Parent = chaosFolder
        
        local sky = Instance.new("Sky")
        sky.Name = "ChaosSky"
        sky.SkyboxBk = "rbxassetid://159454299"
        sky.SkyboxDn = "rbxassetid://159454299"
        sky.SkyboxFt = "rbxassetid://159454299"
        sky.SkyboxLf = "rbxassetid://159454299"
        sky.SkyboxRt = "rbxassetid://159454299"
        sky.SkyboxUp = "rbxassetid://159454299"
        sky.StarCount = 10000
        sky.Parent = chaosFolder
        
        local skyPart = Instance.new("Part")
        skyPart.Name = "AuroraSkyDome"
        skyPart.Size = Vector3.new(4000, 1, 4000)
        skyPart.Transparency = 1
        skyPart.Anchored = true
        skyPart.CanCollide = false
        skyPart.Parent = chaosFolder

        for i = 1, 2 do
            local auroraEmitter = Instance.new("ParticleEmitter")
            auroraEmitter.Name = "AuroraCurtains_" .. i
            auroraEmitter.Texture = "rbxassetid://110170832236629"
            auroraEmitter.Rate = 300
            auroraEmitter.Lifetime = NumberRange.new(8, 14)
            auroraEmitter.Speed = NumberRange.new(18, 38)
            auroraEmitter.VelocitySpread = 180
            auroraEmitter.Orientation = Enum.ParticleOrientation.VelocityPerpendicular
            auroraEmitter.LightEmission = 1
            auroraEmitter.LightInfluence = 0
            auroraEmitter.Size = NumberSequence.new({
                NumberSequenceKeypoint.new(0, 300),
                NumberSequenceKeypoint.new(0.5, 700),
                NumberSequenceKeypoint.new(1, 300)
            })
            auroraEmitter.Transparency = NumberSequence.new({
                NumberSequenceKeypoint.new(0, 1),
                NumberSequenceKeypoint.new(0.15, 0.2),
                NumberSequenceKeypoint.new(0.85, 0.2),
                NumberSequenceKeypoint.new(1, 1)
            })
            auroraEmitter.Color = ColorSequence.new({
                ColorSequenceKeypoint.new(0.0, Color3.fromRGB(0, 255, 150)),
                ColorSequenceKeypoint.new(0.3, Color3.fromRGB(0, 230, 255)),
                ColorSequenceKeypoint.new(0.7, Color3.fromRGB(200, 0, 255)),
                ColorSequenceKeypoint.new(1.0, Color3.fromRGB(0, 255, 150))
            })
            auroraEmitter.Parent = skyPart
        end
        
        local cometEmitter = Instance.new("ParticleEmitter")
        cometEmitter.Name = "CometShower"
        cometEmitter.Texture = "rbxassetid://258129754"
        cometEmitter.Rate = 50
        cometEmitter.Lifetime = NumberRange.new(1.5, 3)
        cometEmitter.Speed = NumberRange.new(400, 650)
        cometEmitter.SpreadAngle = Vector2.new(60, 60)
        cometEmitter.LightEmission = 1
        cometEmitter.LightInfluence = 0
        cometEmitter.Squash = NumberSequence.new(6)
        cometEmitter.Size = NumberSequence.new({
            NumberSequenceKeypoint.new(0, 8),
            NumberSequenceKeypoint.new(1, 0)
        })
        cometEmitter.Color = ColorSequence.new({
            ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)),
            ColorSequenceKeypoint.new(0.3, Color3.fromRGB(0, 255, 255)),
            ColorSequenceKeypoint.new(0.7, Color3.fromRGB(255, 100, 255)),
            ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 240, 120))
        })
        cometEmitter.Parent = skyPart

        task.spawn(function()
            while isChaosActive and chaosFolder and chaosFolder.Parent do
                local char = player.Character
                if char and char:FindFirstChild("HumanoidRootPart") then
                    skyPart.Position = char.HumanoidRootPart.Position + Vector3.new(0, 350, 0)
                end
                task.wait(0.2)
            end
        end)
    else
        spawnNotificationRow("SYSTEM", "CHAOS OF THE SKY DEACTIVATED", false, nil, false)
        Lighting.ClockTime = 14
        Lighting.Brightness = 2
        if chaosFolder then
            chaosFolder:Destroy()
            chaosFolder = nil
        end
    end
end

-- ==========================================================
-- LUCK EGGS & OTHER BANNER FEATURES
-- ==========================================================
local activeLuckBanner = nil
local luckTotalSeconds = 419 
local luckTimerConnection = nil

local function isBlockedTime()
    local dateTable = os.date("*t") 
    if dateTable.wday == 7 then 
        local currentHour = dateTable.hour
        if currentHour >= 22 then
            return true
        end
    end
    return false
end

local function showLuckEggsBanner()
    if isBlockedTime() then
        spawnNotificationRow("SYSTEM", "CANNOT BE USED WHEN ADMIN ABUSED", false, nil, true)
        return
    end

    luckTotalSeconds = luckTotalSeconds + 419
    
    if activeLuckBanner and activeLuckBanner.Parent then
        return
    end
    
    local luckContainer = Instance.new("Frame")
    luckContainer.Name = "LuckEggsBannerContainer"
    luckContainer.Size = UDim2.new(0, 180, 0, 65)
    luckContainer.Position = UDim2.new(1, -160, 0, -38)
    luckContainer.BackgroundTransparency = 1
    luckContainer.Parent = screenGui
    activeLuckBanner = luckContainer
    
    local bannerButton = Instance.new("ImageButton")
    bannerButton.Name = "BannerImage"
    bannerButton.Size = UDim2.new(1, 0, 0, 42)
    bannerButton.Position = UDim2.new(0, 0, 0, 0)
    bannerButton.BackgroundTransparency = 1
    bannerButton.Image = "rbxassetid://137984049408143"
    bannerButton.ScaleType = Enum.ScaleType.Fit
    bannerButton.Parent = luckContainer

    bannerButton.MouseButton1Click:Connect(function()
        if not isBlockedTime() then
            luckTotalSeconds = luckTotalSeconds + 419
        end
    end)

    local timerLabels = {}
    local positionsX = {0.09, 0.33, 0.57} 
    
    for i = 1, 3 do
        local tLabel = Instance.new("TextLabel")
        tLabel.Name = "TimerLabel_" .. i
        tLabel.Size = UDim2.new(0.34, 0, 0, 18)
        tLabel.Position = UDim2.new(positionsX[i], 0, 0, 41)
        tLabel.BackgroundTransparency = 1
        tLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
        tLabel.TextSize = 11
        tLabel.Font = Enum.Font.GothamBold
        tLabel.TextStrokeTransparency = 0
        tLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
        tLabel.Text = "6m 59s"
        tLabel.Parent = luckContainer
        
        table.insert(timerLabels, tLabel)
    end

    if luckTimerConnection then luckTimerConnection:Disconnect() end
    luckTimerConnection = RunService.RenderStepped:Connect(function(dt)
        if isBlockedTime() then
            if luckContainer and luckContainer.Parent then
                luckContainer:Destroy()
            end
            if luckTimerConnection then
                luckTimerConnection:Disconnect()
                luckTimerConnection = nil
            end
            return
        end

        if luckTotalSeconds > 0 then
            luckTotalSeconds = luckTotalSeconds - dt
            if luckTotalSeconds < 0 then luckTotalSeconds = 0 end
            
            local minutes = math.floor(luckTotalSeconds / 60)
            local seconds = math.floor(luckTotalSeconds % 60)
            local timeString = string.format("%dm %ds", minutes, seconds)
            
            for _, lbl in ipairs(timerLabels) do
                if lbl and lbl.Parent then
                    lbl.Text = timeString
                end
            end
        else
            if luckContainer and luckContainer.Parent then
                luckContainer:Destroy()
            end
            if luckTimerConnection then
                luckTimerConnection:Disconnect()
                luckTimerConnection = nil
            end
        end
    end)
end

local ownerBillboard = nil
local ownerConn = nil

local function toggleOwnerGeme()
    if ownerBillboard and ownerBillboard.Parent then
        ownerBillboard:Destroy()
        ownerBillboard = nil
        if ownerConn then
            ownerConn:Disconnect()
            ownerConn = nil
        end
    else
        local character = player.Character or player.CharacterAdded:Wait()
        local head = character:FindFirstChild("Head") or character:WaitForChild("Head", 3)
        
        if not head then return end

        ownerBillboard = Instance.new("BillboardGui")
        ownerBillboard.Name = "OwnerGemeBillboard"
        ownerBillboard.Size = UDim2.new(0, 200, 0, 50)
        ownerBillboard.StudsOffset = Vector3.new(0, 2.5, 0)
        ownerBillboard.AlwaysOnTop = true
        ownerBillboard.Parent = head

        local ownerText = Instance.new("TextLabel")
        ownerText.Size = UDim2.new(1, 0, 1, 0)
        ownerText.BackgroundTransparency = 1
        ownerText.Text = "[OWNER]"
        ownerText.TextColor3 = Color3.fromRGB(255, 0, 0)
        ownerText.TextSize = 26
        ownerText.Font = Enum.Font.GothamBlack
        ownerText.TextXAlignment = Enum.TextXAlignment.Center
        ownerText.TextYAlignment = Enum.TextYAlignment.Center
        ownerText.Parent = ownerBillboard

        local strokeBlack = Instance.new("UIStroke")
        strokeBlack.Thickness = 3.5
        strokeBlack.Color = Color3.fromRGB(0, 0, 0)
        strokeBlack.Parent = ownerText

        local gradient = Instance.new("UIGradient")
        gradient.Color = ColorSequence.new({
            ColorSequenceKeypoint.new(0.0, Color3.fromRGB(255, 0, 0)),
            ColorSequenceKeypoint.new(0.4, Color3.fromRGB(255, 120, 120)),
            ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 255, 255)),
            ColorSequenceKeypoint.new(0.6, Color3.fromRGB(255, 120, 120)),
            ColorSequenceKeypoint.new(1.0, Color3.fromRGB(255, 0, 0))
        })
        gradient.Transparency = NumberSequence.new(0)
        gradient.Rotation = 25
        gradient.Parent = ownerText

        ownerConn = RunService.RenderStepped:Connect(function()
            if not ownerText or not ownerText.Parent then
                if ownerConn then ownerConn:Disconnect() end
                return
            end
            gradient.Offset = Vector2.new((tick() * 1.5) % 3 - 1.5, 0)
        end)
    end
end

local activeCustomBanner = nil

local function showCustomBanner()
    if activeCustomBanner and activeCustomBanner.Parent then
        activeCustomBanner:Destroy()
    end
    
    local customContainer = Instance.new("Frame")
    customContainer.Name = "CustomBannerContainer"
    customContainer.Size = UDim2.new(0, 185, 0, 75)
    customContainer.Position = UDim2.new(0, 10, 1, -115)
    customContainer.BackgroundTransparency = 1
    customContainer.Parent = screenGui
    activeCustomBanner = customContainer
    
    local bannerImage = Instance.new("ImageButton")
    bannerImage.Name = "CustomBannerImage"
    bannerImage.Size = UDim2.new(1, 0, 1, 0)
    bannerImage.BackgroundTransparency = 1
    bannerImage.Image = "rbxassetid://100420031839850"
    bannerImage.ScaleType = Enum.ScaleType.Fit
    bannerImage.Parent = customContainer

    bannerImage.MouseButton1Click:Connect(function()
    end)
end

local function triggerServerCinematic(inputText)
    local fullBlack = Instance.new("Frame")
    fullBlack.Name = "FullscreenBlackout"
    fullBlack.Size = UDim2.new(2, 0, 2, 0)
    fullBlack.Position = UDim2.new(-0.5, 0, -0.5, 0)
    fullBlack.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
    fullBlack.BackgroundTransparency = 1
    fullBlack.BorderSizePixel = 0
    fullBlack.ZIndex = 999999
    fullBlack.Parent = screenGui

    local centerText = Instance.new("TextLabel")
    centerText.Name = "CenterText"
    centerText.Size = UDim2.new(0.9, 0, 0, 350)
    centerText.Position = UDim2.new(0.5, 0, 0.35, 0)
    centerText.AnchorPoint = Vector2.new(0.5, 0.5)
    centerText.BackgroundTransparency = 1
    centerText.Text = ""
    centerText.TextColor3 = Color3.fromRGB(255, 0, 0)
    centerText.TextSize = 70 
    centerText.FontFace = Font.new("rbxasset://fonts/families/GothamSSm.json", Enum.FontWeight.Heavy, Enum.FontStyle.Italic)
    centerText.TextWrapped = true
    centerText.TextXAlignment = Enum.TextXAlignment.Center
    centerText.TextYAlignment = Enum.TextYAlignment.Center
    centerText.ZIndex = 1000000
    centerText.Parent = fullBlack

    local strokeWhite = Instance.new("UIStroke")
    strokeWhite.Thickness = 8
    strokeWhite.Color = Color3.fromRGB(255, 255, 255)
    strokeWhite.Parent = centerText

    local strokeBlack = Instance.new("UIStroke")
    strokeBlack.Thickness = 11
    strokeBlack.Color = Color3.fromRGB(0, 0, 0)
    strokeBlack.Parent = centerText

    local glowGradient = Instance.new("UIGradient")
    glowGradient.Color = ColorSequence.new({
        ColorSequenceKeypoint.new(0.0, Color3.fromRGB(255, 255, 255)),
        ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 255, 255)),
        ColorSequenceKeypoint.new(1.0, Color3.fromRGB(255, 255, 255))
    })
    glowGradient.Transparency = NumberSequence.new({
        NumberSequenceKeypoint.new(0.0, 1),
        NumberSequenceKeypoint.new(0.5, 0.15),
        NumberSequenceKeypoint.new(1.0, 1)
    })
    glowGradient.Rotation = 35
    glowGradient.Enabled = false
    glowGradient.Parent = centerText

    local fadeIn = TweenService:Create(fullBlack, TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 0})
    fadeIn:Play()

    fadeIn.Completed:Connect(function()
        task.spawn(function()
            for i = 1, string.len(inputText) do
                if not centerText or not centerText.Parent then break end
                centerText.Text = string.sub(inputText, 1, i)
                task.wait(0.07)
            end

            task.wait(0.5)

            glowGradient.Enabled = true
            task.spawn(function()
                local conn
                conn = RunService.RenderStepped:Connect(function()
                    if not centerText or not centerText.Parent or not glowGradient.Enabled then
                        if conn then conn:Disconnect() end
                        return
                    end
                    glowGradient.Offset = Vector2.new((tick() * 0.8) % 2 - 1, 0)
                end)
            end)
        end)
    end)

    task.delay(6, function()
        if fullBlack and fullBlack.Parent then
            local fadeOut = TweenService:Create(fullBlack, TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {BackgroundTransparency = 1})
            fadeOut:Play()
            fadeOut.Completed:Connect(function()
                fullBlack:Destroy()
            end)
        end
    end)
end

-- ==========================================================
-- 3. MAIN PANEL BUTTON CONNECTIONS
-- ==========================================================

sendButton.MouseButton1Click:Connect(function()
    playCustomSound()
    local text = textBox.Text
    if text == "" then text = "meanwhile get ready for some eggs" end
    
    spawnNotificationRow("Lifzy", text, true, nil, false)
    textBox.Text = ""
end)

sendServerButton.MouseButton1Click:Connect(function()
    playCustomSound()
    local text = textBoxServer.Text
    if text == "" then text = "MAIN SERVER ANNOUNCEMENT!" end
    
    triggerServerCinematic(text)
    textBoxServer.Text = ""
end)

startHeadButton.MouseButton1Click:Connect(function()
    playCustomSound()
    local text = textBoxHead.Text
    if text == "" then text = "Lifzy Hub" end
    
    triggerHeadText(text)
    textBoxHead.Text = ""
end)

btnAdmin.MouseButton1Click:Connect(function()
    playCustomSound()
    spawnNotificationRow("ADMIN", "DO YOU WANT ADMIN ABUSE WIN?", false, nil, true)
end)

btnLuckEggs.MouseButton1Click:Connect(function()
    playCustomSound()
    showLuckEggsBanner()
end)

btnOwnerGeme.MouseButton1Click:Connect(function()
    playCustomSound()
    toggleOwnerGeme()
end)

btnCustomBanner.MouseButton1Click:Connect(function()
    playCustomSound()
    showCustomBanner()
end)

btnSpawnUnicorn.MouseButton1Click:Connect(function()
    spawnUnicornNotification()
end)

btnSpawnKitsune.MouseButton1Click:Connect(function()
    spawnKitsuneNotification()
end)

btnSpawnNigflame.MouseButton1Click:Connect(function()
    spawnNigflameNotification()
end)

btnSpawnArchangel.MouseButton1Click:Connect(function()
    spawnArchangelNotification()
end)

btnSpawnSkyywhale.MouseButton1Click:Connect(function()
    spawnSkyywhaleNotification()
end)

btnSpawnWorldBurner.MouseButton1Click:Connect(function()
    spawnWorldBurnerNotification()
end)

btnChaosSky.MouseButton1Click:Connect(function()
    playCustomSound()
    toggleChaosOfTheSky()
end)

btnPlayerStatus.MouseButton1Click:Connect(function()
    playCustomSound()
    togglePlayerStatusPanel()
end)

btnEggPrediction.MouseButton1Click:Connect(function()
    playCustomSound()
    toggleEggPredictionPanel()
end)
