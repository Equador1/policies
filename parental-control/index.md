---
title: Politique de confidentialité — Contrôle Parental Web
---

# Politique de confidentialité — Contrôle Parental Web

**Dernière mise à jour : 13 octobre 2026**

## En résumé

Cette extension ne transmet aucune donnée. Tout ce qu'elle enregistre reste sur votre appareil, dans le stockage local du navigateur. Il n'y a ni serveur, ni compte, ni service tiers, ni analyse d'audience, ni publicité.

## Données enregistrées sur votre appareil

Pour fonctionner, l'extension conserve localement :

| Donnée | Pourquoi |
|---|---|
| Liste des sites autorisés, de la liste noire et des sites « sur invitation » | Décider quels sites sont accessibles |
| Limites de temps et plages horaires par site | Appliquer les règles définies par le parent |
| Temps d'utilisation quotidien par site autorisé | Faire respecter les limites de temps ; remis à zéro chaque jour |
| Demandes d'accès en attente | Permettre à l'enfant de demander un site et au parent de répondre |
| Empreinte du mot de passe parent | Protéger l'accès aux réglages. Le mot de passe lui-même n'est jamais enregistré : seule une empreinte PBKDF2-SHA256 (100 000 itérations, sel aléatoire) l'est, et elle ne permet pas de retrouver le mot de passe |
| Horodatage de la dernière activité et périodes d'inactivité prolongée | Signaler au parent que l'extension a été arrêtée ou désactivée |
| Adresse de la page en cours de consultation dans chaque onglet | Savoir quel site a été bloqué et d'où vient un lien ouvert. Effacé à la fermeture de l'onglet et à la fermeture du navigateur |

## Ce que l'extension ne fait pas

- Elle **n'envoie rien sur Internet**. Le code ne contient aucun appel réseau sortant : ni `fetch`, ni `XMLHttpRequest`, ni WebSocket, ni balise de mesure.
- Elle **ne synchronise rien** entre vos appareils. Seul `chrome.storage.local` et `chrome.storage.session` sont utilisés, jamais `chrome.storage.sync`.
- Elle **ne constitue pas d'historique de navigation** consultable. Le temps d'utilisation est un simple compteur de secondes par domaine et par jour, sans les adresses visitées.
- Elle **ne transmet aucune donnée à l'auteur** de l'extension, ni à qui que ce soit d'autre.

## Pourquoi l'extension demande l'accès à tous les sites

L'autorisation « Lire et modifier toutes vos données sur tous les sites » (`<all_urls>`) est nécessaire parce qu'un contrôle parental doit pouvoir décider, pour **n'importe quel** site, s'il est autorisé ou bloqué. Concrètement, cet accès sert uniquement à :

- rediriger vers la page de blocage une navigation vers un site non autorisé ;
- compter le temps passé sur les sites soumis à une limite.

Le contenu des pages n'est ni lu, ni analysé, ni enregistré.

## Effacer vos données

Désinstaller l'extension supprime définitivement tout ce qu'elle a enregistré. Aucune copie ne subsiste ailleurs, puisqu'il n'y en a jamais eu.

## Enfants

Cette extension est conçue pour être installée par un parent sur l'appareil d'un enfant. Elle ne collecte aucune information permettant d'identifier qui que ce soit : ni nom, ni adresse courriel, ni identifiant d'appareil, ni position.

## Modifications

Toute modification de cette politique sera publiée sur cette page, avec une nouvelle date de mise à jour.

## Contact

Pour toute question sur cette politique, ouvrez une issue sur <https://github.com/Equador1/policies/issues>.
