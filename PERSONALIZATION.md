# Guide de Personnalisation du Portfolio

## 📸 1. Ajouter votre photo de profil

### Étape 1: Préparer votre photo
- Dimensions recommandées: **400x400 px** (carré)
- Format: JPG, PNG ou WebP
- Taille du fichier: Max 2MB (pour meilleure performance)
- Conseils: Photo professionnelle, claire, bien éclairée

### Étape 2: Ajouter la photo
1. **Copiez votre photo** dans le dossier `assets/`
2. **Renommez-la** en `profile.jpg` (ou garder votre nom et modifier le HTML)
3. **Éditez** `index.html` ligne ~100 dans la section "About":
   ```html
   <img src="assets/profile.jpg" alt="Profile Photo" class="profile-img">
   ```
   Remplacez `profile.jpg` par le nom de votre fichier

### Exemple de code
```html
<!-- Votre photo s'affichera ainsi -->
<div class="about-image">
    <img src="assets/profile.jpg" alt="Your Name" class="profile-img">
</div>
```

---

## 📄 2. Ajouter votre CV (PDF)

### Étape 1: Préparer votre CV
- Format: **PDF** (recommandé)
- Alternative: Google Drive, Dropbox, ou hébergé en ligne
- Nommez-le: `cv.pdf` ou `resume.pdf`

### Étape 2: Ajouter le lien
1. **Placez votre CV** dans le dossier `assets/`
2. **Modifier le lien** dans `index.html` (dans la section About):
   ```html
   <a href="assets/cv.pdf" class="btn btn-primary" download>Download My CV</a>
   ```

### Options alternatives pour héberger votre CV

**Option A: Google Drive**
```html
<a href="https://drive.google.com/uc?export=download&id=YOUR_FILE_ID" 
   class="btn btn-primary">Download My CV</a>
```

**Option B: Dropbox**
```html
<a href="https://www.dropbox.com/s/your-file-id/cv.pdf?dl=1" 
   class="btn btn-primary">Download My CV</a>
```

**Option C: GitHub Releases**
- Uploadez votre CV sur GitHub
- Utilisez le lien raw

---

## 🎨 3. Personnaliser le contenu texte

### Éditer les informations personnelles
Ouvrez `index.html` et remplacez:

```html
<!-- Ligne 42 - Héro section -->
<h1 class="hero-title">Welcome to My Portfolio</h1>
<p class="hero-subtitle">I'm a creative developer crafting beautiful and functional web experiences</p>

<!-- Ligne 102 - About section -->
<p>I'm a passionate developer with a keen eye for design...</p>

<!-- Ligne 111 - Contact section -->
<a href="mailto:hello@example.com">hello@example.com</a>
<p>Your City, Country</p>

<!-- Ligne 135 - Footer -->
<p>&copy; 2024 Your Name. All rights reserved.</p>
```

### Éditer les projets
Pour chaque projet (environ ligne 138):
```html
<article class="project-card">
    <div class="project-image">
        <img src="assets/project1.jpg" alt="Project Name">
    </div>
    <div class="project-info">
        <h3 class="project-title">Your Project Name</h3>
        <p class="project-description">Your project description</p>
        <div class="project-tags">
            <span class="tag">Technology1</span>
            <span class="tag">Technology2</span>
        </div>
        <a href="https://project-link.com" class="project-link">View Project →</a>
    </div>
</article>
```

### Éditer les compétences
Section Skills (environ ligne 195):
```html
<div class="skill-category">
    <h3>Your Category</h3>
    <ul>
        <li>Skill 1</li>
        <li>Skill 2</li>
        <li>Skill 3</li>
    </ul>
</div>
```

---

## 🖼️ 4. Ajouter les images des projets

### Préparation des images
- Dimensions recommandées: **600x400 px** (ratio 3:2)
- Format: JPG ou WebP (comprimé)
- Taille: Max 1MB par image
- Nommage: `project1.jpg`, `project2.jpg`, etc.

### Modifier le HTML
Dans chaque projet, remplacez le placeholder:
```html
<!-- AVANT (placeholder) -->
<div class="project-image">
    <div class="image-placeholder"></div>
</div>

<!-- APRÈS (avec image) -->
<div class="project-image">
    <img src="assets/project1.jpg" alt="Project Name">
</div>
```

### Ajouter le CSS pour images
Ajoutez à `css/styles.css`:
```css
.project-image img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    transition: var(--transition);
}

.project-card:hover .project-image img {
    transform: scale(1.05);
}
```

---

## 🎨 5. Personnaliser les couleurs

Ouvrez `css/styles.css` et modifiez les variables au début:

```css
:root {
    /* Couleurs actuelles (exemple) */
    --primary-color: #6366f1;        /* Violet */
    --secondary-color: #ec4899;      /* Rose */
    --text-primary: #1e293b;         /* Texte foncé */
    --background-color: #ffffff;    /* Fond blanc */
}
```

### Exemples de palettes modernes

**Palettes bleus (tech moderne)**
```css
--primary-color: #0ea5e9;    /* Cyan */
--secondary-color: #06b6d4;  /* Cyan foncé */
```

**Palettes vertes (eco/naturel)**
```css
--primary-color: #10b981;    /* Vert */
--secondary-color: #059669;  /* Vert foncé */
```

**Palettes oranges (créatif)**
```css
--primary-color: #f97316;    /* Orange */
--secondary-color: #ea580c;  /* Orange foncé */
```

**Palettes noirs/blancs (minimaliste)**
```css
--primary-color: #000000;    /* Noir */
--secondary-color: #666666;  /* Gris */
```

---

## 📱 6. Personnaliser les réseaux sociaux

Modifiez la section Contact (environ ligne 220):
```html
<div class="social-links">
    <a href="https://linkedin.com/in/yourprofile" class="social-link">LinkedIn</a>
    <a href="https://github.com/yourprofile" class="social-link">GitHub</a>
    <a href="https://twitter.com/yourprofile" class="social-link">Twitter</a>
    <a href="https://instagram.com/yourprofile" class="social-link">Instagram</a>
</div>
```

---

## ✅ Checklist de personnalisation

- [ ] Ajouter photo de profil (`assets/profile.jpg`)
- [ ] Ajouter CV (`assets/cv.pdf`)
- [ ] Remplacer le titre et subtitle du Hero
- [ ] Ajouter votre email et localisation
- [ ] Ajouter vos 3 projets avec descriptions
- [ ] Ajouter images des projets
- [ ] Ajouter vos compétences réelles
- [ ] Changer les couleurs (optionnel)
- [ ] Ajouter vos liens réseaux sociaux
- [ ] Mettre à jour le nom au footer

---

## 🚀 Tester vos modifications

1. **Ouvrez** `index.html` dans votre navigateur
2. **Vérifiez** tous les liens (images, CV, externes)
3. **Testez** sur mobile (F12 → Device mode)
4. **Vérifiez** les formulaires fonctionnent
5. **Testez** le menu mobile (< 768px)

---

## 💡 Conseils professionnels

### Pour les photos
✓ Photo professionnelle (tête-épaules)
✓ Fond neutre ou bleu
✓ Bonne qualité et éclairage
✗ Pas de filtre excessif
✗ Pas de photos trop casuelles

### Pour le CV
✓ 1-2 pages maximum
✓ Bien structuré et clair
✓ Dernières expériences en haut
✓ Adaptez à chaque candidature
✗ Pas d'erreurs orthographiques
✗ Pas de photo floue

### Pour le contenu
✓ Compétences vérifiables
✓ Projets avec liens réels
✓ Descriptions claires et concises
✓ Ton professionnel et engageant
✗ Pas d'exagérations
✗ Pas de typos

---

## 🔗 Listes des emplacements à modifier

| Section | Fichier | Ligne approx |
|---------|---------|--------------|
| Photo | index.html | 100 |
| CV | index.html | 109 |
| Email | index.html | 220 |
| Localisation | index.html | 223 |
| Projets | index.html | 138-190 |
| Compétences | index.html | 195-220 |
| Réseaux | index.html | 227-230 |
| Couleurs | css/styles.css | 1-20 |
| Footer | index.html | 235 |

---

**Besoin d'aide supplémentaire? Consultez le README.md principal!**
