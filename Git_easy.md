### Niveau Débutant :

#### 1. Compréhension des bases de Git :

   - Qu'est-ce que Git et pourquoi l'utiliser ?

    Git est un système de contrôle de version qui a été inventé et développé par Linus Torvalds, également connu pour l'invention du noyau Linux, en 2005. Il s'agit d'un outil de développement qui aide une équipe de développeurs à gérer les changements apportés au code source au fil du temps

   "https://www.google.com"
    
   
###  2. création d'un compte GitHub :

   - **c'est quoi GitHub**
  
     GitHub est une plateforme de développement de logiciels basée sur Git. Elle offre une variété de fonctionnalités pour faciliter la collaboration, le partage et le suivi des projets de développement de logiciels. Voici quelques points clés sur ce qu'est GitHub 

       - Contrôle de version distribué 
       - Hébergement de code source 
       - Collaboration 
       - Gestion de projet
       - Communauté et open source

   - **Pour créer un compte GitHub, vous pouvez suivre ce lien : GitHub - S'inscrire.**

   - Suivez les instructions à l'écran pour terminer le processus d'inscription.

#### 3. Configuration de Git :

   - Configuration de l'identité (nom d'utilisateur, e-mail).
  
 ```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre@email.com"
```

#### Configuration des préférences (couleurs, alias,).

- **Configuration des couleurs** :
```bash
git config --global color.ui <valeur>
```
Ceci activera la coloration syntaxique dans la sortie de Git pour une meilleure lisibilité.

- **Remplacez <valeur> par l'une des options suivantes**

   - auto : Git décide d'utiliser la couleur automatiquement en fonction du contexte.
   - true : Force l'utilisation de la couleur.
   - false : Désactive complètement la couleur.

- **Afficher la configuration actuelle**
  Pour afficher la configuration actuelle de la couleur dans Git:

```bash
git config --global --get color.ui
```
 
- **Configuration des alias** :
Les alias permettent de définir des raccourcis pour les commandes Git. Par exemple :

```bash
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
```
Ainsi, vous pourrez utiliser des commandes plus courtes comme `git co` au lieu de `git checkout`, `git br` au lieu de `git branch`, etc.

Pour voir toutes les configurations que vous avez effectuées, vous pouvez utiliser la commande :

```bash
git config --list
```

Cela affichera toutes les configurations Git, y compris celles que vous avez définies.
  


#### 4. Utilisation de Git en ligne de commande :

1. **Initialisation d'un dépôt Git** :

   - Pour commencer à suivre les modifications de vos fichiers, vous devez d'abord initialiser un dépôt Git dans le répertoire de votre projet. Vous pouvez le faire en utilisant la commande suivante dans votre terminal :
  
```bash
git init
```

1. **Ajout de fichiers au suivi de Git** :
   - Une fois que vous avez initialisé le dépôt Git, vous pouvez ajouter des fichiers à suivre en utilisant la commande `git add`. Par exemple, pour ajouter tous les fichiers au suivi de Git, vous pouvez utiliser :
  
```bash
git add .
```
   - Cette commande ajoute tous les fichiers et répertoires du répertoire actuel au suivi de Git. Vous pouvez également spécifier des fichiers individuels si vous le souhaitez.

1. **Création de commits** :
   - Une fois que vous avez ajouté les fichiers que vous souhaitez suivre, vous devez créer un commit pour enregistrer ces modifications dans l'historique de votre dépôt. Utilisez la commande `git commit` pour créer un commit avec un message descriptif :
  
```bash
git commit -m "Message descriptif de votre commit"
```
   - Assurez-vous de fournir un message descriptif qui explique les modifications apportées dans ce commit.

1. **Suivi des modifications** :

   - À partir de ce moment, Git suivra les modifications apportées à vos fichiers. Si vous modifiez un fichier suivi par Git, vous devrez à nouveau utiliser `git add` pour l'ajouter à la zone de staging, puis `git commit` pour créer un nouveau commit enregistrant ces modifications.

2. **Consultation de l'état des fichiers** :
   - Vous pouvez vérifier l'état de vos fichiers et savoir s'ils sont suivis par Git, s'ils ont été modifiés ou s'ils sont prêts à être commités en utilisant la commande :
  
```bash 
git status
```
   - Cette commande affichera l'état actuel de votre dépôt Git et des fichiers qui s'y trouvent.

NB : Tous actions sur un fichier  doivent être  commit 

3. **Unmodified (Non modifié)** : Un fichier se trouve dans cet état lorsqu'il correspond à la version dans le dernier commit et n'a pas été modifié depuis. C'est l'état de base d'un fichier après un commit.

4. **Modified (Modifié)** : Si vous modifiez un fichier qui était dans l'état "Unmodified," il passe dans l'état "Modified." Cela signifie qu'il a été modifié depuis le dernier commit.
  
5. **Staged for Commit (Prêt pour le commit)** : Si vous avez modifié un fichier et que vous l'ajoutez ensuite à la zone de staging avec `git add`, il passe dans cet état. Cela signifie que les modifications apportées au fichier seront incluses dans le prochain commit.

6. **Deleted (Supprimé)** : Si vous supprimez un fichier qui était suivi par GIT, il passe dans cet état. GIT garde une trace des suppressions, de sorte que vous pouvez restaurer le fichier si nécessaire.

7. **Renamed (Renommé)** : Si vous renommez un fichier qui est suivi par GIT, il passe dans cet état. GIT suit le renommage du fichier.

8. **Unmerged (Non fusionné)** : Lorsqu'il y a des conflits de fusion (merge conflicts) entre différentes branches, un fichier peut se trouver dans cet état. Vous devez résoudre les conflits manuellement avant de pouvoir le commit.

9. **Ignored (Ignoré)** : Vous pouvez configurer GIT pour ignorer certains fichiers ou répertoires en les ajoutant à un fichier `.gitignore`. Ces fichiers sont dans l'état "Ignoré" et ne sont pas suivis par GIT.

Il est important de comprendre ces états pour bien gérer vos fichiers et votre workflow GIT.


- **commandes Git que vous pouvez utiliser pour visualiser l'historique des commits**

1. **`git log`** :
   - Affiche l'historique des commits dans le dépôt :
   - 
```bash
git log
```

1. **`git log --oneline`** :
   - Affiche l'historique des commits de manière condensée :
  
```bash 
git log --oneline
```

1. **`git log --graph`** :
   - Affiche l'historique des commits sous forme graphique :
  
```bash 
git log --graph
```

1. **`git diff`** :
   - Affiche les différences entre les modifications non stagées et le dernier commit :
  
```bash 
git diff
```
   - Compare les modifications entre deux commits ou branches :
  
```bash 
git diff commit1 commit2
```

1. **`git diff --cached`** :

   - Affiche les différences entre ce qui a été stagé et le dernier commit :
  
```bash 
git diff --cached
```

1. **`git show`** :
   - Affiche les détails d'un commit spécifique :
     ```
     git show <identifiant_commit>
     ```

2. **`git blame`** :
   - Affiche qui a modifié chaque ligne d'un fichier :
     ```
     git blame nom_du_fichier
     ```

Ces commandes sont très utiles pour examiner l'historique des commits, les différences entre les versions, les détails des commits spécifiques et les responsables des modifications dans un fichier. Utilisez-les dans votre workflow Git pour mieux comprendre l'évolution de votre projet et pour résoudre les conflits éventuels.




#### 5. Gestion des branches :
   - Création, suppression et fusion de branches.
   - Utilisation des commandes `git branch`, `git checkout`, `git merge`, etc.



Commits :

    Un commit est une action dans Git qui enregistre les modifications apportées à un ou plusieurs fichiers dans un dépôt.
    Chaque commit est accompagné d'un message qui décrit les modifications effectuées.
    Les commits permettent de suivre l'historique des modifications et de revenir à des états précédents du code si nécessaire.

Branches :

    Une branche dans Git est une version séparée du code source d'un projet.
    Les branches permettent aux développeurs de travailler sur des fonctionnalités ou des correctifs de manière isolée, sans affecter la branche principale (généralement nommée "master" ou "main").
    Les branches facilitent le développement parallèle et la gestion des fonctionnalités expérimentales.

Fusions (Merges) :

    La fusion est le processus qui consiste à combiner les modifications de deux branches différentes en une seule.
    Elle est souvent utilisée pour intégrer les fonctionnalités développées sur des branches de fonctionnalités dans la branche principale du projet.
    Git gère les fusions de manière automatique dans la mesure du possible, mais parfois des conflits peuvent survenir lorsque les modifications dans deux branches entrent en conflit.

Autres concepts :

    Dépôts (Repositories) : Un dépôt Git est un espace où sont stockés les fichiers et l'historique des modifications d'un projet.
    Remote (Dépôt distant) : Un dépôt distant est une copie du dépôt local hébergée sur un serveur distant, généralement sur des services comme GitHub, GitLab ou Bitbucket.
    Pull Requests : Une demande de tirage est une fonctionnalité de collaboration permettant aux contributeurs de proposer des modifications à un dépôt distant et d'initier une discussion sur ces modifications avant qu'elles ne soient fusionnées dans la branche principale.