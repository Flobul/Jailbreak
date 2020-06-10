Changelog
=========

Liste des versions du plugin Jailbreak.

Version 1.24 (10/06/2020) beta
-------------------------
- Ajout d'une application supplémentaire prise en charge pour la commande Caméra,
- désormais, gestion manuelle de l'application Caméra via menu déroulant (sauvegarder après modification)

Version 1.23 (06/06/2020) beta
-------------------------
* Ajout de l’image de l’appareil sur la page équipement,
* récupération des infos non importantes 1 fois par jour au lieu de toutes les 5 min, (allégement des requêtes),
* ajout d’une commande action avec menu déroulant, listant les App de l’appareil, pouvant ensuite être lancées,
* nouvelle gestion des commandes crées => faites Sauvegarder sur chaque équipement.
* corrections mineures et allègement de code.

Version 1.22 (24/05/2020)
-------------------------
* Ajout d’une commande info "Voix" qui liste les voix disponibles pour pouvoir les utiliser dans la commande say ensuite (-v Thomas),
* ajout de 2 actions messages "Notification" et "Bulletin". Pour envoyer une alerte/notification/bulletin sur son appareil,
* amélioration mineure des log debug.

Version 1.21 (19/05/2020)
-------------------------
* Retrait du volet SMS sur le Dashboard pour les iPad/iWatch... (l’outil smsme ne fonctionne que pour les iPhone),
* correction mineure de cloture de connexion ssh,
* ajout de la commande Photo : pour prendre une photo et l'envoyer via les plugins Telegram ou Mail.

Version 1.20 (10/05/2020)
-------------------------
* inclusion des coordonnées GPS dans une commande de base,
* création d’un outil maison pour envoyer des SMS, (ne fonctionne qu’avec des iPhone ayant une carte SIM fonctionnelle),
* inclusion de sa commande,
* corrections mineures.

Version 1.19 (06/05/2020)
-------------------------
* Ajout de boutons pour lancer manuellement les scripts de màj et update de commandes,
* gestion des cron de màj depuis le menu Installation,
* correction de bugs et amélioration.

Version 1.18 (05/05/2020)
-------------------------
* Correction de bugs et amélioration.

Version 1.17 (26/04/2020)
-------------------------
* Correction script dépendances,
* màj paquet say pour corriger les diacritiques (accents),
* ajout de l'historique dashboard pour uptime/luminosité,
* ajout scripts pour indiquer la page courante (activator nécessaire).

Version 1.16 (24/04/2020)
-------------------------
* Création d'une commande pour afficher la luminosité : affiche sur le dashboard le pourcentage de luminosité reçu par le capteur de l’équipement. (ratio en % = valeur mesurée / valeur max possible(lumière soleil direct)).
* Installation d'un tweak maison : say (Text To Speech)
* Création d'une commande Text To Speech : faites parler votre équipement en écrivant des mots doux depuis le dashboard. La commande action(message) peut être utilisée depuis la commande script/scenario/autre plugin… pour lire au haute voix les messages, la météo…
* API du plugin créée : possibilité d’envoyer des valeurs de commandes info à Jeedom ou récupérer la leur depuis ce lien @IP_jeedom/core/api/jeeApi.php?plugin=Jailbreak&apikey=#api_key#&type=cmd&id=#cmd_id#&value=#value#
(première étape pour mise en place de cron sur les équipements)

Version 1.15 (22/04/2020)
-------------------------
* Correction et amélioration script dépendances
* Correction bugs dashboard

Version 1.14 (14/04/2020)
-------------------------
* Rétablissement de méthode de récupération des information pour compatibilité globale
* Correction et amélioration script dépendances

Version 1.13 (13/04/2020)
-------------------------
* Nouvelle gestion du paquet batterydata qui remonte les infos de batterie.
* Installation de 2 tweak maison (il faut 'envoyer les dépendances' puis 'lancer les dépendances')
    lightsensor : (capteur de luminosité de l’appareil) => il faut l’écran allumé par contre pour que ça marche.
    sensors : (remonte toutes les infos des capteurs de tensions/courant/température : plus de 20 par appareil).
* Modification de la 'Présence des commandes' dans 'Test/Compatibilité''.
* Séparation des commandes de base des commandes perso dans 2 tab différents.

Version 1.12 (07/04/2020)
-------------------------
* Ajout 1 commande perso + 2 info perso
* Allègement des commandes envoyées sur les équipements (économie batterie)
* Correction bug page Santé
* Correction date de dernière communication

Version 1.11 (22/03/2020)
-------------------------
* Correction lastupdate page Installation
* Ajout tab Test dans Installation (test de tweaks et processus actifs...)
* Ajout d'une commande d'info Batterie/Secteur

Version 1.10 (03/03/2020)
-------------------------
* Action commande perso
* Correction commandes action
* Ajout compatibilité multiple modèle iPad/iPhone
* Ajout d'un script activator_send.sh pour envoyer des commandes personnalisées (low-energy, respring, veille, mode avion...)
* Ajout de la documentation pour l'utilisation de la commande perso (notifications, photo, page safari, caméra, **Raccourcis**)

Version 1.03 (26/02/2020)
-------------------------
* Masquage d'îcone si connexion KO
* Corrections mineures

Version 1.02 (25/02/2020)
-------------------------
* Ajout du modèle de l'appareil et sa version iOS
* Corrections mineures

Version 1.01 (24/02/2020)
-------------------------
* Correction de la valeur affichée de Cycle si valeur vide
* Correction des boutons reboot et shutdown
* Suppression de code inutile

Version 1.0 (10/02/2020)
-------------------------
* Gestion des iDevices : envoi de script, execution et récupération de log
* Ajout page Santé et Installation
* Libération de code

Version 0.8 (02/02/2020)
-------------------------
* Ajout intégration de plusieurs modèles d'iPad

Version 0.7 (24/01/2020)
-------------------------

*[Retour à la documentation](index.md)*
