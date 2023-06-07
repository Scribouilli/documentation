---
title : Adresse personnalisée
---

Il y a trois grandes étapes pour avoir votre site Scribouilli derrière votre adresse personnalisée.

On appelle cette adresse personnalisée : **"Nom de domaine"**

## Les 3 étapes

* Acheter votre nom de domaine (cette page explique comment le faire chez Gandi)
* Faire les paramétrages qui vont bien chez votre fournisseur de nom de domaine (ici chez Gandi)
* Faire les paramétrages qui vont bien chez  Github


## Acheter votre nom de domaine chez Gandi


1. Rendez-vous sur [gandi.net](https://shop.gandi.net/fr/domain/suggest/d2495163-a057-41fd-a3ab-8bca338797fd?search=)
1. Vérifiez la disponibilité et le prix du nom de domaine que vous souhaitez (ex : adressedemonsite.fr )
1. Suivez le processus d'achat, et créez-vous un compte au passage

## Paramétrer du coté de Gandi

1. Connectez-vous à [votre compte gandi](https://admin.gandi.net)
1. Dans la barre latérale de gauche, allez dans **"Nom de domaine"**
1. **Cliquez sur votre nom de domaine** (ex : adressedemonsite.fr)
2. Allez sur l'onglet **"Enregistrement DNS"**
3. **Supprimez la ligne** dont le Type est **"A"**
4. Cliquez sur le bouton **"Ajouter un enregistrement"** en haut à droite de l'écran.
 * Pour **"Type"** choisir **"ALIAS"**
 * ne pas toucher à TTL, Unité et Nom
 * Dans **"Nom d'hôte"**, nous allons faire le lien avec Github : 
   * si l'adresse de votre Scribouili est : `votreIdentifiant.github.io/test-website-repo-3796`
   * dans le champ **"Nom d'hôte" indiquez** : `votreIdentifiant.github.io.`
 * Vérifiez bien que vous avez **fini avec un point** (ex: `votreIdentifiant.github.io.` )
 * Cliquez sur **Créer**

## Paramétrer du coté de Github Pages

1. Allez sur [https://scribouilli.github.io/scribouilli](https://scribouilli.github.io/scribouilli)
1. Cliquez sur le lien **"Github"** en haut à droite de l'écran
1. Allez dans l'onglet **"Settings"**
1. Dans la barre latérale de gauche, allez dans **"Pages"**
1. Dans la section **"Custom domain"**, **entrez votre nom de domaine** (ex: adressedemonsite.fr ) et cliquez sur **Save**
1. Juste en-dessous, cochez la case à coté de "Enforce HTTPS"
1. Attendez plusieurs heures que le lien entre votre nom de domaine et votre site Scribouilli soit mis en place par Gandi.
   1. Cette étape peut prendre du temps (maximum 48h)
1. Si tout s'est bien passé et que les étapes ont été bien respectées, votre site Scribouilli est maintenant accessible depuis votre nom de domaine tout neuf ! Bravo !
   1. Si ce n'est pas le cas, vous pouvez nous écrire à scribouilli@lechappeebelle.team





