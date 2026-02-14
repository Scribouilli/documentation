---
title: "Aide"
order: 2
in_menu: true
---

## Avoir une adresse personnalisée

On appelle aussi cette adresse personnalisée : **"Nom de domaine"**

<a href="https://scribouilli.org/adressepersonnalisee.html" class="bouton">Découvrir comment avoir mon adresse personnalisée</a>

---
## Ajouter un encart

 <p class="encart">Un incroyable encart !</p>

Il est possible d'ajouter un encart mettant en avant du texte dans votre site : 
1. en  intégrant le code suivant dans votre page et
2. en modifiant le texte entre les balises `<p class="encart">` et `</p>`

```
 <p class="encart">Un incroyable encart !</p>

```

Si vous souhaitez mettre plusieurs paragraphes dans votre encart, vous pouvez utiliser le code suivant et mettre un paragraphe entre `<p>` et `</p>`

```
 <div class="encart">
<p>Le 1er paragraphe ou juste une phrase</p>
<p>Le second paragraphe</p>
</div>
```

---

## Ajouter un bouton

 <a href="#" class="bouton">Mon joli bouton</a>

Il est possible d'ajouter un bouton dans votre site : 
1. en  intégrant le code suivant dans votre page et
2. en modifiant le texte entre les balises `<a href="#" class="bouton">` et `</a>`
3. en remplaçant le `#` par le lien de la page vers laquelle vous souhaitez que votre bouton emmène

```
 <a href="#" class="bouton">Mon joli bouton</a>
```

---

## Restaurer la page Articles

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

