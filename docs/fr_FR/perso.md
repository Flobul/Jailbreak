Commandes perso
==================

Le plugin contient 2 commandes par défaut lors de la création d'un équipement.
Il est possible d'en créer davantage en cliquant sur le bouton "Ajouter une commande perso".

![Logo plugin](../images/jailbreak_screenshot3.png "Commande perso")

La commande perso permet de personnaliser soi-même une information/action en entrant la commande bash/ssh.

**INFORMATION : à partir des scripts existants**
---------------------

Le script current_page.sh :
- donne le nom de la page actuelle ouverte sur l'équipement (springboard/lockscreen/application) dans le cas d'application, le vrai nom de l'éapplication est recherché et affiché.
- commande à saisir dans le champ : *bash jailed/current_page.sh*
- arguments de la commande (ajouter en fin de ligne...) : aucun
- argument optionnel de la commande : *-i* en fin de commande pour rechercher sur iTunes le nom de l'app.

Exemples de commandes et la valeur de la commande sur Jeedom :  
```bash jailed/current_page.sh``` : ```lockscreen``` (l'écran est verrouillé)  
```bash jailed/current_page.sh``` : ```springboard``` (il s'agit de l'écran d'accueil)  
```bash jailed/current_page.sh``` : ```Books``` (il s'agit de l'application Livres)  
```bash jailed/current_page.sh -i``` : ```Livres``` (il s'agit de l'application Livres)  

> **Note**  
> Pour fonctionner, il faut installer le tweak Activator.

Les commandes ssh :
Si vous connaissez une commande permettant d'obtenir une information utile, n'hésitez pas à me le remonter.

Exemple de commandes et la valeur de la commande sur Jeedom :

| Commande | Résultat | Commentaire |
| ------------------------------------------------------------------------------ | ------ | -------------------------- |
| *batterydata \| grep "BatteryHealth :" \| cut -d: -f2 \| sed -e 's/\ //'*  | *Good* |**affiche l'état de la batterie**
| *batterydata \| grep "InstantAmperage :" \| cut -d: -f2 \| sed -e 's/\ //'*  | *-82* |**affiche la consommation actuelle de l'appareil (en mA)**
| *batterydata \| grep "Watts =" \| cut -d= -f2 \| sed -e 's/\ //' \| sed -e 's/;//'*  | *10* |**affiche la puissance de l'adaptateur (en Watt)**
| *batterydata \| grep "TimeRemaining :" \| cut -d: -f2 \| sed -e 's/\ //'*  | *0* |**affiche le temps restant avant charge complete (en s)**
| *lightsensor \| grep DayLight \| cut -d= -f2 \| sed -e s/\ //g*  | *1* |**1 = lumière directe reçue**
| *sensors \|  grep "Thermal sensors" \| cut -d':' -f2 \| sed -e s/\(//g \| sed -e s/\)//g*  | *30 thermal sensors found* |**nombre de sondes de température disponibles**
| *sensors \| sed -n '/Thermal sensors/,$p'*  | *=> Thermal sensors (°C): (30 thermal sensors found)</br>-------------------------near WiFi (top side) = 20.363647;</br>...</br>Avg: PMGR SOC Die Temp Sensor0 = 21.890625;* |**affiche toutes les sondes de température disponibles et leur valeur en °C**
| *sensors \|  grep "Avg: PMGR SOC Die Temp Sensor0" \| cut -d'=' -f2 \| sed -e s/\ //g \| sed -e 's/;//g'*  | *21.890625* |**affiche la valeur en °C donnée par une sonde de température**


**ACTION : à partir des scripts existants**
-----------------------
Le script activator_send.sh :
- commande à saisir dans le champ : *bash jailed/activator_send.sh XXX*
- arguments de la commande (remplacer XXX par...) : un des paramètres listés ici *[Paramètres](#tocAnchor-1-13-1)* => *low-power/home/respring/sleep/location/rotation/avion/verrou/modesombre/moinsfort/plusfort/audio 100/lumiere 100/screenshot/photo/pluslumiere/moinslumiere*
- argument optionnel de la commande :  un chiffre de de 1 à 10 (répétition de la commande)


Les commandes manuelles :
- Activator : *activator send* *listeners*
avec *listeners* : une des lignes listées dans le champ texte de Menu Installation > Equipement > Activator Listeners.
Cela permet d'ouvrir toutes les applications disponibles sur l\'équipement ou d'éxecuter des actions (activer darkmode, couper bluetooth, couper wifi...)



