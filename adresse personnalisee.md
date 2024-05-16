---
title: "Adresse personnalisée"
order: 3
in_menu: true
---
Il y a trois grandes étapes pour avoir votre site Scribouilli derrière votre adresse personnalisée.

On appelle cette adresse personnalisée : **"Nom de domaine"**

## Les 3 étapes

- Acheter votre nom de domaine (cette page explique comment le faire chez Infomaniak ou Gandi)
- Faire les paramétrages qui vont bien chez votre fournisseur de nom de domaine (ici chez Infomaniak ou Gandi)
- Faire les paramétrages qui vont bien chez Github

## Étape 1 : Acheter votre nom de domaine chez Infomaniak ou Gandi

1. Rendez-vous sur [infomaniak](https://www.infomaniak.com/fr) ou [gandi.net](https://shop.gandi.net/fr/domain/suggest/d2495163-a057-41fd-a3ab-8bca338797fd?search=)
2. Vérifiez la disponibilité et le prix du nom de domaine que vous souhaitez (ex : adressedemonsite.fr )
3. Suivez le processus d'achat en décochant toutes les options payantes supplémentaires si il y en a, et créez-vous un compte au passage

Pour info, un nom de domaine en .fr coûte moins de 8€/an chez Infomaniak (et moins de 20€/an chez Gandi)

## Étape 2 : Paramétrer du coté de Github Pages

1. Allez sur [https://scribouilli.github.io/scribouilli](https://scribouilli.github.io/scribouilli)
2. Cliquez sur le lien **"Github"** en haut à droite de l'écran
3. Allez dans l'onglet **"Settings"**
4. Dans la barre latérale de gauche, allez dans **"Pages"**
5. Dans la section **"Custom domain"**, **entrez votre nom de domaine** (ex: adressedemonsite.fr ) et cliquez sur **Save**
6. Juste en-dessous, cochez la case à coté de "Enforce HTTPS"
7. Attendez plusieurs heures que le lien entre votre nom de domaine et votre site Scribouilli soit mis en place par Infomaniak ou Gandi.
  - Cette étape peut prendre du temps (maximum 48h)
  - Vous allez voir apparaitre un message au fond jaune indiquant " www.adressedemonsite.fr is improperly configured"

## Étape 2 : Paramétrer du coté de ScribouGit et Gitlab Pages

1. Allez sur [https://scribouilli.github.io/scribouilli](https://scribouilli.github.io/scribouilli)
2. Cliquez sur le lien **"Sur git.scribouilli.org"** ou **"Sur gitlab.com"** en haut à droite de l'écran
3. Dans la barre latérale de gauche, allez dans **"Deploy** puis **"Pages"**
4. Décochez la case à coté de "Force HTTPS (requires valid certificates) "
5. Dans la partie "Domains", cliquez sur le bouton **"New domain"**
6. Dans la page "New Pages Domain" qui s'ouvre, remplir le champ **" Domain "**, vérifiez que le "Certificate" est bien en bleu
7. La page "Pages Domain" va vous donner des informations à mettre chez votre fournisseur de nom de domaine :
  

## Étape 3 : Paramétrer du coté d'Infomaniak avec un site sur Github

1. Connectez-vous à [votre compte Infomaniak](https://login.infomaniak.com/)
2. Descendez dans la page jusqu'à la section Produits > Web & Domaines > et cliquez sur Domaine
3. Dans le bloc qui a pour titre votre nom de domaine (ex : adressedemonsite.fr), cliquez sur les 3 petits points en haut à droite > Tableau de bord
4. Allez dans Actions rapides > Modifier la zone DNS
5. Cliquez sur "Ajouter une entrée"
  - Pour **"Type"** choisir **"A"**
  - ne pas toucher à Source
  - Dans **"Cible"**, nous allons faire le lien avec Github : insérez ```185.199.110.153```
  - Ne pas toucher à TTL
  - Cliquez sur **Créer****

## Étape 3 : Paramétrer du coté de Gandi avec un site sur Github

1. Connectez-vous à [votre compte gandi](https://admin.gandi.net)
  
2. Dans la barre latérale de gauche, allez dans **"Nom de domaine"**
  
3. **Cliquez sur votre nom de domaine** (ex : adressedemonsite.fr)
  
4. Allez sur l'onglet **"Enregistrement DNS"**
  
5. **Supprimez la ligne** dont le Type est **"A"**
  
6. Cliquez sur le bouton **"Ajouter un enregistrement"** en haut à droite de l'écran.
  
  - Pour **"Type"** choisir **"ALIAS"**
  - ne pas toucher à TTL, Unité et Nom
  - Dans **"Nom d'hôte"**, nous allons faire le lien avec Github :
  - si l'adresse de votre Scribouili est : `votreIdentifiant.github.io/test-website-repo-3796`
  - dans le champ **"Nom d'hôte" indiquez** : `votreIdentifiant.github.io.`
  - Vérifiez bien que vous avez **fini avec un point** (ex: `votreIdentifiant.github.io.` )
  - Cliquez sur **Créer**

## Étape 3 : Paramétrer du coté d'Infomaniak avec un site sur Gitlab ou Scribougit

1. Connectez-vous à [votre compte Infomaniak](https://login.infomaniak.com/)
2. Descendez dans la page jusqu'à la section Produits > Web & Domaines > et cliquez sur Domaine
3. Dans le bloc qui a pour titre votre nom de domaine (ex : adressedemonsite.fr), cliquez sur les 3 petits points en haut à droite > Tableau de bord
4. Allez dans Actions rapides > Modifier la zone DNS
5. Supprimez la ligne dont le Type est **"A"**
6. Cliquez sur "Ajouter une entrée"
  - Pour **"Type"** choisir **"A"**
  - ne pas toucher à Source
  - Dans **"Cible"**, pour faire le lien avec Gitlab : insérez `35.185.44.232`
  - Dans **"Cible"**, pour faire le lien avec Scribougit : insérez `176.9.171.107`
  - Ne pas toucher à TTL
  - Cliquez sur **Créer**
7. Cliquez sur "Ajouter une entrée"
  - Pour **"Type"** choisir **"TXT"**
  - Dans **"Valeur"**, remplir avec le contenu du champs **"Verification status** de Gitlab ou Scribougit, ça ressemble à un truc du genre `_gitlab-pages-verification-code.adressedemonsite.fr TXT gitlab-pages-verification-code=blablablaPleinDeCaracteres`
  - Ne pas toucher à TTL
  - Cliquez sur **Créer**

## Étape 3 : Paramétrer du coté de Gandi avec un site sur Gitlab ou Scribougit

1. Connectez-vous à [votre compte gandi](https://admin.gandi.net)
  
2. Dans la barre latérale de gauche, allez dans **"Nom de domaine"**
  
3. **Cliquez sur votre nom de domaine** (ex : adressedemonsite.fr)
  
4. Allez sur l'onglet **"Enregistrement DNS"**
  
5. **Supprimez la ligne** dont le Type est **"A"**
  
6. Cliquez sur le bouton **"Ajouter un enregistrement"** en haut à droite de l'écran.
  
  - Pour **"Type"** choisir **"ALIAS"**
  - ne pas toucher à TTL, Unité et Nom
  - Dans **"Nom d'hôte"**, nous allons faire le lien avec Gitlab ou Scribougit :
    - si l'adresse de votre Scribouili est : `votreIdentifiant.monpetitsite.org/test-website-repo-3796`
    - dans le champ **"Nom d'hôte" indiquez** : `votreIdentifiant.monpetitsite.org..`
    - Vérifiez bien que vous avez **fini avec un point** (ex: `votreIdentifiant.monpetitsite.org..` )
  - Cliquez sur **Créer**
  

## C'est fini

Si tout s'est bien passé et que les étapes ont été bien respectées, votre site Scribouilli est maintenant accessible depuis votre nom de domaine tout neuf ! Bravo !

- Si ce n'est pas le cas, vous pouvez nous écrire à coucou@scribouilli.org 