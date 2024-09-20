# <span style="color: #18D5E2">Fiche de cour n°1 et commandes de bases du terminal</span>

**Nom de la promo :** _Skaven_

**Nbr de participants :** _19_

**Réferent promo :** _Fabien Tavernier_

**CPA (conséillé parcour aprenant) :** _Jeanne_

**SAV (Probléme technique) :** _Canal slack#sav_

## <span style="color: #92B">Organisation :</span>

- Pointage tous les jours <span style="color: #26B260">midi</span> et <span style="color: #26B260"> soir </span>
- <span style="color: #26B260">**Vendredi**</span> : sans formateur, quizz, activitées, cours d'anglais, évaluations, opquast certification etc ...
- Les travaux de la formation se dérouleront dans : ..cd/var/www/html

## <span style="color: #92B">Commandes de base du terminal :</span>

|commande|utilité|note|
|---|---|---|
|sudo |Super User DO|pour lancer des cmd en tant que super utilisateur
|sudo apt update|verifie les maj dispo| apt = gestionnaire de paquet|
|sudo apt upgrade|execute les maj dispo|apt = gestionnaire de paquet|
|sudo apt install google-chrome-stable|installe la derniere maj de chrome stable|
|sudo apt install code|installe la derniere version de "code"|
|pwd|affiche le chemin du dossier actuel|
|cd|sert à se déplacer vers le dossier ciblé| ex : cd ../home/student
|ls |liste le contenu du dossier actuel
|mkdir|créer un dossier|
|rmdir|supprimer un dossier|
|touch|créer un fichier| on peut creer un fichier avec un .txt ou .rm par exemple
|rm |supprimer un fichier|
|ls .la|affiche la liste avec les fichier caché|
|rm .fr ._nom_|supprime tous les fichiers et dossier present dans ce dossier|
|rm .ri|demande la confirmation aveant de supprimer tous les fichiers et dossier present dans ce dossier
|cp|sert à copier un fichier|ex : cp jeu-carre.txt catakt/ va copier le fichier jeu-carre.txt dans le dossier catakt
|nano|éditeur de texte qui ouvre le fichier donné|
|cat|affiche le contenu du fichier|
|clear|supprime les lignes actuellement affichées|
|code . |ouvre les fichiers dans VSC|
|mv|si le dossier de sdestination exist ca va déplacer, si le dossier de destination n'existe pas ca va renommer| ex: mv secret.key /inventaire/
|man |affiche le manuel|ex : man ls|
|ls --help|ouvre l'aide|
|ls -Sl|trouve le fichier le plus volumineux|
|find . -name poulette.txt|trouver un fichier particulier|en loqurence poulette.txt|
|.|c'est le dossier courant (actuel)|
|..|c'est le dossier parent (1 cran au dessus)|
|~|c'est le dossier utilisateur|
|/|c'est la racine du systeme de fichier|

## <span style="color: #92B">Commande Git & GitHub :</span>

|commande|utilité|note|
|---|---|---|
|git config --global user.nam**_e_** ""nom.prenom"|   |
|git config --global user.email "adressemail"
|git config --global core.editor code
|git config --global color.ui true
|git add . |
|git commit -m "nomdufichier"|
|git push|envoyer sur le serveur les modifications

## <span style="color: #92B">Projet :</span>

au début du projet, dans le dossier utilisé, faire les commandes :

- git init
- ls -la (pour verifier la création du repertoire)
- **les 3 actions suivantes sont à faire pour chaque maj (nouveau commit)**
- git add . (tous le repertoire sera envoyé à Git)
- git commit -m "nomdecommit"
- git push git@github.com:Matt7474/Test-perso.git (prendre adresse sur son github en ssh)


## <span style="color: #92B">Création de la clé SSH :</span>

Les étapes de la création de la clé SSH (à refaire en cas de cahngement de machine virtuel ou physique) :

1. ssh-keygen -t ed25519 -C "adressemailgithub"
     - -> entrée -> entrée -> entrée (pas de passphrase)
2. afficher sa clé avec :
     - cat ~/.ssh/id_ed25519.pub
3. copier la clés
     - github.com/settings/ssh/new
       - add new key, puis coller la clé
4. pour lance de maniere sécurisé la clé
     - eval "$(ssh-agent -s)"
  