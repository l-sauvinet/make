# Instructions pour tester le prompt de filtrage de mail

## 1. Objectif du test
L'objectif est de tester un prompt conçu pour analyser le contenu d'un email et suggérer un label parmi une liste prédéfinie. ChatGPT utilisera le prompt pour classer un email donné en fonction de son contenu.

## 2. Structure du prompt

Le prompt est structuré de la manière suivante :


- **FINANCE** : Si l'email fait mention d'avis d'échéance, de banque, d'assurance, de virement, de crédit agricole, de loyer, de CAF, ou d'APL.
- **DIVERTISSEMENT** : Si l'email contient des contenus humoristiques, des recommandations de loisirs, des jeux, des liens vers des vidéos ou événements amusants.
- **PUB** : Si l'email est un message publicitaire, contenant des promotions, des appels à l'action, un ton commercial, ou venant d'une entreprise.
- **SPAM** : Si l'email contient des éléments suspects tels que des fautes d'orthographe, des demandes urgentes de renseignements personnels, des liens ou pièces jointes inhabituels, ou une adresse d'expéditeur douteuse.
- **ECOLE** : Si l'email fait mention d'alternance, d'école, du CIFEP, ou de tout contenu éducatif.
- **PERSONNEL** : Si l'email provient d'un particulier, avec un ton familier ou proche, sans éléments douteux.
- **TRAVAIL** : Si l'email est lié à des tâches professionnelles, des projets, ou des communications avec des collègues ou supérieurs.
- **SOCIAL** : Si l'email est lié à des réseaux sociaux, des invitations à des événements sociaux, ou des communications amicales.
- **NEWSLETTER** : Si l'email provient d'une liste de diffusion avec des articles, actualités, ou mises à jour régulières.
- **FACTURE** : Si l'email contient spécifiquement une facture ou un document de paiement.
- **SUPPORT TECHNIQUE** : Si l'email est en lien avec une demande ou un suivi de support client ou technique.
- **RÉSERVATION** : Si l'email concerne des réservations pour des hôtels, vols, restaurants, ou autres services.
- **RAPPEL** : Si l'email contient un rappel pour un rendez-vous, un événement, ou une action à réaliser.
- **OFFRES D'EMPLOI** : Si l'email contient des offres d'emploi ou des opportunités de carrière.
- **Autre** : Si l'email ne correspond à aucun autre label.

Expéditeur :
{{expediteur(mail)}} 

Objet :
{{objet mail}}

Contenu de l'email : 
{{contenu}}

## 3. Utilisation du prompt avec ChatGPT

1. **Préparer les variables** : 
   - Remplis les champs suivants avec les informations de l'email que tu souhaites tester :
     - `{{expediteur(mail)}}` : Adresse de l'expéditeur.
     - `{{objet mail}}` : Objet de l'email.
     - `{{contenu}}` : Contenu textuel de l'email.

2. **Envoyer le prompt** :
   - Copie le texte du prompt dans ChatGPT.
   - Remplace les variables `{{expediteur(mail)}}`, `{{objet mail}}`, et `{{contenu}}` par les informations spécifiques à l'email que tu veux analyser.
   - Envoie le message pour que ChatGPT puisse analyser l'email.

3. **Interpréter la réponse** :
   - ChatGPT analysera le contenu de l'email selon les critères fournis et suggérera le label le plus approprié.
   - Vérifie si la suggestion correspond bien à la catégorie attendue. Si ce n'est pas le cas, tu peux ajuster le prompt ou fournir plus de détails.

## 4. Exemple de test (a envoyer a chatgpt) 

Analyse le contenu de cet email et suggère un 'label' le plus pertinent parmi la liste suivante : 
- **FINANCE** : Si l'email fait mention d'avis d'échéance, de banque, d'assurance, de virement, de crédit agricole, de loyer, de CAF, ou d'APL.
- **DIVERTISSEMENT** : Si l'email contient des contenus humoristiques, des recommandations de loisirs, des jeux, des liens vers des vidéos ou événements amusants.
- **PUB** : Si l'email est un message publicitaire, contenant des promotions, des appels à l'action, un ton commercial, ou venant d'une entreprise.
- **SPAM** : Si l'email contient des éléments suspects tels que des fautes d'orthographe, des demandes urgentes de renseignements personnels, des liens ou pièces jointes inhabituels, ou une adresse d'expéditeur douteuse.
- **ECOLE** : Si l'email fait mention d'alternance, d'école, du CIFEP, ou de tout contenu éducatif.
- **PERSONNEL** : Si l'email provient d'un particulier, avec un ton familier ou proche, sans éléments douteux.
- **TRAVAIL** : Si l'email est lié à des tâches professionnelles, des projets, ou des communications avec des collègues ou supérieurs.
- **SOCIAL** : Si l'email est lié à des réseaux sociaux, des invitations à des événements sociaux, ou des communications amicales.
- **NEWSLETTER** : Si l'email provient d'une liste de diffusion avec des articles, actualités, ou mises à jour régulières.
- **FACTURE** : Si l'email contient spécifiquement une facture ou un document de paiement.
- **SUPPORT TECHNIQUE** : Si l'email est en lien avec une demande ou un suivi de support client ou technique.
- **RÉSERVATION** : Si l'email concerne des réservations pour des hôtels, vols, restaurants, ou autres services.
- **RAPPEL** : Si l'email contient un rappel pour un rendez-vous, un événement, ou une action à réaliser.
- **OFFRES D'EMPLOI** : Si l'email contient des offres d'emploi ou des opportunités de carrière.
- **Autre** : Si l'email ne correspond à aucun autre label.

Expéditeur :
facturation@service-banque.com

Objet :
Avis d'échéance - Loyer août 2024

Contenu de l'email : 
Bonjour,

Veuillez trouver ci-joint l'avis d'échéance pour le loyer du mois d'août 2024. Le montant est à régler avant le 15 août 2024.

Cordialement,
Service de facturation.

Réponse: **FINANCE**
