# By cheaters, bye cheaters.
Plasma Anticheat is developed by exploiters to stop exploiters, you can rest assured your game will be secured from most basic exploits
# Exploiter Tested
We've had multiple exploiters test the anticheat, and we have fixed any bypass they've found.Every exploiter who tested has approved this anticheat to be good.
# Unbiased.
Plasma Anticheat will never have favoritism allowing certain scripts or people to avoid detection. Any whitelist is up to the user of Plasma Anticheat.
# Customizable
Customizable settings, like punishment, and whitelisted users
| Settings |
|:---|
|Punishment|
|Grace Period|
|Check Time|
|Immune Players|
| Webhook Notifier |
# Checks
| Server | Client |
|:---|---:|
| Noclip | IY Float |
| Teleport | JumpBoost |
| Speed | Speed |
| Jumpboost | Console Messages |
| Perma-Death | Player Tampering |
| IY Bang | Spin/Fling |
| Slow Fall | Luarmor |
| Velocity | gcinfo |
| | Gravity |
| | Client Anticheat Tampering |

# We can't do it all.
While Plasma does protect you from a lot of attacks that are universal, there are some attacks specific to your game.

# Remote Events
Remote events is how the client sends data to the server. If you have a remote event thst deals damage to another player as so:
```lua
remoteevent:FireServer(Target, Damage)
```
An exploiter can hook this remote, or fire it themselves.<br><br>An exploiter can use:
```lua
for _, plr in pairs (game:GetService("Players"):GetPlayers()) do
    remoteevent:FireServer(plr, math.huge)
end
```
This would kill every player in your game.<br><br>
To prevent this, add checks to see how much damage the player is trying todo, and add checks to see how far the player is from the target to see if thet attack was even possible.<br>
<br>
Dont use a remote event to set players immune from Plasma Anticheat, an exploiter could just fire this remote to give themselves immunity.



# Cooldowns, client VS server.
If you have an attack remote thet has a cooldown, an exploiter can just spam the remote to bypass the cooldown if you're handling it in a client script.<br><br>
Handle cooldowns in the serverscript where the remote is to precent this
