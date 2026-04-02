# 🧭 Dev Pilot Companion

Le copilote Claude Code qui pilote ton développement après la planification Dev Pilot.

---

## C'est Quoi ?

**Dev Pilot** (dans Claude.ai) planifie ton projet : interview, architecture, fichiers.
**Dev Pilot Companion** (dans Claude Code) pilote la construction : suivi, tâches, diagnostics.

Le Companion lit tes fichiers Dev Pilot (CLAUDE.md, PLAN.md, USER-STORIES.md, etc.)
et te guide directement dans Claude Code — sans retourner dans Claude.ai.

---

## Installation

```bash
claude mcp add-skill https://github.com/[TON-USERNAME]/devpilot-companion
```

Ou manuellement :

```bash
mkdir -p ~/.claude/skills/devpilot
curl -o ~/.claude/skills/devpilot/SKILL.md https://raw.githubusercontent.com/[TON-USERNAME]/devpilot-companion/main/SKILL.md
```

---

## Prérequis

- [Claude Code](https://docs.anthropic.com/en/docs/claude-code) installé
- Un projet planifié par Dev Pilot (avec au minimum `CLAUDE.md` + `PLAN.md` à la racine)

---

## Commandes

| Commande | Ce qu'elle fait |
|----------|----------------|
| `/devpilot` | Activer le companion + voir le statut |
| `/devpilot:status` | Voir ta progression (barres visuelles) |
| `/devpilot:next` | Prochaine tâche à faire |
| `/devpilot:checkpoint` | Vérifier qu'une phase est complète |
| `/devpilot:story CODE-XXX` | Implémenter une user story |
| `/devpilot:help` | Diagnostic si tu es bloqué |
| `/devpilot:launch` | Checklist pré-lancement |

---

## Comment ça Marche

```
1. Tu planifies ton projet avec Dev Pilot (Claude.ai)
2. Tu reçois tes fichiers (CLAUDE.md, PLAN.md, USER-STORIES.md, etc.)
3. Tu les mets à la racine de ton dossier projet
4. Tu installes le Companion (voir Installation)
5. Tu ouvres Claude Code dans ton projet
6. Tu tapes /devpilot → Le Companion prend le relais
```

À partir de là, tout se passe dans Claude Code :

- 📊 Il sait où tu en es dans le plan
- 🎯 Il te donne la prochaine tâche
- 🔧 Il implémente les user stories une par une
- ✅ Il vérifie que chaque phase est terminée
- 🆘 Il diagnostique tes problèmes
- 🚀 Il lance la checklist avant mise en ligne

---

## Fichiers Dev Pilot Reconnus

Le Companion cherche ces fichiers à la racine de ton projet :

| Fichier | Rôle | Obligatoire |
|---------|------|-------------|
| `CLAUDE.md` | Règles et conventions du projet | ✅ |
| `PLAN.md` | Plan de développement en 5 phases | ✅ |
| `USER-STORIES.md` | Fonctionnalités à implémenter | ✅ |
| `BRAND.md` | Identité visuelle | Recommandé |
| `SCHEMA.sql` | Structure de la base de données | Si BDD |
| `API.md` | Documentation des endpoints | Si API |
| `GUIDE-OUTILS.md` | Outils par phase | Recommandé |
| `PRE-LAUNCH.md` | Checklist avant mise en ligne | Recommandé |

---

## Exemple d'Utilisation

```
> /devpilot

🧭 Dev Pilot Companion activé !

📋 Projet : MonSaaS
📊 Phase actuelle : Phase 1 — Fondations
✅ Tâches faites : 3 / 12
⬜ Prochaines : Layout principal, Auth, BDD

💡 Tape /devpilot:next pour commencer !

> /devpilot:next

🎯 Prochaine tâche : Layout principal

📋 User Story : NAV-001
En tant qu'utilisateur, je veux voir un header et une sidebar,
pour naviguer facilement dans l'application.

🔧 Ce que je vais faire :
1. Créer le layout avec header + sidebar
2. Appliquer les couleurs du BRAND.md
3. Rendre responsive (sidebar collapsible sur mobile)

On y va ?
```

---

## Obtenir Dev Pilot

Le Companion fonctionne avec les fichiers générés par **Dev Pilot**, le skill de planification pour Claude.ai.

👉 [Obtenir Dev Pilot]([LIEN-VERS-TA-PAGE-DE-VENTE])

---

## Licence

Inclus avec l'achat de Dev Pilot. Usage personnel et commercial.
Redistribution interdite.
