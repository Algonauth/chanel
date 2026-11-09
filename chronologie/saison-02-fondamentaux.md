# Expédition II — « Les fondamentaux : chercher, trier, ranger, relier »

**12 escales · les concepts de base, chacun ancré dans son histoire · zéro prérequis (S1 = bonus)**

**Fil rouge** : maintenant que la machine existe (fin S1), qu'est-ce qu'on lui demande ?
Chercher, trier, ranger, relier. Chaque concept garde son ancrage historique — la saison 2
n'est jamais un cours : chaque outil est né d'un problème concret.

**À la fin de la saison, l'équipage sait** : lire un O(n), chercher en log n, ce qu'est un
bon tri, pourquoi tableaux/listes/piles/files/casiers/arbres/graphes, et parcourir un labyrinthe.

**Callbacks à semer partout** : le binaire d'E106 revient dans la recherche binaire, la
pile d'E208 explique la récursion d'E205, la dichotomie d'E203 réapparaît dans les arbres E210.

---

### E201 — C'est quoi, un algorithme ? (vraiment)
*Ouverture de l'expédition*

- **Idée unique** : un algorithme = une suite finie d'étapes non ambiguës qui transforme une entrée en sortie — et qui marche sans comprendre pourquoi.
- **Hook** : « Une recette de crêpes, une notice IKEA et Google Maps ont un air de famille. On va le nommer. »
- **La Quête** : retour éclair sur E101 (le nom vient d'Al-Khwarizmi) pour les nouveaux venus, puis la question : qu'est-ce qui fait qu'une suite d'instructions est un *algorithme* ?
- **Le Mécanisme** : le test en 3 conditions : fini (un nombre d'étapes borné), non ambigu (deux personnes exécutent pareil), général (marche pour toutes les entrées du type promis). Démo : une recette de crêpes qui échoue à chaque test (une pincée ? à feu vif ? pour 4 ou pour 40 ?), corrigée pas à pas.
- **Le contre-exemple** : la notice IKEA ambiguë (vis B ou C ?) — l'ambiguïté est l'ennemie ; et un algorithme sans fin (la recette « goûtez et ajustez » en boucle) n'est pas un algorithme.
- **Dans ta vie** : un protocole médical (algorithme au sens strict), Google Maps, l'arbitrage vidéo, le tri du courrier.
- **Visuel clé** : une recette floue qui se réécrit en étapes numérotées, conditions gommées une à une.
- **Récap** : « Fini, non ambigu, général. Trois mots, et tu sais reconnaître un algorithme. »
- **Cap sur…** : « Savoir ce qu'est un algorithme, c'est bien. Savoir s'il est BON, c'est mieux. Et pour ça, il faut une question à un dollar : combien ça coûte quand ça grossit ? »

### E202 — Pourquoi ton téléphone chauffe : la complexité
*Avec la légende de Gauss*

- **Idée unique** : la complexité mesure comment le coût grandit quand le problème grandit — pas combien de temps ça prend.
- **Hook** : « La légende raconte qu'un prof punit sa classe : additionner tous les nombres de 1 à 100. Un gamin de 9 ans rend sa copie en trois secondes. »
- **La Quête** : la légende de Gauss (annoncée comme légende !) : 1+100 = 101, 2+99 = 101… cinquante paires → 5050. Le gamin n'a pas calculé plus vite : il a changé d'algorithme.
- **Le Mécanisme** : dessiner les courbes sur des exemples visuels : O(1) (lire une case numérotée), O(n) (chercher dans une rue de maisons), O(n²) (chaque maison salue chaque maison). Puis le tableau choc : à 1 million d'éléments, n² = mille milliards d'opérations — pourquoi l'app rame et la batterie fond.
- **Le contre-exemple** : deux applis identiques, l'une en n, l'autre en n² — à 100 éléments personne ne voit la différence ; à un million, l'une répond, l'autre fond. La complexité ne punit pas les petits problèmes : elle punit la croissance.
- **Dans ta vie** : le lag en appel vidéo, le feed qui rame avec 10 000 photos, la batterie ; et pourquoi les géants du web ne « jettent pas de hardware » sur un algo en n².
- **La Légende** : Gauss enfant (« la légende raconte ») ; et l'anecdote vraie de Knuth proposant de prononcer « O » comme « de l'ordre de » pour couper court aux abus de langage.
- **Visuel clé** : la courbe rouge n² qui explose hors de l'écran pendant que la droite n reste sage.
- **Récap** : « On ne demande pas "combien de temps", on demande "comment ça se dégrade quand ça grandit". »
- **Cap sur…** : « Mesurer, c'est bien. Cherchons maintenant. Je pense à un nombre entre 1 et un million — tu vas le trouver en 20 questions. »

### E203 — Devine mon nombre en 20 questions : la recherche binaire
*La dichotomie*

- **Idée unique** : couper l'espace de recherche en deux à chaque étape → log n : 20 questions pour un million.
- **Hook** : « Un nombre entre 1 et 1 000 000. Vingt questions oui/non me suffisent pour le trouver. Une seule stratégie gagnante. »
- **Le Mécanisme** : le jeu du plus-ou-moins ; l'annuaire téléphonique (ouvrir au milieu, jeter la moitié) ; l'arithmétique des puissances de 2 (callback E106 : le binaire !) : 2¹⁰ ≈ 1000, 2²⁰ ≈ 1 000 000. La condition d'entrée : il FAUT un ensemble trié.
- **Le contre-exemple** : la recherche linéaire dans un annuaire non trié = lire tout ; et l'erreur d'implémentation classique (déborder d'une case) — pourquoi les pros se plantent dessus.
- **Dans ta vie** : chercher un contact, un mot dans le dictionnaire ; les index de bases de données ; et le fabuleux `git bisect` : les développeurs chassent les bugs par dichotomie sur l'historique — « 12 versions de code, 4 questions, le coupable ».
- **La Légende** : Jon Bentley a demandé à des centaines de programmeurs professionnels d'écrire une recherche binaire : la grande majorité a livré une version buggée. L'algorithme « évident » le plus piégeux du monde. (Et le puzzle des 12 pièces / 3 pesées en bonus.)
- **Visuel clé** : un million de cases qui s'effondrent en 20 coupes nettes.
- **Récap** : « Une question bien choisie vaut mille vérifications. »
- **Cap sur…** : « La dichotomie exige de l'ordre. Mais comment METTRE de l'ordre ? Commençons par le pire tri du monde. »

### E204 — Le pire tri du monde (et pourquoi on l'enseigne quand même)
*Tri à bulles & tri par insertion*

- **Idée unique** : le tri à bulles est pédagogique mais catastrophique (n²) ; le tri par insertion est le tri « humain », et il revient partout.
- **Hook** : « Il existe un tri si médiocre qu'un des plus grands informaticiens l'a publiquement détesté. Exécutons-le en public. »
- **Le Mécanisme** : 5 cartes. Tri à bulles : comparer les voisins, échanger, repasser — les grands remontent comme des bulles (animation marine assumée). Compter : n passes × n comparaisons = n² (callback E202 !). Puis tri par insertion : comme on trie ses cartes en main — prendre la suivante, l'insérer à sa place. Naturel, et rapide sur les petits paquets.
- **Le contre-exemple** : le pire cas du bulles (presque trié mais à l'envers) ; et la rédemption de l'insertion : sur un paquet *presque trié*, il est excellent.
- **Dans ta vie** : Python et Java trient leurs petits tableaux… par insertion (à l'intérieur de TimSort) ; toi aussi, quand tu ranges tes papiers un par un.
- **La Légende** : Dijkstra sur le tri à bulles : il n'a « rien pour lui, sinon un nom accrocheur ». Un si mauvais algorithme, et un si joli nom — la leçon du marketing.
- **Visuel clé** : les cartes qui « bululent » vers la surface, désespérément lentement.
- **Récap** : « Deux tris naïfs, deux leçons : comparer les voisins ne suffit pas ; insérer à sa place, ça marche. »
- **Cap sur…** : « Pour trier un million d'éléments, il fallait un esprit d'un autre caliber. Un homme qui calculait plus vite que les machines de son temps. »

### E205 — Diviser pour régner : le tri fusion
*Von Neumann, 1945*

- **Idée unique** : diviser en deux, trier chaque moitié, fusionner — n log n, et l'ordre de grandeur du tri optimal.
- **Hook** : « 1945. Un mathématicien écrit un programme de tri pour un ordinateur qui n'existe pas encore. Soixante-dix ans plus tard, ce code vit encore dans ton clavier. »
- **La Quête** : John von Neumann — l'homme qui calculait plus vite que les machines (anecdotes de ses prouesses mentales), rapport EDVAC 1945 : le tri fusion compte parmi les tout premiers programmes écrits.
- **Le Mécanisme** : la fusion d'abord (le geste naturel : deux paquets triés, comparer les deux cartes du dessus, prendre la plus petite — animation). Puis la récursion : couper, couper, couper jusqu'à 1 carte, fusionner en remontant. L'arbre de découpe = log n étages × n fusions = n log n. Et pourquoi on ne peut pas faire fondamentalement mieux (l'argument du nombre d'ordres possibles, très vulgarisé).
- **Le contre-exemple** : le prix de la gloire : il faut une deuxième table pour fusionner (mémoire supplémentaire).
- **Dans ta vie** : `sorted()` en Python, les tris de Java, le `ORDER BY` des bases ; et Git : fusionner deux branches, c'est littéralement fusionner deux listes triées de modifications.
- **La Légende** : von Neumann et les anecdotes de calcul mental (le problème de la mouche entre deux trains, sommé en série illimitée — résolu en quelques secondes : « j'ai sommé la série »).
- **Visuel clé** : l'arbre de découpe qui se déplie puis se *replie* en une ligne triée.
- **Récap** : « Couper en deux, régler chaque moitié, fusionner : n log n, le mur optimal du tri. »
- **Cap sur…** : « n log n, c'est le plancher. Mais en 1959, à Moscou, un étudiant britannique trouve plus rapide EN PRATIQUE — en jouant avec un dictionnaire russe. »

### E206 — Moscou, 1960 : le tri qui a conquis le monde
*Quicksort, Tony Hoare*

- **Idée unique** : quicksort — choisir un pivot, répartir autour, récursivité — le tri le plus rapide en pratique, et le gamble du pire cas.
- **Hook** : « Un étudiant en visite à Moscou veut trier des mots russes pour un dictionnaire de traduction. Il invente le tri le plus utilisé de la planète. »
- **La Quête** : Tony Hoare, 25 ans, étudiant en visite à l'université d'État de Moscou, projet de traduction automatique : il faut chercher des mots dans un dictionnaire sur bande — donc le trier.
- **Le Mécanisme** : le pivot : une carte-pivot, les plus petites à gauche, les plus grandes à droite (partition animée en un geste de trieur de cartes) ; puis récursion sur chaque côté. Pourquoi c'est rapide en pratique : peu d'échanges, tout se joue sur place. Le gamble : un pivot horrible (toujours le plus petit) → n². La parade : le pivot aléatoire.
- **Le contre-exemple** : le cas qui dégénère — trier une liste DÉJÀ triée avec le premier élément comme pivot = la catastrophe. (L'ironie : trier ce qui est déjà presque en ordre.)
- **Dans ta vie** : `qsort` en C, les `sort` des langages, l'explorateur de fichiers ; et le monde réel : TimSort (Python/Java) = fusion + insertion + des idées de quicksort — le meilleur des mondes.
- **La Légende** : Hoare racontera qu'il ne connaissait même pas la récursion à l'époque — il a découvert ensuite que ce qu'il faisait s'appelait comme ça.
- **Visuel clé** : le mur du pivot qui se déplace d'un coup, les cartes se répartissant à gauche/droite.
- **Récap** : « Un pivot bien choisi partage le monde en deux. Choisis-le au hasard : en moyenne, personne ne peut te battre. »
- **Cap sur…** : « On sait trier et chercher. Mais où RANGER tout ça ? Ta mémoire est une rue — tout va dépendre de comment tu la lotis. »

### E207 — La mémoire est une rue : tableaux et listes
*Deux façons d'habiter la mémoire*

- **Idée unique** : tableau (cases contiguës numérotées) et liste chaînée (chaque élément connaît le suivant) — deux contrats d'organisation, deux forces opposées.
- **Hook** : « Ta RAM est une rue avec des numéros. Tout le reste n'est qu'architecture urbaine. »
- **La Quête** : 1955-56, Pittsburgh : Newell, Shaw et Simon programment le Logic Theorist — un programme qui démontre des théorimes des *Principia Mathematica* (la boucle est bouclée avec Russell !) — et inventent pour lui les listes chaînées.
- **Le Mécanisme** : le tableau : maisons contiguës → aller au n°34 instantanément (O(1), callback E202) mais insérer au milieu = tout décaler. La liste : chaque maison garde l'adresse de la suivante → insérer/défaire en un geste, mais aller au n°34 = marcher depuis le début (O(n)). Animation double, sur la même rue.
- **Le contre-exemple** : choisir liste pour « accéder vite au 1000ᵉ élément » — l'erreur classique ; choisir tableau pour une structure qui grandit sans cesse au milieu.
- **Dans ta vie** : une playlist (liste : insérer/retirer des titres), une image (tableau de pixels : accéder au pixel x,y), l'historique de navigation, les tampons audio/vidéo.
- **La Légende** : le Logic Theorist a « démontré » un théorème plus élégamment que Russell et Whitehead eux-mêmes — quand on a montré le résultat à Russell, sa réponse est restée dans l'histoire (à vérifier/retrouver au script : sa réaction attestée).
- **Visuel clé** : la même rue vue deux fois — numéros bleus d'un côté, flèches dorées de l'autre.
- **Récap** : « Tableau : j'accède instantanément, j'insère péniblement. Liste : j'insère en un geste, j'accède en marchant. »
- **Cap sur…** : « Il ne reste qu'une question : dans quel ORDRE traiter ce qu'on a rangé ? Il n'existe que deux réponses — la pile et la file. »

### E208 — Pile ou file ? Les deux files d'attente qui dirigent tout
*LIFO / FIFO*

- **Idée unique** : deux contrats d'ordre — dernier entré premier sorti (pile), premier arrivé premier servi (file) — modélisent presque tout.
- **Hook** : « Pourquoi Ctrl+Z annule-t-il toujours la DERNIÈRE action ? Parce que ton ordinateur ne sait faire qu'une chose : empiler. »
- **Le Mécanisme** : la pile d'assiettes : undo, bouton retour, et surtout la pile d'appels — la récursion d'E205 ENFIN expliquée visuellement (chaque appel pose une assiette, chaque retour en démonte une). La file : l'imprimante, les messages entre applications, premier arrivé premier servi.
- **Le contre-exemple** : le mauvais choix — traiter les tickets d'incident en pile = le plus ancien client attend pour toujours ; et l'inverse : l'undo en file = n'importe quoi.
- **Dans ta vie** : Ctrl+Z, le bouton retour du navigateur, la file d'impression, le matchmaking des jeux en ligne, les files de messages derrière chaque application (Kafka, RabbitMQ — sans les nommer, ou une seconde).
- **La Légende** : la récursion rendue possible par la pile d'appels d'ALGOL 60 — Dijkstra parmi ses artisans ; et l'ancêtre culturel de la pile : le fil d'Ariane — Thésée déroule (empile) et rembobine (dépile) pour sortir du labyrinthe. Le mythe grec avait inventé le backtracking.
- **Visuel clé** : une pile d'assiettes-marques-pages qui monte pendant la récursion et descend au retour.
- **Récap** : « Empiler pour revenir sur ses pas. Filer pour servir dans l'ordre. Tout le reste en découle. »
- **Cap sur…** : « Et si, au lieu de chercher DANS une rue, une machine te donnait directement le numéro de casier à partir de ton nom ? Bienvenue dans la plus belle invention du génie logiciel. »

### E209 — Des casiers pour tout : la table de hachage
*Hans Peter Luhn, IBM, 1953*

- **Idée unique** : une fonction de hachage calcule OÙ ranger (et donc OÙ retrouver) — l'accès quasi instantané.
- **Hook** : « À l'entrée, une machine broie ta clé et crache un numéro de casier. Aucune recherche : tu SAIS déjà où c'est. »
- **La Quête** : IBM, années 1950. Hans Peter Luhn — inventeur prolifique (le KWIC, le premier moteur de recherche de textes documentaires) — pose l'idée du hachage à chaînage interne, 1953.
- **Le Mécanisme** : des casiers numérotés ; hacher « ALGO » → n°14 (montrer la « broyeuse » symbolique : une petite fonction qui mélange). La promesse : O(1) en moyenne (callback E202 !). Le grain de sable : les collisions — deux clés, même casier — résolues par le rangement en sous-file (chaînage). Le pari statistique : une bonne broyeuse répartit uniformément.
- **Le contre-exemple** : la broyeuse qui renvoie tout sur le même casier = liste chaînée déguisée (callback E207) ; et en vrai : les « attaques par collision » qui saturent des serveurs — une leçon de conception devenue affaire de sécurité.
- **Dans ta vie** : le cache de ton navigateur, les index de bases de données, les `dict` Python et objets JS (LA structure des langages modernes), la déduplication ; et la famille lointaine : le hachage des mots de passe (SHA…) — même idée de « broyage », mais à sens unique.
- **La Légende** : Luhn a aussi inventé la somme de contrôle qui valide les numéros de cartes bancaires — la « formule de Luhn » (brevet 1954/1960) : une petite arithmetic de casiers qui corrige les fautes de frappe de TOUTES les cartes du monde.
- **Visuel clé** : la broyeuse dorée qui avale un nom-clé et imprime un ticket-casier.
- **Récap** : « Ne cherche pas : calcule où c'est rangé. »
- **Cap sur…** : « Une rue, des casiers… et si le monde était un arbre ? C'est déjà le cas — regarde ton explorateur de fichiers. »

### E210 — Tout est hiérarchie : les arbres
*De l'arbre binaire de recherche aux B-arbres*

- **Idée unique** : organiser par hiérarchie ordonnée → chercher en log n *par construction* ; le drame de l'arbre qui dégénère ; l'équilibrage.
- **Hook** : « Ton disque dur est une forêt. Le web est une forêt. Et la dichotomie d'E203 n'était qu'un arbre déguisé. »
- **La Quête** : des hiérarchies naturelles (généalogies, tournois) aux index des bases : dans les années 60, les compilateurs et les SGBD adoptent les arbres ; 1970, laboratoires Boeing : Bayer et McCreight inventent le B-arbre — l'index de TOUTES les bases du monde.
- **Le Mécanisme** : l'arbre binaire de recherche : à gauche plus petit, à droite plus grand (5 éléments) → chaque comparaison jette la moitié de l'arbre = la dichotomie d'E203 rendue permanente. Le drame : insérer des données déjà triées → l'arbre devient une liste (callback E207 !). La parade : l'équilibrage (AVL, 1962 — deux mathématiciens soviétiques) : l'arbre se « re-redresse » ; et le B-arbre : étagé, large, taillé pour les disques.
- **Le contre-exemple** : l'arbre peigne — dégénéré en liste ; en rouge signal, conformément à la charte.
- **Dans ta vie** : dossiers et sous-dossiers, le DOM d'une page web, les index de bases (chaque requête rapide), les tournois sportifs, la syntaxe des langages (l'arbre d'analyse des compilateurs).
- **La Légende** : Adelson-Velsky et Landis publient en 1962, de l'autre côté du rideau de fer, l'arbre qui se rééquilibre — pendant que l'Ouest réinvente des variantes. (Et le « B » du B-arbre : Bayer n'a jamais dit s'il signifiait « Boeing », « balanced » ou « broad » — le mystère du nom le plus discret de l'informatique.)
- **Visuel clé** : l'arbre qui penche dangereusement, puis se redresse d'un mouvement fluide (rotations).
- **Récap** : « Bien équilibré, un arbre cherche en log n — la dichotomie devenue architecture. »
- **Cap sur…** : « Des nœuds, des liens… et si on laissait les liens aller N'IMPORTE OÙ ? On obtient la structure la plus puissante du monde. Elle est née d'une promenade impossible à Königsberg. »

### E211 — Les 7 ponts de Königsberg : la promenade qui a fondé les graphes
*Euler, 1736 — ÉPISODE PIVOT*

- **Idée unique** : un graphe = des sommets + des arêtes ; abstraire (jeter la carte, garder les liaisons) transforme un problème impossible en problème résoluble.
- **Hook** : « 1736. Les bourgeois de Königsberg cherchent une balade qui traverserait les 7 ponts, chacun une seule fois. Un mathématicien suisse prouve que c'est impossible — et fonde une science entière en le faisant. »
- **La Quête** : Kaliningrad d'alors, la Pregel et ses deux îles ; le maire de Dantzig, Ehler, relance Euler par courrier sur ce casse-tête à la mode ; Euler cède — et change la façon de poser le problème.
- **Le Mécanisme** : l'abstraction en direct : la carte de la ville fond, il ne reste que 4 points et 7 traits. L'argument d'Euler : sur chaque terre, les ponts vont par paires entrée/sortie — sauf départ et arrivée. Donc une promenade complète n'existe que si 0 ou 2 terres ont un nombre impair de ponts. À Königsberg : 4 terres impaires. Impossible. Preuve sans aucun calcul.
- **Le contre-exemple / prolongement** : ajouter UN pont (Kant ?) et tout devient possible — la sensibilité d'une structure entière à une seule arête.
- **Dans ta vie** : le GPS (le réseau routier est un graphe), les réseaux sociaux (amis d'amis), le routage d'internet, les dépendances entre paquets logiciels, les horaires de transports.
- **La Légende** : Euler, déjà aveugle d'un œil, travaillant à moitié de mémoire ; et le pont Kant — une reconstruction de 1935 qui a rendu la promenade possible : la ville a réglé un problème vieux de 200 ans sans le vouloir.
- **Visuel clé** : la gravure de Königsberg qui se dissout en 4 points et 7 traits dorés.
- **Récap** : « Jette la carte, garde les liaisons : tu tiens le bon problème. »
- **Cap sur…** : « Un graphe, très bien. Mais comment le PARCOURIR ? Thésée avait un fil. Ton GPS a une file d'attente. Même combat — c'est la finale. »

### E212 — Le fil d'Ariane : explorer un labyrinthe
*DFS, BFS — ÉPISODE CONFLUENCE*

- **Idée unique** : deux stratégies canoniques d'exploration — en profondeur (avec une pile), en largeur (avec une file) — et la seconde donne le plus court chemin arête par arête.
- **Hook** : « Pour sortir du labyrinthe du Minotaure, Thésée avait un fil. Ton GPS a exactement la même idée, à une différence près : une file au lieu d'une pelote. »
- **Le Mécanisme** : le labyrinthe comme graphe (callback E211). DFS : foncer, marquer au passage, en butant : dérouler le fil (dépiler — callback E208 !). BFS : jeter une pierre dans l'eau à l'entrée : le front d'onde s'élargit case par case ; le premier qui touche la sortie a pris LE plus court chemin — animation circulaire signature. Le mot-clé : marquer les cases visitées, sinon on tourne en rond.
- **Le contre-exemple** : le DFS qui s'englue dans un couloir sans issue à l'opposé de la sortie ; le BFS qui coûte cher en mémoire (toute la frontière). Choisir = savoir ce qu'on veut : explorer tout, ou trouver le plus court.
- **Dans ta vie** : « les personnes que vous pourriez connaître » (BFS à 2 niveaux du graphe social), les solveurs de labyrinthes, les robots d'aspirateur, le crawl du web, le garbage collector ; et le pathfinding des jeux vidéo — teaser E302 (A*).
- **La Légende** : la méthode de Trémaux, publiée par Édouard Lucas dans ses *Récréations mathématiques* (1882) : la bonne façon de visiter un labyrinthe — c'est un DFS écrit 80 ans avant les ordinateurs ; et Edward F. Moore (Bell Labs, 1959) qui formalise le BFS — collègue de Shannon et de sa souris Thésée (callback E110).
- **Visuel clé** : le fil d'Ariane doré qui se déroule (DFS), puis l'onde circulaire cyan (BFS) — les deux univers visuels de la chaîne dans un même plan.
- **Récap** : « Profondeur avec une pile pour tout fouiller ; largeur avec une file pour aller au plus court. »
- **Cliffhanger de saison** : « On sait mesurer, chercher, trier, ranger, relier, explorer. Les fondations sont posées. Prochaine expédition : les algorithmes qui gouvernent ta vie quotidienne — de la route des vacances à la page YouTube qui te recommande celle-ci. » *(méta-final assumé)*

---

## Sources principales de la saison (à re-vérifier au script)

- Knuth, *TAOCP* vol. 3 (*Sorting and Searching*) — l'histoire des tris, de la dichotomie et du hachage
- Hoare, « Quicksort », *Computer Journal* 1962 + entretiens oraux (E206)
- Von Neumann, rapport EDVAC 1945 (E205) ; Knuth pour l'attribution du tri fusion
- Newell, Shaw & Simon, *The Logic Theorist* 1956 (E207)
- Bentley, *Programming Pearls* (E203 — le test de la recherche binaire)
- Bayer & McCreight, « Organization and Maintenance of Large Ordered Indices », 1970 (E210)
- Euler, *Solutio problematis ad geometriam situs pertinentis*, 1736 ; lettre d'Ehler (E211)
- Lucas, *Récréations mathématiques* 1882 (E212) ; Moore, « The Shortest Path Through a Maze », 1959

**Note d'attribution (règle bible §6)** : les priorités d'invention (listes chaînées, hachage, BFS) sont parfois disputées — au script, présenter les attributions avec « l'une des premières mentions » plutôt qu'« l'inventeur », sauf source primaire solide.
