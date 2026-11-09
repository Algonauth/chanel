# Expédition I — « Aux origines : l'algorithme avant l'ordinateur »

**10 escales · de -1800 à 1948 · zéro prérequis**

**Fil rouge** : les algorithmes n'ont pas attendu les ordinateurs. Ils ont 4000 ans.
Cette saison va de l'argile babylonienne au bit de Shannon, et se termine pile avant
l'informatique moderne — la saison 2 pourra demander « et maintenant, comment ça marche ? ».

**À la fin de la saison, l'équipage sait** : ce qu'est un algorithme (intuitivement), d'où
viennent les mots « algorithme » et « algèbre », pourquoi le binaire, ce qu'est une machine
universelle, et ce qu'est un bit.

---

### E101 — L'homme qui a donné son nom aux algorithmes
*Al-Khwarizmi · Bagdad, vers 820 — LE PILOTE*

- **Idée unique** : le mot « algorithme » est le nom latinisé d'un mathématicien de Bagdad.
- **Hook** : « Chaque fois que tu prononces le mot "algorithme", tu dis le nom d'un homme mort depuis 1200 ans. »
- **La Quête** : Bagdad, IXe siècle, la Maison de la Sagesse — l'empire abbasside traduit et fusionne les savoirs grecs, indiens et persans. Al-Khwarizmi écrit deux livres fondateurs : un sur le calcul avec les chiffres indiens (traduit en latin sous le titre *Algoritmi de numero Indorum* — « Al-Khwarizmi sur les nombres indiens »), et un sur la résolution des équations, *al-jabr wa-l-muqabala* — « la remise en place et l'équilibre ».
- **Le Mécanisme** : montrer une « recette » d'al-jabr écrite entièrement en phrases (l'époque n'a pas nos symboles !) et la transformer sous nos yeux en équation moderne. L'algorithme = une recette sans ambiguïté, exécutable par quelqu'un qui ne comprend pas pourquoi ça marche.
- **Dans ta vie** : le mot « algorithme » dans les médias (« l'algo de TikTok ») ; l'algèbre à l'école ; les chiffres que tu utilises (dont on retrouvera le voyage en E105).
- **La Légende** : « al-jabr » désignait aussi la réduction des fractures — et dans *Don Quichotte*, un « algébriste » est un rebouteux, un remetteur d'os. L'algèbre a commencé par réparer des os.
- **Visuel clé** : une phrase en recette rhétorique qui se cristallise en symboles mathématiques.
- **Récap** : « Un algorithme, c'est une recette : des étapes claires, dans l'ordre, qui marchent même si tu ignores pourquoi. »
- **Cap sur…** : « Mais avant même le mot, des algorithmes existaient. Gravés dans l'argile, il y a 3800 ans. »

### E102 — La tablette qui calculait des racines carrées
*Babylone, vers -1800*

- **Idée unique** : l'humanité calcule par recettes itératives depuis ses premiers écrits.
- **Hook** : « 3800 ans avant ta calculatrice, un scribe a gravé la racine de 2 avec cinq décimales exactes. Dans de l'argile. »
- **La Quête** : Babylone, ses écoles de scribes, ses tablettes scolaires. La tablette YBC 7289 et son carré traversé par sa diagonale.
- **Le Mécanisme** : la méthode « de Héron » : estimer, diviser, faire la moyenne, recommencer — animation d'une estimation qui se resserre sur √2 à chaque tour. L'idée d'*itération* : une règle simple répétée converge vers la réponse.
- **Dans ta vie** : ta calculatrice et tes jeux vidéo calculent des racines avec des descendants de cette idée (Newton-Raphson) ; et si nos heures font 60 minutes, c'est l'héritage de la base 60 babylonienne.
- **La Légende** : pourquoi 60 ? Hypothèse des phalanges (3 phalanges × 4 doigts = 12, × 5 mains de l'autre main = 60) — présentée comme hypothèse. Et le statut de YBC 7289 : une tablette d'école, sans nom d'auteur — l'anonymat des premiers algorithmes.
- **Visuel clé** : deux boules qui se rapprochent de la cible √2, tour après tour.
- **Cap sur…** : « 1500 ans plus tard, à Alexandrie, un homme écrit une recette qui tourne encore aujourd'hui — dans ton téléphone. »

### E103 — Le plus vieux programme encore en production
*Euclide · Alexandrie, vers -300*

- **Idée unique** : l'algorithme du PGCD d'Euclide tourne encore, 2300 ans après.
- **Hook** : « Il y a un bout de code vieux de 2300 ans qui tourne encore en production. Aucune maintenance. Zéro mise à jour. »
- **La Quête** : Alexandrie, les *Éléments*, livre VII. Euclide raisonne sur des segments, pas des nombres — géométrie pure.
- **Le Mécanisme** : PGCD(48, 18) : couper 48 avec 18, il reste 12 ; couper 18 avec 12, il reste 6 ; 12 se coupe pile avec 6 → 6. Pas-à-pas animé comme la découpe de deux bâtons. Puis le « secret » : chaque reste rétrécit, donc ça s'arrête forcément — l'idée de *garantie de terminaison*.
- **Dans ta vie** : simplifier des fractions (le PGCD fait le ménage) ; la cryptographie moderne cherche ses nombres premiers avec des cousins de cette idée (teaser E308) ; le formatage d'images et de pixels.
- **La Légende** : d'Euclide lui-même, on ne sait presque rien — pas de portrait fiable, pas de biographie. L'un des hommes les plus influents de l'histoire est un fantôme. (Et l'anecdote de Ptolémée : « il n'y a pas de voie royale en géométrie » — même les rois doivent faire les exercices.)
- **Visuel clé** : deux bâtons qui se découpent l'un l'autre jusqu'au morceau entier.
- **Récap** : « Un bon algorithme prouve qu'il s'arrête. Euclide l'a fait 2300 ans avant les informaticiens. »
- **Cap sur…** : « Trouver le plus grand commun diviseur, très bien. Mais comment débusquer TOUS les nombres premiers ? Un bibliothécaire va avoir l'idée d'un crible. »

### E104 — Le bibliothécaire qui a mesuré la Terre avec un bâton
*Ératosthène · Alexandrie, vers -240*

- **Idée unique** : le crible — éliminer les candidats plutôt que chercher les élus.
- **Hook** : « Un puits, un bâton, et des compteurs de pas. Avec ça, il a mesuré la Terre. »
- **La Quête** : Ératosthène, directeur de la grande bibliothèque d'Alexandrie, surnommé « Bêta » — deuxième en tout par ses contemporains. Le grenier à questions du monde antique.
- **Le Mécanisme** : la mesure de la Terre d'abord (Syène : le soleil éclaire le fond du puits au solstice ; Alexandrie : le bâton projette une ombre de 1/50 de tour ; 5000 stades de distance × 50 = le tour complet — animation carte). Puis le crible : grille de 1 à 100, barrer les multiples de 2, de 3, de 5… ce qui reste : les premiers. La puissance du *par l'élimination*.
- **Dans ta vie** : la cryptographie cherche de très grands nombres premiers (teaser E308) ; la logique « barrer plutôt que vérifier un par un » revient partout : filtres anti-spam, déduplication, candidatures (élimination sur critères).
- **La Légende** : « Bêta » — le compliment insultant. Et il a fini sa vie en se laissant mourir de faim, aveugle et désespéré… (assumé avec pudeur, une ligne).
- **Visuel clé** : la grille 1-100 qui s'épure, les multiples qui s'effacent en cascade.
- **Récap** : « Parfois, le moyen le plus rapide de trouver, c'est d'éliminer. »
- **Cap sur…** : « 1500 ans plus tard, un gamin de Pise ramène d'Afrique du Nord des chiffres qui vont paniquer toute l'Europe. »

### E105 — Les lapins, les chiffres et la loi contre le zéro
*Fibonacci · Pise, 1202*

- **Idée unique** : la suite de Fibonacci — et la plus grande diffusion technologique de l'histoire : les chiffres eux-mêmes.
- **Hook** : « En 1299, Florence interdit par la loi les chiffres que tu es en train d'utiliser. »
- **La Quête** : Pise, le petit Leonardo, fils d'un marchand de la colonie de Béjaïa (Algérie actuelle) — il y apprend les chiffres indo-arabes des calculateurs arabes. En 1202, le *Liber Abaci* les présente aux marchands d'Europe : calculer « avec les chiffres », contre l'abaque à jetons.
- **Le Mécanisme** : les lapins du Liber Abaci : chaque paire adulte engendre une paire par mois → 1, 1, 2, 3, 5, 8, 13… Une règle minuscule (chaque terme = somme des deux précédents) engendre un comportement qui explose. Animation de l'arbre de lapins. (Le nombre d'or : une ligne honnête — oui le ratio converge, non il n'est pas « partout dans la nature/ l'art » ; désamorcer le mythe.)
- **Dans ta vie** : le système décimal positionnel (et le zéro !) ; les spirales de tournesol et de pomme de pin (la vraie phyllotaxie) ; et la suite sera LE cas d'école de la programmation dynamique (teaser S3).
- **La Légende** : la loi florentine de 1299 — l'Arte del Cambio (la guilde des changeurs) interdit les chiffres arabes dans les comptes : trop faciles à falsifier (un 0 se transforme en 6 ou en 9). Le Moyen Âge a eu ses « algoristes » contre « abacistes » — littéralement une guerre des interfaces.
- **Visuel clé** : un registre de comptes où un 0 se métamorphose en 6 sous un stileto.
- **Récap** : « Des règles très simples peuvent engendrer des comportements très riches — retiens ça, c'est le moteur de toute la suite. »
- **Cap sur…** : « Deux siècles plus tard, un philosophe allemand invente une langue où tout s'écrit avec deux signes. Il la croira divine. »

### E106 — La langue à deux lettres
*Leibniz · Hanovor/Paris, 1679*

- **Idée unique** : le binaire — tout l'univers numérique s'écrit avec 0 et 1.
- **Hook** : « Inventer l'ordinateur sans le savoir, il suffit d'inventer une langue à deux mots. »
- **La Quête** : Leibniz — philosophe, diplomate, mathématicien — rêve d'une *caractéristique universelle* : une langue où calculer la vérité. En 1679, son mémoire sur la progression dyadique : tous les nombres avec deux signes.
- **Le Mécanisme** : compter sur ses doigts en binaire (animation mains), pourquoi « deux états » (présent/absent, haut/bas) c'est plus fiable qu' dix états — d'où le transistor : ouverte/fermée. Texte, son, image → tout devient suites de 0 et 1.
- **Dans ta vie** : tout ce qui est numérique ; chaque photo, chaque son ; l'octet et ses 256 valeurs (pourquoi 255 est un nombre fétiche des jeux vidéo).
- **La Légende** : 1701, le père Bouvet, missionnaire jésuite en Chine, lui envoie les hexagrammes du *Yi Jing* — 64 figures faites de traits pleins et brisés. Leibniz, stupéfait : les Chinois écrivent en binaire depuis plus de mille ans. Il y verra un signe divin — la plus belle « convergence inventée deux fois » de l'histoire.
- **Visuel clé** : un hexagramme du Yi Jing qui bascule en `010001` puis en 17.
- **Récap** : « Deux états bien distingués suffisent à tout écrire. C'est pour ça que ta machine est bête et fiable à la fois. »
- **Cap sur…** : « Cette langue va dormir 120 ans. Puis un tisseur lyonnais va s'en servir pour faire de la soie. »

### E107 — Quand le tissu a appris à programmer
*Jacquard · Lyon, 1801-1804*

- **Idée unique** : la carte perforée — des trous qui deviennent des instructions.
- **Hook** : « Le premier programme de l'histoire n'était pas un calcul. C'était un motif de fleurs. En soie. »
- **La Quête** : Lyon, la soie, les canuts penchés sur leurs métiers à la tire. Jacquard combine les inventions de ses prédécesseurs (Bouchon, Falcon, Vaucanson) : le métier à cartes perforées. Le tissage se pilote par des trous.
- **Le Mécanisme** : carte → trou ou non-trou → fil levé ou baissé (le binaire d'E106 en soie !). Série de cartes en boucle = motif reproductible à l'infini = *programme*. Changer les cartes sans changer la machine = la séparation données/instructions, sans le savoir.
- **Dans ta vie** : descendance directe : les cartes d'Hollerith pour le recensement américain de 1890 (naissance d'une petite société qui deviendra IBM), les cartes perforées des ordinateurs jusqu'aux années 80, les pianos mécaniques — et l'idée même qu'une machine se « reprogramme ».
- **La Légende** : les canuts, misérables puis révoltés (1831) — la première révolte ouvrière contre l'automatisation ; et le portrait de Jacquard tissé *en soie par sa propre machine*, en 24 000 cartes. Babbage en achètera un exemplaire pour le montrer à ses visiteurs — le prochain épisode commence là.
- **Visuel clé** : une carte perforée qui glisse dans le métier et fait lever les fils un par un.
- **Récap** : « Un programme, c'est juste une suite d'instructions qu'une machine peut lire. Même une machine à tisser. »
- **Cap sur…** : « Babbage regarde ce portrait de soie et rêve mille fois plus grand : une machine qui tisserait… les nombres. »

### E108 — L'ordinateur né cent ans trop tôt
*Babbage & Lovelace · Londres, 1837-1843*

- **Idée unique** : l'architecture de l'ordinateur (mémoire, calculateur, instructions) a été conçue en 1837, à vapeur et en métal — et le premier programme a été écrit pour une machine jamais construite.
- **Hook** : « En 1843, une comtesse écrit le premier programme de l'histoire. Pour une machine qui n'existe pas. »
- **La Quête** : Babbage saigne le Trésor britannique (plus de 17 000 livres — une fortune) sur sa machine à différences, puis rêve la machine analytique. Ada Byron, fille du poète, éduquée aux mathématiques par une mère voulant l'éloigner de la poésie — elle traduira le mémoire de Menabrea et y annexera ses propres notes, plus longues que l'original.
- **Le Mécanisme** : l'architecture de la machine analytique : le « magasin » (mémoire), le « moulin » (calculateur), les cartes de Jacquard (programme) — poser le schéma side-par-side avec un CPU moderne : registres, ALU, instructions. Même dessin. Le programme des nombres de Bernoulli (note G) : boucles et réutilisations — montré en pseudo-recette simple.
- **Dans ta vie** : ton téléphone est la machine analytique d'Ada et Babbage, en silicium ; et la Note A d'Ada contient la phrase fondatrice : la machine pourrait « composer des morceaux de musique scientifiques et élaborés » — manipuler des symboles, pas juste des nombres. Elle invente l'idée de logiciel.
- **La Légende** : la punition maternelle (les maths contre la poésie) qui a produit la plus poétique des mathématiciennes ; et le projet-mort-né : faute de financement, la machine ne sera jamais construite de son vivant. (Le Science Museum de Londres en a construit une en 2002 — à partir des plans. Elle marche.)
- **Visuel clé** : le schéma vapeur de 1837 qui morphe en die-shot de CPU.
- **Récap** : « Un ordinateur, c'est trois choses : mémoire, calculateur, instructions. Tout le reste est du détail. Depuis 1837. »
- **Cap sur…** : « Il manquait une chose : la preuve qu'une telle machine peut exister. Un Anglais de 24 ans la fournira — en prouvant en même temps ce qu'elle ne pourra JAMAIS faire. »

### E109 — La machine imaginaire qui a prouvé l'impossible
*Turing · Cambridge, 1936*

- **Idée unique** : la machine de Turing — définir ce que « calculer » veut dire, avant les ordinateurs, en prouvant qu'il existe des problèmes incalculables.
- **Hook** : « En 1936, un étudiant de 24 ans invente une machine qui n'existe pas — pour prouver qu'il y a des choses qu'aucune machine ne pourra jamais calculer. »
- **La Quête** : le programme de Hilbert : toute question mathématique peut-elle être tranchée par un calcul ? (l'Entscheidungsproblem). Turing, à King's College, répond avec un objet théorique d'une simplicité insultante.
- **Le Mécanisme** : un ruban, une tête, des règles — animation d'une mini-machine qui lit, écrit, déplace, change d'état (avec des états nommés humainement). Puis le coup de génie : la machine *universelle* — une machine qui lit la description d'une autre machine et la simule. Programme = données. C'est un ordinateur.
- **Dans ta vie** : tout ordinateur est une machine universelle de Turing ; et le prix de l'universalité : le problème de l'arrêt — aucun programme ne peut prédire si un programme va terminer (pourquoi aucun « détecteur de bugs parfait » n'existera jamais).
- **La Légende** : Turing courait le marathon en 2h46 — niveau olympique de l'époque — et croisait parfois ses collègues en courant jusqu'aux réunions ; et la suite de sa vie (Bletchley Park, la guerre, le drame final) — annoncée ici, racontée plus tard dans la chaîne.
- **Visuel clé** : le ruban qui défile sous la tête, les cases qui changent une à une.
- **Récap** : « Turing n'a pas inventé l'ordinateur. Il a inventé la preuve que l'ordinateur est possible — et ses limites. »
- **Cap sur…** : « Les fondations sont posées. Reste une brique si petite qu'on la mesure en bits. Un ingénieur des Bell Labs va lui donner un nom en 1948. »

### E110 — Le bit — la plus petite brique de l'univers numérique
*Shannon · Bell Labs, 1937 & 1948 — ÉPISODE CONFLUENCE*

- **Idée unique** : l'information devient une grandeur mesurable — et cette mesure s'appelle le bit.
- **Hook** : « En 1948, un article de quelques dizaines de pages fonde une science entière. On y apprend qu'on peut mesurer l'information comme on mesure des litres. »
- **La Quête** : Claude Shannon, 21 ans en 1937 : sa thèse de master relie circuits électriques et algèbre de Boole (les portes logiques — le pont définitif vers Leibniz, E106). Puis Bell Labs, le bruit sur les lignes, et 1948 : *Une théorie mathématique de la communication*.
- **Le Mécanisme** : mesurer l'information = mesurer l'incertitude. Le jeu des 20 questions : chaque réponse oui/non divise le monde en deux → une réponse = 1 bit. Le mot « bit » (proposé par John Tukey : *binary digit*). Puis une promesse éblouissante : avec du codage, on transmet fiablement même sur une ligne bruitée — la base des codes correcteurs d'erreurs.
- **Dans ta vie** : mégabits et mégaoctets ; un code QR à moitié déchiré qui marche encore (correction d'erreurs) ; la 5G, le WiFi, les disques durs — tous des enfants de 1948 ; et la compression (teaser S3 : Huffman).
- **La Légende** : Shannon, esprit le plus joueur des Bell Labs — il construisait des machines inutiles et géniales, dont « Thésée » (1950), une souris électrique qui apprend à sortir d'un labyrinthe : la première machine qui apprend. Le prochain épisode de la chaîne s'appellera peut-être un jour comme elle.
- **Visuel clé** : une question oui/non qui fend l'univers en deux, encore et encore.
- **Récap** : « L'information se mesure. Son unité est un choix entre deux : le bit. »
- **Cliffhanger de saison** : « Les algorithmes avaient 4000 ans. L'ordinateur était enfin pensé, jusqu'à sa plus petite brique. Tout est prêt. Prochaine expédition : les fondamentaux — comment on cherche, comment on trie, et pourquoi ça change tout. »

---

## Sources principales de la saison (à re-vérifier au script)

- Knuth, *TAOCP* vol. 1, §1.1 (histoire d'Euclide et d'al-Khwarizmi)
- Jens Høyrup / articles sur l'algèbre arabe médiévale (E101)
- Neugebauer, *The Exact Sciences in Antiquity* (E102 — YBC 7289)
- Dunham, *Journey through Genius* ; lettre d'Euler au maire de Dantzig (E103-E104)
- Sigler, *Fibonacci's Liber Abaci* (traduction) ; statuts de l'Arte del Cambio 1299 (E105)
- Leibniz, *De Progressione Dyadica* ; correspondance Leibniz-Bouvet (E106)
- Essinger, *Jacquard's Web* (E107-E108 — et le portrait tissé)
- Isaacson, *The Innovators* (E107-E109) ; Hodges, *Alan Turing: The Enigma* (E109)
- Gleick, *The Information* ; Shannon, *A Mathematical Theory of Communication*, 1948 (E110)
