-- Noobular's Addons
-- Created by : Noobular (Uncle Gremblo)
-- Last Update: 1/25/2018

Thank you for purchasing my Hopper mod, it's my first for sale mod and anything people give me pushes me forward to keep creating, 
even more since this is my first effort at creating for gmod again for years (minus my vehicle mods ;)) 
basically you're feeding me because I never have food so thank you.


INSTRUCTIONS
INSTRUCTIONS
INSTRUCTIONS

place the folder 'na_hopper' into garrysmod/garrysmod/addons/darkrpmodification/lua/entities

You will probably want to edit the config.lua file that's included in that folder, if you have printers with large props you want to increase the collection radius



Add this into darkrpmodification\lua\darkrp_customthings\categories.lua

<code>DarkRP.createCategory{ <br>
    name = "Printer Hoppers", -- The name of the category.<br>
    categorises = "entities", -- What it categorises. MUST be one of "jobs", "entities", "shipments", "weapons", "vehicles", "ammo".<br>
    startExpanded = true, -- Whether the category is expanded when you open the F4 menu.<br>
    color = Color(50, 50, 200, 255), -- The color of the category header.<br>
    canSee = function(ply) return true end, -- OPTIONAL: whether the player can see this category AND EVERYTHING IN IT.<br>
    sortOrder = 50, -- OPTIONAL: With this you can decide where your category is. Low numbers to put it on top, high numbers to put it on the bottom. It's 100 by default.<br>
}</code>





add the code below into darkrpmodification\lua\darkrp_customthings\entities.lua
<code>
DarkRP.createEntity("Printer Hopper", {
    ent = "na_hopper",
    model = "models/props_combine/combine_interface001.mdl",
    price = 5000, -- Change the price
    max = 2,      -- Change the max amount of hoppers (this tier specifically)
    category = "Printer Hoppers",
    sortOrder = 1,
   -- customCheck = function(ply) return ply:GetUserGroup() == "donator" end,
    cmd = "buy_hopper_t1"
})

DarkRP.createEntity("Money Boost Upgrade", {
    ent = "na_upg_money",
    model = "models/props_combine/combinebutton.mdl",
    price = 5000, -- Change the price
    max = 1,      -- Change the max amount of hoppers (this tier specifically)
    category = "Printer Hoppers",
    sortOrder = 50,
    -- customCheck = function(ply) return ply:GetUserGroup() == "donator" end,
    cmd = "buy_hopper_upg_money"
})

DarkRP.createEntity("Experience Boost Upgrade", {
    ent = "na_upg_xp",
    model = "models/props_combine/combine_light002a.mdl",
    price = 5000, -- Change the price
    max = 1,      -- Change the max amount of hoppers (this tier specifically)
    category = "Printer Hoppers",
    sortOrder = 50,
    -- customCheck = function(ply) return ply:GetUserGroup() == "donator" end,
    cmd = "buy_hopper_upg_xp"
})

DarkRP.createEntity("Capacity Boost Upgrade", {
    ent = "na_upg_capacity",
    model = "models/props_combine/combine_emitter01.mdl",
    price = 5000, -- Change the price
    max = 1,      -- Change the max amount of hoppers (this tier specifically)
    category = "Printer Hoppers",
    sortOrder = 50,
    -- customCheck = function(ply) return ply:GetUserGroup() == "donator" end,
    cmd = "buy_hopper_upg_capacity"
})

</code>