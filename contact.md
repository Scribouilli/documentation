---
title: "Aide et Contact"
order: 4
---

## Nous contacter

Pour nous faire des retours, c'est **coucou@scribouilli.org**

## Aide : Page Articles

Si vous avez cassé votre page Articles en faisant des tests, pas de panique !
Pour revenir à zéro, remplacez le contenu de votre page par le code suivant en le copiant-collant :
```
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
```
