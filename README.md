# NutriFit — nutrition, musculation et courses

Application web responsive de suivi nutritionnel, menus, budget et comparaison indicative des courses.

## Lancer l'application
- Extraire l'archive ZIP.
- Ouvrir `index.html` dans Edge, Chrome ou Firefox.
- Les données du profil et de la liste sont enregistrées localement dans le navigateur (`localStorage`) ; elles ne sont pas synchronisées entre appareils.

## Améliorations de la comparaison des prix
- La recherche Open Prices s'effectue à partir du code-barres (EAN) d'un produit personnalisé.
- Les relevés du secteur Carpentras, Pernes-les-Fontaines, Le Pontet et Avignon sont privilégiés ; aucun relevé national n'est présenté comme un prix local.
- Le bouton « Rechercher les prix locaux de ma liste » relance la recherche pour les produits personnalisés avec code-barres présents dans le panier.
- Les prix locaux vérifiés, le nom/adresse du magasin et la date sont affichés quand ces informations sont présentes dans la source.
- Le comparatif distingue le sous-total des prix locaux vérifiés du total indicatif qui peut contenir des estimations ou des prix saisis. Un magasin n'est déclaré moins cher que lorsque tous les produits du panier ont un prix local vérifié pour les magasins comparés.

## Limites importantes
- Open Prices est une base collaborative dont la couverture locale est incomplète. Un relevé peut être ancien et ne garantit pas le prix actuel en rayon.
- Les prix prédéfinis restent des estimations et ne sont pas des prix officiels en direct.
- Les catalogues des enseignes sont des liens externes ; ils ne sont pas importés automatiquement. L'intégration de prix officiels et exhaustifs nécessite des API, flux ou partenariats autorisés des enseignes.
- L'ouverture directe de `index.html` permet de tester l'application, mais le service worker/PWA nécessite un hébergement HTTPS ou localhost.

## Mises à jour
- Le bouton « Vérifier les mises à jour » contrôle le service worker lorsque NutriFit est servi depuis une adresse HTTPS (ou localhost).
- Si tu ouvres `index.html` directement depuis le ZIP (`file://`), les navigateurs bloquent les mises à jour automatiques. Il faut publier une fois l'application sur un hébergement HTTPS ; ensuite, les nouvelles versions pourront être récupérées sans télécharger un nouveau dossier.
