local function teleportPlayerToMouse()
    local mouse = game.Players.LocalPlayer:GetMouse()
    local targetPosition = mouse.Hit.p
    game.Players.LocalPlayer.Character:SetPrimaryPartCFrame(CFrame.new(targetPosition))
end

local TELEPORT_KEY = Enum.KeyCode.T

game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == TELEPORT_KEY then
        teleportPlayerToMouse()
    end
end)
