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

Le launcher recherche les mises à jour au démarrage. Depuis l’atelier, le bouton **Mises à jour** le rouvre en mettant la séance en pause. Vous pouvez vérifier, télécharger et installer la mise à jour proposée. La séance complète est sauvegardée automatiquement avant installation et redémarrage. Après réouverture, elle est restaurée en pause ; **Reprendre l’entraînement** poursuit la même population et le même essai. Une erreur de sauvegarde suspend la mise à jour sans fermer la séance.

Le launcher vérifie les téléchargements avec SHA-256. Il reçoit uniquement les mises à jour du canal de votre application : Dev ou Joueurs.

## Premier essai

Le dock compact reste fixé au bas de l’écran et relie trois espaces : **Mon voleur** pour choisir vue, odorat et accessoire ; **Entraînement** pour apprendre dans une salle de 8 × 6 cases ; **Évaluation** pour observer une copie du voleur sans modifier son apprentissage.

Un nouveau voleur commence sans sens ni accessoire. Les réussites d’entraînement débloquent la vue (premier butin récupéré), l’odorat (première livraison), la boussole (cinq salles différentes livrées) et la loupe (trois salles avec obstacles livrées). Changer son équipement conserve les poids appris. **La case avec l’œil**, dans l’en-tête de la salle, montre le champ de vision, les odeurs et la direction de la boussole ; les repères grisés ne sont visibles que par le joueur.

Les icônes des compteurs et les boutons d’information donnent leur explication au clic. Fermez l’aide avec **×**, **Échap** ou en cliquant ailleurs.

Dans **Évaluation**, **Essayer un exemple** charge un exemple issu d’un entraînement réel. Le rythme **×16** accélère vos propres essais. Les progrès ne sont pas garantis à chaque génération ; **Évaluer sur 20 salles** permet de mesurer les livraisons sans poursuivre l’apprentissage.

Le prototype contient une créature, un butin et un refuge. Les gardes et les équipes ne sont pas encore présents.

## Signaler un problème

Ouvrez une [issue](https://github.com/sinikebe/heistlings-releases/issues) en précisant le canal et la version de l’application, votre version de Windows, l’écran concerné et les étapes permettant de retrouver le problème. Pour le comportement du voleur, ajoutez la salle, les organes et l’accessoire utilisés.

## Mentions tierces

Le jeu utilise [Godot](https://godotengine.org/) et le [launcher de sinikebe](https://github.com/sinikebe/godot-launcher-template). Leurs licences et notices sont intégrées à l’exécutable, consultables via **Mentions légales**, et également disponibles dans les fichiers de release. Ces licences tierces ne constituent pas une licence de publication des sources du jeu.
