# 🌐 Site Web CovoitApp

Site web officiel de l'application de covoiturage CovoitApp.

## 🚀 Déploiement sur GitHub Pages

### Étape 1 : Créer un repository GitHub

1. Allez sur [GitHub](https://github.com)
2. Cliquez sur le bouton **"New repository"** (en vert)
3. Nom du repository : `covoitapp-site`
4. Cochez **"Public"**
5. Cliquez sur **"Create repository"**

### Étape 2 : Uploader les fichiers

**Option A : Via l'interface web GitHub (plus simple)**

1. Sur la page de votre repository vide, cliquez sur **"uploading an existing file"**
2. Glissez-déposez TOUS les fichiers :
   - `index.html`
   - `privacy.html`
   - `terms.html`
   - `contact.html`
   - `style.css`
3. Cliquez sur **"Commit changes"**

**Option B : Via Git en ligne de commande**

```bash
cd covoitapp-site
git init
git add .
git commit -m "Premier commit - Site web CovoitApp"
git branch -M main
git remote add origin https://github.com/VOTRE_USERNAME/covoitapp-site.git
git push -u origin main
```

### Étape 3 : Activer GitHub Pages

1. Dans votre repository, cliquez sur **"Settings"** (⚙️)
2. Dans le menu de gauche, cliquez sur **"Pages"**
3. Sous **"Source"**, sélectionnez **"Deploy from a branch"**
4. Sous **"Branch"**, sélectionnez **"main"** et **"/ (root)"**
5. Cliquez sur **"Save"**

### Étape 4 : Attendre le déploiement

- Attendez 1-2 minutes
- Rafraîchissez la page
- Vous verrez un message : **"Your site is live at https://VOTRE_USERNAME.github.io/covoitapp-site/"**

## ✅ Votre site est en ligne !

**URL de votre site :**
```
https://VOTRE_USERNAME.github.io/covoitapp-site/
```

### Pages disponibles :
- 🏠 Accueil : `https://VOTRE_USERNAME.github.io/covoitapp-site/`
- 🔒 Politique de confidentialité : `https://VOTRE_USERNAME.github.io/covoitapp-site/privacy.html`
- 📜 Conditions d'utilisation : `https://VOTRE_USERNAME.github.io/covoitapp-site/terms.html`
- 📧 Contact : `https://VOTRE_USERNAME.github.io/covoitapp-site/contact.html`

## 📝 Modifier le contenu

Pour modifier le site après publication :

1. Retournez sur GitHub
2. Cliquez sur le fichier à modifier
3. Cliquez sur l'icône crayon ✏️
4. Faites vos modifications
5. Cliquez sur **"Commit changes"**
6. Le site sera automatiquement mis à jour en 1-2 minutes

## 🎨 Personnalisation

### Changer les couleurs

Ouvrez `style.css` et modifiez les variables :

```css
:root {
    --primary-color: #6200EA;      /* Couleur principale */
    --primary-dark: #4B00B5;       /* Couleur principale foncée */
    --secondary-color: #00BFA5;    /* Couleur secondaire */
}
```

### Ajouter des screenshots

1. Créez un dossier `images/` dans votre repository
2. Uploadez vos captures d'écran
3. Dans `index.html`, ajoutez dans la section Features :

```html
<img src="images/screenshot1.png" alt="CovoitApp Screenshot" style="max-width: 100%; border-radius: 12px;">
```

## 📱 Utilisation pour Google Play

Quand vous soumettrez CovoitApp sur Google Play, utilisez ces URLs :

- **Privacy Policy URL :** `https://VOTRE_USERNAME.github.io/covoitapp-site/privacy.html`
- **Terms & Conditions URL :** `https://VOTRE_USERNAME.github.io/covoitapp-site/terms.html`
- **Website URL :** `https://VOTRE_USERNAME.github.io/covoitapp-site/`

## 📧 Activer le formulaire de contact (optionnel)

Le formulaire de contact utilise actuellement un placeholder. Pour l'activer :

1. Créez un compte sur [Formspree](https://formspree.io) (gratuit)
2. Créez un nouveau formulaire
3. Copiez l'URL du formulaire
4. Dans `contact.html`, remplacez :
   ```html
   <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Par votre URL Formspree

## 🔧 Support

Pour toute question : olirobz31@gmail.com

---

**© 2025 CovoitApp - Toulouse, France**
