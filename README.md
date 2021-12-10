# DansLesEntraillesDeLinux_Session1
Session d'étude et de recherche dans les entrailles de linux (decembre 2021)

Cela sera filmé en camera et si je foire pas et que j'oublie pas alors ce sera sur toutube !!!

Cette note est un condensat de test et petits réglages expérimentaux que je realise et qui pique ma curiosité.....

### Donc le README c'est l'apéro avant d'autres trouvailles...


# La fameuse regle des ports privilegier et restreints jusqua 1024...

_Bha la vous pouvez tout simplement l'anéhentir ou meme la changer, l'augmenter..._

*But login in root is just the requirement !*

***PERMETTRE L'ECOUTE DES PORTS PRIVILEGIES SANS ETRE ROOT ENSUITE***
```
echo 1 > /proc/sys/net/ipv4/ip_unprivileged_port_start
```

***EXEMPLE D'USAGE SANS EN DIRE PLUS...*** 🏴‍☠️
```
netcat -nlvp 80 > donnees_de_la_victime.tar.gz
```
je rigole okay on se calme 🛐

***RETABLIR A LA NORMALE***
```
echo 1024 > /proc/sys/net/ipv4/ip_unprivileged_port_start
```

***ETENDRE A PLUS QUE LA NORMALE.... POURQUOI ET LES RESULTATS ??? ⚗️***
```
echo 2048 > /proc/sys/net/ipv4/ip_unprivileged_port_start
```





PS: IL Y AURA UNE TRADUCTION EN ANGLAIS AUSSI
