local tool = Instance.new("Tool",game.Players.LocalPlayer.Backpack)

tool.RequiresHandle = false

local humanoid = game.Players.LocalPlayer.Character:WaitForChild("Humanoid")

local anim = Instance.new("Animation",game.Players.LocalPlayer.Character.Torso)

anim.AnimationId = "rbxassetid://35654637"

local playback = humanoid:LoadAnimation(anim)

playback.Looped = false	

tool.Activated:Connect(function()
   if playback.IsPlaying == false then
      playback:Play()
      local sound = Instance.new("Sound",game.Players.LocalPlayer.Character.Torso)
      sound.SoundId = "rbxassetid://35930009"
      sound:Play()
   end
end)

