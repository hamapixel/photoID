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
- **QR d'identité professionnelle** : génère un lien ouvrant la fiche du salarié (nom, entreprise, fonction, matricule, validité) et se met à jour quand un champ change. Un bouton permet de créer un nouveau matricule aléatoire.
- **Design premium optimisé pour la lisibilité** : photo de l'employé découpée en cercle au recto, nom/fonction et matricule mieux contrastés et agrandis, police sans-serif soignée, matricule lisible sur les deux faces, QR de matricule présent sur le recto et le verso, en horizontal comme en vertical.
- **Logo d’entreprise mis en valeur** : plaque blanche à coins arrondis dans l’en-tête, zone logo agrandie et recentrage des images avec marges transparentes ou blanches (l’image originale n’est pas modifiée).
- **Crédit BTDIGIT au verso** : « Créé par BTDIGIT » et `hamapixel.github.io/nexora-technologies/` sur les deux orientations de badge. Le pied de page du logiciel renvoie aussi au site [BTDIGIT](https://hamapixel.github.io/nexora-technologies/).
- Cartes de visite : **4 modèles Prestige, Corporate, Minimal et Luxe**, choix avec miniatures cliquables, couleurs personnalisables, logo, recto et verso cliquables, format 90 × 50 mm
- Impression de badges et cartes de visite en **recto-verso sur deux pages A4**, à l'échelle 100 %, avec choix de feuille portrait/paysage, quantité et positions miroirs pour l'alignement au découpage
- Interface entièrement en français, adaptée aux PC et aux mobiles

## Essayer les nouveaux modèles

1. Ouvrez l'atelier **Cartes de visite**.
2. Cliquez sur l'un des quatre modèles : **Prestige**, **Corporate**, **Minimal** ou **Luxe**.
3. Modifiez le nom, le poste, les coordonnées, le logo et la couleur du thème.
4. Cliquez sur les miniatures **Recto** et **Verso** pour voir les deux faces de la carte avant impression.
5. Téléchargez une face en PNG ou créez la planche A4 recto-verso. L'export PNG est généré à 300 DPI.

Le logiciel travaille dans le navigateur sans compte et les logos importés ne sont pas envoyés vers un backend PhotoID.

## Lecture de l'identité professionnelle via le QR

Le QR code intégré au badge ouvre la page **https://hamapixel.github.io/photoID/i.html** avec les informations du titulaire encodées dans le lien.

1. Dans **Badges entreprise**, renseignez le nom, la fonction, l'entreprise, le matricule et la validité.
2. Cliquez sur **Tester la fiche QR** pour voir exactement la page qui s'ouvrira après le scan.
3. Cliquez sur **Copier le lien** pour partager ou tester depuis un téléphone.
4. Exportez le badge en PNG ou imprimez-le : le **même QR code dynamique** apparaît au recto et au verso, horizontal ou vertical.
5. Scannez avec l'appareil photo d'un smartphone connecté à Internet.

La fiche présente **nom, fonction, entreprise, matricule, validité** et un avatar avec initiales. **La photo n'est pas publiée**. La page est une simple lecture des champs du badge, **pas une authentification**. Elle peut être créée ou modifiée par une personne ayant accès au logiciel, puisqu'il n'existe pas de registre central ni de signature numérique des fiches.

La bibliothèque [qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) est incluse sous licence MIT dans `vendor/qrcode-generator.js` avec le fichier `vendor/LICENSE.qrcode-generator.txt`. La génération et l'impression du QR se font localement, mais **ouvrir la fiche web nécessite Internet**. Le lien transporte les champs professionnels du badge ; quiconque possède le lien peut les consulter. Le fragment du lien n'est pas transmis à un serveur PhotoID pour stockage. Les logos et photos importés ne sont pas envoyés à la fiche.

Le bouton « Générer un nouveau matricule » utilise un identifiant aléatoire, mais son unicité entre tous les salariés et entreprises n'est pas garantie sans base de données.

**Lisibilité :** testez le QR après impression sur une vraie carte, particulièrement avec un nom de société ou une fonction très longue. Un QR dense peut être difficile à scanner à la taille CR80.

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
