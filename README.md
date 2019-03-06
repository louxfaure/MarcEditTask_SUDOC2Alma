# MarcEditTask_SUDOC2Alma
Combinaison d'instructions à importer et exécuter dans MarcEdit afin de mettre en forme des notices SUDOC avant de les charger dans Alma

## Présentation
Ces instructions permettent de :
  * Préfixer le PPN de la notice (Champ 001) par (PPN)
  * Déplacer les PPN des zones de liens (Champs 4**) du sous-champ $$0 vers $$1 et préfixer ces derniers par "001(PPN)"
  * Remplacer les carctères de rejets des accents utilisés dans le SUDOC par ceux utilisés dans Alma :
    * \u0098 vers	"<<"
    * \u009c vers ">>"

## Comment l'utiliser ?

### Télécharger et installer MarcEdit
https://marcedit.reeset.net/downloads

### Installer les instructions 
1. Télécharger [l'instruction disponible sur ce dépot ](Sudoc2Alma.txt)
2. Ouvrir l'éditeur de métadonnées (Marc Editor) ![Marc Editor](/img/Capture1.PNG)
3. Aller dans le Menu "Tools" puis sur "Manage Tasks"
4. Dans le Task Manager, dans la colonne de droite "Manage Existing Task",sélectionner l'option "Import Task File"
5. Charger le fichier "Sudoc2Alma.txt" ![Marc Editor](/img/Capture2.PNG)

### Modifier par lot les fichiers SUDOC 
Avant de pouvoir utiliser nos instructions de transformation il est nécessaire de les convertir au format propre à MarcEdit (.mrk)
1. Convetir les notices au format mrk
   1. Rassembler les fichiers fournis par l'Abes dans un répertoire unique
   2. A partir de l'écran d'accueil, aller dans "Tools">"Marc Processing Tools">"Batch Process Records" ![Marc Editor Tools](/img/Capture3.PNG)
   3. Sélectionner le répertoire où sont stockées les notices SUDOC et choisir la fonction "From Marc To Mnemonic" [Batch Process Records](/img/Capture4.PNG)  
   4. Le système va convertir tous les fichiers .RAW au format .mrk. **En fonction des capacités de votre machine l'opération peut prendre plus ou moins de temps !**
   5. Les notices 
2. 
