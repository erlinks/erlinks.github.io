# 🖼️ Guide d'Optimisation des Images

## Problème actuel
Les images PNG peuvent être très lourdes et ralentir le chargement de votre site.

## ✅ Solutions mises en place

### 1. **Préchargement des images critiques**
Le site précharge maintenant automatiquement les images importantes (logo, backgrounds).

### 2. **Loader animé**
Un indicateur de chargement s'affiche pendant que les images se chargent.

### 3. **Optimisations CSS**
- Accélération matérielle (GPU)
- Background placeholder pendant le chargement

---

## 📝 Comment compresser vos images

### Option 1 : Outils en ligne (Facile) ⭐ RECOMMANDÉ

**TinyPNG** (gratuit)
1. Allez sur https://tinypng.com
2. Glissez-déposez vos images PNG
3. Téléchargez les versions compressées
4. Remplacez les anciennes images dans le dossier `images/`

**Squoosh** (gratuit, par Google)
1. Allez sur https://squoosh.app
2. Uploadez votre image
3. Choisissez le format **WebP** ou **MozJPEG** (beaucoup plus léger que PNG)
4. Ajustez la qualité (80-85% recommandé)
5. Téléchargez

### Option 2 : Convertir en WebP (Plus léger, moderne)

WebP réduit la taille des fichiers de **25-35%** par rapport au PNG !

**Sur Squoosh.app :**
1. Uploadez votre PNG
2. Changez le format en sortie vers **WebP**
3. Qualité : 80-85
4. Téléchargez

**Ensuite, mettez à jour votre config dans `script.js` :**
```javascript
profile: {
    picture: "images/logo-variante.webp"  // .webp au lieu de .png
}
```

### Option 3 : Logiciels

- **GIMP** (gratuit) - Exporter avec compression
- **ImageOptim** (Mac, gratuit)
- **FileOptimizer** (Windows, gratuit)

---

## 🎯 Tailles recommandées

| Image | Dimensions | Poids max |
|-------|-----------|-----------|
| Logo/Avatar | 240x240px | < 50 KB |
| Background page | 1920x1080px | < 200 KB |
| Background container | 800x1000px | < 100 KB |
| Background card | 400x200px | < 50 KB |

---

## 🚀 Résultat attendu

Après optimisation de vos images :
- ✅ Chargement **2-5x plus rapide**
- ✅ Moins de données consommées
- ✅ Meilleure expérience utilisateur
- ✅ Meilleur référencement Google (SEO)

---

## 📊 Vérifier la taille actuelle de vos images

### Windows :
Clic droit sur l'image → Propriétés → Détails

### En ligne :
Utilisez https://www.websiteplanet.com/webtools/imagecompressor/

---

## ⚠️ Important

- **Gardez toujours une copie** de vos images originales
- Testez le résultat après compression
- Si l'image est floue, augmentez légèrement la qualité

---

## 🔄 Checklist d'optimisation

- [ ] Compresser `logo.png` et `logo-variante.png` (< 50 KB chacun)
- [ ] Compresser `bg.png` (< 200 KB)
- [ ] Compresser `website-bg.png` (< 100 KB)
- [ ] Optionnel : Convertir en WebP pour encore plus de performances
- [ ] Tester le site après remplacement des images

---

💡 **Astuce Pro :** Utilisez WebP pour les backgrounds et gardez PNG uniquement pour le logo si besoin de transparence.

