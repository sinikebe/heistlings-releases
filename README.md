# Heistlings — téléchargements

Heistlings est un prototype où de petites créatures apprennent à récupérer un butin puis à rejoindre leur refuge. Vous faites grandir votre voleur, lancez son entraînement et observez ce qu’il a appris.

Ce dépôt public contient les applications Windows et les fichiers de mise à jour. Les sources du jeu sont conservées dans un dépôt privé.

## Télécharger

**[Télécharger Heistlings.exe — Dev](https://github.com/sinikebe/heistlings-releases/releases/download/branch-dev/Heistlings.exe)**

**[Télécharger l’APK Android expérimental](https://github.com/sinikebe/heistlings-releases/releases/download/branch-android-experimental/Heistlings-Android-test.apk)**

Android reçoit automatiquement les nouveautés de Dev via son propre canal de mises à jour. L’APK n’est pas testé sur téléphone ou émulateur ; son interface suit celle du jeu source.

Le canal **Dev** reçoit les nouveautés pour les essayer et les valider. La version **Joueurs** sera publiée séparément après cette validation. Les deux canaux auront leurs propres mises à jour et sauvegardes.

1. Enregistrez **Heistlings.exe** dans un dossier accessible en écriture, par exemple un dossier Heistlings Dev dans vos Documents.
2. Lancez directement cet exécutable, puis choisissez **Entrer dans le labo**.

Aucun ZIP, installation de Godot ou compte n’est nécessaire. Le jeu et son launcher sont intégrés à l’exécutable. Le [guide de premier essai](https://github.com/sinikebe/heistlings-releases/releases/download/branch-dev/README.md) explique les commandes.

La [page de la version dev](https://github.com/sinikebe/heistlings-releases/releases/tag/branch-dev) donne les détails et les fichiers de contrôle. Les fichiers `.pck` et `manifest.json` sont utilisés par le launcher ; vous n’avez pas à les installer. Les archives `Source code` ajoutées par GitHub ne sont pas le jeu.

## Mettre à jour depuis le jeu

Le launcher recherche les mises à jour au démarrage et depuis le bouton **Mises à jour**. **Chaque nouvelle version Dev démarre avec de nouveaux voleurs**, sur PC et Android, pendant cette phase de prototype. Fermer et réouvrir la même version conserve la séance. Les sauvegardes automatiques de la version courante sont écrites en arrière-plan pour garder l’interface réactive.

Le launcher vérifie les téléchargements avec SHA-256. Il reçoit uniquement les mises à jour du canal de votre application : Dev ou Joueurs.

## Premier essai

Le dock relie **Entraînement**, **Campagne** et **Mes voleurs**. Trois emplacements permettent de créer, sélectionner et supprimer des voleurs indépendants. Le voleur sélectionné conserve son cerveau, son expérience, ses objectifs, ses compétences et sa campagne.

Choisissez ses **Règles d’entraînement** : pas maximum par simulation, nombre de simulations par candidat, limite de collisions, butin et livraison obligatoires ou simplement récompensés. Réglez les poids des bonus de butin, livraison, rapidité et collisions évitées. Une règle enfreinte arrête l’essai et exclut le candidat de la sélection. Seul le score moyen pondéré départage les candidats admissibles ; le replay montre son résultat et son score.

Dans la salle d’entraînement de **8 × 6 cases**, le départ et le butin peuvent apparaître sur n’importe quelle case libre intérieure. Ils sont tirés au hasard, sans direction privilégiée pour le butin. Le refuge reste dans sa bande de gauche ; les trois positions sont distinctes. Les 100 salles de campagne restent figées et suivent leurs positions enregistrées.

Dans **Mes voleurs → Cerveau**, les nouveaux voleurs ont un petit réseau **4 → 2 → 4** (22 paramètres) : quatre indicateurs de dernière direction, deux neurones de calcul et quatre décisions. Le toucher gratuit ajoute les deux entrées **Collision** et **Butin tenu**, pour un réseau **6 → 2 → 4** de 26 paramètres. Les entrées verrouillées sont absentes. L’entraînement rapporte **1 XP pour 1 000 actions calculées**. Un neurone coûte **100 XP** ; achetez-le, choisissez sa couche, puis cliquez dans le dessin pour le placer. Ses connexions sont automatiques et leur influence commence à zéro pour conserver l’apprentissage. Les neurones peuvent être déplacés dans le dessin sans modifier leurs connexions. Le cerveau, la réserve et les positions sont conservés pendant la même version. Les campagnes et les replays ne donnent pas cette XP ; les points de compétences restent séparés.

**Charger un cerveau sauvegardé**, dans le même onglet, permet de choisir le cerveau initial, le meilleur conservé ou une génération encore archivée, puis de confirmer avec **Charger ce cerveau**. L’apprentissage repart en pause depuis des copies de ses poids, avec les neurones actuels, l’XP, les compétences et les compteurs conservés. Les connexions acquises depuis ce cerveau commencent à zéro ; l’essai incomplet et le replay d’entraînement sont abandonnés. Une campagne déjà lancée garde sa copie figée. Seuls les cerveaux conservés pour ce voleur dans la version Dev courante sont disponibles.

Le **Toucher** est gratuit dès le départ ; les nouveaux points viennent des premières réussites de campagne, une seule fois par voleur. Les organes acquis restent actifs ; ils ne s’équipent plus. Loupe et boussole restent des accessoires à débloquer.

La salle affiche uniquement un replay avec son identité et sa barre de lecture : **×1, ×4 ou ×16 = 1, 4 ou 16 actions rejouées par seconde**, avec déplacements animés. Un halo signale une attente et une croix ambre une collision. Le replay va au bout, puis choisit le dernier essai terminé. Sa pause est distincte de celle de l’apprentissage.

Dans **Entraînement**, les onglets **Replay** et **Progression** permettent de passer de l’essai enregistré à deux graphiques : les scores d’entraînement et de validation du champion conservé, puis le nombre de candidats admissibles comme parents. Les scores viennent de salles différentes ; les admissibles ne sont pas le nombre d’élites effectivement copiées. Un repère rouge signale une génération entièrement éliminée. Affichez les 100 ou 1 000 dernières générations ou toutes celles encore conservées, puis survolez ou touchez un point pour ses détails. Les numéros de génération restent réels ; les anciennes périodes échantillonnées et les valeurs manquantes ne sont pas présentées comme des zéros ni comme un historique complet.

L’apprentissage continue sur les trois écrans avec **la moitié du budget de calcul disponible par défaut**. Activez **Boost** pour utiliser le maximum disponible tout en gardant une marge pour l’interface. Ce partage porte sur le moteur de simulation ; ce n’est pas un quota global de tous les cœurs de votre PC. Les icônes expliquent leur rôle au clic et la case avec l’œil affiche les perceptions.

Le panneau du réseau, à côté des replays, montre les activations à chaque étape et la commande enregistrée. Il affiche le cerveau de l’essai enregistré, même si l’entraînement a continué entre-temps. Les anciens replays sans cerveau enregistré gardent leur lecture et signalent l’absence de ces données.

Ouvrez **Paramètres → Calcul de l’entraînement** : **Désactivé** utilise le CPU, **Auto** choisit le GPU après comparaison sur votre machine lorsqu’il apporte un gain, et **Forcé** le demande indépendamment de la vitesse mesurée. L’état affiché indique le moteur réellement utilisé et explique une indisponibilité. Les campagnes restent évaluées sur CPU. Le launcher proposera un nouvel exécutable pour cette version, qui introduit le calcul GPU.

**Premier butin**, la campagne 1, teste la récupération du butin dans **100 salles figées de 8 × 6**, sans obstacle intérieur ni garde. Chaque salle autorise **60 actions** ; il faut **90 réussites sur 100**, sans livraison. La copie du cerveau reste identique pendant tout l’examen. La première réussite donne **un point d’arbre**, qui permet d’obtenir la **Vue niveau 1, de portée une case**. Chaque évaluation terminée dispose d’un replay à ×1, ×4 ou ×16. La campagne 2 n’est pas encore implémentée.

Le bouton principal passe de **Lancer** à **Pause**, **Reprendre**, puis **Nouvelle tentative** après la fin. Pendant un examen inachevé, **Recommencer les 100 salles** demande confirmation, abandonne les résultats en cours et reprend les 100 salles avec le cerveau actuellement conservé. Reprendre une tentative en pause garde son cerveau initial.

L’historique garde les 100 dernières générations, puis une par dizaine, centaine, millier selon leur âge. Le meilleur cerveau et l’entraînement courant restent indépendants de cet échantillonnage. Aucun ZIP ni installation de Godot n’est nécessaire ; le guide téléchargeable avec la release détaille les commandes.

## Signaler un problème

Ouvrez une [issue](https://github.com/sinikebe/heistlings-releases/issues) en précisant le canal et la version de l’application, votre version de Windows, l’écran concerné et les étapes permettant de retrouver le problème. Pour le comportement du voleur, ajoutez la salle, les organes et l’accessoire utilisés.

## Mentions tierces

Le jeu utilise [Godot](https://godotengine.org/) et le [launcher de sinikebe](https://github.com/sinikebe/godot-launcher-template). Leurs licences et notices sont intégrées à l’exécutable, consultables via **Mentions légales**, et également disponibles dans les fichiers de release. Ces licences tierces ne constituent pas une licence de publication des sources du jeu.
