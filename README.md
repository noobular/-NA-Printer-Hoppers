# Noobular's Addons; Printer Hoppers

Thank you for using the mod, if you'd like to support me since this wasn't accepted onto ScriptFodder(Gmodstore), you can send me dollas at paypal.me/noobular

## Instructions

 Drag the addon folder onto your addons folder and let it merge everything.

### Edit the config!



### Add this into darkrpmodification\lua\darkrp_customthings\categories.lua


    DarkRP.createCategory{ 
        name = "Printer Hoppers", -- The name of the category.<br>
        categorises = "entities", -- What it categorises. MUST be one of "jobs", "entities", "shipments", "weapons", "vehicles", "ammo".
        startExpanded = true, -- Whether the category is expanded when you open the F4 menu.<br>
        color = Color(50, 50, 200, 255), -- The color of the category header.<br>
        canSee = function(ply) return true end, -- OPTIONAL: whether the player can see this category AND EVERYTHING IN IT.
        sortOrder = 50, -- OPTIONAL: With this you can decide where your category is. Low numbers to put it on top, high numbers to put it on the bottom. It's 100 by default.
    }


### Add the code below into darkrpmodification\lua\darkrp_customthings\entities.lua

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
