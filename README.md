# Heistlings — téléchargements

Heistlings est un prototype où de petites créatures apprennent à récupérer un butin puis à rejoindre leur refuge. Vous équipez votre voleur, lancez son entraînement et observez ce qu’il a appris.

Ce dépôt public contient les applications Windows et les fichiers de mise à jour. Les sources du jeu sont conservées dans un dépôt privé.

## Télécharger

**[Télécharger Heistlings.exe — Dev](https://github.com/sinikebe/heistlings-releases/releases/download/branch-dev/Heistlings.exe)**

Le canal **Dev** reçoit les nouveautés pour les essayer et les valider. La version **Joueurs** sera publiée séparément après cette validation. Les deux canaux auront leurs propres mises à jour et sauvegardes.

1. Enregistrez **Heistlings.exe** dans un dossier accessible en écriture, par exemple un dossier Heistlings Dev dans vos Documents.
2. Lancez directement cet exécutable, puis choisissez **Entrer dans le labo**.

Aucun ZIP, installation de Godot ou compte n’est nécessaire. Le jeu et son launcher sont intégrés à l’exécutable. Le [guide de premier essai](https://github.com/sinikebe/heistlings-releases/releases/download/branch-dev/README.md) explique les commandes.

La [page de la version dev](https://github.com/sinikebe/heistlings-releases/releases/tag/branch-dev) donne les détails et les fichiers de contrôle. Les fichiers `.pck` et `manifest.json` sont utilisés par le launcher ; vous n’avez pas à les installer. Les archives `Source code` ajoutées par GitHub ne sont pas le jeu.

## Mettre à jour depuis le jeu

Le launcher recherche les mises à jour au démarrage. Depuis l’atelier, le bouton **Mises à jour** le rouvre en mettant la séance en pause. Vous pouvez vérifier, télécharger et installer la mise à jour proposée. Les trois voleurs sont sauvegardés automatiquement avant installation et redémarrage. Après réouverture, elle est restaurée en pause ; **Reprendre l’entraînement** poursuit la même population et le même essai. Une erreur de sauvegarde suspend la mise à jour sans fermer la séance.

Le launcher vérifie les téléchargements avec SHA-256. Il reçoit uniquement les mises à jour du canal de votre application : Dev ou Joueurs.

## Premier essai

Le dock relie **Entraînement**, **Campagne** et **Mes voleurs**. Trois emplacements permettent de créer, sélectionner et supprimer des voleurs indépendants. Le voleur sélectionné conserve son cerveau, son expérience, ses objectifs, ses compétences et sa campagne.

Choisissez ses **Objectifs d’entraînement** : ramasser, livrer, respecter une limite de pas et/ou de collisions. Chaque essai terminé qui satisfait les conditions donne **10 XP**, soit **un point à répartir dans l’arbre**. Les organes acquis restent actifs ; ils ne s’équipent plus. Loupe et boussole restent des accessoires à débloquer.

La salle affiche uniquement un replay avec son identité et sa barre de lecture : **×1, ×4 ou ×16 = 1, 4 ou 16 actions rejouées par seconde**, avec déplacements animés. Un halo signale une attente et une croix ambre une collision. Le replay va au bout, puis choisit le dernier essai terminé. Sa pause est distincte de celle de l’apprentissage.

L’apprentissage continue sur les trois écrans avec **la moitié du budget de calcul disponible par défaut**. Activez **Boost** pour utiliser le maximum disponible tout en gardant une marge pour l’interface. Ce partage porte sur le moteur de simulation ; ce n’est pas un quota global de tous les cœurs de votre PC. Les icônes expliquent leur rôle au clic et la case avec l’œil affiche les perceptions.

**Premier butin**, la première campagne, utilise une carte fixe de **8 × 6**, sans obstacle intérieur ni garde. Récupérez le butin puis rapportez-le au refuge avec une copie du cerveau de votre voleur. La réussite reste enregistrée pour lui.

Une ancienne séance est conservée dans le premier emplacement. Aucun ZIP ni installation de Godot n’est nécessaire ; le guide téléchargeable avec la release détaille les commandes.

## Signaler un problème

Ouvrez une [issue](https://github.com/sinikebe/heistlings-releases/issues) en précisant le canal et la version de l’application, votre version de Windows, l’écran concerné et les étapes permettant de retrouver le problème. Pour le comportement du voleur, ajoutez la salle, les organes et l’accessoire utilisés.

## Mentions tierces

Le jeu utilise [Godot](https://godotengine.org/) et le [launcher de sinikebe](https://github.com/sinikebe/godot-launcher-template). Leurs licences et notices sont intégrées à l’exécutable, consultables via **Mentions légales**, et également disponibles dans les fichiers de release. Ces licences tierces ne constituent pas une licence de publication des sources du jeu.
