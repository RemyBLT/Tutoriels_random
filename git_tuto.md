# Explications

### <u>Différence entre git et github</u>

Git est l'outils utilisé pour gérer les différentes versions d'un projet, les conflits etc...

Github est un site internet permettant de gérer avec une interface visuelle les différents projets git. Git n'est donc pas la même chose que Github.

### <u>Branch master</u>

Il s'agit de la partie principale d'un projet. Celle-ci doit toujours être fonctionnelle pour que tous les membres de l'équipe puisse avoir, à tout moment, un projet fonctionnel.

### <u>Branch</u> 

Cela va créer une branche qui partira d'un commit de la branch master afin de pouvoir travailler dans une branche dans laquelle on peut mettre du code non-fonctionnel sans perturber les personnes faisant un pull sur la branch master. Il est possible de récupérer à tout moment les nouvelles données de la branch master sur la nouvelle branch tout en continuant de travailler sur son développement. Le plus important ici est la notion de temporalité. 

Une branche qui commence à un commit à l'instant T sera développée en parallèle de ce qu'il se passe dans le master. 

# Commandes

### <u>Gestion de base</u>

Il s'agit d'une liste de toutes les commandes fondamentales pour une bonne utilisation de git.

<i>git init :</i>  Initialise un dossier pour qu'il puisse être traité comme un dossier lié à un projet git.

<i>git add <Nom_fichier> :</i>  ajoute manuellement un fichier dans le repository git. Si le nom du fichier est ".", cela va ajouter tous les nouveaux fichiers.

<i>git status :</i> Montre les différentes modifications sur la branche principale.

<i>git commit -m "<Message_commit>" :</i> Fait un commit sur la branche sélectionnée

### <u>Gestion de branche</u>

Lorsqu'une modification doit être faite sur la branche principale, il est recommandé de créer une branche pour pouvoir développer une solution sans craindre de casser la branche principale.

<i>git checkout -b <nom_branche> :</i> Crée une branche portant le nom donné.

<i>git checkout <nom_branche> :</i> Passe d'une branche à une autre.

<i>git branch -d <Nom_branche> :</i> Supprime la branche. Elle ne doit pas être celle sur laquelle on travaille.

<i>git merge <nom_branche> :</i> fusionne les deux branches.

### <u>Gestion répertoire à distance</u>

Pour qu'un projet local soit en ligne, il faut d'abord créer un projet sur un site comme github. Pour cela, allez sur votre profil, cliquez sur "Repositories" puis sur "New". Créez le projet selon vos désirs puis tapez la commande suivante avec l'URL créé :

<i>git remote add origin <URL_projet github> :</i> Met les changements dans le cloud.

Une fois que c'est fait, tapez ces deux autres commandes pour mieux vous présenter sur le projet.

<i>git config --global user.name "<_pseudo_>" :</i> Attribue un pseudonyme pour vos prochains changements dans ce projet

<i>git config --global user.email "<_pseudo_>" :</i> Attribue une addresse mail pour vos prochains changements dans ce projet

### <u>Authentification</u>

Git vous demandera certainement de vous authentifier. Pour cela, sur Github, cliquez sur votre image en haut à droite, puis sur "Settings". Une fois dans ce menu, allez dans "Developper settings". Cliquez sur "Personnal access tokens" puis cliquez sur "Generate new token". Donnez les autorisations que vous voulez puis quand vous devrez vous authentifier, utilisez la chaîne de caractère générée en tant que mot de passe. Attention à bien la sauvegarder puisqu'elle ne sera donnée qu'une seule fois.

### <u>Gestion de conflits</u>

Si une ligne de code est modifiée par deux utilisateurs en même temps, git ne pourra pas gérer le conflit automatiquement. Il faudra donc passer par différentes commandes pour pouvoir juger de la façon de traiter le conflit.

Pour gérer cela, il faut modifier le fichier manuellement après avoir pull puis il faut à nouveau add puis commit.