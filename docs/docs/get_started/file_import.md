---
sidebar_title: '📁 File import'
sidebar_position: 3
---

# 📁 File import

# Fonctionement général à l'importation

    Transformer le fichier en CSV avec les informations voulu par le type d'activité.
    Puis est envoyé à l'api 

## Les différents état de la données 

### Importation 

    "Non lisible" -> Fichier : état primaire (Fichier FIT)
    "Non lisible" -> Bytes : contenu du fichier
    "Lisible" -> List<Liste<dynamic>> : Type de donnée que FlutterFIt nous donne 
    -> Traitement pour extraire les données qu'on veut 
    "Lisible" -> List<Liste<dynamic>> : Nouvelle liste avec des bonnes données 
    "Lisible" -> String : Transformation en CSV avec un entête 
    "Non lisible" -> Bytes : Transformation pour le transfert vers l'API


### Récupération d'un fichier 

    "Non lisible" -> Bytes : On récupere les bytes de notre fichier par l'API 
    "Lisible " -> List<List<dynamic>> : Conversion des bytes en CSV 
    ***Traitement du CSV***

## Classe importante 

### ManagerFile 

    Classe qui contient toute la logique sur les fichier
    - Conversion 
    - Analyse du FIT 

### Activity Info 

    Classe qui va contenir les infos qu'on va calculer qu'une seule fois 
    - Fonction pour analyser les Liste dynamic pour ressortir les datas
    - Peut s'exporter en json et être aussi importer en json ( Est stocké sur l'api)

### Utile/list_activity_utile 

    Classe qui s'occupe des comportement de la page listActivité 
    - Contient les méthodes qui vont déclancher l'importation et la récupération de fichier 