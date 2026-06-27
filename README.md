🕵️ Undercover
Jeu de déduction sociale à jouer entre amis avec un seul téléphone.
👉 Jouer en ligne ← remplace avec ton URL après déploiement
---
🎮 Comment jouer
Principe
Un joueur parmi vous est Undercover : il reçoit un mot proche mais différent des autres.
Les autres joueurs sont des Civils : ils ont tous le même mot.
En mode Mr White : un joueur supplémentaire n'a aucun mot et doit bluffer.
Déroulement
Entrez les noms des joueurs sur l'écran d'accueil.
Choisissez le mode (Classique ou Mr White).
Lancez la partie.
Chaque joueur prend le téléphone à son tour, appuie sur la carte pour voir son mot en secret, puis passe.
Une fois tous les mots révélés, débattez et votez pour éliminer l'Undercover !
Règles
Civils : décrivez votre mot sans le dire directement.
Undercover : bluffez pour ne pas être repéré.
Mr White : essayez de deviner le mot des civils pour survivre.
---
🚀 Lancer le projet en local
Option 1 – Ouvrir directement (le plus simple)
```bash
# Télécharger le projet
git clone https://github.com/ton-pseudo/undercover.git
cd undercover

# Ouvrir dans le navigateur (double-clic ou :)
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```
> ✅ Aucune installation requise. L'appli fonctionne directement dans le navigateur.
Option 2 – Serveur local (recommandé pour éviter les restrictions CORS)
Avec Python :
```bash
python3 -m http.server 8080
# → http://localhost:8080
```
Avec Node.js :
```bash
npx serve .
# → http://localhost:3000
```
---
🌐 Déployer sur GitHub Pages
Étape 1 – Créer le dépôt GitHub
Allez sur github.com et créez un nouveau dépôt nommé `undercover`.
Cochez "Public" (requis pour GitHub Pages gratuit).
Étape 2 – Envoyer les fichiers
```bash
git init
git add .
git commit -m "🕵️ Initial commit — Undercover"
git branch -M main
git remote add origin https://github.com/TON-PSEUDO/undercover.git
git push -u origin main
```
Étape 3 – Activer GitHub Pages
Dans votre dépôt GitHub → Settings → Pages.
Dans Source, sélectionnez Deploy from a branch.
Branch : `main` / Folder : `/ (root)`.
Cliquez Save.
Attendez ~1 minute → votre jeu est en ligne sur :  
`https://ton-pseudo.github.io/undercover/`
---
📁 Structure du projet
```
undercover/
├── index.html          # Page principale
├── css/
│   └── style.css       # Styles (design sombre, mobile-first)
├── js/
│   ├── words.js        # 120+ paires de mots
│   └── game.js         # Logique du jeu
└── README.md
```
---
✨ Fonctionnalités
✅ Mobile-first — conçu pour un téléphone
✅ 120+ paires de mots intégrées
✅ Mode Classique (1 Undercover)
✅ Mode Mr White (1 Undercover + 1 Mr White sans mot)
✅ Mélange aléatoire des rôles à chaque partie
✅ Joueurs personnalisables (ajout / suppression)
✅ Animation flip card lors de la révélation
✅ Sécurité — le mot est caché avant de passer le téléphone
✅ Aucune installation — fonctionne hors ligne une fois chargé
---
🛠️ Personnalisation
Ajouter des paires de mots
Ouvrir `js/words.js` et ajouter des lignes dans le tableau `WORD_PAIRS` :
```js
["Votre mot civil", "Votre mot undercover"],
```
Changer les joueurs par défaut
Dans `js/game.js`, modifier la ligne :
```js
players: ['Damien', 'Lucas', 'Maxime', 'Mathis'],
```
---
📝 Licence
Projet open source libre d'utilisation — faites-en ce que vous voulez !
