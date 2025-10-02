# Exemples de structures

Ce document présente des exemples concrets de structures de repositories pour différents profils.

---

## 📊 Exemple 1 : Expert-Comptable en Cabinet

### Contexte
Cabinet de 3 collaborateurs, 50 dossiers clients, spécialisé PME/TPE.

### Structure du repository

```
claude-expert-comptable/
├── CLAUD.md                          # Instructions principales
├── README.md                         # Documentation
│
├── profil/
│   ├── competences.md                # Domaines d'expertise détaillés
│   ├── preferences-communication.md  # Style et format préférés
│   └── certifications.md             # Formations et certifications
│
├── contexte/
│   ├── cabinet.md                    # Info sur le cabinet
│   ├── logiciels.md                  # Outils utilisés (Sage, Cegid, etc.)
│   ├── processus-type.md             # Workflow standard
│   └── clients-types.md              # Profils de clients (anonymisés)
│
├── references/
│   ├── plan-comptable-2024.md        # PCG version actuelle
│   ├── baremes-fiscaux-2024.md       # IS, TVA, etc.
│   ├── calendrier-fiscal-2024.md     # Échéances
│   ├── taux-sociaux-2024.md          # Plafonds et taux
│   └── liens-utiles.md               # BOFiP, Légifrance, etc.
│
├── templates/
│   ├── lettre-mission.md             # Template lettre de mission
│   ├── rapport-mensuel.md            # Rapport d'activité client
│   ├── note-honoraires.md            # Note d'honoraires
│   ├── analyse-bilan.md              # Structure d'analyse
│   └── checklist-cloture.md          # Checklist annuelle
│
├── historique/
│   ├── 2024/
│   │   ├── 01-decisions-janvier.md   # Décisions du mois
│   │   ├── 02-decisions-fevrier.md
│   │   └── interactions/             # Échanges importants
│   │       ├── 2024-01-15-tva-cas-complexe.md
│   │       └── 2024-02-03-cloture-difficile.md
│   └── archives/
│       └── 2023/
│
└── veille/
    ├── loi-finances-2024.md          # Changements majeurs
    ├── nouvelle-norme-ANC.md         # Mises à jour normes
    └── jurisprudence-notable.md      # Arrêts importants
```

### Extrait du CLAUD.md

```markdown
## 🎯 Objectif du repository

Assister efficacement dans la gestion comptable et fiscale de mes clients,
en respectant les normes professionnelles et la déontologie de l'Ordre des
Experts-Comptables.

## ⚠️ Contraintes strictes

### Ce que Claude DOIT FAIRE :
- Citer systématiquement les sources (articles CGI, BOFiP, doctrine ANC)
- Proposer plusieurs options quand la doctrine est silencieuse
- Alerter quand une validation humaine est nécessaire
- Vérifier les dates de clôture et régimes fiscaux

### Ce que Claude NE DOIT JAMAIS FAIRE :
- Prendre de décision définitive sans validation humaine
- Inventer des données chiffrées ou des références légales
- Garantir un traitement comptable sans vérification
- Révéler des informations clients (même dans l'historique)
```

### Utilisation typique

**Début de conversation :**
```
"Je travaille sur le dossier d'un client en SAS soumis à l'IS. 
Clôture au 31/12/2024. Peux-tu m'assister sur les écritures de clôture ?"
```

**Claude lit automatiquement CLAUD.md et sait :**
- Citer les sources
- Proposer une checklist de clôture
- Alerter sur les points nécessitant validation
- Utiliser les templates appropriés

---

## 💻 Exemple 2 : Développeur Full-Stack Freelance

### Contexte
Freelance spécialisé React/Node.js, plusieurs projets clients en parallèle.

### Structure du repository

```
claude-dev-fullstack/
├── CLAUD.md                          # Instructions principales
├── README.md
│
├── profil/
│   ├── stack.md                      # Technologies maîtrisées
│   ├── preferences-code.md           # Conventions de code
│   └── outils.md                     # VS Code, extensions, etc.
│
├── contexte/
│   ├── activite.md                   # Type de missions
│   ├── process-dev.md                # Workflow de développement
│   └── contraintes.md                # Limites techniques, délais
│
├── projets/
│   ├── projet-a/
│   │   ├── info.md                   # Contexte du projet
│   │   ├── tech-stack.md             # Technos utilisées
│   │   ├── architecture.md           # Architecture
│   │   └── decisions.md              # Décisions techniques
│   ├── projet-b/
│   └── projet-c/
│
├── snippets/
│   ├── react/
│   │   ├── custom-hooks.md           # Hooks réutilisables
│   │   ├── components.md             # Composants types
│   │   └── patterns.md               # Patterns courants
│   ├── nodejs/
│   │   ├── middleware.md
│   │   ├── auth.md
│   │   └── database.md
│   └── utils/
│       ├── helpers.md
│       └── validators.md
│
├── guides/
│   ├── deployment.md                 # Procédure de déploiement
│   ├── testing.md                    # Stratégie de tests
│   ├── documentation.md              # Comment documenter
│   └── debugging.md                  # Techniques de debug
│
└── historique/
    └── decisions-architecture/
        ├── 2024-01-choix-state-management.md
        ├── 2024-02-migration-typescript.md
        └── 2024-03-api-architecture.md
```

### Extrait du CLAUD.md

```markdown
## 🔧 Guidelines techniques

### Stack principal
- **Frontend** : React 18+, TypeScript, Tailwind CSS
- **Backend** : Node.js, Express, PostgreSQL
- **DevOps** : Docker, GitHub Actions, Vercel/Railway

### Conventions de code
- ESLint + Prettier (config Airbnb)
- Commits conventionnels (feat, fix, docs, refactor, etc.)
- Tests : Jest + React Testing Library
- Documentation : JSDoc pour fonctions complexes

### Préférences
- Composants fonctionnels uniquement (pas de classes)
- Custom hooks pour logique réutilisable
- Typescript strict mode activé
- Prefer functional programming patterns
```

---

## 🎨 Exemple 3 : Designer UI/UX

### Contexte
Designer indépendant travaillant sur applications web et mobile.

### Structure du repository

```
claude-design-uiux/
├── CLAUD.md
├── README.md
│
├── profil/
│   ├── specialites.md                # UI, UX, branding, etc.
│   ├── outils.md                     # Figma, Adobe XD, etc.
│   └── process-design.md             # Méthodologie
│
├── contexte/
│   ├── clients-types.md              # Profils de clients
│   ├── contraintes.md                # Accessibilité, plateformes
│   └── livrables.md                  # Formats de livraison
│
├── projets/
│   ├── app-mobile-saas/
│   │   ├── brief.md
│   │   ├── personas.md
│   │   ├── user-flows.md
│   │   └── iterations.md
│   └── site-ecommerce/
│
├── design-system/
│   ├── colors.md                     # Palettes favorites
│   ├── typography.md                 # Typographies
│   ├── components.md                 # Composants réutilisables
│   └── patterns.md                   # Patterns UI
│
├── references/
│   ├── inspiration.md                # Sources d'inspiration
│   ├── wcag-guidelines.md            # Accessibilité
│   └── responsive-breakpoints.md    # Breakpoints standards
│
└── templates/
    ├── brief-client.md               # Template de brief
    ├── design-review.md              # Grille d'évaluation
    └── presentation-concept.md       # Structure de présentation
```

---

## 📝 Exemple 4 : Gestionnaire de Projet

### Contexte
Chef de projet dans une PME tech, plusieurs projets en parallèle.

### Structure du repository

```
claude-project-management/
├── CLAUD.md
├── README.md
│
├── profil/
│   ├── methodologie.md               # Agile, Scrum, Kanban
│   ├── outils.md                     # Jira, Notion, Slack
│   └── equipe.md                     # Composition d'équipe
│
├── contexte/
│   ├── entreprise.md                 # Contexte organisationnel
│   ├── contraintes.md                # Budget, délais, ressources
│   └── stakeholders.md               # Parties prenantes
│
├── projets/
│   ├── projet-alpha/
│   │   ├── charter.md                # Charte projet
│   │   ├── roadmap.md                # Roadmap
│   │   ├── risks.md                  # Gestion des risques
│   │   ├── meetings/                 # CR de réunions
│   │   └── decisions.md              # Décisions clés
│   └── projet-beta/
│
├── templates/
│   ├── charter-template.md
│   ├── meeting-notes-template.md
│   ├── status-report-template.md
│   ├── risk-register-template.md
│   └── sprint-planning-template.md
│
├── processes/
│   ├── onboarding-projet.md          # Process nouveau projet
│   ├── gestion-changement.md         # Change management
│   ├── communication.md              # Plan de communication
│   └── reporting.md                  # Rapports et KPIs
│
└── historique/
    ├── retrospectives/
    │   ├── 2024-Q1-retro.md
    │   └── 2024-Q2-retro.md
    └── lessons-learned/
        ├── projet-alpha-lessons.md
        └── projet-beta-lessons.md
```

---

## 📚 Exemple 5 : Formateur / Enseignant

### Contexte
Formateur indépendant en développement web, plusieurs sessions par an.

### Structure du repository

```
claude-formation-dev/
├── CLAUD.md
├── README.md
│
├── profil/
│   ├── domaines-expertise.md         # Sujets enseignés
│   ├── pedagogie.md                  # Approche pédagogique
│   └── public-cible.md               # Profils d'apprenants
│
├── contexte/
│   ├── formats-formation.md          # Présentiel, distanciel, etc.
│   ├── durees.md                     # 1 jour, 5 jours, etc.
│   └── certifications.md             # Certifications délivrées
│
├── cours/
│   ├── html-css-debutant/
│   │   ├── programme.md              # Programme détaillé
│   │   ├── objectifs-pedagogiques.md
│   │   ├── exercices/
│   │   ├── evaluations/
│   │   └── ressources.md
│   ├── javascript-avance/
│   └── react-fondamentaux/
│
├── templates/
│   ├── programme-formation.md
│   ├── fiche-exercice.md
│   ├── grille-evaluation.md
│   └── questionnaire-satisfaction.md
│
├── supports/
│   ├── slides/                       # Présentations
│   ├── cheatsheets/                  # Mémos
│   └── demos/                        # Code de démo
│
└── historique/
    ├── sessions/
    │   ├── 2024-01-formation-paris/
    │   │   ├── feedback.md
    │   │   ├── points-blocage.md
    │   │   └── ameliorations.md
    │   └── 2024-02-formation-lyon/
    └── evolution-programmes/
```

---

## 🏢 Exemple 6 : Consultant indépendant

### Contexte
Consultant stratégie digitale pour PME.

### Structure du repository

```
claude-consulting-digital/
├── CLAUD.md
├── README.md
│
├── profil/
│   ├── expertises.md                 # Domaines de conseil
│   ├── methodologie.md               # Approche conseil
│   └── deliverables.md               # Types de livrables
│
├── contexte/
│   ├── positionnement.md             # Positionnement marché
│   ├── clients-ideaux.md             # Profil client idéal
│   └── tarification.md               # Modèle tarifaire
│
├── missions/
│   ├── mission-001/
│   │   ├── brief.md
│   │   ├── diagnostic.md
│   │   ├── recommandations.md
│   │   └── roadmap.md
│   └── mission-002/
│
├── frameworks/
│   ├── audit-digital.md              # Framework d'audit
│   ├── strategie-contenu.md          # Méthodo contenu
│   ├── transformation-digitale.md
│   └── analyse-concurrentielle.md
│
├── templates/
│   ├── proposition-commerciale.md
│   ├── rapport-audit.md
│   ├── plan-action.md
│   └── presentation-client.md
│
├── knowledge-base/
│   ├── tendances-digital.md          # Veille tendances
│   ├── outils-recommandes.md         # Stack d'outils
│   ├── benchmarks.md                 # Benchmarks sectoriels
│   └── best-practices.md             # Bonnes pratiques
│
└── historique/
    └── succes-stories/
        ├── cas-client-a.md
        └── cas-client-b.md
```

---

## 💡 Points communs des bonnes structures

### 1. Clarté et cohérence

Toutes ces structures partagent :
- Un **CLAUD.md** clair et concis
- Une **organisation logique** des dossiers
- Des **noms explicites** pour les fichiers et dossiers
- Une **documentation** à jour

### 2. Adaptabilité

Chaque structure est adaptée au :
- **Métier** de la personne
- **Volume** d'information à gérer
- **Fréquence** d'utilisation
- **Type de livrables** produits

### 3. Évolutivité

Les structures permettent :
- D'**ajouter** facilement de nouveaux projets/clients
- De **migrer** vers une structure plus complexe si besoin
- D'**archiver** sans perdre l'historique

---

## 🚀 Comment adapter ces exemples ?

### Étape 1 : Identifier votre profil

Quel exemple ressemble le plus à votre activité ?
- Métier réglementé (expert-comptable)
- Technique (développeur, designer)
- Gestion (chef de projet)
- Pédagogique (formateur)
- Conseil (consultant)

### Étape 2 : Prendre ce qui vous parle

Ne copiez pas tout ! Prenez uniquement :
- Les dossiers qui correspondent à votre activité
- La profondeur adaptée à votre volume de travail
- Les templates dont vous avez vraiment besoin

### Étape 3 : Simplifier puis enrichir

**Commencez minimal :**
```
mon-repo/
├── CLAUD.md
├── profil/
├── contexte/
├── templates/
└── historique/
```

**Puis ajoutez progressivement** ce dont vous avez besoin.

---

## 📊 Tableau comparatif

| Profil | Complexité | Dossiers clés | Points d'attention |
|--------|------------|---------------|-------------------|
| Expert-comptable | ⭐⭐⭐⭐ | references/, veille/ | Réglementation, confidentialité |
| Développeur | ⭐⭐⭐ | projets/, snippets/ | Documentation technique |
| Designer | ⭐⭐⭐ | design-system/, projets/ | Versioning des assets |
| Chef de projet | ⭐⭐⭐⭐ | projets/, processes/ | Gestion multi-projets |
| Formateur | ⭐⭐⭐ | cours/, supports/ | Réutilisabilité du contenu |
| Consultant | ⭐⭐⭐ | missions/, frameworks/ | Knowledge base |

---

## 🎯 Prochaines étapes

Maintenant que vous avez vu ces exemples :

1. **Choisissez** la structure qui se rapproche le plus de votre activité
2. **Simplifiez-la** pour votre besoin actuel
3. **Créez** votre repository en suivant le [QUICKSTART.md](./QUICKSTART.md)
4. **Itérez** au fil de vos besoins

N'oubliez pas : **Il n'y a pas de structure parfaite, seulement celle qui vous convient !**
