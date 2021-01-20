# Les boîtes

Il existe deux principaux type de boite :

## Les "block"

Un block :

- prend toutes la largeur disponible
- Commence sur une nouvelle ligne
- Ce qui vient après sera sur une nouvelle ligne

## Les "inline"

Un inline :

- adaptera sa taille à son contenu (au besoin en allant à ligne).
- commence sur la même ligne que ce qui le précède
- ce qui vient après sera aussi sur la même ligne

## En CSS

On peut modifier le type de boite d'une balise en utilisant la propriété `display` :

```css
img {
    /*
     * Par défaut les images sont de type inline donc si l'on à du texte qui vient
     * dessuite après une image il sera sur la même ligne que celui ci.
     */
    display: block;
}
```

En fonction du type de boite on peut agir sur différente propriété :

## Les dimensions

Les propriétés `width` et `height` servent à définir les dimensions des boites de type **block** elles n'on aucun effet sur les balises inline.

Même si deux balises block aurait la place de se mettre cote à cote grace à leur width elle ne le feront pas.

## Les marges

Pour "aérer" nos intégration on peu jouer sur les mages de nos boites.

On peut modifier séparément les marge **interne** et **externe**.

Pour les première on touchera à la propriété `padding` et pour les secondes la propriété `margin`.


```css
h1 {
    /*
     * Que ce soit pour le padding ou le margin
     * on peut définir une valeur pour les 4 coté à la fois
     * ou une valeur spécifique pour 1 coté (avec padding-bottom par ex)
     * il existe un raccourcie pour définir le padding horizontal et vertical en une seule propriété :
     */
     padding: 15px 64px;
     /* Ici la boite aura une marge interne verticale de 15px et horizontale de 64px */
}
```

Pour les block les marge horizontale peuvent prendre une valeur spéciale : `auto`.

Pour ça il faut que l'élément ai une width de définit et dans ce cas le navigateur répartira de même la marge à droite et à gauche de notre block de manière à le centrer.

## <div> et <span>

Il arrive qu'on ai besoin de rajouter des balises pour une meilleure mise en forme.

Pour le ça le HTML fourni deux balise :

- `<div>` qui a juste le statut de block
- `<span>` qui a juste le statut de inline
