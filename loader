local function notify(title, text)
    pcall(function()
        game.StarterGui:SetCore("SendNotification", {
            Title = title,
            Text = text,
            Duration = 5
        })
    end)
end

local scripts = {
    [116495829188952] = "https://pastefy.app/UjmPtwcn/raw",      -- Dead Rails
    [1240123653] = "https://pastefy.app/4InnpfNE/raw",           -- Zombie Attack
    [3956818381] = "https://pastefy.app/O1JYZDub/raw",           -- Ninja Legends
    [3101667897] = "https://pastefy.app/PQyKUjYY/raw"            -- Legends Of Speed
}

local scriptURL = scripts[game.PlaceId]

if scriptURL then
    notify("Loader", "Script found! Loading...")
    local success, result = pcall(function()
        loadstring(game:HttpGet(scriptURL))()
    end)
    if success then
        notify("Loader", "Script loaded successfully!")
    else
        notify("Error", "Failed to execute the script.")
        warn(result)
    end
else
    notify("Loader", "script dont support")
    wait(2)
    game.Players.LocalPlayer:Kick("game not support")
end
