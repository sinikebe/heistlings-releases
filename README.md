# Heistlings — téléchargements

Heistlings est un prototype de jeu où de petites créatures apprennent à récupérer
un butin et revenir au refuge. Vous préparez les exercices, lancez l'entraînement
et observez les comportements qui apparaissent.

Ce dépôt est destiné aux versions Windows à télécharger. Les sources du jeu sont
conservées dans un dépôt privé.

## Télécharger et jouer

Consultez [les versions disponibles](https://github.com/sinikebe/heistlings-releases/releases).
La [préversion de développement](https://github.com/sinikebe/heistlings-releases/releases/tag/branch-dev)
sert aux essais. Si aucune version n'apparaît encore, la première publication est
en préparation.

1. Dans les fichiers de la release, téléchargez l'archive **Heistlings…Windows.zip**.
2. Extrayez tout le ZIP dans un dossier où vous pouvez écrire.
3. Ouvrez **Heistlings.exe**, puis choisissez **Entrer dans le labo**.

Vous n'avez pas besoin d'installer Godot ni de créer un compte. Le guide inclus dans
l'archive explique les commandes. Les fichiers `Source code` proposés automatiquement
par GitHub contiennent la documentation de ce dépôt ; utilisez le ZIP Windows pour jouer.

Le launcher peut récupérer les mises à jour du canal de votre version lorsqu'elles
sont disponibles. Les versions de développement suivent `branch-dev` et utilisent
des sauvegardes distinctes des futures versions stables. Le fichier
`content-desktop.pck` est destiné au mécanisme de mise à jour ; le ZIP suffit à
l'installation du jeu.

## Premier essai

Cliquez sur **Exemple entraîné** pour observer immédiatement une créature issue d'un
entraînement réel. Pour commencer votre propre expérience, choisissez un exercice,
lancez l'entraînement et essayez **×16**. **Comparer au début** permet de voir ce qui
a changé. **Évaluer sur 20 salles** mesure le réseau observé sans poursuivre son
apprentissage.

Le prototype utilise un réseau neuronal dont les poids évoluent entre les
générations. Les progrès ne sont pas garantis à chaque génération. Il comprend
une créature, un butin, un refuge et trois familles de salles ; les gardes et les
équipes ne sont pas encore présents.

Les premières expériences atteignent 69,2 % de livraisons en moyenne sur cinq
entraînements. Le seuil de fiabilité visé n'est atteint que sur trois essais sur
cinq : ce prototype reste en développement. Le bilan et la provenance du modèle
d'exemple accompagnent les téléchargements.

## Signaler un problème

Ouvrez une [issue](https://github.com/sinikebe/heistlings-releases/issues) en précisant
la version téléchargée, votre version de Windows, l'exercice et les étapes permettant
de retrouver le problème. Le numéro de salle et une capture sont utiles pour un
problème de comportement.

## Mentions tierces

Le jeu utilise [Godot](https://godotengine.org/) et le
[launcher de sinikebe](https://github.com/sinikebe/godot-launcher-template).
Leurs licences et notices sont incluses dans l'archive. Ces licences tierces
ne constituent pas une licence de publication des sources du jeu.
