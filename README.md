# Guide d'utilisation de Power BI et Déploiement sur Vercel

Ce guide vous expliquera comment utiliser Power BI pour créer des visualisations de données et comment déployer ces visualisations sur Vercel pour les partager en ligne.

![Sales Data](https://github.com/Ayoub-etoullali/Power-BI-Sales-Website/assets/92756846/e4becc50-f3fc-4b77-abba-69886205ad22)

## Étape 1 : Créer des Visualisations de Données avec Power BI

1. Assurez-vous d'avoir Power BI Desktop installé sur votre ordinateur.

2. Lancez Power BI Desktop.

3. Importez vos données dans Power BI à partir de la source de données de votre choix (Excel, SQL, CSV, etc.).

4. Créez des visualisations de données en glissant et déposant des champs sur le canevas de rapport.

5. Personnalisez vos visualisations en utilisant les outils disponibles dans Power BI Desktop.

6. Enregistrez votre rapport dans un fichier .pbix.

## Étape 2 : Publier votre Rapport sur Power BI Service

1. Accédez à [Power BI Service](https://app.powerbi.com/).

2. Connectez-vous avec votre compte Power BI.

3. Cliquez sur "Publish" dans Power BI Desktop et sélectionnez "To Power BI" pour publier votre rapport en ligne.

4. Vous pouvez maintenant accéder à votre rapport sur Power BI Service.

## Étape 3 : Intégration de Power BI dans Vercel

1. Assurez-vous d'avoir un compte Vercel et d'avoir installé Vercel CLI sur votre ordinateur.

2. Clonez ce dépôt ou créez un nouveau dépôt Git pour votre projet.

3. Dans le répertoire de votre projet Vercel, créez un dossier `public` (si ce n'est pas déjà fait).

4. Exportez votre rapport Power BI sous forme de fichier HTML (File > Export > Power BI Service) et placez-le dans le dossier `public`.

5. Créez un fichier `vercel.json` à la racine de votre projet avec le contenu suivant :

```json
{
  "version": 2,
  "builds": [
    {
      "src": "/public/(.*.html)",
      "use": "@vercel/static"
    }
  ]
}
