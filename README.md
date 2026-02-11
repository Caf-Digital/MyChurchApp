
# MyChurchApp

Application web complète pour la gestion d'église.

**Production :** [www.mychurchapp.com](https://www.mychurchapp.com)

---

## Résumé

MyChurchApp permet aux membres, pasteurs et administrateurs de gérer efficacement les activités d'une communauté chrétienne. Solution moderne, sécurisée et évolutive.

---

## Badges

![Licence](https://img.shields.io/badge/licence-MIT-blue)
![Version](https://img.shields.io/badge/version-1.0.3-blue)

---

## Fonctionnalités principales

### Espace Membres
- Prise de rendez-vous pastoraux
- Consultation des prédications et enseignements
- Demandes de prière et partage de témoignages
- Contributions financières sécurisées (CDF)
- Participation aux sondages communautaires

### Espace Pasteurs
- Gestion centralisée des rendez-vous
- Suivi des demandes de prière
- Validation des témoignages
- Communication directe avec les membres

### Administration
- Tableau de bord complet avec analytics
- Gestion des membres et événements
- Système de notifications
- Rapports et statistiques

### Fonctionnalités avancées
- Reconnaissance faciale pour l'assiduité
- Notifications push
- Authentification sécurisée JWT
- API backend Express/Next.js

---

## Stack Technique

| Composant       | Technologie                          |
|-----------------|--------------------------------------|
| Frontend        | Next.js 15, React, TypeScript        |
| Styling         | Tailwind CSS                         |
| Backend         | API Routes Next.js, Express, Supabase|
| Base de données | PostgreSQL (Supabase) / SQLite (dev) |
| Hébergement     | Vercel                               |
| Authentification| JWT avec middleware custom           |
| UI Components   | Composants custom + Lucide React     |

---

## Structure du projet

```
├── src/                # Frontend Next.js
│   ├── app/            # Pages et routes Next.js
│   ├── components/     # Composants React
│   ├── contexts/       # Contextes React
│   ├── hooks/          # Hooks personnalisés
│   ├── lib/            # Utilitaires
│   └── types/          # Types TypeScript
├── api-backend/        # Backend Express/Supabase
│   ├── src/            # Code serveur
│   └── database/       # Scripts SQL
├── database/           # Migrations SQL
├── public/             # Assets statiques
├── docker/             # Configurations Docker
```

---

## Installation locale

### Prérequis

- Node.js 18+
- npm ou yarn

### Étapes

```bash
# Cloner le repository
git clone https://github.com/Caf-Digital/MyChurchApp.git
cd MyChurchApp

# Installer les dépendances
npm install

# Configurer l'environnement
cp .env.example .env.local

# Lancer le serveur de développement
npm run dev
```

L'application sera accessible sur `http://localhost:3000`

---

## Configuration

### Variables d'environnement

Créer un fichier `.env.local` avec les variables suivantes :

```env
# Base de données
DATABASE_URL="file:./database.db"

# Authentification
JWT_SECRET="votre-secret-jwt"
NEXTAUTH_URL="http://localhost:3000"
NEXTAUTH_SECRET="votre-secret-nextauth"

# Supabase (production uniquement)
SUPABASE_URL="https://votre-projet.supabase.co"
SUPABASE_ANON_KEY="votre-anon-key"
```

---

## Déploiement

### Vercel (Recommandé)

1. Connecter le repository GitHub à Vercel
2. Configurer les variables d'environnement de production
3. Le déploiement est automatique à chaque push sur `main`

### Variables de production

```env
DATABASE_URL="postgresql://user:password@host:5432/database"
JWT_SECRET="votre-secret-jwt-production"
NEXTAUTH_URL="https://www.mychurchapp.com"
NEXTAUTH_SECRET="votre-secret-nextauth-production"
SUPABASE_URL="https://votre-projet.supabase.co"
SUPABASE_ANON_KEY="votre-anon-key"
```

---

## Rôles utilisateurs

| Role          | Accès                                    |
|---------------|------------------------------------------|
| FIDELE        | Fonctionnalités membres de base          |
| OUVRIER       | Accès étendu + gestion de service        |
| PASTOR        | Gestion rendez-vous + accès pastoral     |
| ADMIN         | Accès complet à toutes les fonctionnalités|

---

## Scripts disponibles

```bash
npm run dev      # Serveur de développement
npm run build    # Build de production
npm run start    # Démarrer en production
npm run lint     # Vérification du code
```

---

## Sécurité

- Les variables sensibles sont stockées dans `.env.local` (jamais versionnées)
- Respect des bonnes pratiques pour la gestion des secrets
- Authentification JWT sécurisée
- Fichiers `.gitignore` complets pour éviter toute fuite

---

## Contribution

Les contributions sont les bienvenues !

1. Forkez le projet
2. Créez une branche (`feature/ma-fonctionnalite`)
3. Commitez vos modifications
4. Ouvrez une Pull Request

---

## Support & Contact

Pour toute question ou demande de support, ouvrez une issue sur GitHub ou contactez l'auteur.

---

## Licence

Projet privé - MyChurchApp

---

## Auteur

Chris Ngozulu Kasongo - [@kalibanhall](https://github.com/kalibanhall)
