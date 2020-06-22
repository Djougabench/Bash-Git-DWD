# Tutoriel Git 101


- **GIT** est un logiciel de gestion de versions décentralisé.

## Introduction Git

[Git](https://git-scm.com/) est un logiciel de gestion de versions décentralisé et il sera l'un de vos "meilleurs ennemis" pendant toute votre vie de développeur.se :)


### Listes des commandes de base vu en cours

`git init` pour créer un nouveau dépôt.

`git status` pour afficher l'état de l'arborescence de travail.

`git add` pour ajouter le contenu d'un fichier à l'index.

`git commit -m "Votre message"` pour enregistrer les modifications dans le repository.

`git remote add origin https://github.com/nom/nomDuRepo.git` pour gérer un ensemble de repositories suivis.

`git push -u origin master` pour mettre à jour les réfs distantes avec les objets associés par commit.

`git clone` pour cloner un dépôt distant.


### GitHub et la ligne de commande

#### Exemple 1 : contribuer à un référentiel existant
* téléchargez un référentiel depuis GitHub.com à votre machine
`git clone https://github.com/nom/nomDuRepo.git`

* changez de répertoire pour accéder au contenu cloné
`cd monrepo`

* apportez des modifications, par exemple, éditez `fichier1.md` et` fichier2.md` à l'aide de l'éditeur de texte

* ajoutez à staging les fichiers modifiés
`git add fichier1.md fichier2.md`

* prendre un instantané de la zone de transit (tout ce qui a été ajouté)
`git commit -m "mon commit"`

* pousser/ « pusher » les modifications dans github
`git push -u origin master`


#### Exemple 2 : démarrez un nouveau référentiel et publiez-le sur GitHub

Tout d'abord, vous devrez créer un nouveau référentiel sur GitHub comme vu lors de votre dernier cours. N'initialisez pas le référentiel avec un fichier README, .gitignore ou License. Ce référentiel vide attendra votre code.
* créer un nouveau répertoire et l'initialiser avec des fonctions spécifiques à git
`git init monrepo`

* changez de répertoire `monrepo`
`cd monrepo`

* créer le premier fichier du projet
`nano README.md`

* git n'est pas au courant du fichier, mettez-le en scène
`git add README.md`

* prendre un instantané de la zone de transit (tout ce qui a été ajouté)
`git commit -m "add README to initial commit"`

* fournissez le chemin du référentiel que vous avez créé sur github
`git remote add origin https://github.com/nom/nomrepo.git`

* pousser les modifications dans github
`git push --set-upstream origin master`
