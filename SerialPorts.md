# Les ports série de l'e-puck2

Basé sur le wiki [Communicating with the EPuck2](https://github.com/EPFL-MICRO-315/TPs-Wiki/wiki/EPuck2-Communicating-with-the-EPuck2), la connexion de l'e-puck2 sur un ordinateur permet de voir jusqu'à 3 ports série dits virtuels (car passant sous forme de protocole série simulé via l'usb).

La connexion d'un e-puck2 **éteint** sur un ordinateur fera que seul une partie du robot sera sous tension, à savoir grossomodo le programmateur (STF32F413), le chargeur et le hub USB. Le microcontrôleur principal STM32F407 ne sera pas mis sous-tension sans une des 2 actions suivantes le permettant, à savoir :

1. Presser sur le bouton (bleu) `ON`
2. En démarrant un cycle de programmation/debug depuis VSCode

Pour plus de détails, consultez [EPuck2's Power on/off](https://github.com/EPFL-MICRO-315/TPs-Wiki/wiki/EPuck2-Presenting-the-EPuck2#-epuck2s-power-onoff)

Il y a d'autres moyens de faire cela (utilisation directe du client arm-none-eabi-gdb), mais cela sort du contexte de notre cours.

Ce qu'il faut retenir c'est que le robot **éteint**, seul l'usb du programmateur est visible à l'ordinateur et par conséquent seul les 2 ports série virtuels de ce programmateur seront énumérés.

Le problème avec les différents OS de nos ordinateurs est que ces énumérations ne seront pas vues de la même manière et le but de la vidéo est justement de vous montrer ces différences et vous aider à utiliser les ports à bon escient

1. La gestion de l'alimentation du robot, via sa sortie `PWR_ON`. Comme mentionné lors de l'introdution au TPIntro (lecture des schémas), le fait de presser sur ce bouton cela met sous tension juste le programmateur et le hub usb, tout comme u
2. Le firmware du programmateur est constir^tué de plusieurs partie, dont celle de gérer  

3. En utiliVia une commande envoyée à GDBServer demandant de programmer le F407, ce qui est fait lorsque vous essayer de pragrammer 
3. Vi 