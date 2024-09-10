# contact

1. Initialisation du localStorage avec un id unique
   Objectif : Initialiser des contacts fictifs dans le localStorage avec un id unique pour chaque contact.
   Détails : Chaque contact aura un id unique, comme { id: 2024545676, name: "John Doe", phone: "123456789", email: "john@example.com" }. Générer cet id via un Date.now().
   Nom de commit : feat: initialize contacts with unique id in localStorage

2. Récupération et affichage des contacts avec leur id
   Objectif : Afficher les contacts depuis le localStorage en utilisant l’id pour les identifier.
   Détails : Afficher la liste des contacts avec leur id et les informations correspondantes (nom, téléphone, email). Utiliser v-for avec :key="contact.id".
   Nom de commit : feat: display contacts with id from localStorage

3. Ajout d’un contact avec id unique
   Objectif : Ajouter un contact avec un id généré automatiquement.
   Méthode : addOne()
   Détails : Lors de l’ajout d’un contact, générer un id unique (par exemple, utiliser Date.now() pour garantir l’unicité). Ajouter ce contact à contacts et sauvegarder dans le localStorage.
   Nom de commit : feat: add contact with auto-generated unique id

4. Modification d’un contact existant en utilisant l’id
   Objectif : Modifier un contact en utilisant son id.
   Méthodes : editOneById(id) et updateOneById(id)
   Détails : Lorsque l’utilisateur sélectionne un contact pour modification, utiliser l’id pour retrouver le contact correspondant dans contacts et pré-remplir le formulaire. Sauvegarder les modifications dans contacts via l’id.
   Nom de commit : feat: edit and update contact by id

5. Suppression d’un contact par son id
   Objectif : Supprimer un contact en utilisant son id.
   Méthode : deleteOneById(id)
   Détails : Lorsqu’un utilisateur clique sur "Delete", supprimer le contact correspondant à l’id donné de la liste contacts et du localStorage.
   Nom de commit : feat: delete contact by id

6. Gestion du mode ajout/modification par id
   Objectif : Gérer l’ajout et la modification de contacts avec distinction selon l’état (ajout ou édition).
   Méthodes : addOne() et updateOneById(id)
   Détails : Si un contact est en mode édition (grâce à isEditing), utiliser updateOneById(id) pour mettre à jour le contact, sinon utiliser addOne() pour en créer un nouveau avec un id unique.
   Nom de commit : feat: toggle between add and edit modes for contacts

7. Mise en place du watcher pour la sauvegarde automatique
   Objectif : Mettre en place un watcher profond pour sauvegarder automatiquement les modifications dans le localStorage.
   Détails : Surveiller les changements dans contacts et mettre à jour automatiquement le localStorage à chaque modification.
   Nom de commit : feat: implement deep watcher for automatic localStorage sync

8. Tri des contacts par ordre alphabétique (nom)
   Objectif : Trier les contacts par ordre alphabétique avant de les afficher.
   Méthode : sortContacts()
   Détails : Trier la liste des contacts par nom avant de les afficher à l’utilisateur. Utiliser une propriété calculée pour garantir que le tri est toujours actif.
   Nom de commit : feat: sort contacts alphabetically by name

9. Recherche et filtrage des contacts par id
   Objectif : Filtrer les contacts affichés en fonction de la recherche par nom, téléphone ou email.
   Computed property : filteredContacts()
   Détails : Utiliser la propriété searchQuery pour filtrer les contacts dont le nom, le téléphone ou l’email contient la chaîne de recherche. Utiliser l’id pour identifier chaque contact dans la liste affichée.
   Nom de commit : feat: implement search and filter functionality for contacts
