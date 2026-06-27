local border = 0
local side = 0
local max = 24

print("Type your message down below")
local word = io.read()

local length = string.len(word) + 4
if length > max then
    word = string.sub(word, 1, max - 3).. ".."
    length = string.len(word) + 4
end

print("Choose perference")
local perference = io.read()

if perference == "*" then
    perference = true
end
if perference == "#" then
    perference = false
end


if perference == true then
    border = string.rep("*", length)
    side = string.rep("*", 2)
    
end
if perference == false then
    border = string.rep ("#", length)
    side = string.rep("#", 2)
end


print(border)
print(side..word..side)
print(border)
