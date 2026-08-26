# Unlocker → Pennylane Web

Application web Next.js prête à déployer sur Vercel.

## Ce qu'elle fait

- charge directement le lien public Metabase Unlocker via une route serveur ;
- accepte aussi un fichier CSV/XLSX de secours ;
- conserve chaque commission séparément ;
- transforme le TTC en HT ;
- génère les colonnes attendues par le modèle Pennylane ;
- applique la même date d'émission aux lignes du mois ;
- télécharge un fichier `.xlsx`.

## Lancer en local

```bash
npm install
npm run dev
```

Puis ouvrir http://localhost:3000

## Déployer sur Vercel

1. Créer un repository Git avec ce dossier.
2. Importer le repository dans Vercel.
3. Aucun paramètre particulier n'est nécessaire.
4. Cliquer sur Deploy.

## Sécurité

La route `/api/metabase` n'accepte volontairement que les URL commençant par :
`https://bi.unlocker.fr/public/question/`

Cela évite d'utiliser le serveur comme proxy HTTP générique.
