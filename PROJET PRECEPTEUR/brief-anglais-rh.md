# Brief de production — Parcours d'anglais pour les RH

Tu vas produire une série de leçons d'anglais en HTML. Le fichier `Leçon d'anglais n° 0.html`
est la **référence absolue** : gabarit visuel, structure, mécaniques d'exercices et ton y
sont déjà validés. Ta mission n'est pas de réinventer, mais de produire des leçons
**cohérentes avec ce modèle**, de qualité constante, sans dériver.

Ce document te dit comment faire et — tout aussi important — **ce que tu ne dois pas faire**.

---

## 1. La règle non négociable : fiabilité factuelle

Ce support sert à apprendre. Une info fausse y est plus grave que partout ailleurs, parce
qu'elle sera mémorisée comme vraie. Une erreur a déjà été commise et corrigée sur ce projet
(une expression faussement attribuée à Shakespeare) : ne la reproduis pas.

- **N'écris jamais un fait, une date, une origine, une étymologie ou une citation sans en
  être certain.** En cas de doute, vérifie par recherche web avant de l'écrire.
- Si un fait n'est pas vérifiable ou reste incertain après vérification, **ne l'écris pas du
  tout.** On ne meuble pas avec une anecdote « qui sonne bien ». Couper vaut mieux qu'inventer.
- **Pas d'affirmation d'origine gratuite** (« cette expression vient de X »). Ne l'inclus que
  si elle est solidement attestée ET réellement utile à l'apprenante. Le sens d'une expression
  ne nécessite pas son étymologie.
- Vise le **classique utile et sûr**, pas le détail surfait ni la fausse érudition.

C'est le point sur lequel le travail sera vérifié en priorité.

---

## 2. Destinataire et intention

- Apprenante **A2 réel** (débutante avancée, phrases simples), en **alternance en ressources
  humaines**.
- Objectif : progresser en anglais général **et** se familiariser avec le vocabulaire et les
  tournures du métier RH.
- Chaque leçon = **un fichier HTML autonome**, ouvrable hors ligne dans un navigateur, sans
  installation ni dépendance externe (hormis les Google Fonts).
- Durée cible par leçon : **15 à 25 minutes selon la phase** (les leçons s'allongent à mesure
  qu'on avance — voir §7).
- Chaque leçon est **autonome** (compréhensible seule) mais la difficulté **augmente
  progressivement** à travers le parcours.

---

## 3. Progression d'ensemble (4 phases, 4 à 6 leçons chacune)

- **Phase 1 — Fondations (consolidation A2)** : se présenter en contexte pro, parler de son
  poste et de son entreprise ; présent simple vs continu ; chiffres, dates, horaires.
- **Phase 2 — Le quotidien RH écrit** : vocabulaire recrutement / contrat / paie ; rédiger un
  email simple, fixer un rendez-vous, accuser réception ; passé et futur de base.
- **Phase 3 — Oral et interaction** : mener ou passer un entretien, poser des questions, gérer
  un appel ; politesse et nuance (« anglais diplomatique ») ; modaux (can, could, would, should).
- **Phase 4 — Montée en compétence** : réunions, présenter une information, exprimer un
  désaccord poliment ; droit du travail et avantages sociaux ; conditionnel, structures plus
  complexes.

Les leçons 0 (`Breaking the Ice`) et 1 (`Tell Me About Yourself`) sont faites ; la prochaine à
produire est la leçon 2. Continue dans l'ordre indiqué par `plan-pedagogique.md`.

---

## 4. Structure d'une leçon (calquée sur le gabarit)

Reprends l'ordre et les sections-cartes du fichier de référence. **Évolution importante depuis
les leçons 1 et 2 :** le gabarit d'origine **testait plus qu'il n'enseignait**. On rééquilibre.
La leçon doit désormais **enseigner d'abord, puis vérifier**. Pour cela, un nouveau type de
carte — la carte **Focus** — explique le point dur du jour *avant* qu'on le teste, et peut
s'insérer **entre** les exercices, pas seulement en tête.

Rythme cible d'une leçon :

> Warm-up → Toolbox → **Focus** (mini-leçon sur le point dur du jour) → **Exercise 1** qui le
> teste en douceur → (**Focus 2** optionnel) → **Exercise 2** plus exigeant → **Exercise 3**
> (reading in context).

Les sections-cartes, dans l'ordre :

1. **Header** — kicker (phase + n° de leçon), titre avec un mot en italique coloré, sous-titre
   qui annonce l'objectif concret de façon vivante, pastille de progression.
2. **Warm-up** — court dialogue RH réaliste mettant en scène la notion du jour + une note
   utile (`.aside`).
3. **Toolbox** — vocabulaire du jour en grille (anglais / transcription phonétique simplifiée /
   français), puis une structure-clé expliquée avec exemples.
4. **Focus** — *nouvelle carte enseignante* (voir ci-dessous). Mini-leçon ciblée sur le point
   délicat du jour, posée **avant** le premier exercice qui le teste.
5. **Exercise 1 — QCM** : 3 questions de mise en application ancrées RH, qui testent **en
   douceur** le point du Focus.
6. **Focus 2** *(optionnel)* — second point enseignant, glissé **entre** les exercices, si la
   leçon en a réellement besoin.
7. **Exercise 2 — Texte à trous** : 3 phrases à compléter, **plus exigeantes** que l'Exercise 1.
8. **Exercise 3 — Reading in context** : 3 QCM dont le contexte sort du bureau (voir §6).
9. **Nextbox** — encadré sombre annonçant la leçon suivante.
10. **Footer**.

### La carte Focus (`.lesson`)

- **Rôle** : expliquer, pas tester. C'est le moment où l'apprenante *apprend* le point dur,
  avant qu'on le mette en jeu dans un exercice.
- **Contenu** : un **titre** ; une **explication claire en français** du point grammatical ou
  d'usage ; **2-3 exemples anglais commentés** ; et — quand c'est pertinent — un encadré
  `.aside` signalant le **piège francophone typique**.
- **Combien ?** : **1 ou 2 Focus par leçon**, selon le besoin réel du jour. Pas de quota
  rigide : un seul suffit souvent en phases 1-2, deux deviennent fréquents en phases 3-4 (voir §7).
- **Objectif d'ensemble** : que la leçon ne soit plus « que du test ». Elle **enseigne, puis
  vérifie.**

Le besoin technique (style `.lesson` distinct, étiquette teal pour distinguer d'un coup d'œil
« j'apprends » de « je suis testée ») est spécifié en §9.

---

## 5. Mécaniques d'exercices (conserver le code du gabarit tel quel)

- **QCM** : boutons `.opt` dans un conteneur `.opts` portant `data-correct="N"` (index base 0)
  et `data-why="…"`. Au clic : boutons désactivés, bonne réponse en vert. Réponse juste →
  bandeau **vert**. Réponse fausse → la bonne passe en vert ET un **unique bandeau bleu**
  affiche `data-why`, qui **explique pourquoi c'est faux**. **Jamais de second bandeau rouge** ;
  le rouge marque seulement le bouton cliqué par erreur.
- **Texte à trous** : `<input data-answer="…">` + bouton « Check ». Comparaison insensible à la
  casse et aux espaces. Erreur → indice sur la première lettre. Champ vide → invite à écrire.
- Le `data-why` n'est pas un lot de consolation : c'est le moment pédagogique. Il doit
  **corriger le malentendu**, pas juste désigner la bonne réponse.

---

## 6. Conception des questions — les pièges à éviter

Ces calibrages ont demandé plusieurs corrections. Respecte-les, c'est là que la qualité se joue.

- **Interdits : les cognats transparents.** Pas de « que signifie *colleague* ? → collègue ».
  Devinable sans rien savoir, n'apprend rien, vexant.
- **Interdit : l'évidence enfantine** (« dans quel pays est Big Ben »).
- **Interdit aussi : le trivia obscur** (mots étrangers rares, faits insolites inutiles à
  l'oral). Ni l'un ni l'autre extrême.
- **Toujours des distracteurs plausibles** et au moins une vraie subtilité par question : on
  doit avoir à *choisir*, pas à reconnaître l'évidence.
- Énoncés simples (niveau A2), mais le **raisonnement** demandé doit être réel : sens d'une
  expression en contexte, bonne structure grammaticale, faux-sens à éviter.
- **Reprise spiralée** : un point déjà enseigné dans une leçon antérieure peut revenir ici
  comme **distracteur piège**, sans être réexpliqué. C'est voulu (voir §7) : c'est ainsi qu'on
  vérifie qu'un acquis tient sous pression, plutôt que de le retester à l'identique.

### Le volet culturel (Exercise 3)

- L'anglais reste **la seule compétence évaluée**. Le culturel n'est qu'un décor pour aérer.
- Privilégie le **classique utile** : expressions idiomatiques réellement courantes (`a piece
  of cake`, `touch base`, `play it by ear`…), tournures qu'elle entendra et pourra replacer ;
  éventuellement une porte vers la culture/littérature **si et seulement si** c'est attesté
  (voir §1) et amené sans pédanterie.
- La question teste toujours un point d'anglais (sens d'une expression, d'un *phrasal verb*,
  d'une structure) ; l'élément culturel sert de support, jamais d'objet du test.

---

## 7. Gradation de la difficulté et spiralité

La difficulté ne doit pas tomber d'un coup : on l'**étale**, à l'intérieur d'une leçon et d'une
leçon à l'autre. Trois mouvements à tenir.

### a. Gradation intra-leçon

Dans une même leçon, le point vu en **Focus** est d'abord testé **en douceur** (Exercise 1 :
QCM guidé, contexte clair), puis de façon **plus exigeante** ensuite (Exercise 2, Exercise 3 :
moins d'aide, distracteurs plus serrés, contexte moins balisé). On apprend, on essaie sans
risque, on consolide en montant d'un cran.

### b. Spiralité inter-leçons

Un point **introduit et expliqué en leçon N** est **re-testé plus durement en leçon N+1 (ou
au-delà) sans être réexpliqué**. Il revient :

- soit comme **distracteur piège** non aidé (voir §6) ;
- soit comme **brique présupposée** d'une notion nouvelle, qu'on suppose désormais acquise.

Quelques exemples pour rendre la consigne actionnable :

- Le **present continuous**, expliqué et testé simplement en phase 1, réapparaît plus loin comme
  **piège non aidé** (distracteur face à un present simple), puis est **exploité tel quel** pour
  exprimer la **valeur de futur proche** (*I'm meeting the candidate tomorrow*) **sans
  réexplication** du temps lui-même.
- Les **idiomes de l'Exercise 3** (`touch base`, `play it by ear`…) peuvent **réapparaître plus
  tard en Exercise 1** d'une leçon ultérieure, cette fois **en plein contexte RH** et non plus
  comme décor culturel.

Concrètement : avant d'écrire une leçon, repère 1 ou 2 acquis des leçons précédentes que tu
peux **réactiver sans les réenseigner**. C'est ce tissage qui fait progresser.

### c. Densification progressive des phases

Le **nombre de leçons par phase reste stable (~5-6)**, mais les leçons **s'allongent et
s'approfondissent** à mesure qu'on avance :

- **Phases 1-2** — plus légères : durée **~15 min**, Warm-up court, **1 Focus** suffit souvent,
  exercices de mise en confiance.
- **Phases 3-4** — plus denses : durée **~20-25 min**, dialogues plus longs, **souvent 2
  Focus**, exercices plus exigeants et reprises spiralées plus nombreuses.

**Règle d'or** : rester **pertinent et digeste**, jamais d'empilement. On approfondit, on
n'entasse pas.

### d. Pas de double difficulté

On **n'introduit jamais une grammaire neuve ET un champ lexical opaque dans la même leçon**.
Quand la **grammaire est lourde**, le **lexique RH reste familier** ; quand on charge le
**vocabulaire**, la **grammaire reste connue**. Une seule nouveauté difficile à la fois — l'autre
dimension sert d'appui, pas d'obstacle supplémentaire.

---

## 8. Ton (point sensible — relis avant de rédiger)

- **Doux et complice**, avec une **pointe d'humour** discrète (situations de bureau légèrement
  absurdes, clins d'œil). L'humour rehausse, il n'envahit pas.
- **Bannir le condescendant et le faux-cul.** Proscrits : « pause détente sans pression »,
  « réponds au feeling », « petit moment rien que pour toi », et tout paternalisme. On
  s'adresse à une adulte intelligente.
- **Ni scolaire ni austère** : pas de ton de prof qui sanctionne. Les retours d'erreur sont
  **bienveillants et explicatifs**, jamais culpabilisants.
- **Consignes et explications en français ; contenu à apprendre en anglais.** Les notes peuvent
  glisser une remarque amusante sans en faire des tonnes.

---

## 9. Technique

- Reprends **exactement** le CSS du gabarit : palette (papier crème, terracotta, teal, or),
  polices Fraunces (titres) + Outfit (texte), cartes à étiquettes, responsive.
- **Nouveau style à créer : `.lesson`** pour la carte Focus. Elle doit être **distincte
  visuellement des cartes d'exercice** : son étiquette `.sec-tag` passe en **teal** (réutilise
  la variable `--teal` ; le gabarit a déjà `.sec-tag.fun { background: var(--teal); }`, suis la
  même logique). But : qu'on distingue **d'un coup d'œil** « j'apprends » (teal) de « je suis
  testée ». Le **reste du CSS reste inchangé**.
- Conserve les **mécaniques** du `<script>` du gabarit **inchangées** (QCM, trous, pastille de
  progression, révélation de la `nextbox`). La carte Focus est purement explicative : **elle
  n'ajoute aucun JavaScript.**
- **Suivi du score (obligatoire).** Chaque leçon enregistre son résultat pour que `index.html`
  puisse la colorer. Reprends le **bloc de score du gabarit tel quel** et **change uniquement
  `LESSON_ID`** (= le numéro de la leçon). Ce bloc retient le résultat à la **première
  tentative** de chaque question (QCM verrouillé au 1ᵉʳ clic ; trou au 1ᵉʳ *Check* non vide) via
  `recordResult(ex, correct)`, puis persiste `{correct, total, pct, done}` dans `localStorage`
  sous la clé partagée **`hr-en-progress`**. Ne touche à rien d'autre.
- Un seul fichier HTML autonome par leçon, CSS et JS inclus, aucune ressource externe hors
  Google Fonts.
- **Page d'accueil `index.html`** *(produite)* : liste les leçons par phase avec la progression,
  dans le même style visuel, et **reflète la nouvelle logique** (alternance enseigner/tester,
  densification croissante des phases). Elle lit `hr-en-progress` et **colore chaque leçon
  terminée selon son score** : **vert surligné à 100 %** (« Maîtrisé »), **ambre 70-99 %**
  (« À consolider »), **terracotta en dessous** (« À retravailler »). À chaque nouvelle leçon,
  ajoute son entrée (`data-lesson="N"`, titre, sous-titre) dans la phase correspondante.

---

## 10. Checklist avant de livrer une leçon

- [ ] Tout fait/date/origine/citation est vérifié, ou a été coupé en cas de doute.
- [ ] Aucune affirmation d'origine non attestée.
- [ ] **Au moins un Focus enseignant est présent et placé _avant_ l'exercice qui le teste**
  (la leçon enseigne, puis vérifie — ce n'est plus « que du test »).
- [ ] **Gradation intra-leçon respectée** : le point du Focus est testé en douceur d'abord,
  plus durement ensuite.
- [ ] **Reprise spiralée** d'un point antérieur quand c'est pertinent (distracteur piège ou
  brique présupposée), sans réexplication.
- [ ] **Pas de double difficulté** : pas de grammaire neuve ET de lexique opaque dans la même
  leçon.
- [ ] **Distinction visuelle leçon/exercice** : la carte Focus utilise `.lesson` avec étiquette
  teal, le reste du CSS et les mécaniques du `<script>` sont inchangés.
- [ ] **Suivi du score branché** : `LESSON_ID` est correct et le score se persiste dans
  `hr-en-progress` (la leçon apparaît colorée dans `index.html`), avec son entrée ajoutée à `index.html`.
- [ ] Aucun cognat transparent, aucune évidence enfantine, aucun trivia obscur.
- [ ] Chaque QCM a des distracteurs plausibles et un `data-why` qui explique le malentendu.
- [ ] Exercise 3 teste de l'anglais, le culturel n'est que support.
- [ ] Ton complice, zéro formulation condescendante.
- [ ] Le fichier s'ouvre seul, hors ligne, et respecte le CSS/JS du gabarit.
