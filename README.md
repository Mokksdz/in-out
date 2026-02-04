# IN & OUT by Elfartas - Landing Page

Site web moderne et responsive pour IN & OUT, entreprise de construction, rénovation et aménagement.

## 🚀 Déploiement sur Vercel

### Méthode 1: Via l'interface Vercel (Recommandé)

1. Créez un compte sur [Vercel](https://vercel.com)
2. Installez Vercel CLI:
   ```bash
   npm install -g vercel
   ```
3. Dans le dossier du projet, exécutez:
   ```bash
   vercel login
   vercel
   ```
4. Suivez les instructions à l'écran

### Méthode 2: Via GitHub

1. Créez un repository GitHub
2. Poussez votre code sur GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin [URL_DE_VOTRE_REPO]
   git push -u origin main
   ```
3. Connectez votre repository à Vercel:
   - Allez sur [vercel.com](https://vercel.com)
   - Cliquez sur "New Project"
   - Importez votre repository GitHub
   - Cliquez sur "Deploy"

### Méthode 3: Déploiement rapide

```bash
# Installer Vercel CLI
npm install -g vercel

# Se connecter
vercel login

# Déployer
vercel --prod
```

## 📁 Structure du projet

```
In&Out site/
│
├── index.html                  # Page principale
├── styles.css                  # Styles CSS
├── script.js                   # Scripts JavaScript
├── logo_inout.svg              # Logo principal
├── logo_inout_fond_vert.svg    # Logo pour footer
├── vercel.json                 # Configuration Vercel
├── package.json                # Configuration npm
├── robots.txt                  # Directives pour les robots
├── sitemap.xml                 # Plan du site pour SEO
├── .htaccess                   # Configuration Apache (optionnel)
└── README.md                   # Ce fichier
```

## ✨ Fonctionnalités

### Design & UX
- ✅ Design moderne et professionnel
- ✅ 100% responsive (mobile, tablette, desktop)
- ✅ Animations fluides et interactives
- ✅ Loading screen avec animation
- ✅ Navigation smooth scroll
- ✅ Menu mobile avec hamburger

### Formulaire de contact
- ✅ Validation en temps réel
- ✅ Integration mailto
- ✅ États de chargement
- ✅ Messages de notification
- ✅ Champs obligatoires marqués

### SEO
- ✅ Meta tags complets (Open Graph, Twitter Cards)
- ✅ Sitemap.xml
- ✅ Robots.txt
- ✅ Favicon optimisé
- ✅ URLs et structure sémantique

### Accessibilité (WCAG 2.1)
- ✅ Navigation au clavier
- ✅ Skip to content link
- ✅ ARIA labels et roles
- ✅ Focus styles visibles
- ✅ Structure HTML5 sémantique
- ✅ Contraste des couleurs optimisé

### Performance
- ✅ CSS et JS optimisés
- ✅ Images SVG légères
- ✅ Cache navigateur
- ✅ Compression gzip

## 🎨 Personnalisation

### Couleurs

Les couleurs principales sont définies dans `styles.css`:

```css
:root {
    --primary-color: #1a7f64;
    --primary-dark: #155a47;
    --primary-light: #2a9d7a;
}
```

### Contenu

Modifiez le fichier `index.html` pour changer:
- Textes
- Services
- Informations de contact

## 📱 Contact

Pour toute question, contactez:
- Email: contact@inout.build
- Site: inout.build

## 📄 Licence

MIT License - IN & OUT by Elfartas © 2024
