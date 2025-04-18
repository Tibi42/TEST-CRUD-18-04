# Questionnaire sur le code JavaScript -

#### 1. Quels sont les trois tableaux déclarés au début du code ? Et que contiennent-ils ?

**Indice :** Regardez les premières lignes du code qui commencent par `let`.

Les trois tableaux (array) declarés au début du code sont :

- tableau sections, contenant l'objet title avec la valeur Section 1

- tableau containers, contenant l'objet title avec la valeur Listes des taches dont l'index est initialisé à 0

- tableau cards, contenant deux objets title :
  - le premier avec la valeur Apprendre HTML ayant la description Base du HTML ...
  - le second avec la valeur Apprendre CSS ayant la description Styliser les pages web

ils continennent des objets

#### 2. Quel élément HTML est utilisé pour afficher tout le contenu de l'application ?

**Indice :** Cherchez la ligne qui utilise `document.getElementById`.

L'element HTML utilisé pour afficher tout le contenu de l'application est le main ayant l'id content

#### 3. Qu'est-ce que fait la fonction `prompt()` utilisée dans le code ?

**Indice :** Cette fonction apparaît plusieurs fois dans le code, notamment dans les fonctions comme `addSection()`.

La fonction prompt fait apparaitre un fefenetre ou l'on peux taper du nouveua texte pour changer le title de :

- de la section
- du container
- des cards

notemment pour le titre de :

- Titre de la nouvelle section
- Titre du nouveau conteneur
- Titre de la carte
- Description de la carte
  etc...

#### 4. Combien de propriétés (ou "clés") contient un objet dans le tableau `sections` ?

**Indice :** Regardez la structure d'un objet section au début du code.

l'objet de base contient une clé qui est title,
mais un tableau section peut contenir plsuieurs plusieur objets, cela depende du nombre de creation container et de cards,

---

### Fonctions d'ajout

#### 5. Que fait la fonction `addSection()` ?

**Indice :** Cette fonction se termine par un appel à `renderPage()`.

la fonction addsection fait apparaitre un prompt nous demandant le titre de la nouvelle section et pousse cette nouvelle sectiondont la cé qui est créer est title et dont la valeur est sectionTitle dans le main de l'HTML

#### 6. À quoi sert la condition `if (!sectionTitle) return;` dans la fonction `addSection()` ?

**Indice :** Réfléchissez à ce qui se passe si l'utilisateur clique sur "Annuler" dans la boîte de dialogue prompt.

cela signifie que si la section title est vide alors return qui arrete lexecution de la condition

#### 7. Quelle méthode de tableau est utilisée pour ajouter un nouvel élément dans le tableau `sections` ?

**Indice :** C'est une méthode qui permet d'ajouter un élément à la fin d'un tableau.

la methode utiliser pout ajouter un nouvel elelement dnas le tableau est : push()

#### 8. Quelles informations sont demandées à l'utilisateur lors de l'ajout d'une carte avec la fonction `addCard()` ?

**Indice :** La fonction `addCard()` appelle `prompt()` deux fois.

les informations demandées lors de l'ajout de la card sont :

    - en premier le titre de la card
    - en second la description de la card

---

### Fonctions de modification

#### 9. Quand on modifie une section avec la fonction `editSection()`, quelle information peut-on changer ?

**Indice :** Regardez ce qui est demandé à l'utilisateur et ce qui est modifié dans l'objet section.

l'information que l'on peut changé par edditsection() est le titre de la section

#### 10. Examinez cette ligne : `const section = sections[sectionIndex];` dans la fonction `editSection()`. Que fait-elle ?

**Indice :** Pensez à l'accès aux éléments d'un tableau avec les crochets `[]`.

le code de cette ligne selectionne et stocke dans sections (le tableau du debut du code ) l'index de sections

#### 11. Dans la fonction `editCard()`, comment les nouvelles valeurs sont-elles appliquées à la carte ?

**Indice :** Regardez les dernières lignes de la fonction, après les prompts.

les nouvelles valeurs sont appliquées par :

- card.tile = newTitle;
- card.description = newDescription;

et sont executées par renderPage();

#### 12. Pourquoi la fonction `editContainer()` vérifie-t-elle si `container` existe avec `if (!container) return;` ?

**Indice :** Pensez à ce qui pourrait se passer si `containerIndex` n'est pas valide.

la fonction editcontainer verifie si il y a eu un changement dans l'index pour pouvoir l'appliquer sur le tableau containers
si l'index n'etait pas valide alors il ne se passe rien

---

### Fonctions de suppression

#### 13. Que fait la fonction `confirm()` utilisée dans les fonctions de suppression ?

**Indice :** Elle est utilisée avant de supprimer un élément.

la fonction confirm demande de valider ou d'annuler avant de supprimer une section par son index

#### 14. Quelle méthode de tableau est utilisée pour supprimer un élément dans `deleteSection()` ?

**Indice :** Cette méthode permet de supprimer un certain nombre d'éléments à partir d'un index donné.

la methode utilisée pour supproimer les element a partir d'un index est splice()
et pour l'index : sectionIndex, 1 donc a paratir de l'index 1

#### 15. Dans la fonction `deleteContainer()`, qu'arrive-t-il aux cartes qui étaient dans le conteneur supprimé ?

**Indice :** Regardez comment le tableau `cards` est modifié après la suppression d'un conteneur.

Les cards sont aussi supprimées

#### 16. Pourquoi doit-on ajuster les propriétés `containerIndex` des cartes après avoir supprimé un conteneur ?

**Indice :** Pensez à ce qui arrive aux indices des éléments dans un tableau après la suppression d'un élément.

---

### Rendu de la page

#### 17. Quelle est la première chose que fait la fonction `renderPage()` ?

reinitialise la page

**Indice :** C'est une action qui vide le contenu HTML existant.

#### 18. Comment crée-t-on un nouvel élément HTML en JavaScript ?

**Indice :** Cherchez la méthode qui commence par "create" dans le code.

la methode pour creer un element en HTML est createElement("")
par exemple createElement("div") créer une div

#### 19. Comment ajoute-t-on une classe CSS à un élément HTML en JavaScript ?

**Indice :** Regardez ce qui se passe juste après la création d'un élément avec `document.createElement()`.

on joute une classe de CSS a un element HTML en JS par .className = "nom de la classe CSS "

#### 20. Comment ajoute-t-on du contenu HTML à l'intérieur d'un élément ?

**Indice :** C'est une propriété qui permet de définir le contenu HTML d'un élément.

pour ajouter du contenu HTML a l'interieur d'un elememnt on utilise :
.innerHTML = ` et on ajoute les div le paragraphe entre les bactites`

#### 21. Comment ajoute-t-on un élément HTML comme enfant d'un autre élément ?

**Indice :** C'est une méthode qui se termine par "Child".

la methode pour ajouter un element HTML comme enfant eset .appenChild()

#### 22. Examinez cette ligne : `containers.filter(container => container.sectionIndex === sectionIndex)`. Que fait la méthode `filter()` ?

**Indice :** C'est une méthode qui crée un nouveau tableau avec seulement certains éléments.

la methode filter filtres les element dans un tableau plus court que le tebleau d'entré. on filtre par l'index du tableau containers
ici

---

### Organisation et événements

#### 23. Comment le code sait-il quels conteneurs appartiennent à quelle section ?

**Indice :** Chaque conteneur a une propriété qui indique à quelle section il appartient.

chaque containers a un ID unique qui permet de le cibler specifiquement

#### 24. Comment le code sait-il quelles cartes appartiennent à quel conteneur ?

**Indice :** Similaire à la question précédente, chaque carte a une propriété qui indique son conteneur.

de meme que pour les conatineur qui on un ID, les cards on un ID specifique lié a leurs container qui les contients

#### 25. Quelle méthode est utilisée pour exécuter une fonction quand on clique sur un bouton ?

**Indice :** Regardez les attributs ajoutés aux balises `<button>` dans le HTML généré.

l'attribut ajouter au boutton est : onclick

#### 26. Quand la fonction `renderPage()` est-elle appelée dans le code ?

**Indice :** Cherchez toutes les occurrences de `renderPage()` dans le code.

la fonction renderpage() mets a jour dynamiquement la fonction dans la quelle elle est appelé

#### 27. Quelle fonction est exécutée quand la page se charge ?

**Indice :** Cherchez l'événement `DOMContentLoaded`.

la fonction qui est executé quna la parge se charge est l'ecoute au click sur le boutton dont l'id est add-section-btn

---

### Application pratique

#### 28. Si vous avez 2 sections et que vous supprimez la première, que devient la propriété `sectionIndex` des conteneurs qui étaient dans la deuxième section ?

**Indice :** Regardez le code qui met à jour les index dans la fonction `deleteSection()`.

on soustrait 1 a l'index de la deuxieme section

#### 29. Si on ajoute une nouvelle carte, comment le code sait dans quel conteneur la placer ?

**Indice :** Regardez le paramètre de la fonction `addCard()` et ce qu'elle en fait.

le code sait ou placé la card dant le bon caontaineur grace a son Index qui est lié au container dont depend la card, sont tiltle et sa description

#### 30. Que se passerait-il si on supprimait la ligne `renderPage();` à la fin de chaque fonction d'ajout, de modification et de suppression ?

**Indice :** Pensez à ce qui permet de voir les changements sur la page.

les fonctions ne serait plus mis a jour dynamiquement et ne feraient plus apparaitre les changement
