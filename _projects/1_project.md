---
layout: page
title: HSE International Office — Full-Stack Web & Mobile Solutions
description: Front-end JS, CMS Bitrix24, app Android native (Kotlin), bots Python, reporting SQL/Power BI.
img: assets/img/projects/hse/hse-staff.jpg
importance: 1
category: work
related_publications: true
---

Depuis juillet 2024, je conçois, développe et maintiens en autonomie l'ensemble des outils web et mobiles du **Bureau International** de **[HSE University](https://www.hse.ru/staff/hsamran)** — de la maquette Figma jusqu'au déploiement, en méthodologie **Agile/Scrum**.

## Landing pages événementielles

**Objectif** : convertir le trafic des salons étudiants et campagnes de recrutement en inscriptions qualifiées.

**Stack** : maquettage **Figma**, développement **HTML5, CSS3, JavaScript** (vanilla, sans framework lourd pour garder les pages légères), formulaires avec validation côté client, intégration analytics.

**Remarque marché marocain** : ce projet utilise du JavaScript vanilla intégré à Bitrix24 (CMS très répandu en Russie). Je maîtrise également **React.js**, stack dominante sur le marché marocain — voir mon projet Masar Tourism pour un exemple direct en React.

Code source disponible sur mon **[GitHub](https://github.com/Samran-Hamza)**.

<div class="simple-carousel" id="hseSiteCarousel">
  <div class="simple-carousel-track">
    <img src="{{ 'assets/img/projects/hse/hse-site-1.jpg' | relative_url }}" class="active" alt="HSE site 1">
    <img src="{{ 'assets/img/projects/hse/hse-site-2.jpg' | relative_url }}" alt="HSE site 2">
    <img src="{{ 'assets/img/projects/hse/hse-site-3.jpg' | relative_url }}" alt="HSE site 3">
    <img src="{{ 'assets/img/projects/hse/hse-site-4.jpg' | relative_url }}" alt="HSE site 4">
    <img src="{{ 'assets/img/projects/hse/hse-site-5.jpg' | relative_url }}" alt="HSE site 5">
    <img src="{{ 'assets/img/projects/hse/hse-site-6.jpg' | relative_url }}" alt="HSE site 6">
    <img src="{{ 'assets/img/projects/hse/site-hse-7.jpg' | relative_url }}" alt="HSE site 7">
    <img src="{{ 'assets/img/projects/hse/site-hse-8.jpg' | relative_url }}" alt="HSE site 8">
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

## Système d'inscription et de suivi de présence

**Objectif** : automatiser un processus manuel (feuilles Excel partagées par email) pour les inscriptions aux événements de recrutement.

**Stack technique** : formulaire front-end connecté à une **base de données relationnelle (MySQL)**, backend de traitement des requêtes, envoi automatique d'email de confirmation (SMTP), back-office simple pour consultation et export **CSV/Excel** sans intervention développeur.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3">
        <a href="{{ 'assets/img/projects/hse/service1.jpg' | relative_url }}" class="venobox" data-gall="hse-service">
            <img src="{{ 'assets/img/projects/hse/service1.jpg' | relative_url }}" class="img-fluid rounded z-depth-1 uniform-img" alt="Système d'inscription">
        </a>
    </div>
</div>
<div class="caption">
    Interface du service d'inscription et de suivi de présence.
</div>

## Widgets CMS Bitrix24

Plus d'un an d'expérience quotidienne sur **Bitrix24** : calendrier interactif en accordéon (fetch API, DOM dynamique), catalogue de 58 programmes de licence (array JS, filtrage côté client par faculté/langue), pages FAQ multilingues (RU/EN) avec logique conditionnelle selon le profil candidat.

## Application Android native

**Stack principale** : **Kotlin, Android Studio**. Développement de fonctionnalités, tests unitaires, QA fonctionnelle, builds de test iOS via **TestFlight**. Application utilisée par plus de 50 000 étudiants.

**Autres compétences mobile/backend** : je maîtrise également **Spring Boot** pour la construction d'API backend Java/Kotlin, ainsi que **React Native** pour le développement mobile cross-platform — des stacks pertinentes pour des équipes cherchant une flexibilité entre développement natif et cross-platform.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3">
        <a href="{{ 'assets/img/projects/hse/hse-android-scheme.jpg' | relative_url }}" class="venobox" data-gall="hse-android">
            <img src="{{ 'assets/img/projects/hse/hse-android-scheme.jpg' | relative_url }}" class="img-fluid rounded z-depth-1 uniform-img" alt="Schéma applicatif">
        </a>
    </div>
    <div class="col-sm-6 mt-3">
        <a href="{{ 'assets/img/projects/hse/hse-android-scheme-detail.jpg' | relative_url }}" class="venobox" data-gall="hse-android">
            <img src="{{ 'assets/img/projects/hse/hse-android-scheme-detail.jpg' | relative_url }}" class="img-fluid rounded z-depth-1 uniform-img" alt="Détail du schéma">
        </a>
    </div>
</div>
<div class="caption">
    Schéma d'architecture d'un module de l'application.
</div>

## Automatisation backend et data

Bots **Telegram** (**Python**, Telegram Bot API) — plus de 2 000 utilisateurs actifs. Requêtes **SQL** et tableaux de bord **Power BI** sur données d'admission pluriannuelles. Configuration de modules **1C: Enterprise** pour la gestion des dossiers étudiants.

## Stack technique

`Figma` `HTML5` `CSS3` `JavaScript` `React.js` `Bitrix24` `Kotlin` `Android Studio` `TestFlight` `Spring Boot` `React Native` `Python` `Telegram Bot API` `MySQL` `SQL` `Power BI` `1C: Enterprise` `Agile` `Scrum` `Jira`
