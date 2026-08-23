# MatinikStats

Plateforme de stats basket pour la Martinique — prototype front-end (données
fictives, aucun backend pour l'instant).

## Lancer en local

```bash
npm install
npm run dev
```
Puis ouvrir http://localhost:5173

## Compiler pour la mise en ligne

```bash
npm run build
```
Ça crée un dossier `dist/` avec le site prêt à héberger (HTML/CSS/JS statiques).

## Mettre en ligne (Vercel, le plus simple)

1. Pousser ce dossier sur un dépôt GitHub (voir plus bas)
2. Aller sur vercel.com, se connecter avec GitHub
3. "Add New Project" → choisir ce dépôt → Vercel détecte Vite tout seul → Deploy
4. Le site est en ligne sur une URL `xxx.vercel.app`, avec possibilité de brancher
   un vrai nom de domaine ensuite dans les réglages du projet

Netlify fonctionne quasiment pareil si préféré.

## Pousser sur GitHub avec `gh` (GitHub CLI)

```bash
# 1. Se connecter (ouvre le navigateur, pas de mot de passe à taper)
gh auth login

# 2. Depuis ce dossier, créer le dépôt et pousser en un coup
git init
git add .
git commit -m "Premier commit MatinikStats"
gh repo create matinikstats --public --source=. --remote=origin --push
```

## État actuel — important à savoir

- Toutes les données (clubs, joueurs, matchs) sont **générées à la volée** dans
  le navigateur à chaque chargement — rien n'est sauvegardé nulle part.
- Les 20 clubs martiniquais (noms, communes, salles) sont réels ; joueurs et
  matchs sont fictifs.
- Pas de login, pas de base de données, pas de connexion à la pipeline
  PIX4TEAM 2 — c'est l'étape suivante, pas celle-ci.
