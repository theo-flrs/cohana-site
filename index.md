---
layout: default
title: Confidentialité et mentions légales
permalink: /
---
<!-- Fichier généré depuis le dépôt Cohana : ne pas modifier ici. -->

# Confidentialité et mentions légales

Dernière mise à jour : 21 octobre 2026.

Cohana aide les membres d’un foyer de 1 à 12 personnes à organiser leur quotidien
sur iPhone et iPad. Le
responsable du traitement indiqué pour le projet est **Théo Florès** ; contact :
**florstheo@gmail.com**.

## Données et usages

- **Identité iCloud, rôle, nom et couleur de profil** : accéder à son foyer et reconnaître les membres. Partage : Apple pour iCloud ; partenaire pour les informations du foyer.
- **Tâches visibles par tous, budget, décisions, recettes, repas, courses, animaux, entretien et activité** : organiser le quotidien demandé par les membres. Partage : membres acceptés du partage privé du foyer.
- **Profil individuel, favoris, refus de recettes, modèles et tâches privés, préférences de rappel** : personnaliser son expérience. Partage : zone CloudKit privée du membre.
- **Événements des calendriers choisis** : afficher les rendez-vous et préparer les rappels. Partage : lecture sur l’appareil ; aucun envoi au partenaire prévu.
- **Voix dictée dans « Dicter »** : transformer la dictée en tâches et en courses. Partage : aucun ; reconnaissance vocale sur l’appareil uniquement, sans envoi aux serveurs Apple.
- **Chiffres d’un code-barres scanné pour un équipement** : retrouver le nom du produit. Partage : UPCitemdb, Open Products Facts, Open Food Facts, sans compte.
- **Texte tapé dans une saisie de courses ou d’ingrédient** (à partir de trois lettres) : proposer des noms de produits et de catégories, avec leur rayon, leur Nutri-Score et une image. Partage : Open Food Facts, sans compte ; désactivable dans Profil › Sur cet iPhone. Données et images sous licence ODbL et CC BY-SA. Le catalogue de catégories est embarqué dans l’application et ne transmet rien.
- **Préférences d’apparence, modules favoris, calendriers sélectionnés et verrou applicatif** : adapter l’appareil. Partage : stockage local.
- **Aperçu du jour : prénom, prochaines tâches, repas du jour, articles à acheter** : afficher les widgets de l’appareil. Partage : stockage local chiffré, lu par les widgets de Cohana.
- **Sessions de cuisson, courses et défi : titre, étapes, articles et progression** : suivre une session lancée volontairement. Partage : appareil et surfaces système des Live Activities.
- **Titres, corps et échéances des rappels locaux** : rappeler les actions synchronisées. Partage : notifications système sur l’appareil.
- **Fichier JSON exporté volontairement** : obtenir une copie portable. Partage : destinataire choisi dans la feuille de partage iOS.

Les données nécessaires aux fonctions du foyer sont traitées pour fournir le
service demandé. La dictée n’est ni enregistrée ni conservée par Cohana : seul
le texte reconnu est lu, et seules les propositions validées sont ajoutées au
foyer. La reconnaissance vocale se fait sur l’appareil uniquement : quand
l’appareil ne reconnaît pas le français localement, la dictée est indisponible
plutôt que de confier la voix aux serveurs Apple. Le scan d’un code-barres
envoie ses chiffres au service de recherche, sans identifiant de compte, de
foyer ou d’appareil. Comme toute requête Internet, le fournisseur reçoit aussi
l’adresse IP et les données techniques nécessaires à la connexion ; ses règles
d’utilisation et de conservation s’appliquent. Le résultat n’est pas conservé
en cache. Les ingrédients proposés pour un
plat viennent d’une recette du foyer ou du catalogue, sinon du modèle Apple
Intelligence exécuté sur l’appareil : seul le nom du plat lui est transmis, sans
envoi à Cohana. Le même modèle, toujours sur l’appareil, relit le texte dicté
pour corriger la liste proposée. Calendrier et notifications sont facultatifs et
nécessitent les permissions de l’appareil au moment de leur activation. Le client
ne demande pas de mot de passe Cohana, de paiement bancaire, de géolocalisation
précise ou de données de santé. Aucun SDK de publicité, suivi publicitaire ou
analytics n’est installé.

Les titres, étapes et articles des Live Activities sont déclarés sensibles et
retirés de l’accessibilité lorsque le système masque leur contenu privé. Leur
affichage et les aperçus des notifications dépendent des réglages iOS de
l’appareil. Les photos publiques du catalogue sont lues dans CloudKit ; Cohana
ne charge pas les URL d’images externes fournies dans les recettes éditoriales.

## iCloud et partage

Le foyer est dans une zone CloudKit privée de son propriétaire, partagée avec
les autres membres invités. Chaque membre garde une zone personnelle privée. Le
catalogue public contient des recettes éditoriales et photos, sans contenu de
foyer. Le stockage et les services iCloud sont fournis par Apple, selon ses
conditions et [informations de confidentialité](https://www.apple.com/legal/privacy/).

Le partage limite les personnes qui accèdent à la zone ; ses membres en
lecture/écriture peuvent modifier les données du foyer. Le titre du partage est
neutre : il ne reprend pas le nom du foyer, qui n’existe que dans le contenu chiffré. Le contenu des records
du foyer et des zones personnelles est écrit dans le champ `encryptedPayload`,
chiffré par CloudKit via `CKRecord.encryptedValues`, avec des clés du trousseau
iCloud des membres du partage ;
Cohana n’a aucun accès serveur à ce contenu. Les noms techniques des records,
leurs dates, la structure des zones et les photos de recettes (chiffrées au repos par
CloudKit) ne relèvent pas de ce chiffrement. Les miniatures d’articles de courses, elles, sont
dans ce contenu chiffré. Si une personne réinitialise les
données chiffrées de son compte iCloud, le contenu chiffré devient illisible et
ne peut pas être récupéré par Cohana. Voir
[les mécanismes de chiffrement CloudKit](https://developer.apple.com/documentation/cloudkit/encrypting-user-data).

## Conservation sur l’appareil et dans iCloud

Le foyer est conservé en mémoire pendant l’usage et relu depuis iCloud au
lancement. Il n’existe pas de réplique persistée du foyer. Les opérations non
envoyées sont conservées dans une file locale chiffrée, liée au compte et au
foyer, avec une expiration de sept jours. Les widgets lisent un aperçu du jour
chiffré sur l’appareil, effacé chaque nuit, au changement de compte ou de foyer,
et désactivable dans Profil › Sur cet iPhone. Les photos téléchargées et les exports
utilisent des fichiers temporaires purgés selon leur cycle et lors des
changements de contexte.

Les données partagées restent dans iCloud jusqu’à leur suppression par les
actions applicables. Quitter un partage ou effacer l’appareil ne supprime pas
le foyer conservé par le partenaire. L’effacement local et la suppression du
foyer sont deux actions distinctes. Le client n’exécute pas de purge annuelle
automatique de l’Activité ni de purge serveur de calendrier.

Cohana n’exploite aucun serveur et ne fait aucune sauvegarde : le stockage
iCloud, sa durée de conservation, ses sauvegardes et la localisation de ses
serveurs relèvent d’Apple. Pour effacer ses données : le propriétaire supprime
le foyer et le partenaire le quitte depuis Profil ; les données personnelles
restantes s’effacent dans Réglages iOS › votre nom › iCloud › Gérer le stockage
du compte › Cohana. Lors d’un scan de code-barres, les services contactés
reçoivent les chiffres du code, l’adresse IP de l’appareil, l’horodatage et les
en-têtes HTTP techniques : UPCitemdb, service situé aux États-Unis, puis Open
Products Facts et Open Food Facts si la recherche n’aboutit pas. Aucun compte ni
identifiant n’est envoyé.

Pendant la saisie d’un article de courses ou d’un ingrédient, le texte tapé à
partir de trois lettres part vers Open Food Facts pour proposer des noms de produits
et de catégories, sans identifiant de compte ni du foyer. Le catalogue de catégories est
embarqué dans l’application : le consulter n’envoie rien. Les images de produits proposées
sont téléchargées depuis Open Food Facts ; leur adresse révèle, comme le texte tapé, le
produit demandé, et l’adresse IP de l’appareil est transmise. Les miniatures restent en
mémoire le temps de la saisie. Données et images : Open Food Facts (ODbL ; images CC BY-SA).
Ce réglage s’active ou se coupe dans Profil › Sur cet iPhone ; désactivé, aucune
requête n’est envoyée.

## Vos choix et vos droits

Le membre peut modifier les informations accessibles dans Profil, choisir ses
calendriers, retirer les permissions dans Réglages et désactiver les rappels.
Le verrou applicatif est facultatif : il se règle dans Profil › Sur cet iPhone, reste
sur l’appareil et demande Face ID, Touch ID ou le code de l’appareil.
L’export JSON produit les données partagées chargées et les données privées du
membre qui le demande ; il ne copie pas les données privées du partenaire et ne
constitue pas une sauvegarde restaurable.

Pour demander accès, rectification, effacement, limitation ou portabilité,
écrire à **florstheo@gmail.com**. Une demande de retrait d’un partage, de
suppression du foyer ou d’effacement de données privées doit préciser le
périmètre concerné. Une réclamation peut être adressée à la [CNIL](https://www.cnil.fr/).

## Mentions légales

- **Éditeur de l’application** : Théo Florès, personne physique, sans activité commerciale à ce jour. Contact : florstheo@gmail.com.
- **Directeur de la publication** : Théo Florès.
- **Hébergement des données du foyer** : Apple (iCloud / CloudKit), dans le compte iCloud de chaque membre. Apple Distribution International Ltd., Hollyhill Industrial Estate, Hollyhill, Cork, Irlande.
- **Hébergement de cette page** : GitHub, Inc., 88 Colin P Kelly Jr St, San Francisco, CA 94107, États-Unis (GitHub Pages).

## Crédits et licences

- **Données alimentaires** (suggestions d’articles, catalogue de catégories embarqué) : [Open Food Facts](https://world.openfoodfacts.org/), licence [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/). © Open Food Facts contributors.
- **Images de produits** proposées dans les suggestions : [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/). © Open Food Facts contributors.
- **Icônes** : [Lucide](https://lucide.dev/), licence ISC.
- **Polices** DM Sans et Outfit : SIL Open Font License 1.1.

Cette mention ne vaut pas validation juridique : une relecture reste à faire avant publication.

## Assistance

Pour toute question, tout problème ou toute demande (accès, rectification,
effacement), écrire à **florstheo@gmail.com**. Une réponse est donnée dans les
meilleurs délais.

Cette page sert aussi d’URL d’assistance de l’application. Son adresse publique
est https://theo-flrs.github.io/cohana-site/.
