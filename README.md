# Modern Box Records — site GitHub Pages
Site statique responsive, sans abonnement, sans compilation ni dépendance externe. Les fichiers HTML fonctionnent même sans JavaScript.

## Publication
1. Créer un dépôt GitHub public, par exemple `modernbox-bands`.
2. Décompresser l’archive et déposer LE CONTENU du dossier `modernboxrecords` à la racine du dépôt (index.html doit être directement à la racine). Inclure `.nojekyll` et `CNAME`.
3. Settings → Pages → Deploy from a branch → main → / (root) → Save.
4. Custom domain : `bands.modernboxrecords.org`, puis Save.
5. Chez le gestionnaire DNS de modernboxrecords.org, créer :
   - Type : CNAME
   - Nom / hôte : bands
   - Cible : VOTRE-COMPTE-GITHUB.github.io
   - TTL : valeur par défaut
   La cible est le compte ou l’organisation propriétaire du dépôt. Ne mettre ni https:// ni chemin ni nom de dépôt. Supprimer uniquement les enregistrements concurrents sur `bands` s’il en existe.
6. Quand la vérification DNS aboutit, activer Enforce HTTPS. La propagation et l’émission du certificat peuvent prendre jusqu’à 24 h.
7. Vérifier https://bands.modernboxrecords.org/ et les trois pages groupes.

Configurer le domaine dans GitHub AVANT le DNS. La vérification de propriété du domaine dans les paramètres du compte GitHub est recommandée : suivre le TXT exact fourni par GitHub.
Documentation : https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site

## Modifier le contenu
- Accueil : index.html ; groupes : groupes/deftoons.html, schmok.html, vector.html.
- Style : assets/style.css. Les visuels graphiques sont des placeholders CSS, pas des photos de musiciens.
- Remplacer `art(groupe)` dans les pages HTML par `<img src="../assets/photo-groupe.webp" alt="..." width="1200" height="900">` ; à l’accueil, chemin `assets/...`. Ajouter une règle CSS pour adapter les photos à la grille.
- Remplacer les textes entre crochets. Les biographies proposées sont à valider par les groupes.
- Pour les réseaux, remplacer les spans `.pending` par de vrais liens `<a href="URL_VERIFIEE">Instagram ↗</a>`. Instagram et YouTube pour les trois, TikTok uniquement Vector.
- Pour les vidéos, préférer une miniature locale reliée à YouTube ; ne pas créer de faux lecteur.
- Documents : modèles Markdown et plans SVG dans presse/. Les remplacer par des PDF validés et mettre les liens des pages à jour.
- Ne publier des dates qu’une fois confirmées. Adapter les mentions légales aux informations officielles de Radioleg.
- Adresse email conservée EXACTEMENT telle que fournie : modernborecords@gmail.com (sans x).
- Nom public conservé : Vector, et non Vector100k.

## Contenus prioritaires
1. Pour chaque groupe : photo horizontale HD + crédit, biographie validée, ville, prénoms et rôles.
2. Une vidéo live convaincante par groupe et un lien d’écoute si disponible.
3. Comptes Instagram et YouTube ; TikTok pour Vector.
4. Fiche technique validée, patch, plan de scène et contact régie.
5. PDF presse, logo et photos HD téléchargeables.
6. Concerts confirmés et coordonnées officielles Radioleg.

## Référencement
Titres, descriptions, canonical, Open Graph, image de partage, favicon, robots.txt et sitemap.xml inclus. La présence dans Google n’est pas immédiate ni garantie ; après publication, soumettre le sitemap dans Search Console. Les placeholders doivent être remplacés pour obtenir des pages utiles et crédibles.

## Aperçu local
Ouvrir index.html dans un navigateur, ou lancer `python3 -m http.server 8000` dans ce dossier puis ouvrir http://localhost:8000 .
