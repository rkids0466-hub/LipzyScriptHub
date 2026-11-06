Pemain lokal = game:GetService(string.char(80,101,109,97,105,110))
Layanan Tween lokal = game:GetService(string.char(76,97,121,97,110,97,110,32,84,119,101,101,110))
Layanan Suara lokal = game:GetService(string.char(76,97,121,97,110,97,110,32,83,117,97,114,97))
RunService lokal = permainan:GetService(string.char(82,117,110,83,101,114,118,105,99,101))
Pencahayaan lokal = game:GetService(string.char(80,101,110,99,97,104,97,121,97,97,110))
Pemain lokal = Pemain.PemainLokal
jika player.PlayerGui:FindFirstChild(string.char(83,116,101,97,108,65,110,69,103,103,67,117,115,116,111,109,85,73)) maka
player.PlayerGui.StealAnEggCustomUI:Destroy()
akhir
local _0x1E0D = Instance.new(string.char(83,99,114,101,101,110,71,117,105))
_0x1E0D.Name =string.char(83,116,101,97,108,65,110,69,103,103,67,117,115,116,111,109,85,73)_0x1E0D.ResetOnSpawn = false
_0x1E0D.Parent = player.PlayerGui
mainFrame lokal = Instance.new(string.char(70,114,97,109,101))
mainFrame.Size = UDim2.new(0, 400, 0, 400)
mainFrame.Position = UDim2.new(0.5, -200, 0.5, -200)
mainFrame.BackgroundColor3 = Color3.fromRGB(30, 30, 45)
mainFrame.BorderSizePixel = 0
mainFrame.Active = true
mainFrame.Draggable = true
mainFrame.ClipsDescendants = true
mainFrame.Parent = _0x1E0D
uiCorner lokal = Instance.new(string.char(85,73,67,111,114,110,101,114))
uiCorner.CornerRadius = UDim.new(0, 12)
uiCorner.Parent = mainFrame
Label judul lokal = Instance.new(string.char(76,97,98,101,108,32,84,101,107,115))
Ukuran Label Judul = UDim2.baru(1, 0, 0, 40)
titleLabel.Posisi = UDim2.baru(0, 0, 0, 0)
titleLabel.BackgroundTransparency = 1
titleLabel.Text =string.char(67,117,114,105,32,84,101,108,117,114,32,45,32,80,97,110,101,108)titleLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
titleLabel.TextSize = 16
titleLabel.Font = Enum.Font.GothamBold
titleLabel.Parent = mainFrame
local _0x4A59 = Instance.new(string.char(70,114,97,109,101))
_0x4A59.Size = UDim2.new(0.9, 0, 0, 1)
_0x4A59.Position = UDim2.new(0.05, 0, 0, 40)
_0x4A59.BackgroundColor3 = Color3.fromRGB(55, 55, 75)
_0x4A59.BorderSizePixel = 0
_0x4A59.Parent = mainFrame
local _0x7326 = Instance.new(string.char(83,99,114,111,108,108,105,110,103,70,114,97,109,101))
_0x7326.Size = UDim2.new(1, 0, 1, -45)
_0x7326.Position = UDim2.new(0, 0, 0, 45)
_0x7326.BackgroundTransparency = 1
_0x7326.BorderSizePixel = 0
_0x7326.ScrollBarThickness = 5
_0x7326.ScrollBarImageColor3 = Color3.fromRGB(0, 162, 255)
_0x7326.CanvasSize = UDim2.new(0, 0, 0, 0)
_0x7326.AutomaticCanvasSize = Enum.AutomaticSize.Y
_0x7326.Parent = mainFrame
local _0xC3A4 = Instance.new(string.char(85,73,80,97,100,100,105,110,103))
_0xC3A4.PaddingTop = UDim.new(0, 5)
_0xC3A4.PaddingBottom = UDim.new(0, 15)
_0xC3A4.PaddingLeft = UDim.new(0, 15)
_0xC3A4.PaddingRight = UDim.new(0, 15)
_0xC3A4.Parent = _0x7326
local _0x0B10 = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0x0B10.SortOrder = Enum.SortOrder.LayoutOrder
_0x0B10.Padding = UDim.new(0, 8)
_0x0B10.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0x0B10.Parent = _0x7326
Kotak teks lokal = Instance.new(string.char(75,111,116,97,107,32,84,101,107,115))
textBox.Size = UDim2.new(1, 0, 0, 35)
textBox.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
textBox.TextColor3 = Color3.fromRGB(255, 255, 255)
textBox.PlaceholderText =string.char(75,101,116,105,107,32,112,101,115,97,110,32,100,105,32,115,105,110,105,46,46,46)textBox.Text =""textBox.TextSize = 13
textBox.Font = Enum.Font.Gotham
textBox.ClearTextOnFocus = false
textBox.LayoutOrder = 1
textBox.Parent = _0x7326
kotak sudut lokal = Instance.new(string.char(85,73,67,111,114,110,101,114))
boxCorner.CornerRadius = UDim.new(0, 8)
boxCorner.Parent = textBox
local _0x74F7 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0x74F7.Size = UDim2.new(1, 0, 0, 32)
_0x74F7.BackgroundColor3 = Color3.fromRGB(0, 162, 255)
_0x74F7.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x74F7.Text =string.char(75,73,82,73,77,32,80,69,83,65,78)_0x74F7.TextSize = 13
_0x74F7.Font = Enum.Font.GothamBold
_0x74F7.LayoutOrder = 2
_0x74F7.Parent = _0x7326
local _0x9138 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x9138.CornerRadius = UDim.new(0, 8)
_0x9138.Parent = _0x74F7
local _0x68E7 = Instance.new(string.char(84,101,120,116,66,111,120))
_0x68E7.Size = UDim2.new(1, 0, 0, 35)
_0x68E7.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
_0x68E7.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x68E7.PlaceholderText =string.char(75,101,116,105,107,32,112,101,110,103,117,109,117,109,97,110,32,115,101,114,118,101,114,46,46,46)_0x68E7.Text =""_0x68E7.TextSize = 13
_0x68E7.Font = Enum.Font.Gotham
_0x68E7.ClearTextOnFocus = false
_0x68E7.LayoutOrder = 3
_0x68E7.Parent = _0x7326
local _0x9263 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x9263.CornerRadius = UDim.new(0, 8)
_0x9263.Parent = _0x68E7
local _0x6420 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0x6420.Size = UDim2.new(1, 0, 0, 32)
_0x6420.BackgroundColor3 = Color3.fromRGB(255, 80, 0)
_0x6420.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x6420.Text =string.char(75,73,82,73,77,32,83,69,82,86,69,82)_0x6420.TextSize = 13
_0x6420.Font = Enum.Font.GothamBold
_0x6420.LayoutOrder = 4
_0x6420.Parent = _0x7326
local _0xFEF0 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xFEF0.CornerRadius = UDim.new(0, 8)
_0xFEF0.Parent = _0x6420
local _0x477A = Instance.new(string.char(84,101,120,116,66,111,120))
_0x477A.Size = UDim2.new(1, 0, 0, 35)
_0x477A.BackgroundColor3 = Color3.fromRGB(45, 45, 65)
_0x477A.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x477A.PlaceholderText =string.char(75,101,116,105,107,32,116,101,107,115,32,100,105,32,97,116,97,115,32,106,117,100,117,108,46,46,46)_0x477A.Text =""_0x477A.TextSize = 13
_0x477A.Font = Enum.Font.Gotham
_0x477A.ClearTextOnFocus = false
_0x477A.LayoutOrder = 5
_0x477A.Parent = _0x7326
kotakHeadCorner lokal = Instance.new(string.char(85,73,67,111,114,110,101,114))
boxHeadCorner.CornerRadius = UDim.new(0, 8)
boxHeadCorner.Parent = _0x477A
local _0x61B4 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0x61B4.Size = UDim2.new(1, 0, 0, 32)
_0x61B4.BackgroundColor3 = Color3.fromRGB(0, 200, 100)
_0x61B4.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x61B4.Text =string.char(77,85,76,65,73,32,79,86,69,82,72,69,65,68)_0x61B4.TextSize = 13
_0x61B4.Font = Enum.Font.GothamBold
_0x61B4.LayoutOrder = 6
_0x61B4.Parent = _0x7326
local _0xECE9 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xECE9.CornerRadius = UDim.new(0, 8)
_0xECE9.Parent = _0x61B4
gridContainer lokal = Instance.new(string.char(70,114,97,109,101))
gridContainer.Size = UDim2.new(1, 0, 0, 0)
gridContainer.BackgroundTransparency = 1
gridContainer.AutomaticSize = Enum.AutomaticSize.Y
gridContainer.LayoutOrder = 7
gridContainer.Parent = _0x7326
gridLayout lokal = Instance.new(string.char(85,73,71,114,105,100,76,97,121,111,117,116))
gridLayout.CellSize = UDim2.new(0.48, 0, 0, 35)
gridLayout.CellPadding = UDim2.new(0.04, 0, 0, 8)
gridLayout.SortOrder = Enum.SortOrder.LayoutOrder
gridLayout.Parent = gridContainer
fungsi lokal createFeatureButton(nama, warna, urutan)
local _0xF9B3 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0xF9B3.BackgroundColor3 = warna
_0xF9B3.TextColor3 = Color3.fromRGB(255, 255, 255)
_0xF9B3.Text = nama
_0xF9B3.TextSize = 11
_0xF9B3.Font = Enum.Font.GothamBold
_0xF9B3.LayoutOrder = urutan
_0xF9B3.Parent = gridContainer
lokal c = Instance.new(string.char(85,73,67,111,114,110,101,114))
c.CornerRadius = UDim.new(0, 8)
c.Parent = _0xF9B3
tombol kembali
akhir
local _0x5E44 = createFeatureButton(string.char(91,32,78,79,84,73,70,73,75,65,83,73,32,65,68,77,73,78,32,93), Color3.fromRGB(200, 50, 50), 1)
local _0x84E3 = createFeatureButton(string.char(91,32,84,69,76,85,82,32,75,69,66,69,82,85,78,84,85,78,71,65,78,32,93), Color3.fromRGB(255, 170, 0), 2)
local _0x19E8 = createFeatureButton(string.char(91,32,77,69,71,65,32,76,85,67,75,89,32,70,73,83,72,32,93), Color3.fromRGB(138, 43, 226), 3)
local _0xD9F6 = createFeatureButton(string.char(91,32,80,69,77,73,76,73,75,32,71,65,77,69,32,93), Color3.fromRGB(46, 139, 87), 4)
local _0xA8DE = createFeatureButton(string.char(91,32,83,80,65,87,78,32,85,78,73,67,79,82,78,32,93), Color3.fromRGB(199, 21, 133), 5)
local _0xC8D8 = createFeatureButton(string.char(91,32,83,80,65,87,78,32,75,73,84,83,85,78,69,32,93), Color3.fromRGB(255, 105, 180), 6)
local _0x7866 = createFeatureButton(string.char(91,32,83,80,65,87,78,32,78,73,71,70,76,65,77,69,32,93), Color3.fromRGB(180, 0, 0), 7)
local _0x427A = createFeatureButton(string.char(91,32,83,80,65,87,78,32,65,82,67,72,65,78,71,69,76,32,93), Color3.fromRGB(255, 127, 127), 8)
local _0x8E36 = createFeatureButton(string.char(91,32,83,80,65,87,78,32,83,75,89,87,72,65,76,69,32,93), Color3.fromRGB(147, 112, 219), 9)
local _0x15ED = createFeatureButton(string.char(91,32,83,80,65,87,78,32,87,79,82,76,68,66,85,82,78,69,82,32,93), Color3.fromRGB(220, 20, 100), 10)
fungsi lokal createFullWidthButton(nama, warna, urutan)
local _0xF9B3 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
Ukuran tombol = UDim2.baru(1, 0, 0, 32)
_0xF9B3.BackgroundColor3 = warna
_0xF9B3.TextColor3 = Color3.fromRGB(255, 255, 255)
_0xF9B3.Text = nama
_0xF9B3.TextSize = 12
_0xF9B3.Font = Enum.Font.GothamBold
_0xF9B3.LayoutOrder = urutan
_0xF9B3.Parent = _0x7326
lokal c = Instance.new(string.char(85,73,67,111,114,110,101,114))
c.CornerRadius = UDim.new(0, 8)
c.Parent = _0xF9B3
tombol kembali
akhir
local _0xDE09 = createFullWidthButton(string.char(91,32,83,75,89,32,67,72,65,79,83,32,93), Color3.fromRGB(0, 220, 140), 8)
local _0xDA57 = createFullWidthButton(string.char(91,32,83,84,65,84,85,83,32,80,69,77,65,73,78,32,93), Color3.fromRGB(0, 150, 255), 9)
local _0x9006 = createFullWidthButton(string.char(91,32,80,82,69,68,73,75,83,73,32,84,69,76,85,82,32,93), Color3.fromRGB(255, 100, 0), 10)
local _0x6991 = Instance.new(string.char(70,114,97,109,101))
_0x6991.Size = UDim2.new(0, 700, 0, 450)
_0x6991.Position = UDim2.new(0.5, 0, 0.02, 0)
_0x6991.AnchorPoint = Vector2.new(0.5, 0)
_0x6991.BackgroundTransparency = 1
_0x6991.Parent = _0x1E0D
uiListLayout lokal = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
uiListLayout.FillDirection = Enum.FillDirection.Vertical
uiListLayout.HorizontalAlignment = Enum.HorizontalAlignment.Center
uiListLayout.VerticalAlignment = Enum.VerticalAlignment.Top
uiListLayout.SortOrder = Enum.SortOrder.LayoutOrder
uiListLayout.Padding = UDim.new(0, 6)
uiListLayout.Parent = _0x6991
lokal globalOrder = 0
fungsi lokal playCustomSound()
pcall(function())
suara lokal = Instance.new(string.char(83,117,97,114,97))
sound.SoundId =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,51,48,48,49,55,48,57,56,55,55,50,53,55,50)sound.Volume = 1
sound.Parent = SoundService
sound:Play()
game:GetService(string.char(68,101,98,114,105,115)):AddItem(sound, 5)
akhir)
akhir
fungsi lokal getUserThumbnail()
keberhasilan lokal, hasil = pcall(fungsi())
return Players:GetUserThumbnailAsync(player.UserId, Enum.ThumbnailType.HeadShot, Enum.ThumbnailSize.Size420x420)
akhir)
jika berhasil maka
kembalikan hasil
akhir
kembali""akhir
fungsi lokal spawnNotificationRow(senderName, messageText, isPlayer, customAvatar, isGlowingAdmin)
globalOrder = globalOrder + 1
Konten avatar lokal = avatar kustom
jika isPlayer maka
avatarContent = getUserThumbnail()
senderName = player.DisplayName
akhir
notifRow lokal = Instance.new(string.char(70,114,97,109,101))
notifRow.Size = UDim2.new(0, 0, 0, 40)
notifRow.BackgroundTransparency = 1
notifRow.AnchorPoint = Vector2.new(0.5, 0.5)
notifRow.AutomaticSize = Enum.AutomaticSize.X
notifRow.ClipsDescendants = true
notifRow.LayoutOrder = globalOrder
notifRow.Parent = _0x6991
local _0x08AF = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0x08AF.FillDirection = Enum.FillDirection.Horizontal
_0x08AF.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0x08AF.VerticalAlignment = Enum.VerticalAlignment.Center
_0x08AF.SortOrder = Enum.SortOrder.LayoutOrder
_0x08AF.Padding = UDim.new(0, 6)
_0x08AF.Parent = notifRow
jika isPlayer dan avatarContent dan avatarContent ~=string.char(32,109,97,107,97)avatarImg lokal = Instance.new(string.char(73,109,97,103,101,76,97,98,101,108))
avatarImg.Name =string.char(65,118,97,116,97,114,73,109,103)avatarImg.Size = UDim2.new(0, 26, 0, 26)
avatarImg.BackgroundTransparency = 1
avatarImg.Image = avatarContent
avatarImg.LayoutOrder = 0
avatarImg.Parent = notifRow
avatarCorner lokal = Instance.new(string.char(85,73,67,111,114,110,101,114))
avatarCorner.CornerRadius = UDim.new(0, 6)
avatarCorner.Parent = avatarImg
lainnya
spasi lokal = Instance.new(string.char(70,114,97,109,101))
spacer.Name =string.char(83,112,97,99,101,114)spacer.Size = UDim2.new(0, 26, 0, 26)
spacer.BackgroundTransparency = 1
spacer.LayoutOrder = 0
spacer.Parent = notifRow
akhir
Label nama lokal = Instance.new(string.char(76,97,98,101,108,32,84,101,107,115))
nameLabel.Name =string.char(76,97,98,101,108,32,78,97,109,97)nameLabel.Size = UDim2.new(0, 0, 1, 0)
nameLabel.BackgroundTransparency = 1
nameLabel.AutomaticSize = Enum.AutomaticSize.X
nameLabel.Text = senderName
nameLabel.TextColor3 = isGlowingAdmin dan Color3.fromRGB(255, 40, 40) atau Color3.fromRGB(0, 162, 255)
nameLabel.TextSize = 20
nameLabel.Font = Enum.Font.GothamBlack
nameLabel.LayoutOrder = 1
nameLabel.Parent = notifRow
local _0xA462 = Instance.new(string.char(85,73,83,116,114,111,107,101))
_0xA462.Thickness = 2.5
_0xA462.Color = Color3.fromRGB(0, 0, 0)
_0xA462.Parent = nameLabel
jika isGlowingAdmin maka
gradien lokal = Instance.new(string.char(85,73,71,114,97,100,105,101,110,116))
gradient.Color = ColorSequence.new({
ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 80, 80)),
ColorSequenceKeypoint.new(0.3, Color3.fromRGB(255, 255, 255)),
ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 220, 220)),
ColorSequenceKeypoint.new(0.7, Color3.fromRGB(255, 255, 255)),
ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 80, 80))
})
gradient.Rotation = 25
gradient.Parent = nameLabel
task.spawn(function())
koneksi lokal
conn = RunService.RenderStepped:Connect(function()
jika bukan nameLabel atau bukan nameLabel.Parent maka
jika terhubung maka terhubung:Putuskan sambungan()
kembali
akhir
gradient.Offset = Vector2.new((tick() * 2.2) % 3 - 1.5, 0)
akhir)
akhir)
akhir
verifikasi gambar lokal = Instance.new(string.char(76,97,98,101,108,32,71,97,109,98,97,114))
verifyImage.Name =string.char(86,101,114,105,102,121,73,109,97,103,101)verifyImage.Size = UDim2.new(0, 18, 0, 18)
verifyImage.BackgroundTransparency = 1
verifyImage.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,56,48,50,57,48,55,49,56,53,56,52,55,52,56)verifyImage.LayoutOrder = 2
verifyImage.Parent = notifRow
local _0xAF8A = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0xAF8A.Name =string.char(76,97,98,101,108,32,80,101,115,97,110)_0xAF8A.Size = UDim2.new(0, 0, 1, 0)
_0xAF8A.BackgroundTransparency = 1
_0xAF8A.AutomaticSize = Enum.AutomaticSize.X
_0xAF8A.Text =string.char(58,32).. messageText
_0xAF8A.TextColor3 = Color3.fromRGB(255, 255, 255)
_0xAF8A.TextSize = 20
_0xAF8A.Font = Enum.Font.FredokaOne
_0xAF8A.LayoutOrder = 3
_0xAF8A.Parent = notifRow
local _0xFEF1 = Instance.new(string.char(85,73,83,116,114,111,107,101))
_0xFEF1.Thickness = 2
_0xFEF1.Color = Color3.fromRGB(0, 0, 0)
_0xFEF1.Parent = _0xAF8A
playCustomSound()
notifRow.Size = UDim2.new(0, 0, 0, 0)
local _0xB7E9 = TweenService:Create(
notifRow,
TweenInfo.new(0.25, Enum.EasingStyle.Back, Enum.EasingDirection.Out, 0, false, 0),
{Ukuran = UDim2.baru(0, 500, 0, 42)}
)
_0xB7E9:Play()
_0xB7E9.Completed:Connect(function()
local _0xF6AE = TweenService:Create(
notifRow,
TweenInfo.new(0.1, Enum.EasingStyle.Quad, Enum.EasingDirection.Out),
{Ukuran = UDim2.baru(0, 460, 0, 36)}
)
_0xF6AE:Play()
akhir)
task.delay(4, function())
jika notifRow dan notifRow.Parent maka
local _0xAA6A = TweenService:Create(
notifRow,
TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.In),
{Ukuran = UDim2.baru(0, 0, 0, 0)}
)
_0xAA6A:Play()
_0xAA6A.Completed:Connect(function())
notifRow:Destroy()
akhir)
akhir
akhir)
akhir
fungsi lokal spawnCustomTemplate(petName, zoneName, petColor, zoneColor)
playCustomSound()
globalOrder = globalOrder + 1
notifRow lokal = Instance.new(string.char(70,114,97,109,101))
notifRow.Name =string.char(67,117,115,116,111,109,83,112,97,119,110,78,111,116,105,102,82,111,119)notifRow.Size = UDim2.new(0, 0, 0, 0)
notifRow.BackgroundTransparency = 1
notifRow.AnchorPoint = Vector2.new(0.5, 0.5)
notifRow.AutomaticSize = Enum.AutomaticSize.X
notifRow.ClipsDescendants = true
notifRow.LayoutOrder = globalOrder
notifRow.Parent = _0x6991
local _0x8B4E = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0x8B4E.FillDirection = Enum.FillDirection.Vertical
_0x8B4E.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0x8B4E.VerticalAlignment = Enum.VerticalAlignment.Center
_0x8B4E.SortOrder = Enum.SortOrder.LayoutOrder
_0x8B4E.Padding = UDim.new(0, -4)
_0x8B4E.Parent = notifRow
baris lokal1 = Instance.new(string.char(70,114,97,109,101))
line1.Size = UDim2.new(0, 0, 0, 28)
line1.BackgroundTransparency = 1
line1.AutomaticSize = Enum.AutomaticSize.X
line1.LayoutOrder = 1
line1.Parent = notifRow
local _0x07D5 = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0x07D5.FillDirection = Enum.FillDirection.Horizontal
_0x07D5.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0x07D5.VerticalAlignment = Enum.VerticalAlignment.Center
_0x07D5.SortOrder = Enum.SortOrder.LayoutOrder
_0x07D5.Padding = UDim.new(0, 6)
_0x07D5.Parent = baris1
URL thumbnail lokal = getUserThumbnail()
jika thumbUrl ~=string.char(32)maka
avatarImg lokal = Instance.new(string.char(73,109,97,103,101,76,97,98,101,108))
avatarImg.Name =string.char(65,118,97,116,97,114,73,109,103)avatarImg.Size = UDim2.new(0, 26, 0, 26)
avatarImg.BackgroundTransparency = 1
avatarImg.Image = thumbUrl
avatarImg.LayoutOrder = 0
avatarImg.Parent = baris1
avatarCorner lokal = Instance.new(string.char(85,73,67,111,114,110,101,114))
avatarCorner.CornerRadius = UDim.new(0, 6)
avatarCorner.Parent = avatarImg
akhir
local _0x142B = player.DisplayName
nama lokalLbl = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
nameLbl.Size = UDim2.new(0, 0, 1, 0)
nameLbl.BackgroundTransparency = 1
nameLbl.AutomaticSize = Enum.AutomaticSize.X
nameLbl.Text = _0x142B
namaLbl.TeksWarna3 = Warna3.dariRGB(0, 162, 255)
nameLbl.TextSize = 17
nameLbl.Font = Enum.Font.GothamBlack
nameLbl.LayoutOrder = 1
nameLbl.Parent = baris1
lokal s1 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s1.Ketebalan = 2
s1.Warna = Warna3.dariRGB(0, 0, 0)
s1.Parent = nameLbl
verImg lokal = Instance.new(string.char(76,97,98,101,108,32,71,97,109,98,97,114))
verImg.Size = UDim2.new(0, 15, 0, 15)
verImg.BackgroundTransparency = 1
verImg.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,56,48,50,57,48,55,49,56,53,56,52,55,52,56)verImg.LayoutOrder = 2
verImg.Parent = baris1
local _0xD45C = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0xD45C.Size = UDim2.new(0, 0, 1, 0)
_0xD45C.BackgroundTransparency = 1
_0xD45C.AutomaticSize = Enum.AutomaticSize.X
_0xD45C.Text =string.char(32,109,101,109,117,110,99,117,108,107,97,110,32)_0xD45C.TextColor3 = Warna3.fromRGB(255, 255, 255)
_0xD45C.TextSize = 16
_0xD45C.Font = Enum.Font.FredokaOne
_0xD45C.LayoutOrder = 3
_0xD45C.Parent = baris1
lokal s2 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s2.Ketebalan = 1.8
s2.Warna = Warna3.dariRGB(0, 0, 0)
s2.Parent = _0xD45C
lokal rareEggLbl = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
rareEggLbl.Size = UDim2.new(0, 0, 1, 0)
rareEggLbl.BackgroundTransparency = 1
rareEggLbl.AutomaticSize = Enum.AutomaticSize.X
rareEggLbl.Text =string.char(84,69,76,85,82,32,76,65,78,71,75,65)rareEggLbl.TextColor3 = Color3.fromRGB(255, 170, 0)
rareEggLbl.TextSize = 17
rareEggLbl.Font = Enum.Font.GothamBlack
rareEggLbl.LayoutOrder = 4
rareEggLbl.Parent = baris1
lokal s3 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s3.Ketebalan = 2
s3.Warna = Warna3.dariRGB(0, 0, 0)
s3.Parent = rareEggLbl
local _0x6BC2 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
seruan1.Ukuran = UDim2.baru(0, 0, 1, 0)
seru1.TransparansiLatarBelakang = 1
_0x6BC2.AutomaticSize = Enum.AutomaticSize.X
seru1.Teks =string.char(33)_0x6BC2.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x6BC2.TextSize = 16
_0x6BC2.Font = Enum.Font.FredokaOne
seru1.LayoutOrder = 5
seru1.Induk = baris1
lokal s4 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s4.Ketebalan = 1.8
s4.Warna = Warna3.dariRGB(0, 0, 0)
s4.Parent = seru1
baris lokal2 = Instance.new(string.char(70,114,97,109,101))
baris2.Ukuran = UDim2.baru(0, 0, 0, 28)
baris2.Posisi = UDim2.baru(0, 0, 0, -3)
line2.BackgroundTransparency = 1
line2.AutomaticSize = Enum.AutomaticSize.X
line2.LayoutOrder = 2
line2.Parent = notifRow
local _0xE806 = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0xE806.FillDirection = Enum.FillDirection.Horizontal
_0xE806.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0xE806.VerticalAlignment = Enum.VerticalAlignment.Center
_0xE806.SortOrder = Enum.SortOrder.LayoutOrder
_0xE806.Padding = UDim.new(0, 5)
_0xE806.Parent = baris2
spasi lokal2 = Instance.new(string.char(70,114,97,109,101))
spacer2.Size = UDim2.new(0, 26, 0, 26)
spacer2.BackgroundTransparency = 1
spacer2.LayoutOrder = 0
spacer2.Parent = baris2
lokal aLbl = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
aLbl.Size = UDim2.new(0, 0, 1, 0)
aLbl.BackgroundTransparency = 1
aLbl.AutomaticSize = Enum.AutomaticSize.X
aLbl.Text =string.char(65)aLbl.TextColor3 = Color3.fromRGB(255, 255, 255)
aLbl.TextSize = 17
aLbl.Font = Enum.Font.GothamBlack
aLbl.LayoutOrder = 1
aLbl.Parent = baris2
sa lokal = Instance.baru(string.char(85,73,83,116,114,111,107,101))
sa.Ketebalan = 2
sa.Color = Color3.fromRGB(0, 0, 0)
sa.Parent = aLbl
petLbl lokal = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
petLbl.Size = UDim2.new(0, 0, 1, 0)
petLbl.BackgroundTransparency = 1
petLbl.AutomaticSize = Enum.AutomaticSize.X
petLbl.Text =string.char(32,73,108,97,104,105,32).. petName
petLbl.TextColor3 = petColor
petLbl.TextSize = 17
petLbl.Font = Enum.Font.GothamBlack
petLbl.LayoutOrder = 2
petLbl.Parent = baris2
lokal s5 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s5.Ketebalan = 2
s5.Warna = Warna3.dariRGB(0, 0, 0)
s5.Parent = petLbl
local _0x1523 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x1523.Size = UDim2.new(0, 0, 1, 0)
_0x1523.BackgroundTransparency = 1
_0x1523.AutomaticSize = Enum.AutomaticSize.X
_0x1523.Text =string.char(100,105,104,97,115,105,108,107,97,110,32,100,105)_0x1523.TextColor3 = Warna3.fromRGB(255, 255, 255)
_0x1523.TextSize = 16
_0x1523.Font = Enum.Font.FredokaOne
_0x1523.LayoutOrder = 3
_0x1523.Parent = line2lokal s6 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s6.Ketebalan = 1.8
s6.Warna = Warna3.dariRGB(0, 0, 0)
s6.Parent = _0x1523
zona lokal Lbl = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
zoneLbl.Size = UDim2.new(0, 0, 1, 0)
zoneLbl.BackgroundTransparency = 1
zoneLbl.AutomaticSize = Enum.AutomaticSize.X
zoneLbl.Text = zoneName
zoneLbl.TextColor3 = zoneColor
zoneLbl.TextSize = 17
zoneLbl.Font = Enum.Font.GothamBlack
zoneLbl.LayoutOrder = 4
zoneLbl.Parent = baris2
lokal s7 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s7.Ketebalan = 2
s7.Warna = Warna3.dariRGB(0, 0, 0)
s7.Parent = zoneLbl
local _0xC5C4 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
seruan2.Ukuran = UDim2.baru(0, 0, 1, 0)
seru2.TransparansiLatarBelakang = 1
_0xC5C4.AutomaticSize = Enum.AutomaticSize.X
seru2.Teks =string.char(33)_0xC5C4.TextColor3 = Color3.fromRGB(255, 255, 255)
_0xC5C4.TextSize = 16
_0xC5C4.Font = Enum.Font.FredokaOne
seru2.LayoutOrder = 5
seru2.Induk = baris2
lokal s8 = Instance.new(string.char(85,73,83,116,114,111,107,101))
s8.Ketebalan = 1.8
s8.Warna = Warna3.dariRGB(0, 0, 0)
s8.Parent = seru2
local _0xB7E9 = TweenService:Create(
notifRow,
TweenInfo.new(0.3, Enum.EasingStyle.Back, Enum.EasingDirection.Out, 0, false, 0),
{Ukuran = UDim2.baru(0, 480, 0, 56)}
)
_0xB7E9:Play()
task.delay(4, function())
jika notifRow dan notifRow.Parent maka
local _0xAA6A = TweenService:Create(
notifRow,
TweenInfo.new(0.2, Enum.EasingStyle.Quad, Enum.EasingDirection.In),
{Ukuran = UDim2.baru(0, 0, 0, 0)}
)
_0xAA6A:Play()
_0xAA6A.Completed:Connect(function())
notifRow:Destroy()
akhir)
akhir
akhir)
akhir
fungsi lokal spawnUnicornNotification()
spawnCustomTemplate(string.char(85,110,105,99,111,114,110),string.char(67,111,115,109,105,99,32,239,191,189,239,191,189), Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 0, 127))
akhir
fungsi lokal spawnKitsuneNotification()
spawnCustomTemplate(string.char(75,105,116,115,117,110,101),string.char(67,104,101,114,114,121,32,66,108,111,115,115,111,109,239,191,189,239,191,189), Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 255, 0))
akhir
fungsi lokal spawnNigflameNotification()
spawnCustomTemplate(string.char(78,105,103,102,108,97,109,101),string.char(84,105,116,97,110,32,84,101,109,112,108,101,239,191,189,239,191,189), Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 0, 0))
akhir
fungsi lokal spawnArchangelNotification()
spawnCustomTemplate(string.char(65,114,99,104,65,110,103,103,101,108),string.char(65,110,103,101,108,115,32,38,32,68,101,109,111,110,115,226,152,175,239,184,143), Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 140, 160))
akhir
fungsi lokal spawnSkyywhaleNotification()
spawnCustomTemplate(string.char(82,111,121,97,108,32,83,107,121,119,104,97,108,101),string.char(69,110,99,104,97,110,116,101,100,32,70,111,114,101,115,116,239,191,189,239,191,189), Color3.fromRGB(255, 255, 0), Color3.fromRGB(170, 0, 255))
akhir
fungsi lokal spawnWorldBurnerNotification()
spawnCustomTemplate(string.char(87,111,114,108,100,32,66,117,114,110,101,114),string.char(65,110,103,101,108,115,32,38,32,68,101,109,111,110,115,226,152,175,239,184,143), Color3.fromRGB(255, 255, 0), Color3.fromRGB(255, 140, 160))
akhir
Papan reklame lokal = nil
local function _0xC9CE(textInput)
jika headBillboard dan headBillboard.Parent maka
headBillboard:Destroy()
headBillboard = nil
akhir
karakter lokal = pemain.Karakter atau pemain.KarakterDitambahkan:Tunggu()
kepala lokal = karakter:TemukanAnakPertama(string.char(75,101,112,97,108,97)) atau karakter:TungguAnak(string.char(75,101,112,97,108,97), 3)
jika bukan kepala maka kembalikan akhir
headBillboard = Instance.new(string.char(66,105,108,108,98,111,97,114,100,71,117,105))
headBillboard.Name =string.char(67,117,115,116,111,109,72,101,97,100,84,101,120,116,66,105,108,108,98,111,97,114,100)headBillboard.Size = UDim2.new(0, 300, 0, 50)
headBillboard.StudsOffset = Vector3.new(0, 2.5, 0)
headBillboard.AlwaysOnTop = true
headBillboard.Parent = head
innerRow lokal = Instance.new(string.char(70,114,97,109,101))
innerRow.Size = UDim2.new(1, 0, 1, 0)
innerRow.BackgroundTransparency = 1
innerRow.AnchorPoint = Vector2.new(0.5, 0.5)
innerRow.Position = UDim2.new(0.5, 0, 0.5, 0)
innerRow.AutomaticSize = Enum.AutomaticSize.X
innerRow.Parent = headBillboard
local _0x08AF = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0x08AF.FillDirection = Enum.FillDirection.Horizontal
_0x08AF.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0x08AF.VerticalAlignment = Enum.VerticalAlignment.Center
_0x08AF.SortOrder = Enum.SortOrder.LayoutOrder
_0x08AF.Padding = UDim.new(0, 6)
_0x08AF.Parent = innerRow
local _0x9134 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x9134.Size = UDim2.new(0, 0, 1, 0)
_0x9134.BackgroundTransparency = 1
_0x9134.AutomaticSize = Enum.AutomaticSize.X
_0x9134.Text = textInput
_0x9134.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x9134.TextSize = 19
_0x9134.Font = Enum.Font.SourceSans
_0x9134.LayoutOrder = 1
_0x9134.Parent = innerRow
Teks garis lokal = Instance.new(string.char(85,73,83,116,114,111,107,101))
strokeText.Thickness = 1.5
strokeText.Color = Color3.fromRGB(0, 0, 0)
strokeText.Parent = _0x9134
lokal badgeImg = Instance.new(string.char(73,109,97,103,101,76,97,98,101,108))
badgeImg.Size = UDim2.new(0, 18, 0, 18)
badgeImg.BackgroundTransparency = 1
badgeImg.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,56,48,50,57,48,55,49,56,53,56,52,55,52,56)badgeImg.LayoutOrder = 2
badgeImg.Parent = innerRow
akhir
local _0x2993 = nil
fungsi lokal togglePlayerStatusPanel()
jika _0x2993 dan _0x2993.Parent maka
_0x2993:Destroy()
_0x2993 = nil
kembali
akhir
_0x2993 = Instance.new(string.char(70,114,97,109,101))
_0x2993.Name =string.char(80,108,97,121,101,114,83,116,97,116,117,115,87,105,110,100,111,119)_0x2993.Size = UDim2.new(0, 420, 0, 480)
_0x2993.Position = UDim2.new(0.5, -210, 0.5, -240)
_0x2993.BackgroundColor3 = Color3.fromRGB(25, 25, 38)
_0x2993.BorderSizePixel = 0
_0x2993.Active = true
_0x2993.Draggable = true
_0x2993.ClipsDescendants = true
_0x2993.Parent = _0x1E0D
local _0x14E1 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x14E1.CornerRadius = UDim.new(0, 14)
_0x14E1.Parent = _0x2993
Judul teks lokal = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
psTitle.Size = UDim2.new(1, -50, 0, 45)
psTitle.Position = UDim2.new(0, 15, 0, 0)
psTitle.BackgroundTransparency = 1
psTitle.Text =string.char(239,191,189,239,191,189,32,80,85,83,65,84,32,83,84,65,84,85,83,32,80,69,77,65,73,78,32,76,65,78,71,83,85,78,71)psTitle.TextColor3 = Color3.fromRGB(0, 162, 255)
psTitle.TextSize = 15
psTitle.Font = Enum.Font.GothamBold
psTitle.TextXAlignment = Enum.TextXAlignment.Left
psTitle.Parent = _0x2993
local _0x0712 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0x0712.Size = UDim2.new(0, 30, 0, 30)
_0x0712.Position = UDim2.new(1, -38, 0, 8)
_0x0712.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
_0x0712.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x0712.Text =string.char(88)_0x0712.TextSize = 14
_0x0712.Font = Enum.Font.GothamBold
_0x0712.Parent = _0x2993
local _0xBD58 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xBD58.CornerRadius = UDim.new(0, 8)
_0xBD58.Parent = _0x0712
_0x0712.MouseButton1Click:Connect(function()
jika _0x2993 dan _0x2993.Parent maka
_0x2993:Destroy()
_0x2993 = nil
akhir
akhir)
psLine lokal = Instance.new(string.char(70,114,97,109,101))
psLine.Size = UDim2.new(0.92, 0, 0, 1)
psLine.Position = UDim2.new(0.04, 0, 0, 45)
psLine.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
psLine.BorderSizePixel = 0
psLine.Parent = _0x2993
lokal psScroll = Instance.new(string.char(83,99,114,111,108,108,105,110,103,70,114,97,109,101))
psScroll.Size = UDim2.new(1, 0, 1, -55)
psScroll.Position = UDim2.new(0, 0, 0, 52)
psScroll.BackgroundTransparency = 1
psScroll.BorderSizePixel = 0
psScroll.ScrollBarThickness = 5
psScroll.ScrollBarImageColor3 = Color3.fromRGB(0, 162, 255)
psScroll.CanvasSize = UDim2.new(0, 0, 0, 0)
psScroll.AutomaticCanvasSize = Enum.AutomaticSize.Y
psScroll.Parent = _0x2993
local _0xA5DD = Instance.new(string.char(85,73,80,97,100,100,105,110,103))
_0xA5DD.PaddingTop = UDim.new(0, 5)
_0xA5DD.PaddingBottom = UDim.new(0, 15)
_0xA5DD.PaddingLeft = UDim.new(0, 15)
_0xA5DD.PaddingRight = UDim.new(0, 15)
_0xA5DD.Parent = psScroll
local _0xE9B1 = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0xE9B1.SortOrder = Enum.SortOrder.LayoutOrder
_0xE9B1.Padding = UDim.new(0, 8)
_0xE9B1.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0xE9B1.Parent = psScroll
task.spawn(function())
sementara _0x2993 dan _0x2993.Parent melakukan
Pemain lokal saat ini = Pemain:DapatkanPemain()
local _0xFB20 = {}
untuk indeks, p dalam ipairs(currentPlayers) lakukan
_0xFB20[p.UserId] = true
Nama baris lokal =string.char(66,97,114,105,115,80,101,109,97,105,110,95).. p.UserId
baris lokal = psScroll:TemukanAnakPertama(nama baris)
jika tidak baris maka
baris = Instance.new(string.char(70,114,97,109,101))
row.Name = rowName
Ukuran baris = UDim2.baru(1, 0, 0, 55)
baris.WarnaLatarBelakang3 = Warna3.dariRGB(38, 38, 55)
row.BorderSizePixel = 0
row.LayoutOrder = index
row.Parent = psScroll
local _0xE550 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xE550.CornerRadius = UDim.new(0, 8)
_0xE550.Parent = baris
local _0xCFDB = Instance.new(string.char(73,109,97,103,101,76,97,98,101,108))
_0xCFDB.Name =string.char(80,65,118,97,116,97,114)_0xCFDB.Size = UDim2.new(0, 40, 0, 40)
_0xCFDB.Posisi = UDim2.baru(0, 8, 0.5, -20)
_0xCFDB.BackgroundTransparency = 1
_0xCFDB.Parent = baris
local _0x888D = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x888D.CornerRadius = UDim.new(0, 6)
_0x888D.Parent = _0xCFDB
pcall(function())
_0xCFDB.Image = Players:GetUserThumbnailAsync(p.UserId, Enum.ThumbnailType.HeadShot, Enum.ThumbnailSize.Size420x420)
akhir)
nama teks lokal = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
nameText.Name =string.char(78,97,109,101,84,101,120,116)nameText.Size = UDim2.new(0.55, 0, 0, 22)
nameText.Position = UDim2.new(0, 55, 0, 7)
nameText.BackgroundTransparency = 1
namaTeks.Teks = p.NamaTampilan..string.char(32,40,64).. p.Nama..string.char(41)namaTeks.TeksWarna3 = Warna3.dariRGB(255, 255, 255)
nameText.TextSize = 12
nameText.Font = Enum.Font.GothamBold
nameText.TextXAlignment = Enum.TextXAlignment.Left
nameText.Parent = baris
local _0xA2CB = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0xA2CB.Name =string.char(80,68,105,115,116)_0xA2CB.Size = UDim2.new(0.55, 0, 0, 18)
_0xA2CB.Position = UDim2.new(0, 55, 0, 30)
_0xA2CB.BackgroundTransparency = 1
_0xA2CB.TextColor3 = Color3.fromRGB(180, 180, 200)
_0xA2CB.TextSize = 11
_0xA2CB.Font = Enum.Font.Gotham
_0xA2CB.TextXAlignment = Enum.TextXAlignment.Left
_0xA2CB.Parent = baris
local _0x9103 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x9103.Name =string.char(80,83,116,97,116)_0x9103.Ukuran = UDim2.baru(0,4, 0, 0, 18)
_0x9103.Posisi = UDim2.baru(0,58, 0, 0, 18)
_0x9103.BackgroundTransparency = 1
_0x9103.TextSize = 11
_0x9103.Font = Enum.Font.GothamBold
_0x9103.TextXAlignment = Enum.TextXAlignment.Right
_0x9103.Parent = baris
akhir
local _0xA2CB = row:FindFirstChild(string.char(80,68,105,115,116))
local _0x9103 = row:FindFirstChild(string.char(80,83,116,97,116))
local _0xF086 =string.char(74,97,114,97,107,58,32,84,105,100,97,107,32,84,101,114,115,101,100,105,97)local _0xEBB5 =string.char(83,116,97,116,117,115,58,32,84,105,100,97,107,32,65,107,116,105,102)statusColor lokal = Color3.fromRGB(150, 150, 150)
Karakter lokal myChar = pemain.Karakter
Karakter lokal pChar = p.Character
jika myChar dan myChar:FindFirstChild(string.char(72,117,109,97,110,111,105,100,82,111,111,116,80,97,114,116)) dan pChar dan pChar:FindFirstChild(string.char(72,117,109,97,110,111,105,100,82,111,111,116,80,97,114,116)) maka
jarak lokal = (myChar.HumanoidRootPart.Position - pChar.HumanoidRootPart.Position).Magnitudo
_0xF086 = string.format(string.char(74,97,114,97,107,58,32,37,46,49,102,32,115,116,117,100), dist)
humanoid lokal = pChar:TemukanAnakPertamaDariKelas(string.char(72,117,109,97,110,111,105,100))
jika humanoid maka
Kecepatan lokal = pChar.HumanoidRootPart.Velocity.Magnitude
jika humanoid.Duduk lalu
_0xEBB5 =string.char(83,116,97,116,117,115,58,32,239,191,189,239,191,189,32,68,117,100,117,107)statusColor = Color3.fromRGB(255, 170, 0)
jika kecepatan > 18 maka
_0xEBB5 = string.format(string.char(83,116,97,116,117,115,58,32,239,191,189,239,191,189,32,66,101,114,108,97,114,105,32,40,75,101,99,101,112,97,116,97,110,58,32,37,46,48,102,41), velocity)
statusColor = Color3.fromRGB(0, 255, 120)
jika kecepatan > 2 maka
_0xEBB5 =string.char(83,116,97,116,117,115,58,32,239,191,189,239,191,189,32,66,101,114,106,97,108,97,110)statusColor = Color3.fromRGB(0, 200, 255)
lainnya
_0xEBB5 =string.char(83,116,97,116,117,115,58,32,239,191,189,239,191,189,32,66,101,114,100,105,114,105,32,47,32,73,115,116,105,114,97,104,97,116)statusColor = Color3.fromRGB(200, 100, 255)
akhir
akhir
akhir
jika _0xA2CB maka _0xA2CB.Text = _0xF086
jika _0x9103 maka
_0x9103.Text = _0xEBB5
_0x9103.TextColor3 = statusColor
akhir
akhir
untuk _, anak dalam ipairs(psScroll:GetChildren()) lakukan
jika child:IsA(string.char(70,114,97,109,101)) dan string.sub(child.Name, 1, 11) ==string.char(80,108,97,121,101,114,82,111,119,95)maka
ID lokal = tonumber(string.sub(nama anak, 12))
jika pId dan bukan _0xFB20[pId] maka
child:Destroy()
akhir
akhir
akhir
task.wait(0.3)
akhir
akhir)
akhir
local _0x95C8 = nil
fungsi lokal formatTimeDetailed(totalSeconds)
hari lokal = math.floor(totalDetik / 86400)
jam lokal = math.floor((totalDetik % 86400) / 3600)
menit lokal = math.floor((totalDetik % 3600) / 60)
detik lokal = math.floor(totalDetik % 60)
bagian lokal = {}
jika hari > 0 maka tabel.sisipkan(bagian, hari ..string.char(100))
Jika jam > 0 maka masukkan tabel (bagian, jam ..string.char(104))
Jika menit > 0 maka sisipkan tabel (bagian, menit ..string.char(109))
table.insert(parts, seconds ..string.char(115))
kembalikan tabel.gabungkan(bagian,string.char(32))
akhir
fungsi lokal getRandomEggTime()
return math.random(3600, 259200)
akhir
fungsi lokal toggleEggPredictionPanel()
jika _0x95C8 dan _0x95C8.Parent maka
_0x95C8:Destroy()
_0x95C8 = nil
kembali
akhir
_0x95C8 = Instance.new(string.char(70,114,97,109,101))
_0x95C8.Name =string.char(74,101,110,100,101,108,97,32,80,114,101,100,105,107,115,105,32,84,101,108,117,114)_0x95C8.Size = UDim2.new(0, 390, 0, 200)
_0x95C8.Position = UDim2.new(0.5, -195, 0.5, -100)
_0x95C8.BackgroundColor3 = Color3.fromRGB(25, 25, 38)
_0x95C8.BorderSizePixel = 0
_0x95C8.Active = true
_0x95C8.Draggable = true
_0x95C8.ClipsDescendants = true
_0x95C8.Parent = _0x1E0D
local _0x7F86 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x7F86.CornerRadius = UDim.new(0, 12)
_0x7F86.Parent = _0x95C8
local _0x1984 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x1984.Size = UDim2.new(1, -40, 0, 30)
_0x1984.Position = UDim2.new(0, 12, 0, 0)
_0x1984.BackgroundTransparency = 1
_0x1984.Text =string.char(239,191,189,239,191,189,32,80,82,69,68,73,75,83,73,32,84,69,76,85,82,32,75,69,82,65,74,65,65,78)_0x1984.TextColor3 = Color3.fromRGB(255, 170, 0)
_0x1984.TextSize = 13
_0x1984.Font = Enum.Font.GothamBold
_0x1984.TextXAlignment = Enum.TextXAlignment.Left
_0x1984.Parent = _0x95C8
local _0x0712 = Instance.new(string.char(84,101,120,116,66,117,116,116,111,110))
_0x0712.Size = UDim2.new(0, 22, 0, 22)
_0x0712.Position = UDim2.new(1, -28, 0, 4)
_0x0712.BackgroundColor3 = Color3.fromRGB(200, 50, 50)
_0x0712.TextColor3 = Color3.fromRGB(255, 255, 255)
_0x0712.Text =string.char(88)_0x0712.TextSize = 12
_0x0712.Font = Enum.Font.GothamBold
_0x0712.Parent = _0x95C8
local _0xBD58 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xBD58.CornerRadius = UDim.new(0, 6)
_0xBD58.Parent = _0x0712
_0x0712.MouseButton1Click:Connect(function()
jika _0x95C8 dan _0x95C8.Parent maka
_0x95C8:Destroy()
_0x95C8 = nil
akhir
akhir)
epLine lokal = Instance.new(string.char(70,114,97,109,101))
epLine.Size = UDim2.new(0.94, 0, 0, 1)
epLine.Position = UDim2.new(0.03, 0, 0, 30)
epLine.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
epLine.BorderSizePixel = 0
epLine.Parent = _0x95C8
local _0xD044 = Instance.new(string.char(83,99,114,111,108,108,105,110,103,70,114,97,109,101))
_0xD044.Size = UDim2.new(1, 0, 0, 135)
_0xD044.Position = UDim2.new(0, 0, 0, 33)
_0xD044.BackgroundTransparency = 1
_0xD044.BorderSizePixel = 0
_0xD044.ScrollBarThickness = 4
_0xD044.ScrollBarImageColor3 = Color3.fromRGB(255, 170, 0)
_0xD044.CanvasSize = UDim2.new(0, 0, 0, 0)
_0xD044.AutomaticCanvasSize = Enum.AutomaticSize.Y
_0xD044.Parent = _0x95C8
local _0xBC44 = Instance.new(string.char(85,73,80,97,100,100,105,110,103))
_0xBC44.PaddingTop = UDim.new(0, 4)
_0xBC44.PaddingBottom = UDim.new(0, 6)
_0xBC44.PaddingLeft = UDim.new(0, 10)
_0xBC44.PaddingRight = UDim.new(0, 10)
_0xBC44.Parent = _0xD044
local _0xBE9F = Instance.new(string.char(85,73,76,105,115,116,76,97,121,111,117,116))
_0xBE9F.SortOrder = Enum.SortOrder.LayoutOrder
_0xBE9F.Padding = UDim.new(0, 5)
_0xBE9F.HorizontalAlignment = Enum.HorizontalAlignment.Center
_0xBE9F.Parent = _0xD044
statistik lokal kaki = Instance.new(string.char(70,114,97,109,101))
statsFooter.Ukuran = UDim2.baru(1, 0, 0, 30)
statsFooter.Position = UDim2.baru(0, 0, 1, -30)
statsFooter.BackgroundColor3 = Color3.fromRGB(18, 18, 28)
statsFooter.BorderSizePixel = 0
statsFooter.Parent = _0x95C8
local _0x35A9 = Instance.new(string.char(70,114,97,109,101))
_0x35A9.Size = UDim2.new(1, 0, 0, 1)
_0x35A9.Position = UDim2.new(0, 0, 0, 0)
_0x35A9.BackgroundColor3 = Color3.fromRGB(50, 50, 70)
_0x35A9.BorderSizePixel = 0
_0x35A9.Parent = statsFooter
local _0xB001 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0xB001.Size = UDim2.new(1, -20, 1, 0)
_0xB001.Posisi = UDim2.baru(0, 10, 0, 0)
_0xB001.BackgroundTransparency = 1
_0xB001.Text =string.char(80,101,114,107,105,114,97,97,110,32,84,101,108,117,114,32,77,105,110,47,77,97,120,58,32,49,32,104,105,110,103,103,97,32,53,32,124,32,84,105,110,103,107,97,116,32,75,101,109,117,110,99,117,108,97,110,32,72,101,119,97,110,32,80,101,108,105,104,97,114,97,97,110,58,32,53,48,32,104,105,110,103,103,97,32,50,53,48)_0xB001.TextColor3 = Color3.fromRGB(0, 220, 140)
_0xB001.TextSize = 10
_0xB001.Font = Enum.Font.GothamBold
_0xB001.TextXAlignment = Enum.TextXAlignment.Center
_0xB001.Parent = statsFooter
Daftar Data telur lokal = {
{ name =string.char(84,101,108,117,114,32,85,110,105,99,111,114,110), id =string.char(49,50,53,51,55,57,56,51,51,53,49,52,53,57,50)},
{ name =string.char(84,101,108,117,114,32,75,105,116,115,117,110,101), id =string.char(49,50,51,49,57,51,53,51,49,49,48,57,50,49,57)},
{ name =string.char(84,101,108,117,114,32,78,105,103,102,108,97,109,101), id =string.char(49,51,52,51,51,56,50,53,54,49,49,55,51,54,50)},
{ name =string.char(84,101,108,117,114,32,77,97,108,97,105,107,97,116,32,65,103,117,110,103), id =string.char(57,52,52,57,56,56,54,54,56,49,55,55,50,48)},
{ name =string.char(84,101,108,117,114,32,80,101,109,98,97,107,97,114,32,68,117,110,105,97), id =string.char(49,50,55,50,54,51,56,56,53,53,54,48,50,50,50)},
{ name =string.char(84,101,108,117,114,32,80,97,117,115,32,76,97,110,103,105,116,32,75,101,114,97,106,97,97,110), id =string.char(49,48,49,52,56,48,57,53,52,54,54,51,55,50,49)},
}
jika tidak _G.EggPredictionTimers maka
_G.EggPredictionTimers = {}
math.randomseed(os.time())
untuk _, telur dalam ipairs(eggDataList) lakukan
_G.EggPredictionTimers[egg.id] = getRandomEggTime()
akhir
akhir
task.spawn(function())
sementara _0x95C8 dan _0x95C8.Parent melakukan
untuk setiap indeks, telur dalam ipairs(eggDataList) lakukan
Nama baris lokal =string.char(66,97,114,105,115,32,84,101,108,117,114,95).. egg.id
baris lokal = _0xD044:TemukanAnakPertama(nama baris)
jika tidak baris maka
baris = Instance.new(string.char(70,114,97,109,101))
row.Name = rowName
Ukuran baris = UDim2.baru(1, 0, 0, 36)
baris.WarnaLatarBelakang3 = Warna3.dariRGB(35, 35, 50)
row.BorderSizePixel = 0
row.LayoutOrder = index
row.Parent = _0xD044
local _0xE550 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0xE550.CornerRadius = UDim.new(0, 6)
_0xE550.Parent = baris
local _0xD92B = Instance.new(string.char(73,109,97,103,101,76,97,98,101,108))
_0xD92B.Name =string.char(73,107,111,110,32,84,101,108,117,114)_0xD92B.Size = UDim2.new(0, 26, 0, 26)
_0xD92B.Position = UDim2.new(0, 6, 0.5, -13)
_0xD92B.BackgroundTransparency = 1
_0xD92B.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47).. egg.id
_0xD92B.Parent = baris
local _0x0EE3 = Instance.new(string.char(85,73,67,111,114,110,101,114))
_0x0EE3.CornerRadius = UDim.new(0, 4)
_0x0EE3.Parent = _0xD92B
nama teks lokal = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
nameText.Name =string.char(78,97,109,97,32,84,101,108,117,114)nameText.Size = UDim2.new(0.38, 0, 1, 0)
nameText.Position = UDim2.new(0, 38, 0, 0)
nameText.BackgroundTransparency = 1
nameText.Text = egg.name
namaTeks.TeksWarna3 = Warna3.dariRGB(255, 255, 255)
nameText.TextSize = 10
nameText.Font = Enum.Font.GothamBold
nameText.TextXAlignment = Enum.TextXAlignment.Left
nameText.Parent = baris
local _0x6609 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x6609.Name =string.char(72,105,116,117,110,103,32,77,117,110,100,117,114,32,84,101,108,117,114)_0x6609.Size = UDim2.new(0.58, 0, 1, 0)
_0x6609.Position = UDim2.new(0.40, 0, 0, 0)
_0x6609.BackgroundTransparency = 1
_0x6609.TextColor3 = Color3.fromRGB(255, 200, 0)
_0x6609.TextSize = 9
_0x6609.Font = Enum.Font.GothamBold
_0x6609.TextXAlignment = Enum.TextXAlignment.Right
_0x6609.Parent = baris
akhir
waktu lokal Tersisa = _G.EggPredictionTimers[egg.id] atau getRandomEggTime()
jika waktu tersisa > 0 maka
waktu tersisa = waktu tersisa - 1
_G.EggPredictionTimers[egg.id] = timeLeft
lainnya
_G.EggPredictionTimers[egg.id] = getRandomEggTime()
akhir
local _0x5439 = row:FindFirstChild(string.char(69,103,103,67,111,117,110,116,100,111,119,110))
jika _0x5439 maka
_0x5439.Text = formatTimeDetailed(timeLeft)
akhir
akhir
task.wait(1)
akhir
akhir)
akhir
lokal isChaosActive = false
lokal chaosFolder = nil
fungsi lokal toggleChaosOfTheSky()
isChaosActive = bukan isChaosActive
jika isChaosActive maka
spawnNotificationRow(string.char(83,89,83,84,69,77),string.char(77,69,71,65,32,65,85,82,79,82,65,32,66,79,82,69,65,76,73,83,32,65,75,84,73,70,33), false, nil, true)
chaosFolder = Instance.new(string.char(70,111,108,100,101,114))
chaosFolder.Name =string.char(67,104,97,111,115,83,107,121,69,102,102,101,99,116,115)chaosFolder.Parent = ruang kerja
Lighting.ClockTime = 0
Lighting.Brightness = 0.9
Lighting.OutdoorAmbient = Color3.fromRGB(15, 35, 60)
atmosfer lokal = Instance.new(string.char(65,116,109,111,115,102,101,114))
atmos.Name =string.char(67,104,97,111,115,65,116,109,111,115,112,104,101,114,101)atmos.Density = 0.4
atmos.Offset = 0.2
atmos.Color = Color3.fromRGB(0, 255, 170)
atmos.Decay = Color3.fromRGB(50, 10, 140)
atmos.Glare = 0.8
atmos.Haze = 2.0
atmos.Parent = chaosFolder
langit lokal = Instance.new(string.char(76,97,110,103,105,116))
sky.Name =string.char(67,104,97,111,115,83,107,121)sky.SkyboxBk =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.SkyboxDn =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.SkyboxFt =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.SkyboxLf =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.SkyboxRt =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.SkyboxUp =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,53,57,52,53,52,50,57,57)sky.StarCount = 10000
sky.Parent = chaosFolder
skyPart lokal = Instance.new(string.char(80,97,114,116))
skyPart.Name =string.char(65,117,114,111,114,97,83,107,121,68,111,109,101)skyPart.Size = Vector3.new(4000, 1, 4000)
skyPart.Transparency = 1
skyPart.Anchored = true
skyPart.CanCollide = false
skyPart.Parent = chaosFolder
untuk i = 1, 2 lakukan
local _0xC2CA = Instance.new(string.char(80,97,114,116,105,99,108,101,69,109,105,116,116,101,114))
_0xC2CA.Name =string.char(65,117,114,111,114,97,67,117,114,116,97,105,110,115,95).. i
_0xC2CA.Texture =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,49,48,49,55,48,56,51,50,50,51,54,54,50,57)_0xC2CA.Rate = 300
_0xC2CA.Lifetime = NumberRange.new(8, 14)
_0xC2CA.Speed ​​= NumberRange.new(18, 38)
_0xC2CA.VelocitySpread = 180
_0xC2CA.Orientation = Enum.ParticleOrientation.VelocityPerpendicular
_0xC2CA.LightEmission = 1
_0xC2CA.LightInfluence = 0
_0xC2CA.Size = NumberSequence.new({
NumberSequenceKeypoint.new(0, 300),
NumberSequenceKeypoint.new(0.5, 700),
NumberSequenceKeypoint.new(1, 300)
})
_0xC2CA.Transparency = NumberSequence.new({
NumberSequenceKeypoint.new(0, 1),
NumberSequenceKeypoint.new(0.15, 0.2),
NumberSequenceKeypoint.new(0.85, 0.2),
NumberSequenceKeypoint.new(1, 1)
})
_0xC2CA.Color = ColorSequence.new({
ColorSequenceKeypoint.new(0.0, Color3.fromRGB(0, 255, 150)),
ColorSequenceKeypoint.new(0.3, Color3.fromRGB(0, 230, 255)),
ColorSequenceKeypoint.new(0.7, Color3.fromRGB(200, 0, 255)),
ColorSequenceKeypoint.new(1.0, Color3.fromRGB(0, 255, 150))
})
_0xC2CA.Parent = skyPart
akhir
local _0x7A66 = Instance.new(string.char(80,97,114,116,105,99,108,101,69,109,105,116,116,101,114))
_0x7A66.Name =string.char(67,111,109,101,116,83,104,111,119,101,114)_0x7A66.Texture =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,50,53,56,49,50,57,55,53,52)_0x7A66.Rate = 50
_0x7A66.Lifetime = NumberRange.new(1.5, 3)
_0x7A66.Speed ​​= NumberRange.new(400, 650)
_0x7A66.SpreadAngle = Vektor2.baru(60, 60)
_0x7A66.LightEmission = 1
_0x7A66.LightInfluence = 0
_0x7A66.Squash = NumberSequence.new(6)
_0x7A66.Size = NumberSequence.new({
NumberSequenceKeypoint.new(0, 8),
NumberSequenceKeypoint.new(1, 0)
})
_0x7A66.Color = ColorSequence.new({
ColorSequenceKeypoint.new(0, Color3.fromRGB(255, 255, 255)),
ColorSequenceKeypoint.new(0.3, Color3.fromRGB(0, 255, 255)),
ColorSequenceKeypoint.new(0.7, Color3.fromRGB(255, 100, 255)),
ColorSequenceKeypoint.new(1, Color3.fromRGB(255, 240, 120))
})
_0x7A66.Parent = skyPart
task.spawn(function())
selama isChaosActive dan chaosFolder dan chaosFolder.Parent lakukan
karakter lokal = pemain.Karakter
jika char dan char:FindFirstChild(string.char(72,117,109,97,110,111,105,100,82,111,111,116,80,97,114,116)) maka
skyPart.Position = char.HumanoidRootPart.Position + Vector3.new(0, 350, 0)
akhir
task.wait(0.2)
akhir
akhir)
lainnya
spawnNotificationRow(string.char(83,89,83,84,69,77),string.char(83,75,89,32,67,72,65,79,83,32,68,73,83,65,66,76,69,68), false, nil, false)
Lighting.ClockTime = 14
Lighting.Brightness = 2
jika chaosFolder maka
chaosFolder:Destroy()
chaosFolder = nil
akhir
akhir
akhir
local _0x9AD2 = nil
keberuntungan lokalTotalDetik = 419
local _0x436D = nil
fungsi lokal isBlockedTime()
tabel tanggal lokal = os.tanggal(string.char(42,116))
jika dateTable.wday == 7 maka
Jam saat ini lokal = tabel tanggal.jam
jika currentHour >= 22 maka
kembalikan true
akhir
akhir
return false
akhir
fungsi lokal showLuckEggsBanner()
jika isBlockedTime() maka
spawnNotificationRow(string.char(83,89,83,84,69,77),string.char(84,73,68,65,75,32,68,65,80,65,84,32,68,73,71,85,78,65,75,65,78,32,74,73,75,65,32,65,68,77,73,78,32,68,73,83,65,76,65,72,71,85,78,65,75,65,78), false, nil, true)
kembali
akhir
luckTotalSeconds = luckTotalSeconds + 419
jika _0x9AD2 dan _0x9AD2.Parent maka
kembali
akhir
local _0x15AA = Instance.new(string.char(70,114,97,109,101))
_0x15AA.Name =string.char(76,117,99,107,69,103,103,115,66,97,110,110,101,114,67,111,110,116,97,105,110,101,114)_0x15AA.Size = UDim2.new(0, 180, 0, 65)
_0x15AA.Position = UDim2.new(1, -160, 0, -38)
_0x15AA.BackgroundTransparency = 1
_0x15AA.Parent = _0x1E0D
_0x9AD2 = _0x15AA
local _0x488C = Instance.new(string.char(73,109,97,103,101,66,117,116,116,111,110))
_0x488C.Name =string.char(66,97,110,110,101,114,73,109,97,103,101)_0x488C.Size = UDim2.new(1, 0, 0, 42)
_0x488C.Posisi = UDim2.baru(0, 0, 0, 0)
_0x488C.BackgroundTransparency = 1
_0x488C.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,51,55,57,56,52,48,52,57,52,48,56,49,52,51)_0x488C.ScaleType = Enum.ScaleType.Fit
_0x488C.Parent = _0x15AA
_0x488C.MouseButton1Click:Connect(function())
jika isBlockedTime() tidak maka
luckTotalSeconds = luckTotalSeconds + 419
akhir
akhir)
label pengatur waktu lokal = {}
posX lokal = {0.09, 0.33, 0.57}
untuk i = 1, 3 lakukan
tLabel lokal = Instance.baru(string.char(76,97,98,101,108,84,101,107,115))
tLabel.Name =string.char(84,105,109,101,114,76,97,98,101,108,95).. i
tLabel.Ukuran = UDim2.baru(0, 34, 0, 18)
tLabel.Posisi = UDim2.baru(posX[i], 0, 0, 41)
tLabel.BackgroundTransparency = 1
tLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
tLabel.TextSize = 11
tLabel.Font = Enum.Font.GothamBold
tLabel.TextStrokeTransparency = 0
tLabel.TextStrokeColor3 = Color3.fromRGB(0, 0, 0)
tLabel.Text =string.char(54,109,32,53,57,115)tLabel.Parent = _0x15AA
table.insert(timerLabels, tLabel)
akhir
jika _0x436D maka _0x436D:Disconnect() end
_0x436D = RunService.RenderStepped:Connect(function(dt))
jika isBlockedTime() maka
jika _0x15AA dan _0x15AA.Parent maka
_0x15AA:Destroy()
akhir
jika _0x436D maka
_0x436D:Disconnect()
_0x436D = nil
akhir
kembali
akhir
jika luckTotalSeconds > 0 maka
luckTotalSeconds = luckTotalSeconds - dt
Jika luckTotalSeconds < 0 maka luckTotalSeconds = 0
menit lokal = math.floor(luckTotalSeconds / 60)
detik lokal = math.floor(luckTotalSeconds % 60)
string waktu lokal = string.format(string.char(37,100,109,32,37,100,115), menit, detik)
untuk _, lbl dalam ipairs(timerLabels) lakukan
jika lbl dan lbl.Parent maka
lbl.Text = timeString
akhir
akhir
lainnya
jika _0x15AA dan _0x15AA.Parent maka
_0x15AA:Destroy()
akhir
jika _0x436D maka
_0x436D:Disconnect()
_0x436D = nil
akhir
akhir
akhir)
akhir
Pemilik lokal Billboard = nil
pemilik lokalConn = nil
fungsi lokal toggleOwnerGeme()
jika ownerBillboard dan ownerBillboard.Parent maka
ownerBillboard:Destroy()
ownerBillboard = nil
jika ownerConn maka
ownerConn:Disconnect()
ownerConn = nil
akhir
lainnya
karakter lokal = pemain.Karakter atau pemain.KarakterDitambahkan:Tunggu()
kepala lokal = karakter:TemukanAnakPertama(string.char(75,101,112,97,108,97)) atau karakter:TungguAnak(string.char(75,101,112,97,108,97), 3)
jika bukan kepala maka kembalikan akhir
ownerBillboard = Instance.new(string.char(66,105,108,108,98,111,97,114,100,71,117,105))
ownerBillboard.Name =string.char(79,119,110,101,114,71,101,109,101,66,105,108,108,98,111,97,114,100)ownerBillboard.Size = UDim2.new(0, 200, 0, 50)
ownerBillboard.StudsOffset = Vector3.new(0, 2.5, 0)
ownerBillboard.AlwaysOnTop = true
ownerBillboard.Parent = head
local _0x7194 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x7194.Size = UDim2.new(1, 0, 1, 0)
_0x7194.BackgroundTransparency = 1
_0x7194.Text =string.char(91,80,69,77,73,76,73,75,93)pemilikTeks.TeksWarna3 = Warna3.dariRGB(255, 0, 0)
_0x7194.TextSize = 26
_0x7194.Font = Enum.Font.GothamBlack
_0x7194.TextXAlignment = Enum.TextXAlignment.Center
_0x7194.TextYAlignment = Enum.TextYAlignment.Center
_0x7194.Parent = ownerBillboard
strokeBlack lokal = Instance.new(string.char(85,73,83,116,114,111,107,101))
strokeBlack.Thickness = 3.5
strokeBlack.Color = Color3.fromRGB(0, 0, 0)
strokeBlack.Parent = _0x7194
gradien lokal = Instance.new(string.char(85,73,71,114,97,100,105,101,110,116))
gradient.Color = ColorSequence.new({
ColorSequenceKeypoint.new(0.0, Color3.fromRGB(255, 0, 0)),
ColorSequenceKeypoint.new(0.4, Color3.fromRGB(255, 120, 120)),
ColorSequenceKeypoint.new(0.5, Color3.fromRGB(255, 255, 255)),
ColorSequenceKeypoint.new(0.6, Color3.fromRGB(255, 120, 120)),
ColorSequenceKeypoint.new(1.0, Color3.fromRGB(255, 0, 0))
})
gradient.Transparency = NumberSequence.new(0)
gradient.Rotation = 25
gradient.Parent = _0x7194
ownerConn = RunService.RenderStepped:Connect(function()
jika _0x7194 bukan atau _0x7194.Parent bukan maka
jika ownerConn maka ownerConn:Disconnect() end
kembali
akhir
gradient.Offset = Vector2.new((tick() * 1.5) % 3 - 1.5, 0)
akhir)
akhir
akhir
local _0xED4B = nil
fungsi lokal showCustomBanner()
jika _0xED4B dan _0xED4B.Parent maka
_0xED4B:Destroy()
akhir
local _0xC0FA = Instance.new(string.char(70,114,97,109,101))
_0xC0FA.Name =string.char(67,117,115,116,111,109,66,97,110,110,101,114,67,111,110,116,97,105,110,101,114)_0xC0FA.Size = UDim2.new(0, 185, 0, 75)
_0xC0FA.Position = UDim2.new(0, 10, 1, -115)
_0xC0FA.BackgroundTransparency = 1
_0xC0FA.Parent = _0x1E0D
_0xED4B = _0xC0FA
bannerImage lokal = Instance.new(string.char(73,109,97,103,101,66,117,116,116,111,110))
bannerImage.Name =string.char(67,117,115,116,111,109,66,97,110,110,101,114,73,109,97,103,101)bannerImage.Size = UDim2.new(1, 0, 1, 0)
bannerImage.BackgroundTransparency = 1
bannerImage.Image =string.char(114,98,120,97,115,115,101,116,105,100,58,47,47,49,48,48,52,50,48,48,51,49,56,51,57,56,53,48)bannerImage.ScaleType = Enum.ScaleType.Fit
bannerImage.Parent = _0xC0FA
bannerImage.MouseButton1Click:Connect(function()
akhir)
akhir
local function _0x8477(inputText)
local _0x9D6A = Instance.new(string.char(70,114,97,109,101))
_0x9D6A.Name =string.char(70,117,108,108,115,99,114,101,101,110,66,108,97,99,107,111,117,116)_0x9D6A.Size = UDim2.new(2, 0, 2, 0)
_0x9D6A.Position = UDim2.new(-0.5, 0, -0.5, 0)
_0x9D6A.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
_0x9D6A.BackgroundTransparency = 1
_0x9D6A.BorderSizePixel = 0
_0x9D6A.ZIndex = 999999
_0x9D6A.Parent = _0x1E0D
local _0x4531 = Instance.new(string.char(84,101,120,116,76,97,98,101,108))
_0x4531.Name =string.char(67,101,110,116,101,114,84,101,120,116)_0x4531.Size = UDim2.new(0.9, 0, 0, 350)
_0x4531.Position = UDim2.new(0.5, 0, 0.35, 0)
_0x4531.AnchorPoint = Vector2.new(0.5, 0.5)
_0x4531.BackgroundTransparency = 1
_0x4531.Text =""_0x4531.TextColor3 = Color3.fromRGB(255, 0, 0)
_0x4531.TextSize = 70
_0x4531.FontFace = Font.new(string.char(114,98,120,97,115,115,101,116,58,47,47,102,111,110,116,115,47,102,97,109,105,108,105,101,115,47,71,111,116,104,97,109,83,83,109,46,106,115,111,110), Enum.FontWeight.Heavy, Enum.FontStyle.Italic)
_0x4531.TextWrapped = true
_0x4531.TextXAlignment = Enum.TextXAlignment.Center
_0x4531.TextYAlignment = Enum.TextYAlignment.Center
_0x4531.ZIndex = 1000000
_0x4531.Parent = _0x9D6A
strokeWhite lokal = Instance.new(string.char(85,73,83,116,114,111,107,101))
strokeWhite.Thickness = 8
strokeWhite.Color = Color3.fromRGB(255, 255, 255)
strokeWhite.Parent = _0x4531
strokeBlack lokal = Instance.new(string.char(85,73,83,116,114,111,107,101))
strokeBlack.Thickness = 11
strokeBlack.Color = Color3.fromRGB(0, 0, 0)
strokeBlack.Parent = _0x4531
lokal glowGradient = Instance.new(string.char(85,73,71,114,97,100,105,101,110,116))
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
glowGradient.Parent = _0x4531
local _0xB797 = TweenService:Create(_0x9D6A, TweenInfo.new(0.4, Enum.EasingStyle.Quad, Enum.EasingDirection.Out), {BackgroundTransparency = 0})
_0xB797:Play()
_0xB797.Completed:Connect(function())
task.spawn(function())
untuk i = 1, string.len(inputText) lakukan
jika _0x4531 tidak ada atau _0x4531.Parent tidak ada maka kembalikan akhir
_0x4531.Text = string.sub(inputText, 1, i)
task.wait(0.07)
akhir
task.wait(0.5)
glowGradient.Enabled = true
task.spawn(function())
koneksi lokal
conn = RunService.RenderStepped:Connect(function()
jika tidak _0x4531 atau tidak _0x4531.Parent atau tidak glowGradient.Enabled maka
jika terhubung maka terhubung:Putuskan sambungan()
kembali
akhir
glowGradient.Offset = Vector2.new((tick() * 0.8) % 2 - 1, 0)
akhir)
akhir)
akhir)
akhir)
task.delay(6, function())
jika _0x9D6A dan _0x9D6A.Parent maka
local _0x0A4B = TweenService:Create(_0x9D6A, TweenInfo.new(0.5, Enum.EasingStyle.Quad, Enum.EasingDirection.In), {BackgroundTransparency = 1})
_0x0A4B:Play()
_0x0A4B.Completed:Connect(function())
_0x9D6A:Destroy()
akhir)
akhir
akhir)
akhir
_0x74F7.MouseButton1Click:Connect(function()
playCustomSound()
teks lokal = textBox.Teks
jika teks ==""maka teks =string.char(115,101,109,101,110,116,97,114,97,32,105,116,117,32,98,101,114,115,105,97,112,108,97,104,32,117,110,116,117,107,32,98,101,98,101,114,97,112,97,32,116,101,108,117,114)akhir
spawnNotificationRow(player.DisplayName, text, true, nil, false)
textBox.Text =""akhir)
_0x6420.MouseButton1Click:Connect(function()
playCustomSound()
teks lokal = _0x68E7.Text
Jika teks ==""maka teks =string.char(80,69,78,71,85,77,85,77,65,78,32,83,69,82,86,69,82,32,85,84,65,77,65,33)_0x8477(text)
_0x68E7.Text =""akhir)
_0x61B4.MouseButton1Click:Connect(function()
playCustomSound()
teks lokal = _0x477A.Text
jika teks ==""maka teks =string.char(76,105,112,122,121,32,72,117,98)selesai
_0xC9CE(teks)
_0x477A.Text =""akhir)
_0x5E44.MouseButton1Click:Connect(function()
playCustomSound()
spawnNotificationRow(string.char(65,68,77,73,78),string.char(65,80,65,75,65,72,32,65,78,68,65,32,77,69,78,71,73,78,71,73,78,75,65,78,32,75,69,77,69,78,65,78,71,65,78,32,65,84,65,83,32,80,69,78,89,65,76,65,72,71,85,78,65,65,78,32,65,68,77,73,78,63), false, nil, true)
akhir)
_0x84E3.MouseButton1Click:Connect(function()
playCustomSound()
showLuckEggsBanner()
akhir)
_0xD9F6.MouseButton1Click:Connect(function()
playCustomSound()
toggleOwnerGeme()
akhir)
_0x19E8.MouseButton1Click:Connect(function()
playCustomSound()
showCustomBanner()
akhir)
_0xA8DE.MouseButton1Click:Connect(function()
spawnUnicornNotification()
akhir)
_0xC8D8.MouseButton1Click:Connect(function()
spawnKitsuneNotification()
akhir)
_0x7866.MouseButton1Click:Connect(function()
spawnNigflameNotification()
akhir)
_0x427A.MouseButton1Click:Connect(function()
spawnArchangelNotification()
akhir)
_0x8E36.MouseButton1Click:Connect(function()
spawnSkyywhaleNotification()
akhir)
_0x15ED.MouseButton1Click:Connect(function()
spawnWorldBurnerNotification()
akhir)
_0xDE09.MouseButton1Click:Connect(function()
playCustomSound()
toggleChaosOfTheSky()
akhir)
_0xDA57.MouseButton1Click:Connect(function()
playCustomSound()
togglePlayerStatusPanel()
akhir)
_0x9006.MouseButton1Click:Connect(function()
playCustomSound()
toggleEggPredictionPanel()
akhir)
