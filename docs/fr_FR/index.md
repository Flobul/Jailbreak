Plugin Jailbreak
=============

![Logo plugin](../assets/images/Jailbreak_icon.png "Logo plugin")

Plugin pour récépérer les informations et commander les équipements Apple.

> **Note**  
> Pour fonctionner, il faut installer le tweak OpenSSH sur l'appareil.

**Fonctionnalités :**

- Éteindre / redémarrer,
- affichage les informations de l'appareil,
- déverrouiller l'appareil,
- lancer des applications à distance.

**Modèles compatibles**
- iPad / iPhone.

Dashboard
=========

![Visuel du dashboard](../assets/images/Dashboard.png "Visuel du dashboard")

Configuration du plugin
=======================

Après téléchargement du plugin, activer le plugin.

Configuration des équipements
=============================

La configuration des équipements est accessible à partir du menu *Plugins > Monitoring > Jailbreak*.

### Onglet Equipement:

-   **Nom de l'équipement** : nom de votre équipement,
-   **Objet parent** : indique l’objet parent auquel appartient l’équipement,
-   **Catégorie** : les catégories de l’équipement (il peut appartenir à plusieurs catégories),
-   **Activer** : permet de rendre votre équipement actif,
-   **Visible** : rend votre équipement visible sur le dashboard,
-   **Adresse IP** : adresse IP de l'équipement,
-   **Port SSH** : port SSH de l'équipement (installer OpenSSH sur l'équipement),
-   **Identifiant** : identifiant SSH de l'équipement (par défaut : root),
-   **Mot de passe** : mot de passe associé à l'identifiant SSH de l'équipement (par défaut : alpine).

### Onglet Commandes

Les commandes sont générées automatiquement.

### Page Santé

![Page santé](../assets/images/jailbreak_screenshot2.png "Page Santé")

La page Santé est accessible depuis la page de configuration des équipements.
Elle remonte les informations des équipement.

### Page Installation

![Page Installation](../assets/images/jailbreak_screenshot1.png "Page Installation")

La page Installation est accessible depuis la page de configuration des équipements.
Elle permet d'envoyer le fichier d'installation des dépendances des équipements.
C'est-à-dire les Tweaks et paquets dont le plugin a besoin, mais aussi les scripts servant à la commande perso.

### Script commande perso

![Script commande perso](../assets/images/jailbreak_screenshot3.png "Script commande perso")

La commande perso permet de créer soi-même une commande personnalisée.
* Soit en tapant directement la commande complète : *activator send abracadabra*
* Soit en utilisant le script transféré précédemment depuis la page Installation : *bash jailed/activator_send.sh* *<parametre>*
Voici la liste des paramètres :
low-power|power *(bascule le mode d'économie d'énergie)*
homebutton|home *(appuie sur le bouton home)*
respring *(lance un respring)*
sleep|veille *(appuie sur le bouton verrouillage)*
location *(bascule la localisation)*
rotation *(bascule le verrouillage de rotation d'écran)*
airplane-mode|airplane|avion *(bascule le mode avion)*
  
Si votre équipement est verrouillé, pensez à lancer la commande *unlock* avant d'envoyer la commande script perso.
    
### Liste des versions

*[Voir la liste des versions](changelog.md)*
