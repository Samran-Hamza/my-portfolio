---
layout: page
title: Application de recommandation d'universités russes — Projet de fin d'études
description: Android (Jetpack Compose, Kotlin, MVVM), FastAPI (Python), modèle ML hybride (SVD + Sentence-BERT), assistant LLM (ruGPT-3).
importance: 3
category: work
related_publications: false
---

**Projet de fin d'études** (mémoire de diplôme) — application d'analyse des profils d'étudiants étrangers et de recommandation d'universités russes basée sur des méthodes de machine learning.

**Rôle** : Développeur Full-stack / Ingénieur ML (auteur du projet)

**Contexte** : la croissance du nombre d'étudiants étrangers en Russie nécessite des outils numériques personnalisés pour le choix d'université — prenant en compte le GPA, les centres d'intérêt, la langue d'enseignement. Les LLM modernes élargissent les possibilités de dialogue intelligent entre le système et l'utilisateur.

## Architecture (5 niveaux)

- **Niveau client** : application Android (Jetpack Compose, Kotlin, MVVM)
- **Niveau serveur** : FastAPI (Python)
- **Niveau ML / moteur de recommandation** : SVD + Sentence-BERT
- **Niveau LLM** : ruGPT-3 (modèle fine-tuné)
- **Niveau données** : MongoDB

## Algorithme de recommandation hybride
---
layout: page
title: Application de recommandation d'universités russes — Projet de fin d'études
description: Android (Jetpack Compose, Kotlin, MVVM), FastAPI (Python), modèle ML hybride (SVD + Sentence-BERT), assistant LLM (ruGPT-3 / Mistral 7B).
img: assets/img/projects/app/app-1.jpg
importance: 3
category: work
related_publications: false
---

**Projet de fin d'études** (mémoire de diplôme) — application d'analyse des profils d'étudiants étrangers et de recommandation d'universités russes basée sur des méthodes de machine learning.

**Rôle** : Développeur Full-stack / Ingénieur ML (auteur du projet)

**Contexte** : la croissance du nombre d'étudiants étrangers en Russie nécessite des outils numériques personnalisés pour le choix d'université — prenant en compte le GPA, les centres d'intérêt, la langue d'enseignement. Les LLM modernes élargissent les possibilités de dialogue intelligent entre le système et l'utilisateur.

## Architecture (5 niveaux)

- **Niveau client** : application Android (Jetpack Compose, Kotlin, MVVM)
- **Niveau serveur** : FastAPI (Python)
- **Niveau ML / moteur de recommandation** : SVD + Sentence-BERT
- **Niveau LLM** : ruGPT-3 (modèle fine-tuné)
- **Niveau données** : MongoDB

## Algorithme de recommandation hybride

**Formule de scoring** : `Score(u) = α·SVD(s,u) + β·cos(BERT(s), BERT(u))`

- **SVD** (Surprise SVD) — filtrage collaboratif, entraîné sur la matrice d'interactions student–university, évaluation par RMSE (80% train / 20% test)
- **Sentence-BERT** — embeddings sémantiques des intérêts de l'étudiant et des descriptions d'universités, similarité cosinus
- Implémenté comme pipeline asynchrone dans FastAPI

## Assistant IA (LLM)

- Modèle **ruGPT-3small** (Sberbank-AI, fine-tuné sur des données universitaires : sites des universités russes, StudyInRussia, catalogues de bourses)
- Intégration via l'endpoint FastAPI `/ai_assistant`
- Génération de réponses selon le profil de l'étudiant et la filière de l'université, historique des dialogues sauvegardé dans des logs

## Réalisations principales

- Développement d'un **modèle de recommandation hybride** combinant l'algorithme **SVD** (filtrage collaboratif) et **Sentence-BERT** (analyse sémantique des filières d'études)
- Implémentation d'un **prototype d'application** avec interface Android, stockage **MongoDB** et backend **FastAPI**
- Intégration d'un **modèle de langage** (ruGPT-3Small / Mistral 7B), entraîné sur **Google Colab** sur un corpus de questions-réponses liées à l'admission universitaire
- Développement d'un **assistant IA** capable de générer en temps réel des réponses personnalisées, d'expliquer la logique des recommandations et d'accompagner l'étudiant dans le choix de son université
- **Tests fonctionnels** du système confirmant une précision élevée du matching (**Top-1 Match ~79%** pour le modèle hybride) et la pertinence des réponses de l'assistant

## Stack technique

**Application mobile** : Jetpack Compose, Android Studio, Kotlin (MVVM)
**Backend** : FastAPI, Python 3.10, Swagger UI, Pydantic
**ML/IA** : Surprise SVD, Sentence-BERT, ruGPT-3small, Mistral 7B, Google Colab (entraînement)

## Conclusions

Architecture à 5 niveaux développée (client → API → ML → LLM → BDD), algorithme de recommandation hybride implémenté, assistant IA intégré, tous les modules testés et adaptés au client mobile.

<div class="simple-carousel" id="hseSiteCarousel">
  <div class="simple-carousel-track">
    <img src="{{ 'assets/img/projects/app\app-1.jpg' | relative_url }}" class="active" alt="UniPath AI">
    <img src="{{ 'assets/img/projects/app\app-2.jpg' | relative_url }}" alt="Registration">
    <img src="{{ 'assets/img/projects/app\app-3.jpg' | relative_url }}" alt="Recommendation">
    <img src="{{ 'assets/img/projects/app\app-4.jpg' | relative_url }}" alt="UniAI">
  </div>
  <button class="simple-carousel-btn prev" onclick="hseCarouselMove(-1)">&#10094;</button>
  <button class="simple-carousel-btn next" onclick="hseCarouselMove(1)">&#10095;</button>
  <div class="simple-carousel-counter"><span id="hseCarouselCounter">1 / 8</span></div>
</div>
<div class="caption">
    Utilisez les flèches pour naviguer entre les captures d'écran.
</div>

<script>
  let hseCarouselIndex = 0;
  function hseCarouselMove(direction) {
    const imgs = document.querySelectorAll('#hseSiteCarousel .simple-carousel-track img');
    imgs[hseCarouselIndex].classList.remove('active');
    hseCarouselIndex = (hseCarouselIndex + direction + imgs.length) % imgs.length;
    imgs[hseCarouselIndex].classList.add('active');
    document.getElementById('hseCarouselCounter').textContent = (hseCarouselIndex + 1) + ' / ' + imgs.length;
  }
</script>


**Formule de scoring** : `Score(u) = α·SVD(s,u) + β·cos(BERT(s), BERT(u))`

- **SVD** (Surprise SVD) — filtrage collaboratif, entraîné sur la matrice d'interactions student–university, évaluation par RMSE (80% train / 20% test)
- **Sentence-BERT** — embeddings sémantiques des intérêts de l'étudiant et des descriptions d'universités, similarité cosinus
- Implémenté comme pipeline asynchrone dans FastAPI

## Assistant IA (LLM)

- Modèle **ruGPT-3small** (Sberbank-AI, fine-tuné sur des données universitaires : sites des universités russes, StudyInRussia, catalogues de bourses)
- Intégration via l'endpoint FastAPI `/ai_assistant`
- Génération de réponses selon le profil de l'étudiant et la filière de l'université, historique des dialogues sauvegardé dans des logs

## Stack technique

**Application mobile** : Jetpack Compose, Android Studio, Kotlin (MVVM)
**Backend** : FastAPI, Python 3.10, Swagger UI, Pydantic
**ML/IA** : Surprise SVD, Sentence-BERT, ruGPT-3small

## Conclusions

Architecture à 5 niveaux développée (client → API → ML → LLM → BDD), algorithme de recommandation hybride implémenté, assistant IA intégré, tous les modules testés et adaptés au client mobile.
