# 🚀 Guide de démarrage rapide

Ce guide vous permet de créer votre premier repository pour travailler avec Claude en **moins de 30 minutes**.

---

## ⏱️ 5 minutes : Création du repository

### Étape 1 : Créer le repository

1. Allez sur GitHub
2. Cliquez sur **New repository**
3. Nommez-le selon le format `claude-[votre-domaine]`
   - Exemple : `claude-expert-comptable`, `claude-dev-web`, `claude-marketing`
4. Ajoutez une description claire
5. Choisissez **Private** (recommandé) ou Public
6. Cochez **Initialize with README**
7. Cliquez sur **Create repository**

### Étape 2 : Cloner en local (optionnel mais recommandé)

```bash
git clone https://github.com/votre-username/claude-[votre-domaine].git
cd claude-[votre-domaine]
```

---

## ⏱️ 15 minutes : Créer votre CLAUD.md

### Option A : Utiliser le template générique

1. Copiez [templates/template-CLAUD.md](./templates/template-CLAUD.md)
2. Renommez-le en `CLAUD.md` à la racine de votre repo
3. Remplissez les sections entre `[crochets]`

### Option B : Utiliser un template spécialisé

**Pour expert-comptable :**
- Copiez [templates/template-CLAUD-expert-comptable.md](./templates/template-CLAUD-expert-comptable.md)

**Pour développeur :** _(à venir)_

**Pour autre profil :** Adaptez le template générique

### Les sections essentielles à remplir ABSOLUMENT :

```markdown
## 🎯 Objectif du repository
[En 2-3 phrases : pourquoi ce repo existe]

## 👤 Profil utilisateur
- Rôle : [Votre métier/rôle]
- Niveau technique : [Débutant/Intermédiaire/Expert]
- Préférences : [Comment vous aimez communiquer]

## 📋 Contexte du projet
[Votre environnement de travail en quelques lignes]

## ⚠️ Contraintes et limites
### Ce que Claude DOIT faire :
- [Point important 1]
- [Point important 2]

### Ce que Claude NE DOIT PAS faire :
- [Interdiction 1]
- [Interdiction 2]
```

**Conseil** : Ne cherchez pas la perfection au premier coup. Commencez simple et enrichissez au fil du temps.

---

## ⏱️ 10 minutes : Créer la structure de base

### Structure minimale pour démarrer

```bash
# À la racine de votre repository
touch CLAUD.md
touch README.md
mkdir contexte
mkdir historique
mkdir templates
```

Ou via l'interface GitHub :
1. Créez chaque fichier via "Add file" > "Create new file"
2. Pour créer un dossier, tapez `nom-dossier/` suivi du nom de fichier

### Contenu minimal du README.md

```markdown
# Claude [Votre Domaine]

Repository de travail avec Claude pour [votre activité].

## Structure

- `CLAUD.md` : Instructions principales pour Claude
- `contexte/` : Informations de contexte
- `historique/` : Décisions et évolution
- `templates/` : Modèles réutilisables

## Utilisation

Ce repository sert de référence permanente pour mes interactions avec Claude.
```

---

## ⏱️ 5 minutes : Configurer vos préférences Claude

### Dans l'interface Claude

1. Allez dans **Settings** (⚙️)
2. Sélectionnez **Profile**
3. Ajoutez dans vos préférences :

```
Si nous discutons d'un repository GitHub qui contient un fichier CLAUD.md, 
lis-le et suis ses directives pour m'assister.

Mon compte GitHub : https://github.com/[votre-username]/
```

### Pourquoi c'est important ?

Avec cette configuration, vous n'aurez plus besoin de demander à Claude de lire CLAUD.md à chaque fois. Il le fera automatiquement quand vous mentionnerez votre repository.

---

## ✅ Checklist de démarrage

Cochez quand c'est fait :

- [ ] Repository créé sur GitHub
- [ ] CLAUD.md créé et rempli (sections essentielles minimum)
- [ ] Structure de dossiers créée (contexte/, historique/, templates/)
- [ ] README.md créé
- [ ] Préférences Claude configurées
- [ ] Premier commit et push effectués

---

## 🎯 Premier test

### Testez votre configuration

1. Ouvrez une nouvelle conversation avec Claude
2. Dites : "Je vais travailler sur mon repository claude-[domaine]. Peux-tu lire le CLAUD.md ?"
3. Claude devrait accéder à votre repo et lire les instructions
4. Demandez : "Résume-moi les points principaux de mes instructions"

Si Claude répond correctement, **bravo ! Votre setup fonctionne.**

---

## 📈 Prochaines étapes

Maintenant que votre base est en place :

### Semaine 1 : Enrichir le contexte

- [ ] Ajoutez un fichier dans `contexte/` avec des infos spécifiques à votre activité
- [ ] Créez un template dans `templates/` pour une tâche récurrente
- [ ] Documentez votre premier échange important dans `historique/`

### Semaine 2-4 : Affiner et itérer

- [ ] Notez les malentendus ou confusions avec Claude
- [ ] Mettez à jour CLAUD.md pour clarifier ces points
- [ ] Ajoutez des exemples concrets de ce que vous attendez

### Mois 2-3 : Optimiser

- [ ] Identifiez les patterns récurrents dans vos conversations
- [ ] Créez des templates ou guides pour ces situations
- [ ] Simplifiez CLAUD.md en déplaçant les détails dans des fichiers annexes

---

## 💡 Astuces de démarrage

### 1. Commencez minimal

**Ne passez pas des heures à tout documenter parfaitement.** Créez les bases et enrichissez au fur et à mesure de vos besoins réels.

### 2. Documentez vos frustrations

Chaque fois que Claude ne comprend pas quelque chose comme vous le souhaitez, **notez-le** et ajoutez une clarification dans CLAUD.md.

### 3. Utilisez les exemples

Dans CLAUD.md, donnez des **exemples concrets** :
```markdown
❌ "Sois précis"
✅ "Quand tu proposes une solution, inclus toujours : 
   1. Le contexte
   2. Les alternatives considérées  
   3. Pourquoi tu recommandes cette option"
```

### 4. Testez régulièrement

Tous les mois, démarrez une nouvelle conversation et testez si Claude comprend bien votre contexte en lisant CLAUD.md.

### 5. Partagez (optionnel)

Si vous trouvez une structure qui marche bien pour vous, n'hésitez pas à partager votre approche avec la communauté (en anonymisant les données sensibles).

---

## 🆘 Problèmes courants au démarrage

### "Claude ne lit pas mon CLAUD.md"

**Solution** :
1. Vérifiez que le fichier s'appelle exactement `CLAUD.md` (pas `claud.md` ou `CLAUDE.md`)
2. Vérifiez que le repository est accessible (public ou vous êtes connecté)
3. Demandez explicitement : "Peux-tu lire le fichier CLAUD.md dans mon repo ?"

### "Je ne sais pas quoi mettre dans CLAUD.md"

**Solution** : Commencez avec le strict minimum :
```markdown
# Instructions pour Claude

Je suis [votre métier]. J'attends de toi que tu m'assistes en [domaine principal].

Important :
- Toujours [préférence 1]
- Ne jamais [contrainte 1]
```

Vous enrichirez au fil de l'eau.

### "Ma structure ne ressemble pas aux exemples"

**C'est normal et OK !** Les exemples sont des suggestions. Adaptez à votre façon de travailler. L'important est la **cohérence** et que ça vous convienne.

---

## 📚 Ressources pour aller plus loin

Une fois votre base créée, consultez :

- [README.md principal](./README.md) : Guide complet sur les structures avancées
- [FAQ.md](./FAQ.md) : Réponses aux questions fréquentes
- [Templates](./templates/) : Autres modèles disponibles

---

## 🎉 Félicitations !

Vous avez maintenant un repository structuré pour travailler efficacement avec Claude. 

**N'oubliez pas** : C'est un outil vivant qui évolue avec votre pratique. Prenez 10 minutes par mois pour le mettre à jour et l'améliorer.

Bonne collaboration avec Claude ! 🚀
