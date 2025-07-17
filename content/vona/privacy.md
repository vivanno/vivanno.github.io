+++
title = "Vona - Politique de Confidentialité"
date = "2024-07-17"
draft = false
+++

## Engagement de Confidentialité

Vona s'engage à protéger intégralement la vie privée de ses utilisateurs. Cette politique de confidentialité détaille nos pratiques en matière de collecte, utilisation et protection des données.

## Principe Fondamental : Zéro Collecte de Données

### Aucune Collecte de Données Personnelles
- **Aucune donnée de navigation** n'est collectée, stockée ou transmise
- **Aucun historique de navigation** n'est conservé de manière permanente
- **Aucune donnée de localisation** n'est collectée
- **Aucun identifiant unique** n'est généré ou stocké
- **Aucune donnée analytique** n'est collectée

### Aucune Transmission de Données
- **Aucune connexion à des serveurs externes** pour le pistage ou l'analyse
- **Aucune télémétrie** n'est envoyée au développeur ou à des tiers
- **Aucun partage de données** avec des partenaires commerciaux
- **Aucune intégration** avec des services de publicité ou d'analyse

## Fonctionnement Technique de la Confidentialité

### Effacement Automatique des Données
- **Cookies** : Supprimés automatiquement après chaque navigation
- **LocalStorage et SessionStorage** : Vidés automatiquement
- **Cache de navigation** : Nettoyé de manière continue
- **Historique** : Conservé uniquement en mémoire, supprimé à la fermeture de l'app

### Stockage Local Sécurisé
- **Paramètres utilisateur uniquement** : Seuls les paramètres de configuration sont stockés
- **Chiffrement local** : Utilisation de `react-native-encrypted-storage` pour un stockage chiffré
- **Aucune identification** : Les paramètres ne contiennent aucune information identificatrice
- **Contrôle utilisateur** : L'utilisateur peut réinitialiser tous les paramètres à tout moment

### Protection contre le Pistage
- **Rotation des agents utilisateur** : 22 agents utilisateur iOS différents rotent automatiquement
- **Blocage des popups de consentement** : Protection contre les mécanismes de pistage
- **Mode furtif permanent** : Aucune trace de navigation n'est laissée

## Données Stockées Localement

### Paramètres de Configuration (Chiffrés)
Les seules données stockées localement sont :
- Préférences de moteur de recherche
- Paramètres d'interface utilisateur (position des icônes, langue)
- Paramètres de confidentialité (activation/désactivation de certaines fonctionnalités)

### Aucune Donnée de Navigation
- **Aucun site web visité** n'est enregistré
- **Aucune requête de recherche** n'est conservée
- **Aucun contenu de page** n'est mis en cache de manière permanente
- **Aucune donnée de formulaire** n'est sauvegardée

## Sécurité et Protection

### Chiffrement
- **Algorithmes standard** : Utilisation uniquement d'algorithmes de chiffrement approuvés (TLS/SSL, chiffrement système iOS)
- **Stockage local chiffré** : Tous les paramètres sont chiffrés via les API sécurisées d'iOS
- **Pas de chiffrement personnalisé** : Aucun algorithme propriétaire ou non-standard

### Protection des Communications
- **HTTPS obligatoire** : Encouragement de la navigation sur des sites sécurisés
- **Pas d'interception** : Aucune analyse ou modification du trafic réseau
- **Connexions directes** : Communication directe entre l'utilisateur et les sites web visités

## Transparence et Contrôle Utilisateur

### Code Source et Architecture
- **Architecture transparente** : Code organisé de manière claire et documentée
- **Aucune obfuscation** : Fonctionnalités clairement identifiables
- **Documentation complète** : Toutes les fonctionnalités sont documentées

### Contrôle Utilisateur
- **Paramètres accessibles** : Tous les paramètres de confidentialité sont configurables
- **Réinitialisation complète** : Possibilité de supprimer toutes les données stockées
- **Transparence des fonctionnalités** : Chaque fonctionnalité peut être activée/désactivée

## Conformité Réglementaire

### RGPD (Règlement Général sur la Protection des Données)
- **Minimisation des données** : Aucune donnée personnelle collectée
- **Consentement** : Pas de collecte de données, donc pas de consentement requis
- **Droit à l'effacement** : Données automatiquement supprimées
- **Portabilité** : Aucune donnée à exporter

### CCPA (California Consumer Privacy Act)
- **Aucune vente de données** : Aucune donnée à vendre
- **Aucun partage** : Aucune donnée partagée avec des tiers
- **Transparence totale** : Politique de confidentialité claire et accessible

### Autres Réglementations
- **Conformité internationale** : Respect des lois de protection des données dans tous les territoires
- **Aucune géolocalisation** : Pas de restriction géographique des données car aucune collecte

## Modifications de la Politique

### Notification des Changements
- **Versions documentées** : Toute modification sera documentée
- **Engagement maintenu** : Le principe de zéro collecte sera maintenu
- **Transparence** : Les utilisateurs seront informés de tout changement significatif

## Contact et Questions

### Support
Pour toute question concernant cette politique de confidentialité :
- Les questions peuvent être adressées via les canaux de support de l'App Store
- Cette politique est disponible dans l'application et peut être consultée à tout moment

### Audit et Vérification
- **Code vérifiable** : L'architecture du code permet la vérification des pratiques de confidentialité
- **Aucune connexion externe** : Facilite l'audit de l'absence de transmission de données

## Engagement à Long Terme

Vona s'engage à maintenir ces standards de confidentialité élevés dans toutes les versions futures de l'application. Notre mission est de fournir une navigation web véritablement privée, sans compromis sur la protection des données utilisateur.

---

**Dernière mise à jour** : 17 juillet 2025
**Version de l'application** : 1.0
**Politique applicable** : Toutes les versions de Vona 