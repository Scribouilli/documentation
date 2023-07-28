---
title : Adresse personnalisée
---

Il y a trois grandes étapes pour avoir votre site Scribouilli derrière votre adresse personnalisée.

On appelle cette adresse personnalisée : **"Nom de domaine"**

## Les 3 étapes

* Acheter votre nom de domaine (cette page explique comment le faire chez Infomaniak ou Gandi)
* Faire les paramétrages qui vont bien chez votre fournisseur de nom de domaine (ici chez Infomaniak ou Gandi)
* Faire les paramétrages qui vont bien chez  Github


## Étape 1 : Acheter votre nom de domaine chez Infomaniak ou Gandi

1. Rendez-vous sur [infomaniak](https://www.infomaniak.com/fr) ou [gandi.net](https://shop.gandi.net/fr/domain/suggest/d2495163-a057-41fd-a3ab-8bca338797fd?search=)
1. Vérifiez la disponibilité et le prix du nom de domaine que vous souhaitez (ex : adressedemonsite.fr )
1. Suivez le processus d'achat en décochant toutes les options payantes supplémentaires si il y en a, et créez-vous un compte au passage

Pour info, un nom de domaine en .fr coûte moins de 8€/an chez Infomaniak (et moins de 20€/an chez Gandi)

## Étape 2 : Paramétrer du coté d'Infomaniak

1. Connectez-vous à [votre compte Infomaniak](https://login.infomaniak.com/)
1. Descendez dans la page jusqu'à la section Produits > Web & Domaines > et cliquez sur Domaine
1. Dans le bloc qui a pour titre votre nom de domaine (ex : adressedemonsite.fr), cliquez sur les 3 petits points en haut à droite > Tableau de bord
1. Allez dans Actions rapides >  Modifier la zone DNS 
1. cliquez sur "Ajouter une entrée"
 * Pour **"Type"** choisir **"A"**
 * ne pas toucher à Source
 * Dans **"Cible"**, nous allons faire le lien avec Github : insérez ```185.199.110.153```
 * Ne pas toucher à TTL
 * Cliquez sur **Créer**




## Étape 2 : Paramétrer du coté de Gandi

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

## Étape 3 : Paramétrer du coté de Github Pages

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





