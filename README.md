# Spawn_skript
A simple and functional Spawn Skript 
-------------------------------------------------------------------------------------------------------------------------------------------
command /setspawn:
    permission: op
    trigger:
        set {spawn} to location of block at location of player
        send "&aSet spawn to: &e%{spawn}%" to player

command /spawn:
    trigger:
        send "&B&lTeleporting to spawn in 5 seconds..." to player
        loop 5 times:
            send actionbar "&6Teleporting in %loop-number% seconds!" to player
            wait 1 second
        wait 1 second
        teleport player to {spawn}
        send "&6Teleporting to spawn!" to player
