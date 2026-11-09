# La chronologie — vue d'ensemble des 5 expéditions

## 1. La logique de progression (« de la base vers l'avancé »)

La chaîne avance sur deux chronologies en même temps :

- **La chronologie de l'invention** (saison 1) : l'algorithme existe depuis 4000 ans — on commence à Babylone, bien avant les ordinateurs. Zéro prérequis : on entre par l'histoire.
- **La chronologie conceptuelle** (saisons 2 → 5) : chaque saison suppose *un peu plus* du spectateur, mais chaque concept est reconstruit à partir des précédents (les « callbacks » entre épisodes sont la colonne vertébrale pédagogique de la chaîne).

| # | Expédition | Fil rouge | Épisodes | Prérequis |
|---|---|---|---|---|
| S1 | **Aux origines** | « L'algorithme est né bien avant l'ordinateur » | 10 | Aucun |
| S2 | **Les fondamentaux** | « Chercher, trier, ranger, relier — les gestes de base » | 12 | Aucun (S1 = bonus) |
| S3 | **Ceux qui gouvernent** | « Les algorithmes invisibles du monde moderne » | 10 | S2 conseillée |
| S4 | **L'ère de l'apprentissage** | « Quand les machines ont appris à apprendre » | 7 | S2 + E301-E303 |
| S5 | **Les frontières** | « Cap sur l'inconnu » | 6 | Épisodique |

≈ 45 escales ≈ 21 mois à 1 épisode / 2 semaines.

## 2. Les épisodes pivots (ceux qui peuvent « porter » la chaîne)

- **E101 — Al-Khwarizmi** : le pilote. L'origine du mot = l'origine de la chaîne.
- **E211 — Les 7 ponts de Königsberg** : histoire parfaite, visuel simple, potentiel viral fort.
- **E204/E205/E206 — la trilogie des tris** : la séquence la plus « partageable » par l'audience étudiante.
- **E305 — P vs NP** : le problème à 1 million — aimant à curiosité.
- **E308 — RSA** : « comment deux inconnus peuvent se parler en secret sous les yeux de tous ».
- **E401 — Le perceptron** : promesses brisées de l'IA — résonance avec l'actualité permanente.

## 3. Règles d'articulation entre saisons

- Chaque saison se clôt par un **épisode confluence** qui ouvre narrativement sur la suivante.
- **Callbacks systématiques** : chaque épisode réutilise au moins une brique d'un épisode
  précédent (la recherche binaire revient dans les arbres, la pile revient dans la traversée
  de graphes…). C'est ce qui donne le sentiment de *série* — et la raison de s'abonner.
- À partir de S2 : **1 épisode sur 4 choisi par l'équipage** (sondage).
- Les fichiers détaillés : `saison-01-origines.md`, `saison-02-fondamentaux.md`,
  `saison-03-algorithmes-qui-gouvernent.md`. Les saisons 4 et 5 restent volontairement en
  aperçu ci-dessous : elles s'affineront avec les retours de la communauté.

---

## 4. Aperçu — Expédition IV : L'ère de l'apprentissage (7 escales)

> « Tous les algorithmes précédents ont un point commun : des humains écrivaient les règles.
> Et si la machine écrivait ses propres règles ? »

| # | Titre provisoire | Idée |
|---|---|---|
| E401 | La machine qui a déçu le New York Times | Le perceptron (1958), le hype, le XOR de Minsky & Papert (1969), le premier hiver de l'IA |
| E402 | Descendre la montagne dans le brouillard | La descente de gradient — un algorithme de 1847 (Cauchy) qui entraîne les IA d'aujourd'hui |
| E403 | L'algorithme qui a réveillé les réseaux | Rétropropagation (1986) — apprendre à blâmer chaque neurone |
| E404 | La nuit où l'IA a appris à voir | ImageNet/AlexNet (2012) — quand les GPU changent tout |
| E405 | « Attention is all you need » | Transformers (2017) → la famille des LLM (le papier aux 100 000 citations) |
| E406 | Le million de Netflix | Systèmes de recommandation (2006-2009) — et le drame des 20 minutes |
| E407 | Le casino de Los Alamos | Méthodes de Monte Carlo (Ulam, 1946) — du solitaire à AlphaGo (le coup 37) |

## 5. Aperçu — Expédition V : Les frontières (6 escales)

| # | Titre provisoire | Idée |
|---|---|---|
| E501 | L'algorithme qui menace tes cartes bleues | Shor (1994) et le calcul quantique |
| E502 | Chercher dans l'univers quantique | Grover (1996) — √n, quand même |
| E503 | Aligner le vivant | Bio-informatique : Needleman-Wunsch (1970), BLAST, séquençage |
| E504 | Le parlement à temps partiel | Consensus distribué : Paxos (Lamport), Raft — les algorithmes qui gardent le monde cohérent |
| E505 | Compter un milliard sans le stocker | HyperLogLog & les algorithmes probabilistes — l'erreur maîtrisée comme outil |
| E506 | La carte et l'horizon | Épisode final : ce que 4000 ans d'algorithmes disent du futur |

## 6. Références transverses (à garder à portée de script)

- Donald Knuth, *The Art of Computer Programming* (vol. 1 & 3 — sections historiques)
- Thomas Cormen et al., *Introduction to Algorithms* (le point technique de référence)
- James Gleick, *The Information* (Shannon, le bit — arrière-plan E110)
- Walter Isaacson, *The Innovators* (Lovelace → Turing → internet, très narratif)
- Andrew Hodges, *Alan Turing: The Enigma* (E109)
- David Harel, *Algorithmics: The Spirit of Computing*
- Articles primaires cités dans les fiches d'épisodes (lettres, papers, autobiographies)

Chaque fait d'une fiche doit être re-vérifié au moment du script (voir `bible/02-ton-et-pedagogie.md` §6).
