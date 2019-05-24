# MarcEditTask_SUDOC2Alma
Combinaison d'instructions à importer et exécuter dans MarcEdit afin de mettre en forme des notices SUDOC avant de les charger dans Alma

>Avant d'envisager une migration depuis le SUDOC, il est nécessaire :
>  * de vous assurer que votre base locale est correctement synchronisée avec le système universitaire de documentation
>  * que les identifiants systèmes des notices bibliographiques dans votre sigb soient versés dans le SUDOC_
## Présentation
Ces instructions permettent de :
  * Préfixer le PPN de la notice (Champ 001) par (PPN)
  * Déplacer les PPN des zones de liens (Champs 4**) du sous-champ $$0 vers $$1 et préfixer ces derniers par "001(PPN)"
  * Remplacer les caractères de rejets des accents utilisés dans le SUDOC par ceux utilisés dans Alma :
    * \u0098 vers "<<"
    * \u009c vers ">>"

## Comment l'utiliser ?

### Télécharger et installer MarcEdit
https://marcedit.reeset.net/downloads

### Installer les instructions 
1. Télécharger [l'instruction disponible sur ce dépôt ](Sudoc2Alma.txt)
2. Ouvrir l'éditeur de métadonnées (Marc Editor) ![Marc Editor](/img/Capture1.PNG)
3. Aller dans le Menu "Tools" puis sur "Manage Tasks"
4. Dans le Task Manager, dans la colonne de droite "Manage Existing Task",sélectionner l'option "Import Task File"
5. Charger le fichier "Sudoc2Alma.txt" ![Marc Editor](/img/Capture2.PNG)

### Modifier par lot les fichiers SUDOC 
Avant de pouvoir utiliser nos instructions de transformation il est nécessaire de convertir les notices au format propre à MarcEdit (.mrk)
1. Convertir les notices au format mrk
   1. Rassembler les fichiers fournis par l'Abes dans un répertoire unique **En fonction des capacités de votre machine l'opération peut prendre plus ou moins de temps !**
   2. A partir de l'écran d'accueil, aller dans "Tools">"Marc Processing Tools">"Batch Process Records" ![Marc Editor Tools](/img/Capture3.PNG)
   3. Sélectionner le répertoire où sont stockées les notices SUDOC et choisir la fonction "From Marc To Mnemonic" ![Batch Process Records convert to MRK](/img/Capture4.PNG)  
   4. Le système va convertir tous les fichiers .RAW au format .mrk. **En fonction des capacités de votre machine l'opération peut prendre plus ou moins de temps !**
   5. Les notices transformées seront stockées dans le répertoire "processed_files" sous votre répertoire de travail
2. Transformer les notices SUDOC
   1. Rester dans le module "Batch Process Records"
   2. Sélectionner le répertoire "processed_files" où ont été stockées les notices au format .mrk
   3. Sous le menu Task, coché l'option "Load Tasks" puis sélectionner les instructions "Sudoc2Alma.txt" ![Batch Process Records Load Tasks](/img/Capture5.PNG)  
   4. Lancer le traitement. 
   5. Les notices transformées seront stockées sous [votre répertoire de travail]/processed_files/processed_files
3. Convetir les notices du format mrk vers unimarc
   1. Rester dans le module "Batch Process Records"
   2. Sélectionner le répertoire où se trouvent les notices transformées [votre répertoire de travail]/processed_files/processed_files
   3. Sélectionnées la fonction "From Mnemonic to Marc"
   4. Lancer le traitement
   5. C'est prêt !
