# SmartEvent - Système de Gestion d'Événements Intelligents

Application web de gestion d'événements intelligents développée avec ASP.NET Core et architecture en couches, offrant une API REST complète et une interface frontend moderne.

## 📋 Description

SmartEvent est un système complet de gestion d'événements développé dans le cadre d'un Projet de Fin d'Année (PFA). L'application permet de gérer efficacement tous les aspects d'un événement : création, planification, réservation, suivi et analyse. Elle est construite avec une architecture moderne en couches utilisant ASP.NET Core pour le backend et une interface utilisateur responsive pour le frontend.

## 🎯 Fonctionnalités Principales

- ✅ **Gestion des événements** : Création, modification et suppression d'événements
- ✅ **Réservations** : Système de réservation et de billetterie
- ✅ **Gestion des utilisateurs** : Authentification et autorisation
- ✅ **API REST** : Endpoints RESTful pour l'intégration
- ✅ **Interface moderne** : Frontend responsive et intuitif
- ✅ **Base de données** : Migration et gestion avec Entity Framework Core

## 🛠️ Technologies Utilisées

### Backend
- **ASP.NET Core** (.NET 8.0) - Framework web moderne
- **Entity Framework Core** - ORM pour l'accès aux données
- **C#** - Langage de programmation
- **SQL Server / MySQL** - Base de données

### Frontend
- **JavaScript** - Langage de programmation
- **HTML5 / CSS3** - Structure et style
- **Responsive Design** - Interface adaptative

### DevOps & Outils
- **Docker** - Conteneurisation
- **Git** - Contrôle de version
- **Visual Studio** - IDE de développement

## 📁 Architecture du Projet

Le projet suit une architecture en couches (Clean Architecture) :

```
SmartEvent_PFA/
│
├── SmartEvent.API/              # Couche API (Controllers, Endpoints)
│   └── Controllers/            # Contrôleurs REST API
│
├── SmartEvent.Core/            # Couche Métier (Business Logic)
│   └── Models/                 # Modèles de domaine
│
├── SmartEvent.Data/            # Couche Accès aux Données
│   └── DbContext/              # Contexte Entity Framework
│
├── SmartEvent.Services/        # Couche Services
│   └── Services/               # Services métier
│
├── frontend/                    # Interface utilisateur
│   ├── src/                    # Code source frontend
│   └── public/                 # Fichiers statiques
│
├── Migrations/                  # Migrations de base de données
├── Dockerfile                  # Configuration Docker
├── appsettings.json            # Configuration de l'application
└── Program.cs                  # Point d'entrée de l'application
```

## 🚀 Installation et Configuration

### Prérequis

- [.NET 8.0 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Node.js](https://nodejs.org/) (pour le frontend)
- [SQL Server](https://www.microsoft.com/sql-server) ou [MySQL](https://www.mysql.com/)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) ou [Visual Studio Code](https://code.visualstudio.com/)
- [Docker](https://www.docker.com/) (optionnel)

### Installation

1. **Cloner le dépôt**
   ```bash
   git clone https://github.com/AmalChegdali/SmartEvent_PFA.git
   cd SmartEvent_PFA
   ```

2. **Configurer la base de données**
   - Modifiez `appsettings.json` avec vos paramètres de connexion
   - Exécutez les migrations :
   ```bash
   dotnet ef database update
   ```

3. **Installer les dépendances frontend**
   ```bash
   cd frontend
   npm install
   ```

4. **Lancer l'application**
   ```bash
   # Backend
   dotnet run --project SmartEvent.API
   
   # Frontend (dans un autre terminal)
   cd frontend
   npm start
   ```

## 🐳 Déploiement avec Docker

```bash
# Construire l'image Docker
docker build -t smartevent-api .

# Lancer le conteneur
docker run -p 5000:80 smartevent-api
```

## 📚 Documentation API

L'API REST expose plusieurs endpoints pour la gestion des événements :

- `GET /api/events` - Liste tous les événements
- `GET /api/events/{id}` - Détails d'un événement
- `POST /api/events` - Créer un nouvel événement
- `PUT /api/events/{id}` - Mettre à jour un événement
- `DELETE /api/events/{id}` - Supprimer un événement

*(Ajoutez ici la documentation complète de vos endpoints)*

## 🧪 Tests

```bash
# Exécuter les tests unitaires
dotnet test

# Exécuter les tests avec couverture de code
dotnet test /p:CollectCoverage=true
```

## 📝 Structure de la Base de Données

Les migrations Entity Framework sont disponibles dans le dossier `Migrations/`. Pour créer une nouvelle migration :

```bash
dotnet ef migrations add NomDeLaMigration --project SmartEvent.Data
```

## 🔐 Sécurité

- Authentification JWT
- Hashage des mots de passe
- Validation des entrées
- Protection CORS configurée

## 🎨 Interface Utilisateur

L'interface frontend offre :
- Design moderne et responsive
- Navigation intuitive
- Formulaires de gestion d'événements
- Tableaux de bord interactifs

## 📊 Fonctionnalités Avancées

- **Gestion multi-utilisateurs** : Rôles et permissions
- **Notifications** : Système de notifications en temps réel
- **Rapports** : Génération de rapports et statistiques
- **Export** : Exportation des données (CSV, PDF)

## 🤝 Contribution

Ce projet est un Projet de Fin d'Année. Pour toute question ou suggestion, n'hésitez pas à ouvrir une issue.

## 📄 Licence

Ce projet est développé dans le cadre académique. Tous droits réservés.

## 👤 Auteur

**Amal Chegdali**

- GitHub: [@AmalChegdali](https://github.com/AmalChegdali)
- LinkedIn: [Amal Chegdali](https://www.linkedin.com/in/amal-chegdali-37a5b9239/)
- Email: a.chegdali@gmail.com

## 🙏 Remerciements

- Équipe pédagogique pour l'encadrement
- Communauté .NET pour les ressources et le support
- Tous les contributeurs open-source dont les bibliothèques ont été utilisées

## 📚 Ressources

- [Documentation ASP.NET Core](https://docs.microsoft.com/aspnet/core)
- [Documentation Entity Framework Core](https://docs.microsoft.com/ef/core)
- [Guide .NET](https://docs.microsoft.com/dotnet)

---

⭐ Si ce projet vous a été utile, n'hésitez pas à lui donner une étoile !
