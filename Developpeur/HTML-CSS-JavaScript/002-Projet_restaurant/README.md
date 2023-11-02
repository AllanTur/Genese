# Excercice Grafikart

## Objectif : Consolider les bases

## Lien :

- [Le site du restaurant le Fiasco](https://allantur.github.io/Genese/Developpeur/HTML-CSS-JavaScript/002-Projet_restaurant/index.html)

### Créer un site de restaurant HTML/CSS

### CSS = Cascading Style Sheet = le Style d'une page

Sélecteur -> propriété -> valeur

Exemple :

```css
/* h2 -> Sélecteur, color -> Propriété, red -> Valeur*/
h2 {
  color: red;
}

/* Règle CSS spécifique : Il prend la règle la plus spécifique dans se cas, 
    c'est le h1 spécifier avec la classe "title-big"*/

.title-big {
    color: red;
}

/* Règle CSS : Dans ce cas ci, il prend la dernière règle à appliquer sur tous les h1, 
    càd la couleur blueviolet */

h1 {
    color: green;
    color: blueviolet;
}

/* Combinateur descendant */

table h2 {
    color: red;
}
/* Combinateur Enfant direct */

td > h2 {
    color: aqua;
}

h2 {
    color: green;
}
```
