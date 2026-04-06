# PointagePro — CLAUDE.md

## Contexte projet
Application web de gestion des fiches de semaine (FDS) pour 200+ intervenants.
Prototype de démonstration — données simulées, pas de backend.
Fichier unique : index.html (vanilla JS, zéro dépendance externe)

## Stack technique
- HTML/CSS/JS vanilla pur — JAMAIS de React, Babel, ou librairies externes
- Hébergement : Netlify (auto-deploy depuis GitHub)
- Repo GitHub : https://github.com/zd-flux/pointage-pro
- URL live : https://cosy-sundae-2b0d85.netlify.app

## Architecture du code (index.html)
- Tout le code est dans un seul fichier index.html
- State global : objet S (role, tab, view, sel, fd, fiches...)
- Fonction principale : R() — re-render complet à chaque action
- Routing : S.role → S.view → S.tab

## Les 3 rôles
- Intervenant (Marie Dupont) : 2 onglets — Faire ma FDS / Mes FDS
- Responsable (Jean Martin) : 3 onglets — Faire ma FDS / Mes FDS / Valider les FDS  
- Assistante RH (Claire Dubois) : 2 onglets — FDS à saisir / FDS saisies

## Données métier
- 6 types d'heures : normal, sup25, sup50, nuit, ferie, dim
- 7 primes : repas 15€, déplacement 100€, Prime A-E (10€ à 50€)
- Statuts FDS : brouillon → soumis → validé/refusé

## Règles importantes
- NE JAMAIS casser le vanilla JS — pas de React, pas de Babel
- Toujours garder un seul fichier index.html
- Après chaque modification : git add . && git commit -m "description" && git push
- Le site se met à jour automatiquement sur Netlify après chaque push

## Déploiement
git add . && git commit -m "message" && git push
