# Expédition III — « Les algorithmes qui gouvernent le monde »

**10 escales · l'âge d'or 1950-2000 · S2 conseillée en prérequis**

**Fil rouge** : ces algorithmes sont invisibles et pourtant ils décident de ta route, de tes
recommandations, de tes achats sécurisés et de ton temps libre. Chaque épisode répond à la
question : « qu'est-ce qui a bien pu motiver ÇA ? » — et la réponse est presque toujours une
histoire humaine.

**Format** : fiches semi-détaillées — le script final reprendra le template complet de
`bible/03-structure-episode.md`. À affiner au moment de la production, avec les retours de l'équipage.

---

### E301 — Vingt minutes sans crayon
*Dijkstra, 1956*

- **Idée** : le plus court chemin quand les routes n'ont pas la même longueur — la vague qui s'étend, du départ vers toutes les destinations.
- **Hook** : « 1956, un café d'Amsterdam. Un jeune mathématicien conçoit en vingt minutes, sans crayon, l'algorithme qui guide aujourd'hui des milliards de trajets. »
- **Histoire** : Edsger Dijkstra veut démontrer les capacités du nouvel ordinateur ARMAC ; il cherche un problème que « tout le monde comprend ». Rotterdam → Groningen. Il racontera que l'absence de crayon l'a forcé à éviter toute complexité inutile.
- **Mécanisme** : BFS (callback E212) ne suffit plus : les arêtes ont des poids. L'animation : une vague qui s'étend du port, chaque ville « verrouille » sa distance minimale définitive — jamais on ne revient en arrière.
- **Dans ta vie** : GPS, routage réseau (OSPF), planification de tâches, robots.
- **Anecdote** : publiée en 1959 dans un journal de mathématiques appliquées — un article de trois pages parmi les plus cités de l'histoire.
- **Cap sur…** : « Dijkstra explore tout. Mais un robot myope qui cherche sa porte de garage n'a pas le temps d'explorer la ville entière… »

### E302 — Le robot myope et la boussole optimiste
*A*, 1968*

- **Idée** : une heuristique — un « flair » — guide l'exploration vers le but : la recherche informée.
- **Hook** : « Shakey le robot voyait à trois mètres, calculait sur un ordinateur de la taille d'un frigo, et devait traverser des salles pleines d'obstacles. Ses créateurs ont inventé la boussole des jeux vidéo. »
- **Histoire** : SRI, fin des années 60, le projet Shakey (DARPA) : Hart, Nilsson, Raphael conçoivent A* pour que Shakey planifie sans tout explorer.
- **Mécanisme** : Dijkstra + une estimation optimiste du reste du chemin (« à vol d'oiseau ») ; animation : la vague ne s'étale plus en cercle, elle s'étire vers le but. La condition d'honnêteté : ne jamais surestimer la distance restante.
- **Dans ta vie** : le pathfinding des jeux vidéo ( RTS, RPG) — littéralement la même heuristique ; planification robotique, puzzles.
- **Anecdote** : « A* » — le nom vient de la notation mathématique ; 50 ans plus tard, aucun jeu ne l'a remplacé.
- **Cap sur…** : « Trouver son chemin, c'est utile. Mais résoudre un problème géant en ne résolvant chaque sous-problème qu'UNE fois — ça s'appelle la programmation dynamique, et son nom est un chef-d'œuvre de marketing. »

### E303 — Le nom le plus mystérieux de l'informatique
*Programmation dynamique, Bellman, années 1950*

- **Idée** : ne pas recalculer deux fois la même chose : résoudre chaque sous-problème une fois, le retenir, remonter.
- **Hook** : « "Programmation dynamique" ne veut rien dire. C'est exactement ce que son inventeur voulait : un nom si impressionnant que personne n'oserait couper son budget. »
- **Histoire** : Richard Bellman, RAND Corporation, guerre froide ; le secrétaire à la Défense détestait le mot « recherche » — Bellman raconte dans son autobiographie avoir choisi « programmation » (planification) et « dynamique » (ça sonne bien) pour protéger ses fonds.
- **Mécanisme** : les lapins de Fibonacci (callback E105) recalculés en cascade — puis le tableau qui *retient* ; puis un vrai problème : le sac à dos (que mettre dans la valise) ou l'alignement de textes.
- **Dans ta vie** : `git diff` (alignement de séquences !), la bio-informatique (teaser E503), la gestion de portefeuille, le calcul de mots de passe « robustes ».
- **Anecdote** : le nom ne voulait rien dire — et il a fonctionné : la technique a « survécu » là où d'autres projets tombaient aux oubliettes.
- **Cap sur…** : « Retenir pour ne pas recalculer, très bien. Mais parfois, la meilleure stratégie est la plus simple : être glouton. »

### E304 — Rendre la monnaie : l'algorithme glouton
*Greedy*

- **Idée** : le glouton prend toujours la plus grosse pièce — parfois c'est optimal, parfois catastrophique : savoir quand.
- **Hook** : « En euros, la caisse automatique te rend toujours la monnaie parfaitement. Avec les pièces britanniques d'avant 1971, elle se serait trompée. »
- **Histoire** : le système £sd (12 pence = 1 shilling…) où le glouton échoue ; et les siècles de commerce où rendre la monnaie fut un art.
- **Mécanisme** : animation caisse enregistreuse : toujours la plus grande pièce ≤ reste ; contre-exemple canonique (pièces 1, 3, 4 ; rendre 6 : glouton = 4+1+1 = trois pièces, optimal = 3+3 = deux) ; quand le système de pièces est « canonique », le glouton EST optimal — la preuve par l'exemple.
- **Dans ta vie** : le rendu de monnaie, les plannings (salles de réunion : finir au plus tôt), le remplissage de camions, et Dijkstra qui est glouton à sa façon (callback E301).
- **Cap sur…** : « Jusqu'ici, nos algorithmes trouvent LA bonne réponse. Mais il existe des problèmes où TOUT algorithme connu patine. La communauté a mis un prix dessus : un million de dollars. »

### E305 — Le problème à un million de dollars
*P vs NP*

- **Idée** : certains problèmes sont faciles à *vérifier* mais apparemment difficiles à *résoudre* — et personne ne sait prouver si c'est fondamental (P ≠ NP ?).
- **Hook** : « Une grille de sudoku complétée : 2 secondes pour vérifier. La remplir : parfois des heures. Cet écart entre vérifier et résoudre vaut un million de dollars. »
- **Histoire** : la lettre de Gödel à von Neumann (1956, retrouvée dans les années 80) qui anticipe la question ; Cook (1971), Karp (1972) — la naissance de NP-complétude ; le prix Clay (2000).
- **Mécanisme** : vérifier vs résoudre (sudoku, mots croisés) ; le voyageur de commerce ; la classe des problèmes « aussi durs les uns que les autres » (réductions, montrées comme des traductions de problèmes) ; ce qui se casse si P = NP (la crypto s'effondre — teaser E308).
- **Dans ta vie** : chaque fois qu'une appli « optimise » un trajet, un emploi du temps, un planning de livraisons — elle négocie avec la NP-difficulté ; la sécurité de tes paiements repose (en partie) sur cet écart.
- **Anecdote** : la lettre de Gödel — écrite à un von Neumann déjà malade, elle dort 30 ans dans les archives avant d'être découverte.
- **Cap sur…** : « L'un des problèmes de notre million de dollars concerne les COUPLES : comment apparier tout le monde sans qu'aucun couple ne veuille s'enfuir ensemble ? »

### E306 — L'algorithme des couples stables
*Gale-Shapley, 1962*

- **Idée** : l'appariement stable — on ne peut pas rendre tout le monde heureux, mais on peut empêcher toute « fuite à deux ».
- **Hook** : « Chaque année aux États-Unis, un algorithme décide de l'affectation de dizaines de milliers de jeunes médecins dans les hôpitaux. Il a empêché une révolution. Il a un Nobel. »
- **Histoire** : le chaos des internats médicaux américains (années 40-50 : offres deux ans à l'avance, marché qui s'effondre) ; Gale et Shapley (1962) formalisent la solution ; Alvin Roth l'applique partout — Nobel d'économie 2012.
- **Mécanisme** : la danse des propositions : un camp propose, l'autre garde « le meilleur reçu pour l'instant » et renvoie le reste — animation bal de promo ; à la fin : stable par construction (personne ne peut former un couple mutuellement préférable). Théorème : ça converge TOUJOURS.
- **Dans ta vie** : affectations med-school américaines (le Match), Parcoursup et les attribations scolaires (variantes), dons croisés de reins, … et les applications de rencontre comme contre-exemple instructif (leurs marchés ne sont PAS stables par construction — d'où l'infinité de swiping).
- **Cap sur…** : « Parlons maintenant de ta valise. Plus précisément : de pourquoi tes photos tiennent dans ton téléphone. »

### E307 — Le devoir qui est devenu une légende
*Huffman, 1952 — la compression*

- **Idée** : les symboles fréquents reçoivent des codes courts — l'arbre de Huffman approche la limite de Shannon (callback E110).
- **Hook** : « 1951, MIT. Un étudiant peut choisir : passer l'examen final, ou écrire un devoir maison. David Huffman choisit le devoir — et invente la compression moderne, quelques jours avant de jeter l'éponge. »
- **Histoire** : le cours de Robert Fano ; le problème posé (trouver le meilleur code de longueur variable) ; Huffman racontera que l'idée lui est venue au moment même où il allait jeter ses notes à la poubelle. (Ironie : Fano travaillait sur le sujet avec… Shannon.)
- **Mécanisme** : construire l'arbre : prendre les deux plus rares, les fusionner, recommencer (animation à 5 lettres avec fréquences) ; décoder sans virgule : aucun code n'est le début d'un autre — l'arbre est son propre délimiteur.
- **Dans ta vie** : ZIP, gzip, PNG (Deflate = Ziv-Lempel 1977 + Huffman), et l'idée mère de tous les codecs (JPEG, MP3 — avec des cousins) ; chaque fichier que tu télécharges voyage compressé.
- **Cap sur…** : « Un dernier géant dans cette expédition : celui qui garde tes secrets. Comment deux inconnus peuvent-ils convenir d'un secret… sous les yeux de tout le monde ? »

### E308 — Des secrets sans secret partagé
*Diffie-Hellman & RSA*

- **Idée** : la cryptographie à clé publique — chiffrer avec une clé publique, déchiffrer avec une privée ; l'arithmétique de l'horloge.
- **Hook** : « Pendant 3000 ans, se parler en secret exigeait d'échanger une clé au préalable. En 1976, deux chercheurs ont détruit cette règle — avec une fonction à sens unique. »
- **Histoire** : Diffie et Hellman, « New Directions in Cryptography » (1976) ; Rivest, Shamir, Adleman : RSA (1977) — l'histoire raconte que l'idée est venue à Rivest le lendemain d'une soirée arrosée ; et le secret le mieux gardé : GCHQ, Ellis (1969) puis Cocks (1973) avaient tout inventé en secret — déclassifié seulement en 1997.
- **Mécanisme** : le cadenas public : n'importe qui peut le fermer, seul le propriétaire a la clé ; l'horloge arithmétique (l'exposant qui mélange, l'inverse qui démêle) ; le lien avec les nombres premiers — le crible d'Ératosthène (callback E104) et le PGCD d'Euclide (callback E103) : la saison 1 servait À ÇA.
- **Dans ta vie** : le cadenas du navigateur, HTTPS, les signatures numériques (mises à jour logicielles vérifiées), la carte bancaire sans contact, WhatsApp/Signal.
- **Anecdote** : le chiffre RSA-129 « indéchiffrable » lancé comme défi en 1977 — factorisé en 1994 par des centaines de bénévoles ; le secret classifié 24 ans avant d'être révélé publiquement.
- **Cap sur…** : « Sécurité, trajets, valises, couples… Il reste le plus célèbre de tous. Celui qui a transformé une pub pour navigateur en empire : le PageRank. »

### E309 — Quand la toile est devenue une carte
*PageRank, 1998*

- **Idée** : un lien = un vote, pondéré par l'importance du votant — l'importance circule le long des liens.
- **Hook** : « 1998. Le web compte des millions de pages et les moteurs de recherche renvoient n'importe quoi. Deux étudiants de Stanford ont une idée : la page est importante si des pages importantes pointent vers elle. C'est circulaire — et c'est la solution. »
- **Histoire** : BackRub, le projet de recherche de Larry Page et Sergey Brin ; l'article de 1998 ; le nom Google, déformation de « googol » (10¹⁰⁰).
- **Mécanisme** : le surfeur aléatoire : il clique au hasard sur un lien — à l'infini, la probabilité d'être sur une page = son importance ; animation : la « masse d'importance » qui circule et se stabilise ; la boucle vertueuse (le rank d'aujourd'hui nourrit le vote de demain).
- **Dans ta vie** : chaque recherche Google (parmi ~200 signaux aujourd'hui — le fondateur reste), les suggestions d'articles, les indices de spam, la bibliométrie (qui cite qui).
- **Anecdote** : le premier datacenter de Google : des disques durs dans une tour de LEGO ; et le doodle Halloween 1998 déjà griffonné « BackRub » — non, vérifier au script : le logo « Google ! » de 1998 avec le point d'exclamation yahooïen (à fact-checker).
- **Cap sur…** : « Reste une question d'urgence — littéralement. Qui passe en premier quand tout arrive en même temps ? »

### E310 — Qui passe en premier ? Les urgences et le tas
*Files de priorité & tas binaire*

- **Idée** : la file de priorité — l'ordre d'entrée n'est pas l'ordre de sortie ; le tas binaire la rend quasi gratuite.
- **Hook** : « Aux urgences, le premier arrivé n'est pas le premier servi. Cette règle a été inventée par le chirurgien de Napoléon — et ton ordinateur l'applique 10 000 fois par seconde. »
- **Histoire** : Dominique Jean Larrey, chirurgien des armées napoléoniennes, invente le triage des blessés (« les plus gravement atteints passent d'abord ») ; Williams, 1964 : le tas binaire (heap) rend la file de priorité efficace.
- **Mécanisme** : le tas : un tableau LU comme un arbre (callbacks E207 + E210 !) — le plus grand « bulle » en racine ; insérer et extraire en log n ; animation « salle d'attente intelligente ».
- **Dans ta vie** : l'ordonnanceur de ton OS (qui a le processeur maintenant ?), les files d'événements des interfaces, le rendu priorisé des jeux, et… Dijkstra et A* qui en dépendent (callbacks E301-E302 — tout se tient).
- **Cliffhanger de saison** : « Tous ces algorithmes ont un point commun : des humains en ont écrit chaque règle. Et si la machine écrivait ses propres règles ? Prochaine expédition : l'ère de l'apprentissage. » *(ouverture sur S4)*

---

## Sources principales de la saison (à re-vérifier au script)

- Dijkstra, « A Note on Two Problems in Connexion with Graphs », 1959 + entretien oral (E301)
- Hart, Nilsson & Raphael, « A Formal Basis for the Heuristic Determination of Minimum Cost Paths », 1968 (E302)
- Bellman, *Eye of the Hurricane* (autobiographie — l'histoire du nom, E303)
- Cook, « The Complexity of Theorem-Proving Procedures », 1971 ; lettre Gödel-von Neumann 1956 (E305)
- Gale & Shapley, « College Admissions and the Stability of Marriage », 1962 (E306)
- Huffman, « A Method for the Construction of Minimum-Redundancy Codes », 1952 + entretien oral (E307)
- Diffie & Hellman 1976 ; Rivest-Shamir-Adleman 1977 ; déclassification GCHQ 1997 (E308)
- Brin & Page, « The Anatomy of a Large-Scale Hypertextual Web Search Engine », 1998 (E309)
- Williams, « Algorithm 232: Heapsort », 1964 ; histoire du triage militaire (E310)

**À fact-checker impérativement au script** (signalées « légende » si non confirmées) :
le lendemain-de-soirée de Rivest (E308), les anecdotes LEGO/doodle de Google (E309),
la réaction de Russell au Logic Theorist (E207, S2).
