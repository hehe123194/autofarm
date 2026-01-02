local player = game.Players.LocalPlayer
local char = player.Character or player.CharacterAdded:Wait()
local hrp = char:WaitForChild("HumanoidRootPart")

for _, prompt in pairs(workspace:GetDescendants()) do
    if prompt:IsA("ProximityPrompt") then
        prompt.HoldDuration = 0
    end
end

while true do
    local postes = workspace:FindFirstChild("Postes")
    if postes then
        for _, poste in pairs(postes:GetChildren()) do
            if poste.Name == "Poste" then
                local estragado = poste:FindFirstChild("Estragado")
                local luz = poste:FindFirstChild("Luz")
                if estragado and luz then
                    hrp.CFrame = luz.CFrame + Vector3.new(0, 3, 0)
                    wait(0.1)
                    
                    for _, prompt in pairs(poste:GetDescendants()) do
                        if prompt:IsA("ProximityPrompt") then
                            fireproximityprompt(prompt)
                        end
                    end

                    wait(0.1)
                end
            end
        end
    else
        warn("")
    end
    wait(0.1)
end# autofarm
