# CampusConnect — agile-team-project

Projet du TD5 « Gestion collaborative d'un projet Agile » (Jira · Git · GitHub) — **Groupe Phonk**.

CampusConnect est l'application des événements du campus : les organisateurs publient des événements, les étudiants les consultent et s'y inscrivent.

## Sprint Goal (CCG2 Sprint 1)

> Permettre à un étudiant de découvrir les événements du campus publiés par un organisateur, de les retrouver facilement et de s'y inscrire : première livraison utilisable de CampusConnect.

## Équipe et répartition

| Membre | User Story Jira | Branche | Fichier |
|---|---|---|---|
| Noé de Rosny | CCG2-4 — US06 Créer et publier un nouvel événement | `feature/CCG2-4-create-event` | `create-event.html` |
| Nathan Gaudin | CCG2-5 — US01 Consulter la liste des événements à venir | `feature/CCG2-5-events-list` | `events.html` |
| Fatih Emiral | CCG2-6 — US03 S'inscrire à un événement | `feature/CCG2-6-event-registration` | `event-detail.html` |

## Liens

- Projet Jira : https://efrei-team-wowz5nfw.atlassian.net/jira/software/projects/CCG2/boards/34
- Tableau GitHub Projects : onglet **Projects** du dépôt

## Dépendances entre les Stories

US06 (créer) → US01 (lister) → US03 (s'inscrire). Pour travailler en parallèle, les trois pages partagent un même format de données, stocké dans le navigateur (`localStorage`, clé `campusconnect.events`) :

```json
{ "id": "evt-1", "title": "Soirée d'intégration", "date": "2026-11-25", "time": "19:00",
  "location": "Amphi A", "description": "...", "registered": false }
```

Chaque page fonctionne seule avec des événements d'exemple si la liste est vide.

## Lancer le projet

Ouvrir `events.html` dans un navigateur (aucune installation nécessaire).

## Règles de l'équipe

1. Pas de push direct sur `main` : une branche `feature/<CLE-JIRA>-<description>` par Story.
2. Messages de commit et titres de PR préfixés par la clé Jira (`CCG2-4: ...`).
3. Toute fusion passe par une Pull Request relue et approuvée par un autre membre.
4. Jamais de mot de passe, jeton ou secret dans le dépôt.

## Definition of Done

- Critères d'acceptation de la Story vérifiés et testés
- PR relue, commentaires traités, approuvée puis fusionnée dans `main`
- Ticket Jira lié à la branche et à la PR, puis passé à « Terminé »
