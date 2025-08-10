# 🏛️ Générateur de Documents Officiels - Los Santos

Un système web complet pour générer des documents officiels PDF pour votre serveur GTA RP sur FiveM. Compatible LSPD et EMS avec authentification sécurisée.

## 🚀 Fonctionnalités

### 👮‍♂️ Documents LSPD
- **Rapport d'incident** - Documentation complète des incidents
- **Procès-verbal d'arrestation** - Formulaire d'arrestation officiel
- **Contravention routière** - Amendes et infractions routières
- **Mandat de perquisition** - Documents légaux de perquisition
- **Rapport d'enquête** - Suivi détaillé des enquêtes

### 🚑 Documents EMS
- **Rapport médical** - Interventions médicales complètes
- **Certificat de décès** - Documentation officielle des décès
- **Évaluation psychiatrique** - Évaluations de santé mentale
- **Ordonnance médicale** - Prescriptions médicamenteuses
- **Rapport d'ambulance** - Rapports de transport d'urgence

## 🔐 Sécurité

### Système d'authentification
- **Comptes LSPD** : Accès sécurisé pour les forces de l'ordre
- **Comptes EMS** : Accès dédié au personnel médical
- **Sessions isolées** : Chaque département a ses propres documents

### Comptes par défaut
**LSPD:**
```
Username: badge1234 | Password: lspd123
Username: john.smith | Password: police456
Username: sarah.connor | Password: lspd789
```

**EMS:**
```
Username: dr001 | Password: ems123
Username: jane.doe | Password: medical456
Username: mike.johnson | Password: ems789
```

## 📋 Installation

### Option 1: GitHub Pages (Recommandé)
1. **Fork ce repository**
2. **Activez GitHub Pages**
   - Allez dans Settings > Pages
   - Source: Deploy from a branch
   - Branch: main / root
3. **Accédez à votre site** : `https://votre-username.github.io/nom-du-repo`

### Option 2: Hébergement local
```bash
# Clonez le repository
git clone https://github.com/votre-username/gta-rp-documents.git

# Naviguez dans le dossier
cd gta-rp-documents

# Ouvrez avec un serveur local
python -m http.server 8000
# ou
npx serve .
```

## ⚙️ Configuration

### Personnaliser les identifiants
Modifiez l'objet `credentials` dans le fichier HTML :

```javascript
const credentials = {
    lspd: {
        'votre_badge': 'votre_mot_de_passe',
        'badge_numero': 'mot_de_passe_secure'
    },
    ems: {
        'id_medecin': 'mot_de_passe_ems',
        'dr_nom': 'password_medical'
    }
};
```

### Personnaliser l'apparence
- **Couleurs LSPD** : Modifiez les classes `.btn-lspd` et `.auth-tab.lspd.active`
- **Couleurs EMS** : Modifiez les classes `.btn-ems` et `.auth-tab.ems.active`
- **Logo** : Ajoutez votre logo du serveur dans la section header

### Ajouter des types de documents
```javascript
// Dans l'objet documentTypes
nouveauDocument: {
    id: 'nouveau_document',
    title: 'Nouveau Document',
    description: 'Description du nouveau document'
}
```

## 🎨 Fonctionnalités avancées

### ✨ Interface moderne
- **Design glassmorphism** avec effets de transparence
- **Animations fluides** et transitions CSS
- **Responsive design** compatible mobile/desktop
- **Thème sombre/bleu** professionnel

### 📄 Génération PDF
- **Numérotation automatique** des documents
- **En-têtes officiels** avec logos départementaux
- **Mise en page professionnelle**
- **Export haute qualité**

### 🔄 Fonctionnalités temps réel
- **Aperçu instantané** des documents
- **Validation des formulaires**
- **Sauvegarde temporaire** des données
- **Interface intuitive**

## 📱 Compatibilité

### Navigateurs supportés
- ✅ Chrome/Edge (Chromium) 88+
- ✅ Firefox 85+
- ✅ Safari 14+
- ✅ Mobile (iOS Safari, Chrome Mobile)

### Technologies utilisées
- **HTML5** - Structure moderne
- **CSS3** - Styles avancés et animations
- **JavaScript ES6+** - Logique interactive
- **jsPDF** - Génération de PDF côté client

## 🛠️ Développement

### Structure du projet
```
/
├── index.html          # Application principale
├── README.md          # Documentation
└── assets/            # (optionnel) Images et ressources
```

### Ajouter de nouvelles fonctionnalités
1. **Nouveau type de document** : Ajoutez dans `documentTypes`
2. **Nouveau formulaire** : Créez une fonction `createNouveauForm()`
3. **Génération de contenu** : Ajoutez `generateNouveauContent()`
4. **Ajoutez dans le switch** de `previewDocument()`

## 🚨 Sécurité en production

⚠️ **IMPORTANT** : Les identifiants sont stockés côté client pour la démonstration.

### Pour la production :
1. **Backend sécurisé** : Implémentez une API d'authentification
2. **Base de données** : Stockez les utilisateurs en base
3. **HTTPS obligatoire** : Chiffrement des communications
4. **Tokens JWT** : Authentification robuste

## 🎯 Utilisation pour votre serveur

### Intégration Discord
- **Webhooks** : Notifications automatiques des nouveaux documents
- **Commandes bot** : Accès direct via commandes Discord
- **Liens rapides** : Intégration dans vos channels dédiés

### Suggestions d'amélioration
- **Base de données** : Stockage permanent des documents
- **Recherche avancée** : Filtres par date, type, officier
- **Signatures numériques** : Authentification renforcée
- **Templates personnalisés** : Modèles spécifiques au serveur

## 📞 Support

### Problèmes courants
- **PDF ne se génère pas** : Vérifiez que jsPDF est chargé
- **Authentification échoue** : Vérifiez les identifiants dans le code
- **Design cassé** : Videz le cache du navigateur

### Contributions
1. Fork le projet
2. Créez une branche (`git checkout -b feature/nouvelle-fonctionnalite`)
3. Committez (`git commit -am 'Ajout nouvelle fonctionnalité'`)
4. Push (`git push origin feature/nouvelle-fonctionnalite`)
5. Créez une Pull Request

## 📜 Licence

Ce projet est sous licence MIT. Libre d'utilisation pour vos serveurs AOA RP.

## 🎮 Crédits

Développé pour la communauté GTA RP sur FiveM. Parfait pour serveurs sérieux nécessitant une documentation professionnelle.

---

**⭐ N'oubliez pas de star le projet si il vous aide !**

*Fait avec ❤️ pour la communauté AOA RP*
