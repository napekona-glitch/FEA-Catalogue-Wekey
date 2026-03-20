<!-- Architecte : Napé Kona -->
# FEA Wekey - Catalogue de Services Architecture & Transformation

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub stars](https://img.shields.io/github/stars/username/FEA-Catalogue-Wekey.svg)](https://github.com/username/FEA-Catalogue-Wekey/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/username/FEA-Catalogue-Wekey.svg)](https://github.com/username/FEA-Catalogue-Wekey/network)

🏗️ **Catalogue interactif de 15 services spécialisés en Architecture & Transformation** avec chatbot IA intégré

---

## 🎯 Vue d'ensemble

Ce projet présente un catalogue moderne et interactif des services d'architecture et transformation digitale de Wekey. Conçu pour les entreprises cherchant à accélérer leur modernisation, sécuriser leurs systèmes d'information et industrialiser leurs usages data & IA.

### ✨ Fonctionnalités principales

- 🎯 **15 offres de services spécialisées** (Cloud, DevOps, Data, Sécurité, etc.)
- 🤖 **Chatbot intelligent** avec IA Groq pour recommandations personnalisées
- 📱 **Design responsive** adapté mobile/desktop/tablette
- 🔍 **Recherche avancée** dans toutes les fiches de services
- 📄 **Export PDF/DOCX** des fiches détaillées
- ⚡ **Performance optimisée** avec lazy loading et cache

---

## 🚀 Démarrage rapide

### Prérequis
- Navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Python 3.x (pour le serveur de développement)

### Installation et lancement

```bash
# Cloner le repository
git clone https://github.com/username/FEA-Catalogue-Wekey.git
cd FEA-Catalogue-Wekey

# Démarrer le serveur local
python -m http.server 8000

# Ouvrir dans le navigateur
http://localhost:8000
```

### Configuration du chatbot (optionnel)

Pour activer les réponses IA du chatbot :

1. Créez un compte sur [Groq](https://groq.com/)
2. Générez votre clé API (commence par `gsk_`)
3. Configurez-la dans `groq-config.js` :
   ```javascript
   apiKey: 'votre_cle_api_groq_ici'
   ```

---

## 📁 Structure du projet

```
FEA-Catalogue-Wekey/
├── 📄 index.html                    # Page principale avec catalogue
├── 📄 storyline.html                 # Parcours client narratif
├── 📄 test-pdf.html                  # Tests fonctionnalités PDF
├── 📄 groq-config.js                 # Configuration API Groq
├── 📁 CSS/                           # Feuilles de style
│   ├── catalog-style.css
│   └── service-detail.css
├── 📁 JS/                            # Logique JavaScript
│   ├── catalog-script.js            # Chatbot et interactions
│   ├── chatbot-responses.js         # Réponses prédéfinies
│   ├── fiche-script.js             # Logique fiches détaillées
│   └── html-to-docx.js              # Export DOCX
├── 📁 fiche-*.html                   # 15 fiches de services détaillées
├── 📁 pdf-*.html                     # Versions PDF des fiches
├── 🖼️ Assets/                        # Images et illustrations
├── 🐍 deploy_word_button*.py        # Scripts de déploiement
└── 📚 Documentation/                 # README files
    ├── README.md                     # Ce fichier
    ├── README-DOCUMENTATION.md       # Documentation technique complète
    ├── README-GROQ.md                # Guide intégration API Groq
    └── STORYLINE.md                  # Documentation parcours client
```

---

## 🛠️ Technologies utilisées

### Frontend
- **HTML5** & **CSS3** avec variables CSS modernes
- **JavaScript ES6+** avec architecture modulaire
- **Font Awesome 6.0** pour les icônes
- **Google Fonts** (Inter) pour la typographie

### Backend & APIs
- **Groq API** pour le chatbot IA (Llama 3.1, Mixtral)
- **Python HTTP Server** pour le développement
- **GitHub Pages** pour le déploiement en production

### Outils & Déploiement
- **Git** pour le versioning
- **Python** pour les scripts utilitaires
- **Static hosting** (GitHub Pages, Netlify, Vercel)

---

## 📋 Services disponibles

| Catégorie | Services | Fiches |
|-----------|----------|--------|
| 🏗️ **Architecture** | Urbanisation SI, Monolithe → Microservices | 2 |
| ☁️ **Cloud & Infrastructure** | Migration Cloud Hybride, IaC, SD-WAN/SASE | 3 |
| 🔧 **DevOps & Industrialisation** | CI/CD, Observabilité, Audit Qualité | 3 |
| 🔒 **Sécurité** | Zero Trust & IAM, PCA/PRA Continuité | 2 |
| 📊 **Data & IA** | Data Mesh, MLOps IA, RAG IA Générative | 3 |
| 💼 **Digital Workplace** | Modernisation Workplace | 1 |
| 🔌 **Intégration** | API Management & Integration | 1 |

---

## 🤖 Chatbot IA

Le chatbot offre deux niveaux d'assistance :

### Chatbot global (page d'accueil)
- Réponses sur l'ensemble du catalogue
- Recommandations croisées entre services
- Aide à la navigation

### Chatbots spécialisés (fiches détaillées)
- Expertise focus sur un service spécifique
- Réponses techniques détaillées
- Cas d'usage et bénéfices spécifiques

### Mode fallback
Si l'API Groq est indisponible, le chatbot bascule automatiquement en mode recherche locale basé sur les mots-clés.

---

## 📱 Déploiement

### Développement local
```bash
python -m http.server 8000
# http://localhost:8000
```

### Production (GitHub Pages)
1. Activer GitHub Pages dans les settings du repository
2. Sélectionner la branche `main`
3. Le site sera disponible à `https://username.github.io/FEA-Catalogue-Wekey`

### Autres options de déploiement
- **Netlify** : Glisser-déposer le dossier
- **Vercel** : Importer le repository GitHub
- **Firebase Hosting** : `firebase deploy`

---

## 🔧 Configuration avancée

### Personnalisation du chatbot
Modifier `groq-config.js` :
```javascript
const GROQ_CONFIG = {
    apiKey: 'votre_clé_api',
    defaultParams: {
        temperature: 0.7,    // Créativité (0.0-1.0)
        max_tokens: 500,     // Longueur max réponse
        model: 'llama-3.1-8b-instant'  // Modèle choisi
    }
};
```

### Ajout de nouveaux services
1. Créer `fiche-nouveau-service.html`
2. Ajouter le fichier à `existingFiles` dans `JS/catalog-script.js`
3. Mettre à jour l'index de recherche

---

## 📊 Performance & Optimisation

### Métriques cibles
- **First Contentful Paint** < 1.5s
- **Largest Contentful Paint** < 2.5s
- **Cumulative Layout Shift** < 0.1
- **First Input Delay** < 100ms

### Optimisations implémentées
- CSS minifié et optimisé
- Images en formats WebP/SVG
- Lazy loading des fiches
- Cache navigateur approprié

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment participer :

1. **Fork** le repository
2. Créer une branche (`git checkout -b feature/amélioration`)
3. Commiter les changements (`git commit -m 'Ajout nouvelle fonctionnalité'`)
4. Pusher la branche (`git push origin feature/amélioration`)
5. Ouvrir une **Pull Request**

### Types de contributions souhaitées
- 🐛 Corrections de bugs
- ✨ Nouvelles fonctionnalités
- 📚 Améliorations documentation
- 🎨 Améliorations UI/UX
- ⚡ Optimisations performance

---

## 📝 License

Ce projet est sous license **MIT** - voir le fichier [LICENSE](LICENSE) pour les détails.

---

## 📞 Support & Contact

### Documentation
- 📖 **[Documentation technique complète](README-DOCUMENTATION.md)**
- 🤖 **[Guide intégration API Groq](README-GROQ.md)**
- 📋 **[Documentation parcours client](STORYLINE.md)**

### Dépannage courant
- **Chatbot ne répond pas** : Vérifier la clé API Groq et la console (F12)
- **Styles cassés** : Vider le cache navigateur
- **Liens brisés** : Vérifier les chemins relatifs

### Contact
- 📧 Email : [contact@wekey.com](mailto:contact@wekey.com)
- 🌐 Site web : [wekey.com](https://wekey.com)
- 💼 LinkedIn : [Wekey](https://linkedin.com/company/wekey)

---

## 🏆 Remerciements

Merci à toutes les personnes qui ont contribué à ce projet :

- L'équipe **Architecture & Transformation** de Wekey
- Les **experts métiers** pour leur expertise technique
- La communauté **open source** pour les outils utilisés

---

<div align="center">

**[⭐ Donnez une étoile](https://github.com/username/FEA-Catalogue-Wekey)** si ce projet vous a été utile !

Made with ❤️ by [Wekey Architecture Team](https://wekey.com)

</div>
