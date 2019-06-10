# Git For Noobs

Plus tu vas évoluer dans le monde de la technologie, plus tu vas entendre parler de _'repos' ou 'dépôt' ou 'git' ou 'hub'_, bref des termes qui parraîssent venir d'une autre dimension, mais qui, crois moi sont extrêment simple.
Tout d'abord il faut faire la différence en *git* et les autres ennumérés; en effet, ils fonctionnent tellement de manière synchro, et sont tellement utilisés ensemble que l'on laisserait croire que c'est la même chose.

## Qu'est ce que git

Git est ce qu'on appel un _version controller_ en simple un controlleur de versions de l'ensemble des fichiers d'un projet. Peux importe le type du projet.

* Qu'est-ce que _version controller_?

    Well on peut disont que quand tu évolues dans ton projets tu crées des fichiers, tu en supprimes d'autres, tu modifies le contenue de certains et tu renommes certains fichiers; git peux te permettre de garder cette évolution au fur et à mesure que tu avances dans ton travail; c'est à dire tous les changements que tu fais git te permet de non seulement les sauvegarder, mais aussi de revenir dessus même après plusieurs jours, et ce, sans rien supprimer, car il garde chaque versions de chaque fichier.

### Qu'est qu'un dépôt

Tout d'abord il faut savoir que son appelation diffère (hub, repos ...), mais ils veulent dire la même chose.
Un dépôt c'est un serveur distant permettant de sauvegarder tes projets ainsi que gèrer aussi de manière graphique les versions de tes fichiers ainsi faire des modifications sur certains fichiers, revenir en arrière, re-télécharger le projet ... car git tout seul sans repos reste toujours en local c'est-à-dire sur ta machine, d'où l'importance d'utiliser un repos (ou dépôt çà veut dire la même chose)
Et plus important, mettre ton projet au niveau d'un dépôt te permet de pouvoir travailler à plusieurs dessus
Il y a plusieurs dépôts mais les plus connus sont [Github](https://github.com/), [BitBucket](https://bitbucket.org/), [Gitlab](https://gitlab.com/) ...

#### Comment utiliser git

Installer git, et ouvrir ta ligne de commande.
Tout ce qu'il y a de plus simple.
Maintenant dans l'utilisation pratiques qui consite à écrire dans ta ligne de commande git puis une commande nous auront:
Une fois dans votre projet depuis la ligne de commande, il faudra d'abord initialiser l'environnement git pour lui dire 'hey! gères moi mon projet steuplé ^_^' et c'est avec la commande

* git init

    Une fois fait, tu as l'environement gi sur ton projet et tu peux commencer à travailler.

En faisant un

* git status

    Tu peux voir toutes les interactions que tu as eu avec les différents fichiers de ton projet (fichiers modifiés, supprimés, renommés, ajoutés ...)

Mais jusqu'ici, git n'a pas encore pris en compte tout ce que vous venez de faire, et c'est normal parce qu'il attend que vous le lui disiez et c'est pourquoi quand vous faites un _git status_ vous les voyez en rouge.
Pour que git les prennent en compte il vous faudra faire

* git add .

    Le '.' signifie tous les fichiers, mais parfois vous n'aurez pas envie de tout prendre, mais juste un fichier, et vous pouvez simplement faire:
    git add nom_du_fichier

Après quoi, refais un _git status_ tu verras que les fichiers ajoutés à la prise en charge de git seront en vert.
Maintenant tu arrives à initialiser un projet avec git, voir tes modifications et ajouter des fichiers à la prise en charge de git (Hourra !!)

CEPENDANT tu n'as pas encore dis à git de sauvegarder ce que tu as fais. C'est très simple aussi, tu fais juste

* git commit

    Cette commande vient avec des options, celle que tu as besoin de connaître c'est le -m qui te permet entre autres de nommer ta sauvegarde qu'on appellera version comme çà tu te retrouveras plus facilement lors de la recherches sur les différentes versions (sauvegardes). Donc:
    git commit -m "Nom de la sauvegarde"

Maintenant comme dit plus haut même si tu as l'historique de l'évolution de ton travail sur chaque fichier bien organisé et tout, ton projet est toujours sur ta machine et les changement ne sont visibles que par toi.
Pour pouvoir mettre ton projet sur un serveur distant (ici un repos) tu vas sur un:

* [Github](https://github.com/) (conseil)
* [BitBucket](https://bitbucket.org/)
* [Gitlab](https://gitlab.com/)
* ...

De base ils fonctionnent tous de la même manière.
Tu crées un compte si tu en avez pas déjà un (c'est gratuis pour la vie bon il ne faut pas utiliser certaines options non plus façons tu en as pas besoin -_-)
Et puis tu cliques sur créer un repos puis les étapes sont trés faciles à suivre (de préférence mets le nom du repos, scrolles jusqu'en bas et cliques sur créer le reste nous en parlerons une autre fois)

Une fois fait tu verras clone or download quelque part sur l'écran (sur github c'est sur ta droite)
Cliques dessus et copies le lien
Maintenant reviens sur ta ligne de commande (toujours étant sur ton projet) et met la commande suivante

* git remote add origin lien_copié

    En somme, cette commande veut dire que dorénavent, à chaque fois que tu fais une modification sur ton projet, tu l'envoies sur le dépôt qui se trouve sur ce lien

Et pour envoyer les modifications sur le dépot il vous suffit de faire tout simplement

* git push

    Dans un premier temps il peut vous dire que vous devez d'abord taper une autre commande, et c'est normal c'est la première fois que tu envoies le contenue du projet sur lequel tu es, copies juste la commande qu'il t'a donné et appuis sur entrer

Très important aussi, si nous travaillons à plusieurs, pour récupérer les modifications qu'un membre de ton équipe à faites il suffit simplement de faire

* git pull

    git testera d'aord s'il y a eu des changements sur le projets que tu n'as pas encore, et si c'est le cas, il va lui même créer un point de sauvegarde (une version) et puis mettre à jour ton projet

Voilà ^_^
