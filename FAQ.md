# FAQ - Questions fréquentes

## 📋 Table des matières

- [Questions générales](#questions-générales)
- [Structure et organisation](#structure-et-organisation)
- [Le fichier CLAUD.md](#le-fichier-claudmd)
- [Utilisation pratique](#utilisation-pratique)
- [Problèmes courants](#problèmes-courants)

---

## Questions générales

### Pourquoi créer une structure GitHub pour travailler avec Claude ?

Claude n'a pas de mémoire persistante entre les conversations. En créant une structure GitHub bien organisée :
- Vous donnez à Claude un contexte permanent et accessible
- Vous documentez votre collaboration et vos décisions
- Vous créez une base de connaissances réutilisable
- Vous facilitez la reprise de conversations précédentes

### Est-ce que mes repositories doivent être publics ou privés ?

**Recommandation** : Privés par défaut, surtout si :
- Vous y mettez des informations personnelles ou professionnelles sensibles
- Vous documentez des processus internes d'entreprise
- Vous travaillez avec des données clients (même anonymisées)

Rendez-les publics uniquement si vous souhaitez partager votre approche avec d'autres.

### Combien de temps faut-il pour mettre en place cette structure ?

- **Setup initial** : 30-60 minutes pour créer le repository et le fichier CLAUD.md
- **Peaufinage** : 2-3 heures pour bien documenter le contexte
- **Maintenance** : 10-20 minutes par mois pour les mises à jour

L'investissement initial est rapidement rentabilisé par le gain de temps dans vos interactions avec Claude.

---

## Structure et organisation

### Dois-je vraiment créer un repository par profil ?

**Ça dépend de vos besoins** :

**Un repo par profil** si :
- Vous avez des contextes très différents (ex: comptabilité ET développement)
- Vous voulez des permissions différentes
- Les profils évoluent indépendamment

**Un mono-repo** si :
- Vous avez peu de profils (2-3 maximum)
- Ils partagent beaucoup de ressources communes
- Vous préférez la simplicité

### Quelle est la différence entre /contexte/, /profil/ et /historique/ ?

- **`/profil/`** : Informations sur VOUS (compétences, préférences, style de travail)
- **`/contexte/`** : Informations sur VOTRE ENVIRONNEMENT (entreprise, projet, contraintes)
- **`/historique/`** : ÉVÉNEMENTS et DÉCISIONS passés (ce qui s'est passé chronologiquement)

### Dois-je versionner mes fichiers de contexte ?

**Oui, absolument !** Git est fait pour ça :
- Vous pouvez voir l'évolution de votre contexte
- Vous pouvez revenir en arrière si besoin
- Vous documentez naturellement les changements

### Comment organiser plusieurs clients/projets ?

**Option 1** : Un dossier par client dans le même repo
```
claude-expert-comptable/
├── CLAUD.md
├── clients/
│   ├── client-a/
│   ├── client-b/
│   └── client-c/
```

**Option 2** : Un repo par client (si très gros clients)
```
claude-comptable-client-a/
claude-comptable-client-b/
```

**Recommandation** : Option 1 sauf si vous avez des clients avec des besoins très spécifiques ou des contraintes de confidentialité strictes.

---

## Le fichier CLAUD.md

### Le fichier doit-il vraiment s'appeler "CLAUD.md" ?

**Non**, c'est une convention recommandée mais pas obligatoire. Vous pouvez l'appeler :
- `INSTRUCTIONS.md`
- `CONTEXT.md`
- `README-CLAUDE.md`

L'important est d'être cohérent et de le mentionner dans vos préférences utilisateur.

### Combien de détails dois-je mettre dans CLAUD.md ?

**Règle d'or** : Assez pour que Claude comprenne votre contexte sans vous, mais pas au point que le fichier devienne illisible.

**Trop peu** ❌ :
```markdown
# Instructions
Je suis comptable. Aide-moi.
```

**Trop** ❌ :
```markdown
[50 pages de documentation exhaustive sur chaque détail de votre pratique]
```

**Juste bien** ✅ :
```markdown
[2-4 pages avec l'essentiel : qui vous êtes, votre contexte, 
vos contraintes, vos préférences, et des liens vers des docs détaillées]
```

### Dois-je tout mettre dans CLAUD.md ou créer d'autres fichiers ?

**Structure recommandée** :
- **CLAUD.md** : Vue d'ensemble et références (2-5 pages max)
- **Autres fichiers** : Détails spécifiques (procédures, templates, références)

CLAUD.md doit être comme une table des matières commentée.

### À quelle fréquence dois-je mettre à jour CLAUD.md ?

**Mettez à jour quand** :
- Vos objectifs changent significativement
- Vous découvrez un malentendu récurrent avec Claude
- Vos contraintes ou processus évoluent
- Vous ajoutez un nouveau domaine d'activité

**Minimum recommandé** : Relecture trimestrielle, même si pas de changement majeur.

---

## Utilisation pratique

### Comment dire à Claude de lire mon CLAUD.md ?

**Méthode 1** : Via les préférences utilisateur (RECOMMANDÉ)
```
Dans Settings > Profile, ajoutez :
"Si nous discutons d'un repository GitHub avec un fichier CLAUD.md, 
lis-le et suis ses directives."
```

**Méthode 2** : Au début de chaque conversation
```
"Nous allons travailler sur le repo X. Peux-tu lire le fichier CLAUD.md 
et suivre ses instructions ?"
```

### Claude lit-il automatiquement CLAUD.md ?

**Non**, Claude n'a pas d'accès automatique à vos fichiers. Vous devez :
1. Soit lui demander explicitement de lire le fichier
2. Soit configurer vos préférences utilisateur pour qu'il le fasse systématiquement
3. Soit copier-coller le contenu dans la conversation

### Comment utiliser ce système pour plusieurs conversations en parallèle ?

**Chaque conversation est indépendante**. Pour chaque nouvelle conversation :
1. Mentionnez le repository concerné
2. Demandez à Claude de lire CLAUD.md
3. Claude aura le contexte pour cette conversation

### Puis-je modifier CLAUD.md pendant une conversation ?

**Oui**, mais Claude ne verra les changements que si :
- Vous lui demandez de relire le fichier
- Vous démarrez une nouvelle conversation

Dans une conversation en cours, Claude garde en mémoire la version qu'il a lue au début.

---

## Problèmes courants

### Claude ne semble pas suivre les instructions de mon CLAUD.md

**Causes possibles** :
1. **Claude n'a pas lu le fichier** : Demandez-lui explicitement de le lire
2. **Instructions contradictoires** : Vos instructions dans la conversation contredisent CLAUD.md
3. **Instructions trop vagues** : Soyez plus précis dans CLAUD.md
4. **Trop d'informations** : Simplifiez et priorisez l'essentiel

**Solution** : Testez en demandant "Quelles sont les instructions principales de mon CLAUD.md ?"

### Mon CLAUD.md devient trop long et difficile à maintenir

**Solutions** :
1. **Déplacez les détails** dans des fichiers séparés et faites des liens
2. **Créez une section "Essentiel"** au début avec le strict minimum
3. **Archivez** les sections obsolètes dans /historique/
4. **Utilisez des tableaux** et listes pour condenser l'information

### Je ne sais pas quoi mettre dans mon premier CLAUD.md

**Commencez minimal** :
```markdown
# Instructions pour Claude

## Qui suis-je
[Votre rôle en une phrase]

## Ce que je veux
[Votre objectif principal]

## Ce qu'il faut savoir
[2-3 points importants sur votre contexte]

## Comment communiquer
[Vos préférences de style]
```

Puis **enrichissez progressivement** au fil de vos interactions.

### Claude mélange les contextes de mes différents profils

**Cause** : C'est normal, chaque conversation est isolée.

**Solution** :
1. Commencez chaque conversation en précisant le profil
2. Demandez à Claude de lire le bon CLAUD.md
3. Si confusion : "Je te parle maintenant dans mon contexte [profil X]"

### Comment gérer les informations sensibles ?

**Options** :
1. **Repository privé** : Seul vous y avez accès
2. **Anonymisation** : Utilisez des codes plutôt que des noms réels
3. **Fichiers exclus** : Ajoutez les infos sensibles dans .gitignore et gérez-les localement
4. **Vault séparé** : Gardez les données ultra-sensibles hors de Git

**Rappel** : Claude ne stocke pas vos données mais respectez vos obligations de confidentialité.

---

## ❓ Question non résolue ?

Si votre question n'est pas dans cette FAQ :
1. Créez une issue dans ce repository
2. Consultez les discussions existantes
3. Adaptez les templates à vos besoins spécifiques

**Ce guide évolue** : N'hésitez pas à contribuer avec vos retours d'expérience !
