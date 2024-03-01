Un exemple d'une page HTML simple qui intègre un script JavaScript pour générer un passcode APRS (Automatic Packet Reporting System) basé sur un indicatif (callsign) saisi par l'utilisateur. 
<br>
Le système APRS est largement utilisé dans la communauté radio amateur pour transmettre des données de télémétrie, de positionnement et d'autres types de données en temps réel.
<br>

Script JavaScript

La fonction aprspass() récupère la valeur de l'indicatif saisie, retire tout suffixe après un tiret (pour ne travailler qu'avec l'indicatif de base), et convertit l'indicatif en majuscules.

Elle initialise une variable hash à 0x73e2 et traite l'indicatif deux caractères à la fois, appliquant un algorithme de hachage simple pour générer un nombre.

Le résultat du hachage est ensuite masqué pour s'assurer qu'il est positif, en appliquant un AND logique avec 0x7fff.

Finalement, le passcode généré est affiché dans l'élément HTML ayant l'identifiant passcodeResult.

Utilisation

L'utilisateur saisit son indicatif dans le champ prévu, clique sur le bouton "Générer Passcode", et le script calcule puis affiche le passcode APRS correspondant. Ce processus permet aux utilisateurs de radio amateur d'obtenir facilement un passcode pour utiliser le réseau APRS.

