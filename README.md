# Linktree Personnalisé

Un linktree moderne et ultra-personnalisable avec vos liens sociaux.

## 🚀 Fonctionnalités

- ✅ Design moderne et responsive
- ✅ Animations fluides en cascade
- ✅ Support pour **9 plateformes** : Site Web, TikTok, X (Twitter), Discord, YouTube, Twitch, Instagram, Email, SoundCloud
- ✅ **Logos SVG officiels** en blanc (personnalisables) pour toutes les plateformes
- ✅ **Personnalisation complète** : texte, images, couleurs, fonds
- ✅ **Images de fond** pour chaque carte de lien
- ✅ **Cartes personnalisables** avec hauteurs ajustables
- ✅ **Background de la carte principale** : solid, gradient, image, glassmorphism
- ✅ **Styles de boutons** : solid, glassmorphism, outline, minimal, gradient
- ✅ **Titre et favicon** personnalisables

## 📝 Configuration Complète

Ouvrez le fichier `script.js` et modifiez l'objet `config` pour personnaliser tout !

### 📄 Titre et Favicon

Personnalisez le titre de la page (onglet du navigateur) et le favicon :

```javascript
page: {
    title: "Mon Linktree",           // Titre de la page (onglet du navigateur)
    favicon: "images/logo.png"        // Chemin vers votre favicon (icône de l'onglet)
}
```

**Exemples :**
```javascript
// Titre personnalisé
title: "Erlow - Linktree"

// Favicon (peut être une image PNG, SVG, ICO, etc.)
favicon: "images/logo-variante.png"
```

### 👤 Profile

```javascript
profile: {
    name: "Votre Nom",              // Texte du nom
    bio: "Votre bio ici",           // Texte de la bio
    picture: "images/logo.png"      // Chemin vers votre photo/logo
}
```

### 🎨 Fond de la page

Choisissez entre **gradient**, **couleur unie**, ou **image** :

```javascript
background: {
    type: "gradient",  // "gradient", "solid", ou "image"
    
    // Si type = "gradient"
    gradient: "linear-gradient(135deg, #667eea 0%, #764ba2 100%)",
    
    // Si type = "solid"
    solidColor: "#667eea",
    
    // Si type = "image"
    image: "images/background.jpg",
    imageSize: "cover"  // "cover", "contain", ou "auto"
}
```

### 🎨 Fond de la carte principale (container)

Choisissez le style de fond pour la carte principale :

```javascript
container: {
    type: "solid",  // "solid", "gradient", "image", ou "glassmorphism"
    
    // Si type = "solid"
    solidColor: "rgba(255, 255, 255, 0.95)",
    
    // Si type = "gradient"
    gradient: "linear-gradient(135deg, rgba(255,255,255,0.9) 0%, rgba(255,255,255,0.8) 100%)",
    
    // Si type = "image"
    image: "images/container-bg.jpg",
    imageSize: "cover",  // "cover", "contain", ou "auto"
    
    // Si type = "glassmorphism"
    glassBlur: "20px",  // Intensité du flou
    glassOpacity: "0.3",  // Opacité du fond
    glassBg: "rgba(255, 255, 255, 0.1)"  // Couleur de base
}
```

### 🎨 Couleurs personnalisées

```javascript
colors: {
    nameColor: "#fff",                                    // Couleur du nom
    bioColor: "#fff",                                    // Couleur de la bio
    avatarBorderColor: "#667eea",                       // Couleur de la bordure de l'avatar
    linkBorderColor: "#e2e8f0",                         // Bordures des liens
    linkHoverGradient: "linear-gradient(135deg, #667eea 0%, #764ba2 100%)"
}
```

### 🎨 Style des boutons/liens

Choisissez le style pour tous les boutons de liens :

```javascript
buttonStyle: {
    type: "glassmorphism",  // "solid", "glassmorphism", "outline", "minimal", "gradient"
    
    // Si type = "solid"
    solidColor: "#ffffff",
    textColor: "#2d3748",  // Couleur du texte
    
    // Si type = "gradient"
    gradient: "linear-gradient(135deg, #667eea 0%, #764ba2 100%)",
    gradientTextColor: "white",  // Couleur du texte
    
    // Si type = "glassmorphism" - TOUTES LES COULEURS PERSONNALISABLES
    glassBlur: "2px",  // Intensité du flou
    glassBg: "rgba(0, 0, 0, 0.2)",  // Couleur de fond
    glassTextColor: "rgba(255, 255, 255, 0.95)",  // Couleur du texte
    glassBorderColor: "rgba(255, 255, 255, 0.3)",  // Couleur de la bordure
    glassHoverBg: "rgba(0, 0, 0, 0.3)",  // Couleur au survol
    
    // Si type = "outline"
    outlineWidth: "2px",
    borderStyle: "solid",  // "solid", "dashed", "dotted"
    outlineTextColor: "#2d3748",  // Couleur du texte
    
    // Si type = "minimal"
    textColor: "#2d3748"  // Couleur du texte
}
```

**Types de styles disponibles :**
- **solid** : Fond coloré uniforme (couleur du texte personnalisable)
- **glassmorphism** : Effet de verre dépoli avec transparence (toutes les couleurs personnalisables : fond, texte, bordure, hover)
- **outline** : Bordure uniquement, fond transparent (couleur du texte personnalisable)
- **minimal** : Aucune bordure ni ombre, très épuré (couleur du texte personnalisable)
- **gradient** : Fond avec dégradé de couleurs (couleur du texte personnalisable)

**💡 Personnalisation des textes :**
Les textes des liens peuvent être modifiés individuellement dans la section `links` de chaque lien (voir section "Configuration des liens").

### 🎨 Logos des applications

Activez les logos SVG officiels en blanc pour remplacer les emojis :

```javascript
icons: {
    useLogos: true,     // true pour utiliser les vrais logos SVG, false pour utiliser les emojis
    logoColor: "#fff"   // Couleur des logos SVG (par défaut: blanc)
}
```

**Plateformes avec logos disponibles :**
- Website, TikTok, X (Twitter), Discord, YouTube, Twitch, Instagram, Email, SoundCloud

### 🔗 Configuration des liens

Chaque lien est entièrement personnalisable :

```javascript
links: {
    website: {
        url: "https://rocket-decals.com",    // URL du lien
        text: "Mon Site Web",                 // Texte affiché
        icon: "🌐",                           // Emoji/icône
        enabled: true,                        // true pour afficher, false pour masquer
        
        // Image de fond pour cette carte (optionnel)
        backgroundImage: "images/website-bg.jpg",
        
        // Rendre la carte plus haute
        tall: true,                           // true pour hauteur standard élevée
        customHeight: "200px"                 // Ou hauteur personnalisée exacte
    },
    instagram: {
        url: "https://www.instagram.com/votre-compte",
        text: "Instagram",
        icon: "📷",
        enabled: true,
        backgroundImage: "",
        tall: false,
        customHeight: ""
    },
    mail: {
        url: "mailto:votre-email@example.com",  // Utilisez mailto: pour les emails
        text: "Email",
        icon: "📧",
        enabled: true,
        backgroundImage: "",
        tall: false,
        customHeight: ""
    },
    soundcloud: {
        url: "https://soundcloud.com/votre-compte",
        text: "SoundCloud",
        icon: "🎵",
        enabled: true,
        backgroundImage: "",
        tall: false,
        customHeight: ""
    }
    // ... même structure pour les autres plateformes (tiktok, x, discord, youtube, twitch)
}
```

### 📐 Exemples de configuration avancée

#### Carte avec image de fond

```javascript
youtube: {
    url: "https://www.youtube.com/@votre-chaine",
    text: "YouTube",
    icon: "▶️",
    enabled: true,
    backgroundImage: "images/youtube-banner.jpg",  // Image de fond
    tall: true,                                      // Carte plus haute
    customHeight: ""                                 // Ou spécifiez "250px"
}
```

#### Carte normale avec texte personnalisé

```javascript
tiktok: {
    url: "https://www.tiktok.com/@mon-compte",
    text: "Suivez-moi sur TikTok ! 🎵",
    icon: "🎵",
    enabled: true,
    backgroundImage: "",  // Pas d'image de fond
    tall: false,
    customHeight: ""
}
```

#### Masquer un lien

```javascript
discord: {
    url: "https://discord.gg/votre-serveur",
    text: "Discord",
    icon: "💬",
    enabled: false,  // Le lien ne sera pas affiché
    backgroundImage: "",
    tall: false,
    customHeight: ""
}
```

#### Exemple : Lien Email (mailto)

```javascript
mail: {
    url: "mailto:contact@example.com",  // Utilisez mailto: pour ouvrir le client de messagerie
    text: "Me contacter",
    icon: "📧",
    enabled: true,
    backgroundImage: "",
    tall: false,
    customHeight: ""
}
```

#### Exemple : Lien Instagram

```javascript
instagram: {
    url: "https://www.instagram.com/votre-compte",
    text: "Suivez-moi sur Instagram",
    icon: "📷",
    enabled: true,
    backgroundImage: "images/instagram-bg.jpg",  // Optionnel : image de fond
    tall: true,
    customHeight: ""
}
```

#### Exemple : Container avec glassmorphism

```javascript
container: {
    type: "glassmorphism",
    glassBlur: "25px",
    glassBg: "rgba(255, 255, 255, 0.15)"
}
```

#### Exemple : Boutons en style glassmorphism avec couleurs personnalisées

```javascript
buttonStyle: {
    type: "glassmorphism",
    glassBlur: "15px",
    glassBg: "rgba(0, 0, 0, 0.2)",        // Fond sombre transparent
    glassTextColor: "rgba(255, 255, 255, 0.95)",  // Texte blanc
    glassBorderColor: "rgba(255, 255, 255, 0.3)",  // Bordure blanche
    glassHoverBg: "rgba(0, 0, 0, 0.4)"    // Fond plus foncé au survol
}
```

#### Exemple : Glassmorphism avec fond clair

```javascript
buttonStyle: {
    type: "glassmorphism",
    glassBlur: "10px",
    glassBg: "rgba(255, 255, 255, 0.3)",     // Fond clair
    glassTextColor: "#2d3748",                // Texte foncé
    glassBorderColor: "rgba(0, 0, 0, 0.1)",   // Bordure foncée
    glassHoverBg: "rgba(255, 255, 255, 0.5)"  // Plus clair au survol
}
```

#### Exemple : Boutons avec bordure (outline)

```javascript
buttonStyle: {
    type: "outline",
    outlineWidth: "2px",
    borderStyle: "dashed"  // ou "solid", "dotted"
}
```

### 📄 Footer

Personnalisez le texte et la couleur du footer :

```javascript
footer: {
    text: "Made by Erlow",      // Changez ce texte pour personnaliser le footer
    textColor: "#718096",       // Couleur du texte (ex: "#fff", "#718096", etc.)
    enabled: true               // true pour afficher, false pour masquer complètement
}
```

**Exemples :**
```javascript
// Texte personnalisé avec couleur blanche
text: "© 2024 Mon Nom",
textColor: "#fff"

// Masquer le footer
enabled: false

// Footer avec couleur personnalisée
text: "Fait avec ❤️",
textColor: "#FF6B6B"
```

## 🖼️ Organisation des images

Créez un dossier `images/` pour organiser vos images :

```
linktree/
├── images/
│   ├── logo.png           # Votre logo/photo de profil
│   ├── logo-variante.png  # Votre favicon (icône de l'onglet)
│   ├── background.jpg     # Image de fond (optionnel)
│   ├── website-bg.jpg     # Image de fond pour le lien "website"
│   ├── youtube-banner.jpg # Image de fond pour YouTube
│   └── ...
├── index.html
├── style.css
└── script.js
```

## 🎨 Personnalisation rapide

**Changer le titre et le favicon :**
- Modifiez `config.page.title` pour le titre de l'onglet
- Modifiez `config.page.favicon` pour l'icône de l'onglet

**Changer le texte :**
- Modifiez `config.profile.name`, `config.profile.bio`
- Modifiez `config.links.*.text` pour chaque lien
- Modifiez `config.footer.text` pour le footer
- Modifiez `config.footer.textColor` pour la couleur du texte du footer

**Changer les images :**
- Modifiez `config.profile.picture` pour votre logo/avatar
- Modifiez `config.page.favicon` pour le favicon de l'onglet
- Modifiez `config.links.*.backgroundImage` pour les images de fond des liens

**Changer les couleurs :**
- Modifiez `config.colors.nameColor` pour la couleur du nom
- Modifiez `config.colors.bioColor` pour la couleur de la bio
- Modifiez `config.colors.avatarBorderColor` pour la couleur de la bordure de l'avatar
- Modifiez `config.icons.logoColor` pour la couleur des logos SVG
- Modifiez `config.buttonStyle.*` pour personnaliser les couleurs des boutons (voir section "Style des boutons")

**Changer le fond :**
- Modifiez `config.background.type` et les valeurs correspondantes
- Modifiez `config.container.type` pour le fond de la carte principale

**Cartes plus hautes avec image :**
- Mettez `backgroundImage: "chemin/vers/image.jpg"` et `tall: true`

## 📱 Utilisation

1. Ouvrez `index.html` dans votre navigateur
2. Ou servez les fichiers avec un serveur web local :
   ```bash
   # Avec Python
   python -m http.server 8000
   
   # Avec Node.js (http-server)
   npx http-server
   ```

## 🌐 Déploiement

Vous pouvez déployer ce linktree sur :
- **GitHub Pages** (gratuit)
- **Netlify** (gratuit)
- **Vercel** (gratuit)
- Ou tout autre hébergeur statique

---

Fait avec ❤️