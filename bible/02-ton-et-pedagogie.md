# Bible Algonauth · 2 — Ton & pédagogie

## 1. La voix d'Algonauth

- **Curieux, chaleureux, un brin malicieux.** On est le guide embarqué, pas le professeur.
- **Le « on » collectif** : on explore ensemble. « On va essayer », « regarde ce qui se passe », « et là, attention… ».
- **Tutoiement** — standard YouTube francophone, crée la proximité.
- **Phrases courtes, rythme oral.** Le script se lit à voix haute pour être testé ; si une phrase essouffle à la lecture, elle est trop longue.
- **Le sourire audible.** Même en voix off, on « entend » le plaisir de raconter.

## 2. La colonne vertébrale narrative : les 3 actes

Chaque épisode suit la même structure profonde :

1. **La Quête** — le problème *humain* qui a motivé l'algorithme, dans son contexte historique. Le problème précède toujours la solution.
2. **Le Mécanisme** — comment l'algorithme fonctionne : métaphore, pas-à-pas animé, contre-exemple.
3. **L'Héritage** — ce qu'il est devenu, où il se cache dans la vie du spectateur aujourd'hui.

Règle d'or : **on ne montre jamais un algorithme « dans le vide »**. Un tri sans le problème
de trier, c'est un cours. Un tri né du besoin d'un traducteur de Moscou en 1960, c'est une histoire.

## 3. Les 7 principes pédagogiques

1. **Une seule idée par épisode** — tout le reste sert cette idée.
2. **La métaphore d'abord, le formalisme ensuite** — jamais l'inverse. Le « O(n log n) » arrive après l'avoir *vu*.
3. **Règle des 90 secondes** — jamais plus de 90 secondes sans un exemple concret, une image ou une relance narrative.
4. **Le pas-à-pas sur un exemple minuscule** — 5 éléments maximum. Le cerveau du spectateur doit *suivre*, pas *calculer*.
5. **Le jargon en 5 secondes** — « table de hachage — en gros, des casiers étiquetés par une machine à hacher les clés ». On continue, on ne s'attarde pas.
6. **L'erreur est pédagogique** — montrer le cas où l'algorithme échoue (le tri à bulles qui rame, le glouton qui rend mal la monnaie, l'arbre qui dégénère). On apprend plus d'un échec bien montré que d'un succès récité.
7. **Le récap en une phrase** — chaque épisode tient dans une phrase mémorisable, dite à la fin (« Un graphe, c'est jeter la carte, garder les liaisons »).

## 4. Les rubriques signature (les rituels)

La récurrence crée l'identité. Le spectateur doit *reconnaître* les moments de l'épisode.

| Rubrique | Moment | Rôle |
|---|---|---|
| **« Il était une fois… »** | Cold open (0:00-0:45) | On commence par l'histoire, in medias res. Jamais « Salut c'est Algonauth » en premier. |
| **« La Quête »** | Acte I | Le contexte historique, les personnages, le problème. |
| **« La Légende »** | Dans l'acte I ou II | L'anecdote historique centrale — vérifiée, ou signalée « la légende raconte ». |
| **« Démontons-le »** | Acte II | Le pas-à-pas animé sur un mini-exemple, éléments qui entrent un par un. |
| **« Dans ta vie »** | Acte III | 3 endroits où le spectateur côtoie l'algorithme sans le savoir. |
| **« La ligne d'horizon »** | Fin | Le récap-une-phrase + l'ouverture vers plus loin. |
| **« Cap sur… »** | Tout dernier plan | Teaser de 10 s de l'épisode suivant, toujours formulé en vocabulaire maritime. |

Ces rubriques ont leurs **cartes-titres visuelles fixes** (voir `04-identite-visuelle.md`) —
la répétition visuelle ancre le rituel.

## 5. Ce qu'on ne fait jamais

- « C'est très simple ! » — si c'était simple, on n'aurait pas besoin d'un épisode.
- Une formule, un diagramme ou un graphe sans animation d'accompagnement.
- Un schéma avec plus de 6 éléments visibles en même temps.
- Du clickbait mensonger — la curiosité oui, la trahison non. Le titre promet une histoire vraie, l'épisode la raconte.
- Sacrifier l'histoire « pour gagner du temps » : c'est précisément elle qui différencie la chaîne.
- Rire d'un personnage historique — on peut sourire *avec* lui (Ératosthène surnommé « Bêta »), jamais *de* lui.
- Présumer d'un savoir : jamais « comme tout le monde le sait ».

## 6. La règle de véracité historique

- Chaque fait historique de la fiche d'épisode porte sa source (ouvrage, article, lettre).
- Les anecdotes célèbres mais invérifiables sont présentées comme telles : « la légende raconte que Gauss… ». Ce réflexe honnête est un atout : il distingue Algonauth du contenu recyclé.
- Quand l'attribution est disputée (qui a *vraiment* inventé tel concept), l'assumer en une phrase — « et comme souvent dans l'histoire des sciences, trois personnes l'ont inventé en même temps » est même un excellent hook.
- Les sources transverses de référence sont listées en tête de chaque fichier de saison. Au moment du script, croiser au minimum : une source primaire ou un historien sérieux + vérifier que l'anecdote n'est pas un mythe Internet récent.

## 7. Le test de fin d'épisode (checklist qualité)

Avant de valider un montage, l'épisode doit passer ce test :

- [ ] Le spectateur peut raconter l'anecdote à un dîner (test de viralité orale)
- [ ] Le spectateur peut expliquer le mécanisme avec ses mots (test pédagogique)
- [ ] Le spectateur a reconnu au moins 2 rubriques signature (test d'identité)
- [ ] Aucune séquence de 90 s sans image nouvelle ou exemple (test de rythme)
- [ ] La phrase-récap existe et claque (test mémorable)
