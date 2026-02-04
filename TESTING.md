# Guide de Test - IN & OUT Website

## ✅ Tests à effectuer

### 1. Navigation
- [ ] Le logo ramène à l'accueil
- [ ] Tous les liens de navigation fonctionnent (Qui sommes-nous, Services, Contact)
- [ ] Le scroll est fluide (smooth scroll)
- [ ] Le menu mobile s'ouvre et se ferme correctement
- [ ] Le header se cache/affiche au scroll

### 2. Responsive Design
- [ ] **Desktop** (1920px+) : Layout à 2 colonnes, tous les éléments visibles
- [ ] **Tablet** (768px-1024px) : Layout adapté, images redimensionnées
- [ ] **Mobile** (320px-767px) : Menu hamburger, layout 1 colonne
- [ ] Les images ne débordent pas
- [ ] Les textes sont lisibles sur tous les écrans

### 3. Formulaire de Contact
- [ ] La validation des champs obligatoires fonctionne
- [ ] L'email est validé en temps réel
- [ ] Le message d'erreur s'affiche si email invalide
- [ ] Le bouton se désactive pendant l'envoi
- [ ] Le texte du bouton change pendant l'envoi
- [ ] La notification de succès s'affiche
- [ ] Le formulaire se réinitialise après envoi
- [ ] Le client email s'ouvre avec les données du formulaire

### 4. Accessibilité
- [ ] Navigation au clavier (Tab) fonctionne
- [ ] Le lien "Skip to content" apparaît au focus (Tab)
- [ ] Les focus sont visibles (bordure verte)
- [ ] Les images ont des attributs alt
- [ ] Les formulaires ont des labels corrects
- [ ] ARIA attributes présents (vérifier dans le code)
- [ ] Contraste des couleurs suffisant

### 5. Performance
- [ ] Le loading screen s'affiche au chargement
- [ ] Le loading screen disparaît après 800ms
- [ ] Les animations sont fluides (pas de lag)
- [ ] Le site charge en moins de 3 secondes
- [ ] Les images SVG se chargent rapidement

### 6. SEO
- [ ] Le titre de la page est correct
- [ ] La meta description est présente
- [ ] Les meta tags Open Graph sont présents (vérifier le code source)
- [ ] Le favicon s'affiche dans l'onglet
- [ ] robots.txt est accessible : `/robots.txt`
- [ ] sitemap.xml est accessible : `/sitemap.xml`

### 7. Compatibilité Navigateurs
Tester sur :
- [ ] Chrome (dernière version)
- [ ] Firefox (dernière version)
- [ ] Safari (dernière version)
- [ ] Edge (dernière version)
- [ ] Mobile Safari (iOS)
- [ ] Chrome Mobile (Android)

### 8. Interactions
- [ ] Le hover sur les boutons fonctionne
- [ ] Les cartes de services ont un effet au hover
- [ ] Les liens du footer ont un effet au hover
- [ ] Les animations au scroll se déclenchent correctement
- [ ] Les transitions sont fluides

## 🐛 Bugs Connus
Aucun bug connu pour le moment.

## 📝 Notes
- Le formulaire utilise `mailto:` qui ouvre le client email par défaut
- Pour une vraie intégration backend, remplacer par une API
- Le site est optimisé pour Vercel mais fonctionne sur n'importe quel hébergeur

## 🔗 URLs de Test
- Production : `https://in-out.vercel.app`
- GitHub : `https://github.com/Mokksdz/in-out`

## 📊 Outils de Test Recommandés
- **Lighthouse** (Chrome DevTools) : Performance, SEO, Accessibilité
- **WAVE** : Test d'accessibilité
- **PageSpeed Insights** : Performance Google
- **Mobile-Friendly Test** : Test responsive Google
- **W3C Validator** : Validation HTML/CSS