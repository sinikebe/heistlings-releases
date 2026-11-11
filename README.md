# Heistlings — téléchargements

Heistlings est un prototype où de petites créatures apprennent à explorer des salles et récupérer un butin. Vous faites grandir votre voleur, lancez son entraînement et observez ce qu’il a appris.

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

Un seul voleur est disponible. Dans **Campagne**, les cinq défis proposent des salles sans obstacle intérieur ni refuge. Les dimensions comptent les cases jouables ; une bordure s’ajoute autour. Le ramassage termine immédiatement l’essai. Les positions distinctes départ/butin sont toutes évaluées dans un ordre fixe, avec un cerveau figé par tentative.

| Défi | Cases jouables | Référence / limite | Évaluations | Récompense de complétion |
|---|---|---|---|---|
| 1.1 | 2 × 2 | 5 / 25 actions | 12 | Toucher |
| 1.2 | 2 × 3 | 8 / 28 | 30 | Fil d’Ariane 0 |
| 1.3 | 4 × 3 | 24 / 44 | 132 | Fil d’Ariane 1 |
| 1.4 | 6 × 4 et 4 × 6 | 48 / 68 | 1 104 | Fil d’Ariane 2 |
| 1.5 | 8 × 6 | 80 / 100 | 2 256 | Un neurone en réserve |

La **complétion** exige 100 % de ramassages à la limite et ouvre le défi suivant. L’**efficacité** exige au moins 70 % sous le seuil de référence ; en 1.4, cette étoile s’appelle **Adaptation** et ce taux doit être atteint dans chacune des deux orientations. Le **perfect bleu** exige 100 % sous la référence. Efficacité et perfect donnent chacun **20 XP**, une seule fois par défi : 200 XP au maximum. Les cinq perfects débloquent la **Vue 0**, qui distingue mur et butin sur la case devant le voleur. Les défis rejoués conservent leurs restrictions de sens, y compris le 2 × 2 sans toucher.

Le fil est l’unique accessoire du chapitre : niveau 0, une visite antérieure sur la case actuelle ; niveau 1, zéro/une/deux visites antérieures ou davantage ; niveau 2, traces sur les quatre voisines. Les traces repartent de zéro par simulation. Un mouvement bloqué ou une attente ne compte pas comme une entrée et ne change pas le signal de la visite actuelle. Le replay montre les traces, les perceptions et les activations du cerveau enregistré.

L’éditeur du cerveau devient disponible dès l’accès au défi 1.3. Un neurone coûte 100 XP. Ses nouvelles connexions sortantes commencent à zéro pour conserver les décisions apprises. Les gains d’entraînement restent très lents : 1 XP par 10 millions d’actions réellement simulées ; les évaluations et replays n’en rapportent pas. Les étoiles ne peuvent pas être récoltées plusieurs fois.

Dans **Entraînement**, choisir le défi à préparer, puis ajuster actions, simulations, récompense de butin et vitesse dans le panneau de droite. Les changements restent en brouillon jusqu’à **Appliquer**. L’entraînement tire départ et butin sur toutes les cases libres ; les évaluations restent exhaustives et fixes. Le cerveau et les graphiques du replay sont accessibles dès le début. Les vitesses ×1/×4/×16 et les pauses de lecture restent indépendantes de l’apprentissage.

Quand une boucle est prouvée, le replay s’arrête plus tôt et affiche **Boucle détectée** avant de passer au suivant. Le résultat et le nombre d’actions comptabilisées restent ceux de la simulation complète.

Le calcul utilise 50 % du budget disponible par défaut ; l’éclair Boost demande le maximum en préservant l’interface. Les paramètres CPU/GPU proposent Désactivé, Auto et Forcé. Le calcul Vulkan utilise les mêmes visites, capteurs et salles que le CPU ; la campagne reste évaluée sur CPU. Ce partage concerne le moteur de simulation, pas un quota global de tous les cœurs du PC.

Le [guide de premier essai](https://github.com/sinikebe/heistlings-releases/releases/download/branch-dev/README.md) décrit les récompenses et commandes. Les expériences historiques sont documentées séparément dans le dépôt de recherche privé.

## Signaler un problème

Ouvrez une [issue](https://github.com/sinikebe/heistlings-releases/issues) en précisant le canal et la version de l’application, votre version de Windows, l’écran concerné et les étapes permettant de retrouver le problème. Pour le comportement du voleur, ajoutez la salle, les organes et l’accessoire utilisés.

## Mentions tierces

Le jeu utilise [Godot](https://godotengine.org/) et le [launcher de sinikebe](https://github.com/sinikebe/godot-launcher-template). Leurs licences et notices sont intégrées à l’exécutable, consultables via **Mentions légales**, et également disponibles dans les fichiers de release. Ces licences tierces ne constituent pas une licence de publication des sources du jeu.
