Rapport sur la création et la gestion d'un dépôt GitHub

1. Création du dépôt sur GitHub

Pour commencer, je me suis rendu sur GitHub et j'ai créé un nouveau dépôt intitulé "joe.github.io" en cliquant sur "Create a new repository". Ce dépôt servira à héberger mon projet.

2. Configuration du projet local

Ensuite, j'ai ouvert le terminal et créé un dossier de projet local avec les commandes suivantes :
Créer un dossier pour le projet :  
 mkdir Module-1

Créer les fichiers principaux du projet :  
 touch index.html style.css

J'ai ensuite ouvert ce dossier et ses fichiers dans Visual Studio Code (VS Code) à l'aide de la commande:
code .

3. Initialisation du fichier HTML

Dans VS Code, dans le fichier index.html, j'ai tapé ! suivi de la touche "Entrée". Cette action a automatiquement généré la structure de base HTML (doctype, balises HTML, head et body).

4. Ouverture du terminal dans VS Code

Pour ouvrir le terminal dans VS Code, j'ai cliqué sur Terminal dans la barre de menus en haut, puis sélectionné Nouveau terminal. Le terminal s'est alors ouvert directement dans mon dossier Module-1.

5. Initialisation du dépôt Git local

Dans le terminal, j'ai initialisé un dépôt Git local avec la commande:
git init

Cela a créé un sous-dossier .git qui contient toutes les informations nécessaires pour suivre les versions du projet.

6. Ajout des fichiers à Git

Ensuite, j'ai ajouté les fichiers index.html et style.css à la zone de transit Git (zone de préparation des fichiers avant commit) avec la commande :
git add index.html styles.css

7. Premier commit

Pour sauvegarder cette première version du projet, j'ai utilisé la commande suivante :
git commit -m 'first commit'

Cette commande crée un instantané de mon travail à ce stade précis.

8. Connexion du dépôt local à GitHub

Afin de lier mon dépôt local à celui que j'ai créé sur GitHub, j'ai exécuté la commande :
git remote add origin git@github.com:Joe19071991/joe.github.io.git

Ensuite, j'ai renommé la branche par défaut de master à main (comme recommandé par les nouvelles conventions GitHub) avec la commande : git branch -M main

Enfin, j'ai envoyé les modifications locales vers GitHub avec la commande suivante :
git push -u origin main

9. Vérification sur GitHub

Je suis retourné sur GitHub et, après avoir rafraîchi la page, j'ai vérifié que mon dépôt et les fichiers étaient bien présents.

10. Modifications et synchronisation des changements

Dans VS Code, j'ai apporté des modifications au fichier index.html en changeant le contenu du title et du h1. Pour envoyer ces modifications vers GitHub, j'ai suivi les étapes suivantes dans le terminal :

git add index.html
git commit -m 'update title and h1 in index.html'
git push

Ces changements ont bien été synchronisés avec GitHub, et j'ai pu voir mon commit apparaître sur le dépôt distant.

11. Gestion des conflits avec GitHub

Plus tard, j'ai modifié le fichier index.html directement sur GitHub. Par la suite, j'ai effectué des modifications en locales sur le même fichier. Lorsque j'ai essayé de pousser mes modifications locales avec la commande git push, j'ai rencontré un problème : Git m'a indiqué que le dépôt distant contenait des changements que je n'avais pas récupérés localement.

Pour résoudre ce problème, j'ai suivi les étapes suivantes :

1. J'ai d'abord récupéré les modifications du dépôt distant en utilisant la commande :
   git pull

   Cela a permis de fusionner les modifications distantes avec mon travail local.

2. Une fois les conflits résolus, j'ai pu pousser mes propres modifications avec la commande :
   git push

Enfin, pour m'assurer que tout était bien en ordre, j'ai vérifié le statut de mon projet avec :
git status

Cette commande m'a confirmé que tout était synchronisé correctement entre mon dépôt local et GitHub.

Conclusion

Ce processus m'a permis de créer un projet local, de le connecter à un dépôt GitHub, de gérer les changements et de résoudre les conflits entre les versions locales et distantes. Grâce aux commandes Git (init, add, commit, push, pull), j'ai pu suivre les versions de mon code et collaborer efficacement avec le dépôt distant.
