local L = game:GetService("Lighting")
local B = "https://githubusercontent.com"
writefile("fb.png", game:HttpGet(B.."front_back.png"))
writefile("lr.png", game:HttpGet(B.."left_right.png"))
writefile("ud.png", game:HttpGet(B.."up_down.png"))
for _, v in ipairs(L:GetChildren()) do if v:IsA("Sky") or v:IsA("Clouds") then v:Destroy() end end
local s = Instance.new("Sky", L)
s.SkyboxFt, s.SkyboxBk = getcustomasset("fb.png"), getcustomasset("fb.png")
s.SkyboxLf, s.SkyboxRt = getcustomasset("lr.png"), getcustomasset("lr.png")
s.SkyboxUp, s.SkyboxDn = getcustomasset("ud.png"), getcustomasset("ud.png")
s.CelestialBodiesShown = false
