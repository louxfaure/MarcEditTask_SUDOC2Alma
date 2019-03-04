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
La suite du tutoriel est basé sur une interface en français. Pour modifier la langue 

### Installer les tasks 
