# Équipe marketing IA

Un **directeur commercial** pilote 7 agents spécialisés pour faire la promotion du site web.

```
directeur-commercial
├── image-de-marque        → marketing/marque/
├── reseaux-sociaux        → marketing/reseaux-sociaux/
├── publicite              → marketing/publicite/
├── seo-contenu            → marketing/seo-contenu/
├── emailing-crm           → marketing/emailing/
├── relations-presse       → marketing/relations-presse/
└── analyste-performance   → marketing/performance/
```

Les définitions des agents se trouvent dans `.claude/agents/`.

## Utilisation

Le directeur doit tourner dans la session principale pour pouvoir déléguer. En effet, un sous-agent ne peut pas lancer d'autres sous-agents.

- **Claude Code (web, application ou CLI)** : `/directeur-commercial lance la promo du site https://…`
- **CLI, session dédiée** : `claude --agent directeur-commercial`
- **Un spécialiste seul** : « Utilise l'agent `seo-contenu` pour auditer la page d'accueil ».

## Déroulé du premier lancement

1. Le directeur analyse le site, puis te pose les questions indispensables : objectif, budget, cible. Il remplit `brief.md`.
2. `image-de-marque` crée la plateforme de marque, socle de tous les autres agents.
3. Le directeur rédige `plan-marketing.md` (objectifs, canaux, feuille de route sur 90 jours).
4. Les spécialistes produisent leurs livrables en parallèle. Le directeur les contrôle et consigne tout dans `journal.md`.

## Exemples de demandes

- `/directeur-commercial prépare le plan du mois prochain`
- `/directeur-commercial crée une campagne pour le lancement de la v2, budget 300 €`
- `/directeur-commercial voici l'export Google Analytics du mois, que faut-il changer ?`

## Garde-fous

- Rien n'est publié, envoyé ni dépensé sans ta validation. Les agents livrent des brouillons prêts à l'emploi.
- Aucun chiffre ni témoignage inventé.
- Conformité RGPD et mentions obligatoires pour l'influence (loi du 9 juin 2023).
