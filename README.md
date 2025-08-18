# DAR AL AMANA – Site statique (FR/AR/EN)

Service réservé **uniquement aux Tunisiens résidant à l’étranger**. Déploiement simple via **GitHub Pages**.

## Fichiers
- `index.html` – Page d’accueil trilingue (FR/AR/EN), TailwindCDN, WhatsApp, bannières “expats only”
- `CNAME` – Domaine personnalisé: `daralamana.fr`

## Mise en ligne (rapide)
1. Crée un repo public sur GitHub (ex: `dar-al-amana-site`).
2. Ajoute ces fichiers à la racine (`index.html`, `CNAME`), puis *Commit*.
3. Va dans **Settings → Pages** :
   - **Build and deployment → Source**: `Deploy from a branch`
   - **Branch**: `main` & `/ (root)` puis **Save**.
   - **Custom domain**: `daralamana.fr` puis **Save**.
   - Coche **Enforce HTTPS** dès que disponible.

## DNS (chez ton registrar du .fr)
- **Apex** `daralamana.fr` → 4 A records :
  - `185.199.108.153`
  - `185.199.109.153`
  - `185.199.110.153`
  - `185.199.111.153`
- **www.daralamana.fr** → `CNAME` vers `<ton-user>.github.io`

> Après propagation DNS (parfois ~quelques minutes), retourne dans **Settings → Pages** et active **Enforce HTTPS**.

## Modifier le contenu
- Change le numéro WhatsApp, les tarifs, les annonces, les textes (FR/AR/EN) directement dans `index.html`.
- Le bouton langue (FR/AR/EN) bascule l’affichage via l’attribut `lang` du `<html>`.

## Option Formulaire
Le contact utilise **Formspree** (`action="https://formspree.io/f/your-id"`). Remplace `your-id` par ton endpoint Formspree si tu veux recevoir les messages par e‑mail.

## License
Libre d’usage pour DAR AL AMANA.
