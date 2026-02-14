---
title: "Aide"
order: 2
in_menu: true
---

## Avoir une adresse personnalisée

Il y a **3 grandes étapes pour avoir votre site Scribouilli derrière votre adresse personnalisée.**

On appelle cette adresse personnalisée : **"Nom de domaine"**

### Les 3 étapes

- **Acheter votre nom de domaine** (cette page explique comment le faire chez Infomaniak, un chouette fournisseur de nom de domaine)
- **Faire les paramétrages** qui vont bien **chez votre fournisseur de nom de domaine** (ici chez Infomaniak)
- **Faire les paramétrages** qui vont bien chez **Gitlab, ScribouGit**, ou Github

### Étape 1 : Acheter votre nom de domaine chez Infomaniak

1. Rendez-vous sur [Infomaniak.com](https://www.infomaniak.com/fr)
2. Vérifiez **la disponibilité et le prix** du nom de domaine que vous souhaitez (ex&nbsp;:&nbsp;adressedemonsite.fr)
3. Suivez le processus d'achat en décochant toutes les options payantes supplémentaires si il y en a, et créez-vous un compte au passage

Pour info, un nom de domaine en .fr coûte moins de 8€/an chez Infomaniak.

### Étape 2-Gitlab/ScribouGit : Paramétrer du coté de ScribouGit et Gitlab Pages

1. Allez sur [https://atelier.scribouilli.org/](https://atelier.scribouilli.org/)
2. Cliquez sur le lien **"Sur git.scribouilli.org"** ou **"Sur gitlab.com"** en haut à droite de l'écran
3. Dans la barre latérale de gauche, allez dans **"Deploy"** puis **"Pages"**
4. Décochez la case à coté de "Force HTTPS (requires valid certificates)"
5. Dans la partie "Domains", cliquez sur le bouton **"New domain"**
6. Dans la page "New Pages Domain" qui s'ouvre, remplir le champ **"Domain & Settings"**, vérifiez que le "Certificate" est bien en bleu
7. La page "Pages Domain" va vous donner des informations à mettre chez votre fournisseur de nom de domaine

### Étape 2-Github : Paramétrer du coté de Github

1. Allez sur [https://atelier.scribouilli.org/](https://atelier.scribouilli.org/)
2. Cliquez sur le lien **"Github"** en haut à droite de l'écran
3. Allez dans l'onglet **"Settings"**
4. Dans la barre latérale de gauche, allez dans **"Pages"**
5. Dans la section **"Custom domain"**, **entrez votre nom de domaine** (ex: adressedemonsite.fr ) et cliquez sur **Save**
6. Juste en-dessous, cochez la case à coté de "Enforce HTTPS"
7. Attendez plusieurs heures que le lien entre votre nom de domaine et votre site Scribouilli soit mis en place par Infomaniak.
  - Cette étape peut prendre du temps (maximum 48h)
  - Vous allez voir apparaitre un message au fond jaune indiquant "www.adressedemonsite.fr is improperly configured"

### Étape 3-Gitlab/ScribouGit : Paramétrer du coté d'Infomaniak avec un site sur Gitlab ou Scribougit

1. Connectez-vous à [votre compte Infomaniak](https://login.infomaniak.com/)
2. Descendez dans la page jusqu'à la section Produits > Web & Domaines > et cliquez sur Domaine
3. Dans le bloc qui a pour titre votre nom de domaine (ex : adressedemonsite.fr), cliquez sur les 3 petits points en haut à droite > Modifier la zone DNS
4. Supprimez les carrés dont le Type est **"A"** (visible en bas à gauche, l'étiquette en bas à droite sera "Adresse web")
5. Cliquez sur "Ajouter un enregistrement"
  - Pour **"Type"** choisir **"A"**
  - Ne pas toucher à Source
  - Dans **"Cible"**, pour faire le lien avec
     - Gitlab : insérez `35.185.44.232`
     - Scribougit : insérez `176.9.171.107`
  - Ne pas toucher à TTL
  - Cliquez sur **Créer**
6. Cliquez sur "Ajouter un enregistrement"
  - Pour **"Type"** choisir **"TXT"**
  - Dans **"Valeur"**, remplir avec le contenu du champ **"Verification status"** de Gitlab ou Scribougit
     - qui ressemble à `_gitlab-pages-verification-code.adressedemonsite.fr TXT gitlab-pages-verification-code=blablablaPleinDeCaracteres`
  - Ne pas toucher à TTL
  - Cliquez sur **Créer**

### Étape 3-Github : Paramétrer du coté d'Infomaniak avec un site sur Github

1. Connectez-vous à [votre compte Infomaniak](https://login.infomaniak.com/)
2. Descendez dans la page jusqu'à la section Produits > Web & Domaines > et cliquez sur Domaine
3. Dans le bloc qui a pour titre votre nom de domaine (ex : adressedemonsite.fr), cliquez sur les 3 petits points en haut à droite > Tableau de bord
4. Allez dans Actions rapides > Modifier la zone DNS
5. Cliquez sur "Ajouter une entrée"
  - Pour **"Type"** choisir **"A"**
  - Ne pas toucher à Source
  - Dans **"Cible"**, nous allons faire le lien avec Github : insérez ```185.199.110.153```
  - Ne pas toucher à TTL
  - Cliquez sur **Créer**

  

### C'est fini !

Si tout s'est bien passé et que les étapes ont été bien respectées, votre site Scribouilli est maintenant accessible depuis votre nom de domaine tout neuf ! Bravo ! 🎉

Si ce n'est pas le cas, vous pouvez nous écrire à [coucou@scribouilli.org](mailto:coucou@scribouilli.org) pour que l'on essaie de comprendre le souci ensemble.


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

