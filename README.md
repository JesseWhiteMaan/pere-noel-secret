# Père Noël secret

Petite appli web pour tirer au sort le Père Noël secret, depuis un téléphone (iPhone ou Android) ou un ordinateur.

- Participants, couples qui ne peuvent pas se tirer, échanges réciproques interdits si on veut.
- Chacun reçoit un **lien secret** (par SMS, WhatsApp…) qui lui révèle à qui il offre un cadeau. L'organisateur ne voit jamais les noms tirés.
- Mode **« passer le téléphone »** pour un tirage en direct.
- Une personne qui ne participe pas peut recevoir la liste complète, au cas où.

Rien n'est envoyé à un serveur : la liste reste dans le téléphone de l'organisateur, et le nom tiré est brouillé dans la partie du lien après le `#`, que le navigateur ne transmet pas. Ce brouillage évite de lire un nom par accident, ce n'est pas un chiffrement.

## Installer sur le téléphone

Ouvrir le lien de l'appli, puis :

- **iPhone (Safari)** : bouton Partager, puis « Sur l'écran d'accueil ».
- **Android (Chrome)** : menu ⋮, puis « Ajouter à l'écran d'accueil » ou « Installer l'application ».

## Mise en ligne

Fichiers statiques, servis tels quels par GitHub Pages (Settings > Pages > Deploy from a branch > `main` / racine).
