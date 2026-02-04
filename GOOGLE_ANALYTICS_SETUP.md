# Configuration Google Analytics 4 - IN & OUT

## 📊 Guide d'Installation

### Étape 1: Créer un Compte Google Analytics

1. Allez sur [analytics.google.com](https://analytics.google.com)
2. Connectez-vous avec votre compte Google
3. Cliquez sur **"Commencer à mesurer"**

### Étape 2: Configurer la Propriété

1. **Nom du compte**: `IN & OUT`
2. **Nom de la propriété**: `IN & OUT Website`
3. **Fuseau horaire**: `(GMT+01:00) Afrique/Alger`
4. **Devise**: `DZD - Dinar algérien`

### Étape 3: Détails de l'Entreprise

- **Secteur d'activité**: Construction
- **Taille de l'entreprise**: Petite entreprise (1-10 employés)
- **Objectifs**:
  - ✅ Générer des prospects
  - ✅ Examiner le comportement des utilisateurs

### Étape 4: Créer un Flux de Données

1. Sélectionnez **"Web"**
2. **URL du site web**: `https://inout.build`
3. **Nom du flux**: `IN & OUT Production`
4. Cliquez sur **"Créer un flux"**

### Étape 5: Récupérer l'ID de Mesure

Vous allez obtenir un **ID de mesure** au format:
```
G-XXXXXXXXXX
```

### Étape 6: Mettre à Jour le Site

Dans `index.html`, remplacez `G-XXXXXXXXXX` par votre vrai ID:

```html
<!-- Google Analytics 4 -->
<script async src="https://www.googletagmanager.com/gtag/js?id=G-VOTRE-ID-ICI"></script>
<script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());
    gtag('config', 'G-VOTRE-ID-ICI');
</script>
```

**Exemple**:
```javascript
gtag('config', 'G-ABC123DEF4');
```

### Étape 7: Vérifier l'Installation

1. Déployez le site sur Vercel
2. Dans Google Analytics, allez dans **"Rapports en temps réel"**
3. Visitez votre site `https://inout.build`
4. Vous devriez voir votre visite apparaître dans les 30 secondes

## 📈 Événements à Suivre

### Événements Automatiques (Déjà Configurés)
- ✅ Page views
- ✅ Scrolls
- ✅ Clics sortants
- ✅ Recherche sur site
- ✅ Engagement vidéo (si vous ajoutez des vidéos)

### Événements Personnalisés Recommandés

Ajoutez ces événements au script pour un meilleur suivi:

#### 1. Soumission du Formulaire

Modifiez `script.js` ligne 119:

```javascript
// Après showNotification
gtag('event', 'form_submission', {
    'event_category': 'Contact',
    'event_label': 'Contact Form',
    'value': 1
});
```

#### 2. Clic sur Téléphone

```javascript
document.querySelector('a[href^="tel:"]').addEventListener('click', () => {
    gtag('event', 'phone_click', {
        'event_category': 'Contact',
        'event_label': '+213 (0) 770 684 699'
    });
});
```

#### 3. Clic sur Email

```javascript
document.querySelector('a[href^="mailto:"]').addEventListener('click', () => {
    gtag('event', 'email_click', {
        'event_category': 'Contact',
        'event_label': 'fahd@inout.build'
    });
});
```

#### 4. Clic sur Devis

```javascript
document.querySelector('.btn-primary').addEventListener('click', () => {
    gtag('event', 'cta_click', {
        'event_category': 'Engagement',
        'event_label': 'Demander un devis'
    });
});
```

## 📊 Rapports Importants à Suivre

### 1. Acquisition
- **Source du trafic**: D'où viennent vos visiteurs?
- **Canaux**: Direct, Organique, Social, Référent

### 2. Engagement
- **Pages et écrans**: Quelles pages sont les plus visitées?
- **Temps d'engagement**: Combien de temps sur le site?

### 3. Conversions
- **Événements**: Combien de soumissions de formulaire?
- **Taux de conversion**: % de visiteurs qui contactent

### 4. Données Démographiques
- **Pays/Ville**: Algérie, Alger, autres?
- **Appareil**: Mobile, Desktop, Tablette?
- **Navigateur**: Chrome, Safari, etc.

## 🎯 Objectifs à Configurer

Dans Google Analytics, créez ces objectifs:

### 1. Soumission Formulaire
- **Type**: Événement
- **Nom**: `form_submission`
- **Valeur**: 1 prospect

### 2. Clic Téléphone
- **Type**: Événement
- **Nom**: `phone_click`

### 3. Clic Email
- **Type**: Événement
- **Nom**: `email_click`

## 🔒 Confidentialité et RGPD

### Anonymisation IP (Recommandé)
Déjà activé par défaut dans GA4.

### Consentement des Cookies

Ajoutez une bannière de consentement (optionnel mais recommandé):

```html
<!-- Cookie Consent (à ajouter avant </body>) -->
<div id="cookie-consent" style="display: none;">
    <p>Ce site utilise des cookies pour améliorer votre expérience.</p>
    <button onclick="acceptCookies()">Accepter</button>
</div>

<script>
function acceptCookies() {
    localStorage.setItem('cookieConsent', 'true');
    document.getElementById('cookie-consent').style.display = 'none';
}

if (!localStorage.getItem('cookieConsent')) {
    document.getElementById('cookie-consent').style.display = 'block';
}
</script>
```

## 📱 Intégration avec Google Search Console

1. Allez dans **Search Console**: [search.google.com/search-console](https://search.google.com/search-console)
2. Ajoutez `https://inout.build`
3. Vérifiez via Google Analytics (option recommandée)
4. Liez les deux comptes pour avoir les données de recherche

## ✅ Checklist de Vérification

- [ ] Compte Google Analytics créé
- [ ] Propriété GA4 configurée
- [ ] ID de mesure obtenu (G-XXXXXXXXXX)
- [ ] ID remplacé dans index.html
- [ ] Site déployé sur Vercel
- [ ] Vérification en temps réel OK
- [ ] Événements personnalisés ajoutés (optionnel)
- [ ] Objectifs configurés
- [ ] Google Search Console lié

## 🆘 Dépannage

### Analytics ne fonctionne pas?

1. **Vérifiez l'ID**: Assurez-vous que G-XXXXXXXXXX est remplacé
2. **Cache**: Videz le cache du navigateur (Ctrl+F5)
3. **Bloqueur de pub**: Désactivez AdBlock temporairement
4. **Console**: Vérifiez les erreurs dans F12 > Console
5. **Temps**: Attendez 24-48h pour les premiers rapports complets

### Pas de données en temps réel?

1. Visitez le site en navigation privée
2. Vérifiez que JavaScript est activé
3. Attendez 1-2 minutes
4. Rafraîchissez Google Analytics

## 📞 Support

- Documentation GA4: [support.google.com/analytics](https://support.google.com/analytics)
- Communauté: [support.google.com/analytics/community](https://support.google.com/analytics/community)

---

**Dernière mise à jour**: 2024-02-04
**Version Google Analytics**: GA4 (Google Analytics 4)