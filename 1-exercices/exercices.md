# Exercices en autonomie

---

## Modalités

1. Le but du jeu est que chacun travail sur une branche dédiée sur les mêmes fichiers donc nommez vos fichiers et dossiers à l'identique. Par contre le contenu doit être différent donc vous ne devez pas vous concertez pour avoir les mêmes recettes.

2. Je suis en soutien, n'hésitez pas à m'appeler **EN PREMIER** au-delà de 10 min sans trouver la solution en cas de blocage, incompréhension, application etc. avant d'aller voir sur Internet.
Vous avez aussi la possibilité de solliciter l'aide de toute personne volontaire via le canal dédié en mettant une capture d'écran accompagné de quelques mots pour expliquer dans le cas ou l'image ne suffit pas.

3. Un temps est donné pour la réalisation de chaque partie.

4. **Pour la partie création des sandwichs, il est interdit au binôme de se concerter pour choisir les ingrédients à mettre dans vos fichiers cependant vous devez avoir absolument la même architecture au niveau des dossiers et avoir les mêmes noms pour les dossiers et fichiers.** Il n'est pas interdit d'avoir des sandwichs différents de votre collègue cependant vous devez en avoir au moins un commun uniquement au niveau du nom du fichier (même nom et arborescence mais contenu différent)

---

## Ressources

- Cours dans son intégralité (PDF)
- Le formateur
- La terminologie du cours (PDF)
- [Recap des commandes](../README.md)
- Git cheat sheet sur (SLACK)

---

## Organisation

Pour les exercices en binôme :

1. Un seul dépôt distant pour le binôme depuis **UN SEUL compte GitHub**.
2. Celui qui a créé le dépôt, invite l'autre à travailler sur ce dépôt depuis `settings > collaborators > add peole` en indiquant son adresse e-mail.

![](../3-tp/img/jpg/access.jpg)

3. Chacun travail sur une branche dédiée, nommez vos branches en suivant le pattern donné à chaque partie de l'exercice .
**Attention vous devez toujours créer vos branches à partir de la branche principale `main` ou `master`** (main ou master on parle de la même chose), la convention a juste changée entre temps avant la branche principale était nommée master, aujourd'hui c'est main.
Pour créer une nouvelle branche :
- S'assurer d'être bien sur la branche main ou master à l'aide de la commande git branch qui doit afficher un * sur la branche courante
- Ensuite exécutez la commande suivante : `git checkout -b {pattern}`en remplaçant *{pattern}* par le motif demandé pour chaque exercice.
4. Ensuite chacun travail sur l'exercice depuis sa branche en suivant l'énoncé.
5. Lorsque vous avez fini vous devez faire un commit
- Pour faire un commit vous devez d'abord ajouter les fichiers concernés dans l'index ou stage à l'aide de la commande `git add fichier dossiers`
- Ensuite, il faut ajouter le message de commit qui explique les raisons de vos modifications/ajouts/suppressions etc cf. appuyez-vous sur les conventions de nommage d'[Angular](https://github.com/angular/angular/blob/22b96b9/CONTRIBUTING.md#-commit-message-guidelines), tous les commits doivent être en ANGLAIS
6. Vous devez envoyer vos modifications depuis votre branche en local vers votre branche distant à l'aide de la commande `git push -u  origin {pattern}`. Toujours en remplaçant *{pattern}* par celui demandé.

---

## Enoncé des exercices

---

### Partie 1

**Pattern pour le nom des branches est `feature/prenom_collaborateur/part1`, en remplaçant prenom_collaborateur par votre prénom sans espace, sans accent, sans caractères spéciaux**

1. Récupérez le dépôt distant en local.
- `git clone url`
2. Créez et placez-vous sur une nouvelle branche (cf. explications ci-dessus point 3 du chapitre `Organisation`)
- S'assurer d'être sur la main ou master 
3. Créez un répertoire (dossier) sandwich. 
4. Créez un fichier à l’intérieur du répertoire sandwich nommé `burger.md` qui contient la liste des ingrédients qui compose un burger (un ingrédient par ligne).
Ajoutez une photo, pour ajouter une photo depuis un fichier markdown (.md), vous devez écrire `![un titre](chemin_relatif_de_votre_fichier_image_a_partir_de_votre_fichier_actuel_tout_en_respectant_les_dossiers_ou_sous_dossiers)`

Exemple rendu final : 

Steak

Salade

Tomate

Cornichon

Fromage

![img](https://www.vegetalsquare.fr/1017-large_default/fish-filets-26kg-moving-mountains.jpg)

---

## Partie 2

**Pattern pour le nom des branches est `feature/prenom_collaborateur/nom_du_sandwich`, en remplaçant prenom_collaborateur par votre prénom et nom_du_sandwich par le nom du sandwich concernée, le tout sans espace, sans accent, sans caractères spéciaux**

- **Un nouveau sandwich = une nouvelle branche.**
1. Créez d'autres sandwichs de votre choix avec les ingrédients qui les composent (ex: hot_dog.md, jambon_beurre.md, vegan.md, etc.).
2. Modifiez également le contenu de `burger.md` en y ajoutant selon vous un ingrédient insolite qui permettrait à votre sandwich de se démarquer.
3. Regardez l’état de votre dépôt à l'aide de la commande `git status` et faite une capture d'écran et ajoutez la photo dans les fichiers de votre dépôt.
4. Ajoutez d'autres photos à votre dépôts.
5. Regardez l’historique de vos commits.
- `git log` pour voir toutes les options possibles `git log --help`.
6. Effectuez au moins 5 modifications au total sur l’ensemble de vos fichiers.
Chaque modification doit donner lieu à un nouveau commit qui explique la raison de votre modification. Par exemple **5 modifications = 5 commits différents**.

---

## Partie 3

**Pas de pattern ici, le but est de faire des modifications depuis GitHub et de fusionner en local tous vos travaux en reglant les conflits.**
1. Depuis GitHub, effectuez une modification et faite un *commit* sur l'un de vos fichiers.

2. En local, récupérez cette modification.

3. En local, récupérez les branches de votre collègue.
- Au préalable, à l'aide d'une commande git, il faut se déplacer dans la branche qui porte le même nom que celui que vous devez récupérer depuis Github.
- Ensuite à l'aide de la commande `git fetch`, vous pouvez récupérer toutes les modifications effectuées sur GitHub.

4. Mergez toutes les branches une par une qui sont en rapport avec le sandiwch traité par votre collègue. Par exemple `feature/glodie/burger` avec `feature/pamela/burger`. 
5. Résolvez les conflits et commitez.
5. Mergez toutes les branches dans main ou master.
6. Supprimez toutes les autres branches sauf la main ou master.
