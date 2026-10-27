# Père Noël secret

Petite appli web pour tirer au sort le Père Noël secret, depuis un téléphone (iPhone ou Android) ou un ordinateur.

- Participants, couples qui ne peuvent pas se tirer, échanges réciproques interdits si on veut.
- Chacun reçoit un **lien secret** (par SMS, WhatsApp…) qui lui révèle à qui il offre un cadeau. L'organisateur ne voit jamais les noms tirés.
- Mode **« passer le téléphone »** pour un tirage en direct.
- Une personne qui ne participe pas peut recevoir la liste complète, au cas où.

Rien n'est envoyé à un serveur : la liste reste dans le téléphone de l'organisateur, et le contenu des liens est placé après le `#`, que le navigateur ne transmet pas.

## Deux modes

- **Simple** : l'organisateur saisit les prénoms. Le nom tiré est seulement brouillé dans le lien, pour éviter de le lire par accident.
- **Anti-triche** : chacun s'inscrit depuis son téléphone, qui crée une clé secrète (ECDH P-256, non exportable, gardée dans le navigateur). L'organisateur ne reçoit que la clé publique et chiffre chaque mission pour son destinataire (AES-GCM). Il ne garde aucun résultat en clair et ne peut lire aucune mission, pas même en refaisant le tirage. Une mission ne s'ouvre que sur le téléphone et dans le navigateur de l'inscription.
  Chaque mission est aussi signée (ECDSA P-256) par une clé d'organisateur dont la partie publique voyage dans l'invitation : une mission fabriquée par quelqu'un d'autre est refusée.

## Installer sur le téléphone

Ouvrir le lien de l'appli, puis :

- **iPhone (Safari)** : bouton Partager, puis « Sur l'écran d'accueil ».
- **Android (Chrome)** : menu ⋮, puis « Ajouter à l'écran d'accueil » ou « Installer l'application ».

## Mise en ligne

Fichiers statiques, servis tels quels par GitHub Pages (Settings > Pages > Deploy from a branch > `main` / racine).
