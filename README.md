# Guide GitHub pour travailler avec Claude

Ce repository contient les bonnes pratiques et recommandations pour structurer vos repositories GitHub afin de collaborer efficacement avec Claude.

---

## 🚀 Démarrage rapide

**Nouveau ?** Commencez par le [Guide de démarrage rapide](./QUICKSTART.md) (30 minutes chrono)

**Besoin d'exemples ?** Consultez les [Exemples de structures](./examples/EXAMPLES.md)

**Questions ?** Voir la [FAQ](./FAQ.md)

---

## 📚 Documentation complète

### 📋 Guides principaux

1. **[Guide de démarrage rapide](./QUICKSTART.md)** ⚡
   - Créer votre premier repository en 30 minutes
   - Configuration minimale
   - Premier test avec Claude

2. **[Exemples de structures](./examples/EXAMPLES.md)** 📊
   - Expert-Comptable
   - Développeur Full-Stack
   - Designer UI/UX
   - Chef de projet
   - Formateur
   - Consultant

3. **[FAQ - Questions fréquentes](./FAQ.md)** ❓
   - Questions générales
   - Structure et organisation
   - Le fichier CLAUD.md
   - Utilisation pratique
   - Problèmes courants

### 📄 Templates disponibles

Dans le dossier [templates/](./templates/) :

- **[template-CLAUD.md](./templates/template-CLAUD.md)** - Template générique complet
- **[template-CLAUD-expert-comptable.md](./templates/template-CLAUD-expert-comptable.md)** - Template spécialisé comptabilité

---

## 🎯 Pourquoi une structure dédiée ?

Travailler avec Claude sur des projets nécessite une organisation claire pour :
- **Persistance du contexte** : Claude peut retrouver rapidement les informations importantes
- **Traçabilité** : Historique clair des interactions et décisions
- **Autonomie** : Permettre à Claude de comprendre le projet sans explications répétées
- **Collaboration** : Faciliter le travail sur plusieurs profils ou projets

---

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

---

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

👉 Voir [template-CLAUD.md](./templates/template-CLAUD.md) pour un modèle complet.

---

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

---

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

---

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

---

## 📖 Table des matières complète

### Guides
- [🚀 Démarrage rapide](./QUICKSTART.md) - 30 minutes pour démarrer
- [📊 Exemples de structures](./examples/EXAMPLES.md) - Cas concrets par profil
- [❓ FAQ](./FAQ.md) - Questions fréquentes

### Templates
- [📄 Template CLAUD.md générique](./templates/template-CLAUD.md)
- [📄 Template CLAUD.md Expert-Comptable](./templates/template-CLAUD-expert-comptable.md)

### Ressources
- Structure recommandée (ci-dessus)
- Bonnes pratiques (ci-dessus)
- Migration (ci-dessus)

---

## 🤝 Contribution

Ce guide est évolutif ! N'hésitez pas à :
- Proposer des améliorations via **Issues**
- Soumettre des **Pull Requests**
- Partager votre expérience et vos structures

### Comment contribuer ?

1. Forkez ce repository
2. Créez une branche pour votre contribution
3. Ajoutez votre contenu ou modification
4. Soumettez une Pull Request avec une description claire

**Contributions bienvenues :**
- Nouveaux templates pour d'autres profils
- Exemples de structures supplémentaires
- Corrections et améliorations
- Traductions

---

## 📄 Licence

MIT - Libre d'utilisation et d'adaptation

Vous êtes libre de :
- Utiliser ce guide pour vos projets personnels ou professionnels
- Modifier et adapter les templates à vos besoins
- Partager et redistribuer

---

## 🌟 Pour aller plus loin

### Configuration dans Claude

N'oubliez pas de configurer vos préférences utilisateur dans Claude :

```
Dans Settings > Profile, ajoutez :

"Si nous discutons d'un repository GitHub qui contient un fichier CLAUD.md, 
lis-le et suis ses directives pour m'assister.

Mon compte GitHub : https://github.com/[votre-username]/"
```

### Ressources externes

- [Documentation GitHub](https://docs.github.com)
- [Guide Markdown](https://www.markdownguide.org)
- [Conventional Commits](https://www.conventionalcommits.org)

---

## 📞 Support

Des questions ? Plusieurs options :
- Consultez la [FAQ](./FAQ.md)
- Créez une [Issue](../../issues) sur ce repository
- Consultez les [Discussions](../../discussions)

---

**Note** : Ce guide est conçu pour optimiser la collaboration entre vous et Claude. Adaptez-le à vos besoins spécifiques !

**Dernière mise à jour** : Octobre 2025  
**Version** : 1.0
