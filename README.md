-- Seu script base corrigido para Blox Fruits

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local hrp = character:WaitForChild("HumanoidRootPart")

-- NPC alvo do seu script original
local npcName = "Bandit" -- altere conforme seu script

-- Função de ataque do seu script base
local function attack(npc)
    if npc:FindFirstChild("Humanoid") and npc.Humanoid.Health > 0 then
        -- Aqui você coloca a lógica que já tinha no seu script
        print("Atacando NPC: "..npc.Name)
        -- Exemplo: ataque básico ou habilidade da fruta
    end
end

-- Loop principal de farm
while true do
    local npc = workspace:FindFirstChild(npcName)
    if npc and npc:FindFirstChild("HumanoidRootPart") then
        -- Move até o NPC
        hrp.CFrame = npc.HumanoidRootPart.CFrame + Vector3.new(0,3,0)
        -- Executa ataque do script base
        attack(npc)
    end
    wait(0.5) -- espera entre ataques
end
