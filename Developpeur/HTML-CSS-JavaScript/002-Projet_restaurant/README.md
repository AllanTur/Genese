# Excercice Grafikart

## Lien :

- [Le site du restaurant le Fiasco](https://allantur.github.io/Genese/Developpeur/HTML-CSS-JavaScript/002-Projet_restaurant/index.html)

## Objectif : Consolider les bases

### Créer un site de restaurant HTML/CSS

### CSS = Cascading Style Sheet = le Style d'une page

## Les Sélecteurs

- [CSS : Les sélecteurs](https://developer.mozilla.org/fr/docs/Web/CSS/Attribute_selectors)
- [CSS : Les Combinateurs](https://developer.mozilla.org/fr/docs/Learn/CSS/Building_blocks/Selectors/Combinators)

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

## Le Modèle de Boite

- [CSS : Le Modèle de Boite](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model)


Le navigateur applique automatique du CSS (sur les balises HTML), même si on utilise que du HTML.

Fusion de marge : Lorsque deux éléments adjacent on des marges, c'est celui qui la marge la plus grande qui l'emporte.

```css
/* Si y'a un autre contenu qui est en display block, le met en dessous */
div {
    display: block;
}

/* Si y'a un autre contenu qui est en display inline, le met juste à ça droite (comme une nav) */
div {
    display: inline;
}

div {
    display: inline-block;
}

/* Exemple de mise en page des block et d'écrasement de style CSS (des style HTML mis de base par le navigateur) */

body {
    margin: 0;
}

.header {
    background: grey;
    padding: 20px;
    height: auto;
}

.header-title {
    margin-top: 0;
}

.header-nav {
    margin: 20px 0;
}

.header-nav a {
    padding:  0 10px;
}

.header img {
    width: 100%;
    height: auto;
}

.main {
    background: lightgray;
    padding: 20px;
}

.footer {
    background: gray;
    padding: 10px 20px;

}
```