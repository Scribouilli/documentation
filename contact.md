---
title: "Aide et Contact"
order: 4
---

## Nous contacter

Pour nous faire des retours, c'est **coucou@scribouilli.org**

## Aide : Gitlab, publier votre site

Nous avons réalisé que par défaut, Gitlab cache votre site aux personnes qui n'ont pas de compte chez eux.

Pour rendre votre site public, voici la marche à suivre : 

1. Allez sur [https://atelier.scribouilli.org/](https://atelier.scribouilli.org/)
2. Cliquez sur le lien **“Sur gitlab.com”** en haut à droite de l’écran
3. Dans la barre latérale de gauche, allez dans **"Paramètres"** puis **"Général"**
4. Dépliez la section **"Visibilité, fonctionnalités du projet, autorisations"**
5. Descendez jusqu'à la section **"Pages"** et sélectionnez **"Toute personne ayant accès"**
6. Descendez jusqu'au bouton et cliquez sur **"Enregistrer les modifications"**

Votre site devrait maintenant être accessible à tous·tes.

## Aide : Page Articles

Si vous avez cassé votre page Articles en faisant des tests, pas de panique !
Pour revenir à zéro, remplacez le contenu de votre page par le code suivant en le copiant-collant :

```
{% raw %}
<aside>
  S'abonner via le <a href="{{ '/feed.xml' | relative_url }}">flux RSS</a>
  (<a href="https://flus.fr/carnet/a-quoi-servent-les-flux.html">c'est quoi ?</a>)
</aside>

{% for post in site.posts %}
<article class="blog-item">
  <h2>
    <a href="{{post.url | relative_url}}"> {{ post.title }} </a>
  </h2>

  <a href="{{post.url | relative_url}}"> Lire l'article ➞ </a>
</article>
<hr />
{% endfor %}
{% endraw %}
```
