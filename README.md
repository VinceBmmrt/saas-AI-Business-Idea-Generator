# 🚀 saas-AI-Business-Idea-Generator

> **AI-powered SaaS application that generates business ideas in real-time — with authentication, payments, and a modern full-stack architecture.**

---

## 🇬🇧 English

### Overview

**saas-AI-Business-Idea-Generator** is a full-stack SaaS application that leverages AI to generate business ideas on demand. It features a modern React/Next.js frontend, a FastAPI Python backend, real-time streaming responses, enterprise-grade authentication, and subscription management.

### ✨ Features

- ⚡ **Real-time AI streaming** — responses rendered progressively via Server-Sent Events
- 🔐 **Authentication** — sign in with Google, GitHub, or Email via [Clerk](https://clerk.com)
- 💳 **Subscription & payments** — integrated payment processing
- 🎨 **Beautiful Markdown rendering** — powered by `react-markdown` + `remark-gfm`
- 🌐 **Production-ready** — deployed seamlessly on Vercel
- 🛡️ **Secure API** — JWT tokens verified on every backend request

### 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js 16 (Pages Router), React 19, TypeScript |
| Styling | Tailwind CSS v4 |
| Auth | Clerk (`@clerk/nextjs`) |
| AI Streaming | `@microsoft/fetch-event-source` |
| Markdown | `react-markdown`, `remark-gfm`, `remark-breaks` |
| Backend | Python, FastAPI |
| Deployment | Vercel |

### 📦 Installation & Setup

#### Prerequisites

- Node.js >= 18
- Python >= 3.9
- A [Clerk](https://clerk.com) account
- A Vercel account (for deployment)

#### 1. Clone the repository

```bash
git https://github.com/VinceBmmrt/saas-AI-Business-Idea-Generator.git
cd saas-AI-Business-Idea-Generator
```

#### 2. Install frontend dependencies

```bash
npm install
```

#### 3. Install backend dependencies

```bash
cd backend
pip install -r requirements.txt
```

#### 4. Configure environment variables

See the [Environment Variables](#environment-variables) section below.

#### 5. Run the development servers

**Frontend:**
```bash
npm run dev
```

**Backend:**
```bash
cd backend
uvicorn main:app --reload
```

The frontend will be available at `http://localhost:3000` and the backend at `http://localhost:8000`.

### 🔑 Environment Variables

Create a `.env.local` file at the root of the project with the following variables:

```env
# ── Clerk Authentication ──────────────────────────────────────────
# Get these from https://dashboard.clerk.com → Your App → API Keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Clerk redirect routes (do not change unless customizing auth flow)
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

# ── Backend API ───────────────────────────────────────────────────
# URL of your FastAPI backend (use http://localhost:8000 for local dev)
NEXT_PUBLIC_API_URL=http://localhost:8000
```

Create a `.env` file in the `backend/` folder:

```env
# ── OpenAI ────────────────────────────────────────────────────────
# Get your key from https://platform.openai.com/api-keys
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# ── Clerk (backend JWT verification) ─────────────────────────────
# Get these from https://dashboard.clerk.com → Your App → API Keys
CLERK_SECRET_KEY=sk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# JWKS endpoint for JWT verification — format:
# https://<your-clerk-domain>/.well-known/jwks.json
CLERK_JWKS_URL=https://your-clerk-domain.clerk.accounts.dev/.well-known/jwks.json
```

> ⚠️ **Never commit your `.env` files.** They are already listed in `.gitignore`.

### 🚀 Deploy to Vercel

1. Push your project to GitHub
2. Import the repository in [Vercel](https://vercel.com)
3. Add all environment variables from `.env.local` in the Vercel dashboard under **Settings → Environment Variables**
4. Deploy — Vercel handles the rest automatically

### 📁 Project Structure

```
saas-AI-Business-Idea-Generator/
├── pages/              # Next.js pages (Pages Router)
│   ├── index.tsx       # Main idea generator page
│   ├── sign-in/        # Clerk sign-in page
│   └── sign-up/        # Clerk sign-up page
├── components/         # Reusable React components
├── styles/             # Global CSS / Tailwind config
├── backend/            # FastAPI Python backend
│   ├── main.py         # API entrypoint
│   └── requirements.txt
├── .env.local          # Frontend env variables (not committed)
└── package.json
```

---

## 🇫🇷 Français

### Présentation

**saas-AI-Business-Idea-Generator** est une application SaaS full-stack qui utilise l'IA pour générer des idées de business à la demande. Elle propose un frontend moderne React/Next.js, un backend Python FastAPI, du streaming temps réel, une authentification enterprise-grade et la gestion des abonnements.

### ✨ Fonctionnalités

- ⚡ **Streaming IA en temps réel** — réponses affichées progressivement via Server-Sent Events
- 🔐 **Authentification** — connexion avec Google, GitHub ou Email via [Clerk](https://clerk.com)
- 💳 **Abonnements & paiements** — traitement des paiements intégré
- 🎨 **Rendu Markdown soigné** — grâce à `react-markdown` + `remark-gfm`
- 🌐 **Prêt pour la production** — déploiement simplifié sur Vercel
- 🛡️ **API sécurisée** — tokens JWT vérifiés à chaque requête backend

### 🛠️ Stack Technique

| Couche | Technologie |
|---|---|
| Frontend | Next.js 16 (Pages Router), React 19, TypeScript |
| Style | Tailwind CSS v4 |
| Auth | Clerk (`@clerk/nextjs`) |
| Streaming IA | `@microsoft/fetch-event-source` |
| Markdown | `react-markdown`, `remark-gfm`, `remark-breaks` |
| Backend | Python, FastAPI |
| Déploiement | Vercel |

### 📦 Installation & Configuration

#### Prérequis

- Node.js >= 18
- Python >= 3.9
- Un compte [Clerk](https://clerk.com)
- Un compte Vercel (pour le déploiement)

#### 1. Cloner le dépôt

```bash
git clone https://github.com/your-username/saas-AI-Business-Idea-Generator.git
cd saas-AI-Business-Idea-Generator
```

#### 2. Installer les dépendances frontend

```bash
npm install
```

#### 3. Installer les dépendances backend

```bash
cd backend
pip install -r requirements.txt
```

#### 4. Configurer les variables d'environnement

Voir la section [Variables d'environnement](#variables-denvironnement) ci-dessous.

#### 5. Lancer les serveurs de développement

**Frontend :**
```bash
npm run dev
```

**Backend :**
```bash
cd backend
uvicorn main:app --reload
```

Le frontend sera accessible sur `http://localhost:3000` et le backend sur `http://localhost:8000`.

### 🔑 Variables d'environnement

Créez un fichier `.env.local` à la racine du projet :

```env
# ── Authentification Clerk ────────────────────────────────────────
# Récupérez ces clés sur https://dashboard.clerk.com → Votre App → API Keys
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Routes de redirection Clerk (ne pas modifier sauf personnalisation)
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/

# ── API Backend ───────────────────────────────────────────────────
# URL de votre backend FastAPI (http://localhost:8000 en développement)
NEXT_PUBLIC_API_URL=http://localhost:8000
```

Créez un fichier `.env` dans le dossier `backend/` :

```env
# ── OpenAI ────────────────────────────────────────────────────────
# Récupérez votre clé sur https://platform.openai.com/api-keys
OPENAI_API_KEY=sk-xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# ── Clerk (vérification JWT backend) ─────────────────────────────
# Récupérez ces clés sur https://dashboard.clerk.com → Votre App → API Keys
CLERK_SECRET_KEY=sk_test_xxxxxxxxxxxxxxxxxxxxxxxxxxxx

# Endpoint JWKS pour la vérification des JWT — format :
# https://<votre-domaine-clerk>/.well-known/jwks.json
CLERK_JWKS_URL=https://your-clerk-domain.clerk.accounts.dev/.well-known/jwks.json
```

> ⚠️ **Ne committez jamais vos fichiers `.env`.** Ils sont déjà listés dans `.gitignore`.

### 🚀 Déployer sur Vercel

1. Poussez votre projet sur GitHub
2. Importez le dépôt sur [Vercel](https://vercel.com)
3. Ajoutez toutes les variables d'environnement depuis `.env.local` dans **Settings → Environment Variables**
4. Déployez — Vercel s'occupe du reste automatiquement

### 📁 Structure du projet

```
saas-AI-Business-Idea-Generator/
├── pages/              # Pages Next.js (Pages Router)
│   ├── index.tsx       # Page principale du générateur
│   ├── sign-in/        # Page de connexion Clerk
│   └── sign-up/        # Page d'inscription Clerk
├── components/         # Composants React réutilisables
├── styles/             # CSS global / config Tailwind
├── backend/            # Backend Python FastAPI
│   ├── main.py         # Point d'entrée de l'API
│   └── requirements.txt
├── .env.local          # Variables d'env frontend (non committé)
└── package.json
```

---

## 📄 License

MIT — feel free to use, modify, and distribute.