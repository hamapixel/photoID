# PhotoID Studio Premium — BTDIGIT

Application web gratuite pour créer des **photos d’identité**, **badges professionnels** et **cartes de visite**.

## Ouvrir le logiciel

Quand GitHub Pages est activé, rendez-vous sur :

**https://hamapixel.github.io/photoID/**

## Fonctionnalités

- Photos d'identité : import, choix des formats 35 × 45 mm, quantité de photos, impression A4 ou 10 × 15 cm, export PNG
- Cadrage du visage assisté par MediaPipe
- Détourage du fond par IA avec @imgly/background-removal
- Badges salariés : logo, nom, fonction, matricule, portrait, formats horizontal 86 × 54 mm et vertical 54 × 86 mm, recto employé et verso entreprise cliquables
- Cartes de visite : modèles, logo, recto et verso cliquables, format 90 × 50 mm
- Impression de badges et cartes de visite en **recto-verso sur deux pages A4**, à l'échelle 100 %, avec choix de feuille portrait/paysage, quantité et positions miroirs pour l'alignement au découpage
- Interface entièrement en français, adaptée aux PC et aux mobiles

## Impression recto-verso

1. Dans **Badges entreprise** ou **Cartes de visite**, cliquez sur **Recto** ou **Verso** pour prévisualiser et personnaliser une face.
2. Choisissez le format de la feuille **A4 Portrait** ou **A4 Paysage**, puis le nombre d'exemplaires.
3. Cliquez sur **Recto-verso A4 / PDF**. La fenêtre propose **deux pages**, recto puis verso. Imprimez en duplex, **retournement sur les bords longs**, échelle 100 %, sans ajustement.
4. Si nécessaire, choisissez **Enregistrer au format PDF** dans le dialogue d'impression. Testez avec une feuille ordinaire avant d'imprimer sur carte ou papier épais.

**Important :** selon l'imprimante et ses marges, un décalage de quelques millimètres peut se produire. Vérifiez les deux faces et les repères avant découpe.

## Hébergement gratuit avec GitHub Pages

1. Ouvrez les [paramètres GitHub Pages du dépôt](https://github.com/hamapixel/photoID/settings/pages).
2. Dans **Build and deployment**, choisissez **Deploy from a branch**.
3. Sélectionnez **main** et **/(root)**, puis **Save**.
4. Après la publication, ouvrez [PhotoID Studio Premium](https://hamapixel.github.io/photoID/).

Le dépôt contient déjà `index.html` à sa racine, aucun serveur ou build n'est requis.

## Confidentialité et limites

L'édition et les exports sont effectués dans le navigateur : les images importées ne sont pas envoyées vers un backend PhotoID. Le cadrage et le détourage nécessitent le téléchargement de bibliothèques et de modèles externes au premier usage, donc Internet. Aucun compte ni base de données n'est requis.

**Attention :** une photo destinée à un document officiel doit respecter les normes du pays et de l'administration. Les résultats du détourage IA doivent être vérifiés. Pour des usages commerciaux, vérifiez les conditions de licence de [@imgly/background-removal](https://github.com/imgly/background-removal-js), notamment AGPL.

## Licence

Le code propre à PhotoID Studio Premium est fourni ici pour consultation et utilisation. Les bibliothèques tierces conservent leurs licences respectives.
