# Guide GitHub pour travailler avec Claude

Ce repository contient les bonnes pratiques et recommandations pour structurer vos repositories GitHub afin de collaborer efficacement avec Claude.

## 📋 Table des matières

- [Pourquoi une structure dédiée ?](#pourquoi-une-structure-dédiée)
- [Structure recommandée](#structure-recommandée)
- [Le fichier CLAUD.md](#le-fichier-claudmd)
- [Organisation multi-profils](#organisation-multi-profils)
- [Exemples de structures](#exemples-de-structures)
- [Bonnes pratiques](#bonnes-pratiques)

## 🎯 Pourquoi une structure dédiée ?

Travailler avec Claude sur des projets nécessite une organisation claire pour :
- **Persistance du contexte** : Claude peut retrouver rapidement les informations importantes
- **Traçabilité** : Historique clair des interactions et décisions
- **Autonomie** : Permettre à Claude de comprendre le projet sans explications répétées
- **Collaboration** : Faciliter le travail sur plusieurs profils ou projets

## 🏗️ Structure recommandée

### Option 1 : Un repository par profil/projet (RECOMMANDÉ)

```
github.com/votre-username/
├── claude-expert-comptable/
│   ├── CLAUD.md
│   ├── README.md
│   ├── profil/
│   ├── contexte/
│   └── historique/
│
├── claude-dev-web/
│   ├── CLAUD.md
│   ├── README.md
│   └── ...
│
└── claude-github-guide/
    └── README.md (ce fichier)
```

**Avantages :**
- Isolation complète entre profils
- Gestion des permissions par profil
- Historique git dédié
- Facilité de partage

### Option 2 : Mono-repository avec sous-dossiers

```
github.com/votre-username/claude-profiles/
├── README.md
├── expert-comptable/
│   ├── CLAUD.md
│   └── ...
├── dev-web/
│   ├── CLAUD.md
│   └── ...
└── shared/
    └── templates/
```

**Avantages :**
- Centralisation
- Ressources partagées
- Un seul repo à gérer

**Inconvénients :**
- Moins flexible
- Historique git mélangé

## 📄 Le fichier CLAUD.md

Le fichier `CLAUD.md` est **essentiel**. C'est le premier fichier que Claude devrait lire pour comprendre le contexte du repository.

### Structure type d'un CLAUD.md

```markdown
# Instructions pour Claude

## 🎯 Objectif du repository
[Description claire du but du repository]

## 👤 Profil utilisateur
- **Rôle** : [ex: Expert-comptable, Développeur, etc.]
- **Niveau technique** : [Débutant, Intermédiaire, Expert]
- **Préférences** : [Communication, format de code, etc.]

## 📋 Contexte du projet
[Informations importantes sur le projet, l'entreprise, les contraintes]

## 🔧 Guidelines techniques
- Langages/frameworks utilisés
- Conventions de code
- Structure des fichiers
- Outils et dépendances

## 📝 Historique et décisions
[Liens vers les documents d'historique ou décisions importantes]

## ⚠️ Contraintes et limites
[Ce qu'il faut éviter, limitations spécifiques]

## 📚 Ressources
[Liens vers documentation externe, standards, etc.]
```

Voir [template-CLAUD.md](./templates/template-CLAUD.md) pour un modèle complet.

## 🎭 Organisation multi-profils

### Quand créer un nouveau profil ?

Créez un repository séparé quand :
- **Domaine d'expertise différent** : comptabilité vs développement
- **Contexte métier distinct** : projets clients différents
- **Équipe différente** : permissions et accès différents
- **Cycle de vie indépendant** : archivage séparé

### Nommage des repositories

**Format recommandé :** `claude-[domaine]-[spécificité]`

Exemples :
- `claude-expert-comptable`
- `claude-dev-frontend`
- `claude-legal-contrats`
- `claude-marketing-contenus`

## 📁 Exemples de structures

### Structure pour un profil Expert-Comptable

```
claude-expert-comptable/
├── CLAUD.md                    # Instructions pour Claude
├── README.md                   # Documentation utilisateur
├── profil/
│   ├── competences.md          # Domaines d'expertise
│   └── preferences.md          # Préférences de travail
├── contexte/
│   ├── entreprise.md           # Info sur l'entreprise
│   ├── reglementations.md      # Cadre légal
│   └── processus.md            # Processus métier
├── historique/
│   ├── 2025-01-decisions.md   # Décisions importantes
│   └── interactions/           # Résumés d'échanges
│       ├── 2025-01-15.md
│       └── 2025-01-22.md
├── templates/
│   ├── rapport-mensuel.md
│   └── analyse-bilan.md
└── references/
    ├── plan-comptable.pdf
    └── baremes-fiscaux.md
```

### Structure pour un profil Développeur

```
claude-dev-web/
├── CLAUD.md
├── README.md
├── project/
│   ├── architecture.md
│   ├── tech-stack.md
│   └── conventions.md
├── docs/
│   ├── api/
│   └── guides/
├── snippets/
│   ├── react/
│   └── utils/
└── historique/
    └── decisions/
```

## ✅ Bonnes pratiques

### 1. Commits clairs et structurés

Utilisez des commits conventionnels :
```
feat: add monthly report template
docs: update CLAUD.md with new guidelines
fix: correct accounting calculation in template
refactor: reorganize context folder structure
```

### 2. Mise à jour régulière

- Mettez à jour `CLAUD.md` après chaque décision importante
- Documentez les changements de processus
- Archivez les anciens documents si nécessaire

### 3. Documentation du contexte

- Gardez les informations importantes dans le repository
- Évitez les références à des documents externes inaccessibles
- Datez les informations qui peuvent devenir obsolètes

### 4. Utilisation des issues

Pour suivre :
- Questions récurrentes
- Tâches à accomplir
- Améliorations du profil

### 5. Branches et workflow

Pour les profils simples :
- Travaillez directement sur `main`
- Utilisez des branches pour tester de nouvelles structures

Pour les profils complexes :
- `main` : version stable
- `dev` : modifications en cours
- Feature branches : expérimentations

## 🔄 Migration depuis une structure existante

Si vous avez déjà un repository `docs` avec plusieurs profils :

1. **Créer les nouveaux repositories**
   ```bash
   # Via GitHub ou l'API
   ```

2. **Migrer le contenu**
   ```bash
   # Copier le dossier du profil
   cp -r docs/expertComptable/* claude-expert-comptable/
   ```

3. **Créer le fichier CLAUD.md**
   ```bash
   # Utiliser le template fourni
   ```

4. **Conserver l'historique (optionnel)**
   ```bash
   # Utiliser git filter-branch ou git subtree
   ```

## 🚀 Pour commencer

1. Clonez ce repository comme référence
2. Copiez le template `CLAUD.md` approprié
3. Créez votre premier repository de profil
4. Adaptez la structure à vos besoins
5. Itérez et améliorez au fil du temps

## 📖 Ressources complémentaires

- [Templates](./templates/) : Modèles prêts à l'emploi
- [Exemples](./examples/) : Cas d'usage concrets
- [FAQ](./FAQ.md) : Questions fréquentes

## 🤝 Contribution

Ce guide est évolutif ! N'hésitez pas à proposer des améliorations via issues ou pull requests.

## 📄 Licence

MIT - Libre d'utilisation et d'adaptation

---

**Note** : Ce guide est conçu pour optimiser la collaboration entre vous et Claude. Adaptez-le à vos besoins spécifiques !
