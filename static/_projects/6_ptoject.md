---
layout: page
title: Chatbot étudiant multicanal — Site universitaire & Telegram
description: Python (aiogram, FastAPI), PostgreSQL, intégration Omnidesk, widget web.
importance: 6
category: work
related_publications: false
---

**Stack technique** :

- **Backend** : Python, **FastAPI** (API REST pour le widget web), **aiogram** (bot Telegram, async)
- **Base de données** : **PostgreSQL** — stockage des profils étudiants, historique des conversations, base de connaissances (FAQ)
- **Cache/queue** : Redis (gestion des sessions, files d'attente des messages)
- **Widget web** : JavaScript vanilla, intégré en pop-up sur le site de l'université, communication via WebSocket avec le backend
- **Intégration Omnidesk** : API REST pour création automatique de tickets et transfert vers le support humain
- **Déploiement** : Docker, Nginx (reverse proxy), VPS

**Architecture** : bot Telegram (aiogram) et widget web (FastAPI + WebSocket) partagent le même backend et la même base PostgreSQL. Les questions non résolues automatiquement sont escaladées via l'API Omnidesk vers un agent humain.