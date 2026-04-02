# 🧭 Dev Pilot Companion — Ton Copilote Dans Claude Code

Le skill Claude Code qui pilote ton développement après la planification Dev Pilot.

---

## C'est Quoi ?

**Dev Pilot** (dans Claude.ai) planifie ton projet : interview, architecture, fichiers.
**Dev Pilot Companion** (dans Claude Code) pilote la construction : suivi, tâches, diagnostics.

Le Companion lit tes fichiers Dev Pilot (CLAUDE.md, PLAN.md, USER-STORIES.md, etc.)
et te guide directement dans Claude Code — sans retourner dans Claude.ai.

---

## Installation

```bash
npx skills add slimcoh/devpilot-companion
```

Ou manuellement :
```bash
# Copie le dossier dans tes skills Claude Code
mkdir -p ~/.claude/skills/devpilot
# Copie le SKILL.md dans ce dossier
```

---

## Commandes

| Commande | Ce qu'elle fait |
|----------|----------------|
| `/devpilot` | Activer le companion + voir le statut |
| `/devpilot:status` | Voir ta progression (barres + tâches) |
| `/devpilot:next` | Prochaine tâche à faire |
| `/devpilot:checkpoint` | Vérifier qu'une phase est complète |
| `/devpilot:story CODE-XXX` | Implémenter une user story |
| `/devpilot:help` | Diagnostic si tu es bloqué |
| `/devpilot:launch` | Checklist pré-lancement |

---

## Prérequis

- Claude Code installé
- Un projet planifié par Dev Pilot (avec au minimum CLAUDE.md + PLAN.md)

---

## Comment ça Marche

1. Tu planifies ton projet avec Dev Pilot dans Claude.ai
2. Tu reçois tes fichiers (CLAUDE.md, PLAN.md, USER-STORIES.md, etc.)
3. Tu les mets dans ton dossier projet
4. Tu installes le Companion (`npx skills add ...`)
5. Tu ouvres Claude Code et tu tapes `/devpilot`
6. Le Companion lit tes fichiers et te pilote

À partir de là, tout se passe dans Claude Code :
- Il sait où tu en es dans le plan
- Il te donne la prochaine tâche
- Il implémente les user stories une par une
- Il vérifie que chaque phase est terminée
- Il diagnostique tes problèmes
- Il lance la checklist avant mise en ligne

---

## Licence

Inclus avec l'achat de Dev Pilot. Usage personnel et commercial.
Redistribution interdite.
