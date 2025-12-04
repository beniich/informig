# Déploiement Backend sur cPanel - Résumé Rapide

## 🎯 Étapes Principales

### 1. Setup Node.js App (cPanel)
- Créer application Node.js
- Version : 18.x+
- Startup file : `server.js`
- URL : `api.votredomaine.com`

### 2. Variables d'Environnement
```bash
DB_HOST=localhost
DB_USER=votre_user
DB_PASSWORD=votre_password
DB_NAME=crm_hub_auth
JWT_SECRET=cle_secrete_longue
STRIPE_SECRET_KEY=sk_live_...
OPENAI_API_KEY=sk-...
FRONTEND_URL=https://votre-frontend.pages.dev
```

### 3. MySQL Database
- Créer base : `crm_hub_auth`
- Importer : `backend/config/database.sql` via phpMyAdmin

### 4. Upload Fichiers
Via FTP, uploadez le dossier `backend/` complet

### 5. Installer & Démarrer
- Run NPM Install dans cPanel
- Start App

### 6. Tester
```
https://api.votredomaine.com/health
```

### 7. Configurer Stripe Webhook
URL : `https://api.votredomaine.com/api/subscriptions/webhook`

### 8. Mettre à Jour Frontend
Cloudflare Pages → `VITE_API_URL` = `https://api.votredomaine.com/api`

## ✅ Checklist
- [ ] App Node.js créée
- [ ] Variables d'environnement configurées
- [ ] Base MySQL créée et importée
- [ ] Fichiers uploadés
- [ ] npm install exécuté
- [ ] App démarrée
- [ ] Test /health OK
- [ ] Webhook Stripe configuré
- [ ] Frontend mis à jour

Voir [CPANEL_DEPLOYMENT.md](file:///C:/Users/pc%20gold/.gemini/antigravity/brain/70032d84-ad34-4d83-aa0b-8c9eed185143/CPANEL_DEPLOYMENT.md) pour le guide complet.
