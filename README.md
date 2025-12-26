# 🚗 CovoitApp - Application de Covoiturage Android

[![Kotlin](https://img.shields.io/badge/Kotlin-1.9.0-purple.svg)](https://kotlinlang.org/)
[![Jetpack Compose](https://img.shields.io/badge/Jetpack%20Compose-1.5.4-green.svg)](https://developer.android.com/jetpack/compose)
[![Firebase](https://img.shields.io/badge/Firebase-Latest-orange.svg)](https://firebase.google.com/)
[![Stripe](https://img.shields.io/badge/Stripe-Latest-blue.svg)](https://stripe.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

Application mobile moderne de covoiturage développée en Kotlin avec Jetpack Compose, intégrant Firebase et Stripe pour une expérience utilisateur complète et sécurisée.

---

## 📱 Aperçu

CovoitApp est une application de covoiturage qui permet aux utilisateurs de créer et réserver des trajets, communiquer en temps réel, et effectuer des paiements sécurisés. L'application met l'accent sur la simplicité d'utilisation et la sécurité des transactions.

### 🎥 Vidéo Démo
> 🔗 [Voir la démo complète](LIEN_YOUTUBE_ICI)

---

## ✨ Fonctionnalités

### 🔐 Authentification & Profils
- Inscription et connexion sécurisées via Firebase Authentication
- Profils utilisateurs personnalisables avec photo et biographie
- Système de notes et évaluations ⭐ (sur 5 étoiles)
- Profils conducteurs détaillés et cliquables

### 🚗 Gestion des Trajets
- Création de trajets avec :
  - Lieu de départ et destination
  - Date et heure
  - Prix par personne
  - Nombre de places disponibles
  - Photos du trajet (optionnel)
- Réservation en temps réel
- Historique complet avec 3 onglets :
  - Tous les trajets disponibles
  - Mes trajets créés
  - Historique des trajets passés

### 🔍 Recherche & Filtres
- Recherche par ville de départ/destination
- Filtres avancés :
  - Prix minimum et maximum
  - Date du trajet
  - Nombre de places
- Tri par prix (croissant/décroissant)
- Actualisation par glissement (pull-to-refresh)

### 💳 Paiement Sécurisé
- Intégration Stripe pour les paiements
- Formulaire de carte bancaire sécurisé
- Mode test pour démonstration
- Confirmation de réservation après paiement
- Gestion des remboursements

### 💬 Communication
- Chat en temps réel entre conducteurs et passagers
- Notifications push pour :
  - Nouvelles réservations
  - Messages reçus
  - Confirmations de paiement
  - Rappels de trajets

### 🗺️ Carte Interactive
- Visualisation des trajets sur carte OpenStreetMap
- Calcul d'itinéraire avec OSRM
- Affichage du trajet complet
- Informations de distance et durée

### 🔔 Notifications
- Notifications push en temps réel
- Système de tracking des réservations
- Alertes personnalisées

### 📤 Partage
- Partage de trajets via applications natives
- Intégration avec WhatsApp, Messenger, SMS, etc.

---

## 🛠️ Stack Technique

### **Langage & Framework**
- **Kotlin** - Langage moderne et concis
- **Jetpack Compose** - UI déclarative et réactive
- **Material Design 3** - Interface utilisateur moderne

### **Architecture**
- **MVVM** (Model-View-ViewModel)
- **Repository Pattern** pour l'accès aux données
- **Coroutines** pour la programmation asynchrone
- **StateFlow** pour la gestion d'état réactif

### **Backend & Base de données**
- **Firebase Authentication** - Gestion des utilisateurs
- **Cloud Firestore** - Base de données NoSQL en temps réel
- **Firebase Storage** - Stockage des images
- **Firebase Cloud Messaging** - Notifications push

### **Paiements**
- **Stripe Android SDK** - Traitement des paiements
- **Stripe Payment Intents** - Sécurisation des transactions

### **Cartes & Navigation**
- **OpenStreetMap** - Affichage des cartes
- **OSRM (Open Source Routing Machine)** - Calcul d'itinéraires
- **osmdroid** - Bibliothèque Android pour OSM

### **Dépendances principales**
```gradle
// Jetpack Compose
implementation("androidx.compose.ui:ui:1.5.4")
implementation("androidx.compose.material3:material3:1.1.2")
implementation("androidx.navigation:navigation-compose:2.7.5")

// Firebase
implementation("com.google.firebase:firebase-auth-ktx:22.3.0")
implementation("com.google.firebase:firebase-firestore-ktx:24.10.0")
implementation("com.google.firebase:firebase-storage-ktx:20.3.0")
implementation("com.google.firebase:firebase-messaging-ktx:23.4.0")

// Stripe
implementation("com.stripe:stripe-android:20.37.0")

// Maps
implementation("org.osmdroid:osmdroid-android:6.1.14")

// Image Loading
implementation("io.coil-kt:coil-compose:2.5.0")

// Coroutines
implementation("org.jetbrains.kotlinx:kotlinx-coroutines-android:1.7.3")
```

---

## 📂 Structure du Projet

```
CovoitApp/
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/covoitapp/
│   │   │   │   ├── ui/
│   │   │   │   │   ├── theme/           # Thème Material Design 3
│   │   │   │   │   ├── AuthScreens.kt   # Connexion/Inscription
│   │   │   │   │   ├── HomeScreen.kt    # Liste des trajets
│   │   │   │   │   ├── CreateTripScreen.kt
│   │   │   │   │   ├── PaymentScreen.kt # Paiement Stripe
│   │   │   │   │   ├── ChatScreen.kt
│   │   │   │   │   ├── MapScreen.kt
│   │   │   │   │   ├── ProfileScreen.kt
│   │   │   │   │   ├── RatingScreen.kt
│   │   │   │   │   └── ...
│   │   │   │   ├── data/
│   │   │   │   │   ├── FirebaseRepository.kt
│   │   │   │   │   ├── AuthManager.kt
│   │   │   │   │   └── models/
│   │   │   │   │       ├── Trajet.kt
│   │   │   │   │       ├── User.kt
│   │   │   │   │       ├── Message.kt
│   │   │   │   │       └── Reservation.kt
│   │   │   │   ├── services/
│   │   │   │   │   ├── NotificationService.kt
│   │   │   │   │   └── OSRMService.kt
│   │   │   │   ├── Navigation.kt
│   │   │   │   ├── Routes.kt
│   │   │   │   └── MainActivity.kt
│   │   │   └── res/
│   │   └── ...
│   └── build.gradle.kts
├── gradle/
└── build.gradle.kts
```

---

## 🚀 Installation & Configuration

### Prérequis
- Android Studio Hedgehog ou supérieur
- JDK 17+
- Compte Firebase
- Compte Stripe (mode test)
- SDK Android minimum : API 26 (Android 8.0)

### Configuration Firebase

1. **Créez un projet Firebase** sur [console.firebase.google.com](https://console.firebase.google.com)

2. **Activez les services nécessaires :**
   - Authentication (Email/Password)
   - Cloud Firestore
   - Firebase Storage
   - Cloud Messaging

3. **Téléchargez `google-services.json`**
   - Placez-le dans `app/`

4. **Règles Firestore** (à configurer dans Firebase Console) :
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /trajets/{trajetId} {
      allow read: if true;
      allow write: if request.auth != null;
    }
    match /users/{userId} {
      allow read: if true;
      allow write: if request.auth != null && request.auth.uid == userId;
    }
    match /messages/{messageId} {
      allow read, write: if request.auth != null;
    }
    match /reservations/{reservationId} {
      allow read, write: if request.auth != null;
    }
  }
}
```

### Configuration Stripe

1. **Créez un compte** sur [stripe.com](https://stripe.com)

2. **Récupérez vos clés API** (mode test) depuis le Dashboard

3. **Créez `local.properties`** à la racine du projet :
```properties
sdk.dir=CHEMIN_VERS_ANDROID_SDK
STRIPE_PUBLISHABLE_KEY=pk_test_xxxxx
STRIPE_SECRET_KEY=sk_test_xxxxx
```

⚠️ **Important** : Ne commitez JAMAIS `local.properties` sur Git !

### Compilation

1. **Clonez le repository** :
```bash
git clone https://github.com/olirobz31/CovoitApp.git
cd CovoitApp
```

2. **Ouvrez avec Android Studio**

3. **Synchronisez Gradle** :
   - File → Sync Project with Gradle Files

4. **Lancez l'application** :
   - Run → Run 'app'

---

## 📸 Captures d'écran

> 🖼️ *Screenshots à ajouter*

| Écran d'accueil | Paiement Stripe | Chat |
|:---:|:---:|:---:|
| ![Home](screenshots/home.png) | ![Payment](screenshots/payment.png) | ![Chat](screenshots/chat.png) |

| Carte | Profil | Historique |
|:---:|:---:|:---:|
| ![Map](screenshots/map.png) | ![Profile](screenshots/profile.png) | ![History](screenshots/history.png) |

---

## 🧪 Mode Test

L'application est actuellement configurée en **mode test** :

### Paiements Stripe
Utilisez la carte test suivante :
- **Numéro** : `4242 4242 4242 4242`
- **Date** : n'importe quelle date future (ex: 12/28)
- **CVV** : n'importe quel code à 3 chiffres (ex: 123)
- **Nom** : n'importe quel nom

### Comptes de test
Pour tester l'application, vous pouvez créer des comptes avec n'importe quelle adresse email.

---

## 🔒 Sécurité

### Bonnes pratiques implémentées
- ✅ Authentification Firebase sécurisée
- ✅ Règles Firestore pour contrôler l'accès aux données
- ✅ Clés API Stripe stockées dans `local.properties` (non versionné)
- ✅ Validation des données côté client et serveur
- ✅ Chiffrement des communications (HTTPS)

### Pour la production
- [ ] Implémenter Firebase Functions pour traiter les paiements côté serveur
- [ ] Passer Stripe en mode production
- [ ] Activer le plan Blaze de Firebase
- [ ] Configurer ProGuard pour obfusquer le code
- [ ] Implémenter le signature d'APK

---

## 🚦 Roadmap

### ✅ Terminé (v1.0)
- [x] Authentification utilisateurs
- [x] Création et réservation de trajets
- [x] Paiement Stripe
- [x] Chat en temps réel
- [x] Notifications push
- [x] Carte interactive
- [x] Système de notation

### 🔜 Prévu (v1.1)
- [ ] Backend Firebase Functions pour Stripe
- [ ] Mode production
- [ ] Publication sur Google Play (Internal Testing)
- [ ] Système de vérification d'identité
- [ ] Mode sombre
- [ ] Support multilingue (FR/EN)

### 💡 Idées futures (v2.0)
- [ ] Trajets récurrents
- [ ] Partage de frais automatique
- [ ] Intégration calendrier
- [ ] Statistiques utilisateur
- [ ] Programme de fidélité
- [ ] Version iOS

---

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 👤 Auteur

**Olivier** - [olirobz31](https://github.com/olirobz31)

📧 Email : olirobz31@gmail.com  
🌐 Site web : [https://olirobz31.github.io/covoitapp-site/](https://olirobz31.github.io/covoitapp-site/)

---

## 🙏 Remerciements

- [Firebase](https://firebase.google.com/) pour le backend
- [Stripe](https://stripe.com/) pour les paiements
- [OpenStreetMap](https://www.openstreetmap.org/) pour les cartes
- [Material Design](https://m3.material.io/) pour les guidelines UI
- La communauté Android pour les ressources et tutoriels

---

## 📞 Support

Pour toute question ou problème :
- 📧 Email : olirobz31@gmail.com
- 🌐 Site web : [CovoitApp](https://olirobz31.github.io/covoitapp-site/contact.html)
- 🐛 Issues : [GitHub Issues](https://github.com/olirobz31/CovoitApp/issues)

---

## ⭐ Si ce projet vous plaît

N'hésitez pas à mettre une étoile ⭐ sur le repository et à le partager !

---

<p align="center">
  Fait avec ❤️ à Toulouse, France
</p>
