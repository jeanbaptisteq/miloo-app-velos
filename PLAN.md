# Application Tablette Vendeur Miloo

## Summary
Créer une application HTML hors-ligne, utilisable directement sur tablette, pour présenter les 7 familles de vélos Miloo issues des brochures: Mighty, Classy, Cargo, Adventure, Maverick, Xplorer et Classy Infinite by Nespresso.  
L’app servira de fiche vendeur complète: sélection rapide du vélo, variantes 25/45 km/h, arguments client, specs clés, prix/options, accessoires recommandés et accès aux PDF sources.

## Key Changes
- Créer une page HTML autonome, par exemple `app_velos_miloo.html`, avec CSS et JavaScript intégrés pour pouvoir l’ouvrir sans serveur.
- Structurer les données vélos dans le fichier HTML sous forme d’objet JavaScript: famille, variantes, vitesse, prix, moteur, batterie, autonomie, freins, roues, poids/charge si disponible, points forts, usages recommandés, options et accessoires.
- Utiliser les brochures dans `sources/brochures/` comme source commerciale/technique principale, et compléter avec `sources/website/back_office_bike.md` pour les prix, options configurateur et produits liés.
- Ajouter une navigation tablette:
  - grille de sélection des 7 familles;
  - onglets ou boutons 25/45 km/h quand une variante existe;
  - sections “Pitch client”, “Specs clés”, “Comparer 25 vs 45”, “Options/accessoires”, “PDF”.
- Garder une interface dense, claire et orientée vente: gros boutons tactiles, contraste lisible, zéro landing page, contenu directement exploitable avec un client.
- Inclure des liens locaux vers les PDF brochures/manuels correspondants pour consultation détaillée.

## Public Interfaces / Files
- Nouveau fichier principal: `app_velos_miloo.html`.
- Sources utilisées:
  - `sources/brochures/*.pdf`
  - `sources/website/back_office_bike.md`
- Aucun serveur requis; l’app s’ouvre directement dans un navigateur via le fichier HTML.

## Test Plan
- Ouvrir `app_velos_miloo.html` dans le navigateur et vérifier que les 7 familles apparaissent.
- Tester la sélection de chaque vélo et chaque variante 25/45 disponible.
- Vérifier que les sections vendeur affichent des informations cohérentes et lisibles sur tablette.
- Vérifier que les liens vers les brochures PDF locales fonctionnent.
- Contrôler l’affichage responsive sur largeur tablette et mobile: pas de texte coupé, pas de chevauchement, boutons tactiles utilisables.

## Assumptions
- Les “7 vélos” correspondent aux 7 familles brochure: Mighty, Classy, Cargo, Adventure, Maverick, Xplorer, Classy Infinite/Nespresso.
- Le format choisi est un HTML hors-ligne autonome.
- Le contenu attendu est une fiche vendeur complète, pas seulement une fiche technique.
- Les prix/options du fichier back-office peuvent compléter les brochures quand les PDF ne donnent pas un prix actuel.
