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

## Polices et textes

line-height = Hauteur de ligne

```css
/* La valeur de color est en hexadécimal #FFFFFF (~Blanc) et
     font-size permet de déterminer la taille de la police dans ce cas 14 pixels */
p {
    color : #FFFFFF;
    font-size : 14px;
    /* Le grasage utiliser */
    font-weight: bold;
    /* Le style de la police */
    font-style: italic;
    /* Espace entre les lettres*/
    letter-spacing: 0.2px;
     /* La police à utiliser, toujours mettre à la fin soit sans-serif ou serif */
    font-family: "Source Sans Pro" ,sans-serif;
    /* text-align sert a aligné un texte */
    text-align: justify;
    /* Aligne la dernière ligne d'un texte */
    text-align-last: right;
    /* Pour "casser" le texte */
    overflow-wrap: break-word;
    /* Avec plus de controle pour casser un texte */
    word-break: break-word;
    /* Casse le texte met rajoute une césure avec un tiret "-" */
    hyphens: auto;

    /* Sert à indenter un text */
    text-indent: 100px;
    
    /* Dans ce cas text-transform met le texte en majuscule */
    text-transform : uppercase;
}

/* Applique se style à la première lettre du premier paragraphe */
p:first-of-type::first-letter {
    font-weight: bold;
    font-size: 100px;
}

/* text-decoration */

.header-nav a {
    padding:  0 10px;
    color: inherit;
    text-decoration: none;
}

.header-nav a:hover {
    text-decoration: underline;
}

```
Ou pour casser le texte on peut directement le faire en HTML avec :
```html 
&shy; 
```

```html

<p> blablablablablablablablablablab&shy;lablablablablablablablablablablablablablablablablabla </p>

```

## Les formats de couleurs

```css

/* Valeurs avec un mot-clé */
color: currentcolor;

/* Valeurs avec un mot-clé pour une couleur nommée */
color: red;
color: orange;
color: tan;
color: rebeccapurple;

/* Valeurs hexadécimales <hex-color> */
color: #090;
color: #009900;
color: #090a;
color: #009900aa;

/* Valeurs utilisant la fonction <rgb()> */
color: rgb(34, 12, 64, 0.6);
color: rgba(34, 12, 64, 0.6);
color: rgb(34 12 64 / 0.6);
color: rgba(34 12 64 / 0.3);
color: rgb(34 12 64 / 60%);
color: rgba(34.6 12 64 / 30%);

/* Valeurs <hsl()> */
color: hsl(30, 100%, 50%, 0.6);
color: hsla(30, 100%, 50%, 0.6);
color: hsl(30 100% 50% / 0.6);
color: hsla(30 100% 50% / 0.6);
color: hsl(30 100% 50% / 60%);
color: hsla(30.2 100% 50% / 60%);

/* Valeurs globales */
color: inherit;
color: initial;
color: unset;
```