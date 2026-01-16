# 🚀 Guide de Déploiement et Utilisation - La Bergerie d'Urcy

## 📦 Ce que vous avez

Votre site complet avec **interface d'administration** pour gérer :
- ✅ Statut des ventes (Ouvert/Fermé)
- ✅ Dates de retrait (calendrier)
- ✅ Produits et prix
- ✅ Informations de contact
- ✅ **Sans toucher au code !**

---

## 🎯 DÉPLOIEMENT SUR NETLIFY (15 minutes)

### Étape 1 : Préparer les fichiers

Vous avez reçu un dossier `bergerie-urcy/` contenant :
```
bergerie-urcy/
├── index.html (votre site)
├── admin/
│   ├── index.html (interface admin)
│   └── config.yml (configuration)
├── content/
│   ├── ventes.json (dates et statut)
│   ├── produits.json (colis et prix)
│   └── contact.json (vos infos)
└── images/
    └── logo.png (votre logo)
```

### Étape 2 : Créer un compte GitHub (gratuit)

1. Allez sur **https://github.com**
2. Cliquez sur **"Sign up"**
3. Créez votre compte avec l'email : **earlbossong@gmail.com**
4. Confirmez votre email

### Étape 3 : Créer un repository

1. Cliquez sur le **+** en haut à droite → **"New repository"**
2. Remplissez :
   - **Repository name** : `bergerie-urcy`
   - **Description** : "Site de vente directe - La Bergerie d'Urcy"
   - Cochez **"Public"**
   - Cochez **"Add a README file"**
3. Cliquez sur **"Create repository"**

### Étape 4 : Uploader vos fichiers

1. Dans votre repository, cliquez sur **"Add file"** → **"Upload files"**
2. Glissez-déposez **TOUT le contenu** du dossier `bergerie-urcy/` :
   - Le fichier `index.html`
   - Le dossier `admin/` (avec tout son contenu)
   - Le dossier `content/` (avec les 3 fichiers JSON)
   - Le dossier `images/` (avec votre logo)
3. En bas, écrivez : "Premier déploiement du site"
4. Cliquez sur **"Commit changes"**

✅ **Vos fichiers sont maintenant sur GitHub !**

### Étape 5 : Connecter à Netlify

1. Allez sur **https://www.netlify.com**
2. Cliquez sur **"Sign up"**
3. Choisissez **"Sign up with GitHub"**
4. Autorisez Netlify à accéder à votre GitHub
5. Une fois connecté, cliquez sur **"Import from Git"**
6. Sélectionnez **GitHub**
7. Cherchez et sélectionnez votre repository **"bergerie-urcy"**
8. Cliquez sur **"Deploy site"**

⏳ **Attendez 1-2 minutes...**

🎉 **Votre site est en ligne !**

### Étape 6 : Personnaliser l'URL

1. Dans Netlify, cliquez sur **"Site settings"**
2. **"Site details"** → **"Change site name"**
3. Entrez : `bergerie-urcy` ou `la-bergerie-urcy`
4. **Save**

✅ **Votre site est maintenant accessible à** : `https://bergerie-urcy.netlify.app`

---

## 🔧 CONFIGURER L'INTERFACE ADMIN (5 minutes)

### Étape 7 : Activer Netlify Identity

1. Dans votre site Netlify, allez dans **"Identity"** (menu de gauche)
2. Cliquez sur **"Enable Identity"**
3. Dans **"Registration preferences"**, choisissez **"Invite only"** (pour sécuriser)
4. Allez dans **"Services"** → **"Git Gateway"**
5. Cliquez sur **"Enable Git Gateway"**

### Étape 8 : S'inviter comme admin

1. Toujours dans **"Identity"**, cliquez sur **"Invite users"**
2. Entrez votre email : **earlbossong@gmail.com**
3. Cliquez sur **"Send"**
4. **Allez dans votre boîte mail** et cliquez sur le lien d'invitation
5. Créez votre mot de passe admin

✅ **Vous êtes maintenant administrateur !**

---

## 🎛️ UTILISER L'INTERFACE ADMIN

### Accéder à l'admin

Allez sur : **`https://bergerie-urcy.netlify.app/admin`**

Connectez-vous avec votre email et mot de passe.

### Interface de gestion

Vous voyez 3 sections :

#### 1️⃣ **Gestion des Ventes**

Cliquez sur **"Gestion des Ventes"**

Vous pouvez :
- **Statut des commandes** : Choisir "Ouvertes" ou "Fermées"
- **Message prochaine vente** : Ex: "Mars 2026" ou "Samedi 15 mars 2026"
- **Dates de retrait disponibles** : 
  - Cliquez sur **"Add dates_retrait"**
  - Entrez : "Samedi 15 mars 2026 - 9h-12h"
  - Ajoutez autant de dates que vous voulez
  - Supprimez une date en cliquant sur la ❌

**Après modification, cliquez sur "Publish" en haut à droite !**

#### 2️⃣ **Produits et Prix**

Cliquez sur **"Produits et Prix"**

Vous pouvez :
- Modifier le nom d'un colis
- Changer le poids
- **Modifier les prix**
- Ajouter/supprimer des lignes de détails
- Ajouter un nouveau colis entier

**Exemple** : Pour changer le prix du Colis Découverte de 85€ à 90€
1. Cliquez sur le colis
2. Modifiez "Prix (€)" : 90
3. Cliquez sur **"Publish"**

**Le site est mis à jour automatiquement !**

#### 3️⃣ **Informations de Contact**

Cliquez sur **"Informations de Contact"**

Vous pouvez modifier :
- Adresse de la ferme
- Email
- Téléphone
- Labels et certifications

**Cliquez sur "Publish" pour sauvegarder.**

---

## 📧 CONFIGURER FORMSPREE (Emails de commande)

### Dernière étape : Recevoir les commandes par email

1. Allez sur **https://formspree.io**
2. Créez un compte gratuit avec **earlbossong@gmail.com**
3. Cliquez sur **"+ New Form"**
4. Nommez-le : "Commandes Bergerie"
5. Vous obtenez un **ID** comme : `xyzabc123`

### Ajouter l'ID à votre site

**MÉTHODE 1 : Via l'interface GitHub (recommandé)**

1. Retournez sur votre repository GitHub
2. Cliquez sur le fichier **`index.html`**
3. Cliquez sur l'icône **crayon** (Edit)
4. Cherchez (Ctrl+F) : `VOTRE_ID_FORMSPREE`
5. Remplacez par votre vrai ID : `xyzabc123`
6. En bas : **"Commit changes"**

**MÉTHODE 2 : Via Netlify CMS**

1. Dans l'admin Netlify CMS, allez dans **"Workflow"**
2. Cliquez sur **"Media"**
3. Uploadez une nouvelle version de index.html avec l'ID modifié

⏳ **Attendez 2-3 minutes**

✅ **Le formulaire fonctionne ! Vous recevez maintenant les commandes par email.**

---

## 🎨 WORKFLOW D'UNE VENTE TYPE

### 📅 2 semaines avant

1. Connectez-vous à l'admin : `votre-site.com/admin`
2. Allez dans **"Gestion des Ventes"**
3. Ajoutez vos **dates de retrait**
4. Changez le **statut** à **"Ouvertes"**
5. Cliquez sur **"Publish"**

🎉 Le site affiche maintenant "✅ Commandes ouvertes" !

### 📥 Pendant la période de commande

- Les clients commandent via le formulaire
- Vous recevez chaque commande par email
- Vous pouvez voir les commandes dans votre compte Formspree

### 🔒 3 jours avant le retrait

1. Retournez dans l'admin
2. Changez le statut à **"Fermées"**
3. Mettez à jour "Message prochaine vente" : "Avril 2026"
4. **Publish**

Le site affiche : "🔒 Commandes fermées - Prochaine vente : Avril 2026"

### 📅 Jour du retrait

- Imprimez la liste des commandes depuis votre email
- Cochez au fur et à mesure

---

## 🎯 AVANTAGES DE CETTE SOLUTION

✅ **Aucun code à toucher** - tout se fait via l'interface  
✅ **Gratuit à 100%** (Netlify + Formspree + GitHub)  
✅ **Professionnel** - logo, couleurs personnalisées  
✅ **Mobile-friendly** - parfait sur smartphone  
✅ **Sécurisé** - HTTPS automatique  
✅ **Rapide** - mise à jour en 2 minutes  

---

## 📱 PARTAGER VOTRE SITE

### Créer un QR Code

1. Allez sur **qr-code-generator.com**
2. Collez votre URL : `https://bergerie-urcy.netlify.app`
3. Téléchargez le QR code
4. Imprimez-le sur vos flyers !

### Liens à partager

- **Site principal** : https://bergerie-urcy.netlify.app
- **Admin** : https://bergerie-urcy.netlify.app/admin (à garder secret !)

---

## 🆘 DÉPANNAGE

### "Je ne peux pas me connecter à l'admin"

- Vérifiez que vous avez bien activé Netlify Identity
- Vérifiez que vous avez accepté l'invitation par email
- Essayez de réinitialiser votre mot de passe

### "Les modifications ne s'affichent pas"

- Attendez 2-3 minutes après avoir cliqué sur "Publish"
- Videz le cache : Ctrl+F5
- Vérifiez dans GitHub que le fichier a bien été modifié

### "Je ne reçois pas les commandes par email"

- Vérifiez vos spams
- Vérifiez que l'ID Formspree est correct dans index.html
- Testez une commande test depuis le site

### "J'ai oublié mon mot de passe admin"

1. Allez sur votre site `/admin`
2. Cliquez sur "Forgot password?"
3. Suivez les instructions par email

---

## 🎁 BONUS : AJOUTER UN NOM DE DOMAINE

Si vous voulez **www.bergerie-urcy.fr** au lieu de `.netlify.app` :

1. Achetez un nom de domaine chez **OVH** ou **Gandi** (~12€/an)
2. Dans Netlify : **"Domain settings"** → **"Add custom domain"**
3. Suivez les instructions pour configurer les DNS
4. Attendez 24-48h

Netlify gère automatiquement le certificat HTTPS !

---

## 📞 CONTACT

Pour toute question sur cette solution :
- GitHub : repository "bergerie-urcy"
- Netlify Support : https://www.netlify.com/support/
- Formspree Help : https://help.formspree.io

---

## ✅ CHECKLIST FINALE

Avant d'annoncer le site à vos clients :

- [ ] Site déployé sur Netlify
- [ ] URL personnalisée configurée
- [ ] Netlify Identity activé
- [ ] Compte admin créé
- [ ] Connexion à l'admin testée
- [ ] Formspree configuré
- [ ] ID Formspree ajouté à index.html
- [ ] Commande test envoyée et reçue
- [ ] Dates de vente ajoutées
- [ ] QR code créé
- [ ] Site testé sur mobile

---

## 🎉 FÉLICITATIONS !

Vous avez maintenant un site professionnel avec une interface d'administration complète !

**Temps total de setup : 20-25 minutes**  
**Coût : 0€/an**  
**Gestion future : 2 minutes par vente**  

C'est parti ! 🚀

---

*Guide créé le 15 janvier 2026*  
*Version 1.0 - Solution complète Netlify CMS*