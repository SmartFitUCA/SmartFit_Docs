---
sidebar_title: '📈 AI'
sidebar_position: 5
---

# AI 

## Fonctionnement générale 

    Un script va demander tout les jours à l'API (a 8H),les activity info de tous les users qui ont ajouté un fichier.
    Le script va calculer le modele en fonction de ces données 
    - 1 model pour la catégorie d'un utilisateur 
    Renvoie à l'API le model à la fin 
    Puis l'utilisateur pourra juste demander à l'API le modele

### Modèle d'apprentissage 

    On utilise une regresion linéaire multiple de la bibiothèque sklearn 

    En entré on donne : 

    - La date de l'activité 
    - Les données de l'activité 

    En sortie : 

    - Le model (Coef et interception pour chaque donnée)

### Utilisation du model 

    On transforme notre model en json -> coef,intercept 

    On va avoir un coef et une interception pour chaque valeur de l'activité
    (On va juste calculer le Y d'une droit)

    Calcul : 

    - ("Date où on prédit" * "coef de la donnée" ) + "Interception de la donnée" 



