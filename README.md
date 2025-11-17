> **Guide complet pour installer et configurer Stremio sur tous vos appareils**
> 
> Dernière mise à jour : Novembre 2024

---

## 📖 Table des matières

1. [Introduction](#introduction)
2. [Qu'est-ce que Stremio ?](#quest-ce-que-stremio)
3. [Prérequis](#prérequis)
4. [Création d'un compte Stremio](#création-dun-compte-stremio)
5. [Installation selon votre appareil](#installation-selon-votre-appareil)
   - [Windows](#installation-sur-windows)
   - [Android TV / Box TV (Xiaomi Mi Box, etc.)](#installation-sur-android-tv--box-tv)
   - [Smart TV Samsung/LG](#installation-sur-smart-tv)
   - [Smartphone Android](#installation-sur-smartphone-android)
6. [Real-Debrid : Pourquoi et comment ?](#real-debrid--pourquoi-et-comment)
7. [Configuration des addons essentiels](#configuration-des-addons-essentiels)
8. [Configuration des sous-titres](#configuration-des-sous-titres)
9. [Conseils et astuces](#conseils-et-astuces)
10. [Dépannage](#dépannage)

---

## Introduction

Ce guide vous permettra d'installer et de configurer Stremio de A à Z, quel que soit votre appareil. Stremio est une solution légale qui devient extrêmement puissante lorsqu'elle est couplée à un service debrid comme Real-Debrid.

**💡 Recommandation importante :** Effectuez la configuration initiale sur un ordinateur ou un appareil Android. Une fois configuré, vous pourrez simplement vous connecter sur n'importe quel autre appareil avec le même compte, et toute votre configuration sera automatiquement synchronisée.

---

## Qu'est-ce que Stremio ?

Stremio est une application de streaming multimédia qui agrège du contenu provenant de différentes sources via un système d'extensions (addons). C'est une plateforme légale en elle-même, mais comme tout lecteur multimédia, son utilisation dépend du contenu que vous y diffusez.

**Avantages principaux :**
- Interface moderne et intuitive, similaire à Netflix
- Synchronisation entre tous vos appareils
- Suivi automatique de votre progression
- Gestion de bibliothèque personnalisée
- Compatible avec une large gamme d'appareils

---

## Prérequis

Avant de commencer, assurez-vous d'avoir :

- ✅ Une connexion Internet stable (recommandé : 10 Mbps minimum, 50+ Mbps pour du 4K)
- ✅ Un appareil compatible (voir la liste ci-dessous)
- ✅ Une adresse email pour créer un compte Stremio
- ✅ (Optionnel mais recommandé) Un abonnement Real-Debrid

**Appareils compatibles :**
- PC Windows / Mac / Linux
- Android (smartphone et tablette)
- Android TV / Box TV (Mi Box, Nvidia Shield, Fire TV, etc.)
- Smart TV Samsung (2019+)
- Smart TV LG (2020+)
- iOS / iPadOS (version limitée)
- Et bien d'autres...

---

## Création d'un compte Stremio

Votre compte Stremio vous permet de synchroniser votre configuration et votre progression sur tous vos appareils.

### Étapes :

1. Rendez-vous sur [stremio.com](https://stremio.com/)
2. Cliquez sur **"Sign Up"** (S'inscrire)
3. Vous avez deux options :
   - **Inscription par email :** Entrez votre email et choisissez un mot de passe
   - **Connexion via Facebook :** Utilisez votre compte Facebook
4. Validez votre email si vous avez choisi l'inscription par email
5. Gardez vos identifiants en lieu sûr !

---

## Installation selon votre appareil

### Installation sur Windows

#### Téléchargement

1. Allez sur [stremio.com/downloads](https://www.stremio.com/downloads)
2. Téléchargez la version Windows (fichier .exe)
3. Lancez l'installateur téléchargé
4. Suivez les instructions à l'écran
5. Une fois installé, lancez Stremio
6. Connectez-vous avec votre compte créé précédemment

#### Configuration recommandée sur Windows

1. Ouvrez Stremio
2. Allez dans **Paramètres** (icône d'engrenage)
3. Activez **"Hardware Accelerated Decoding"** (Décodage accéléré matériel)
4. Si vous prévoyez d'utiliser des torrents :
   - Réglez **"Torrent Profile"** sur **"Ultra Fast"**
   - Réglez **"Cache Size"** sur **10GB** ou **Illimité**

---

### Installation sur Android TV / Box TV

**Cette section est parfaite pour votre Xiaomi Mi TV Box 3e gen !**

#### Méthode 1 : Via le Google Play Store (recommandée si disponible)

1. Sur votre TV/Box, ouvrez le **Google Play Store**
2. Recherchez **"Stremio"**
3. Cliquez sur **"Installer"**
4. Une fois installé, lancez l'application
5. Connectez-vous avec votre compte Stremio

> **Note :** Stremio n'est pas disponible dans toutes les régions sur le Play Store. Si vous ne le trouvez pas, passez à la méthode 2.

#### Méthode 2 : Installation manuelle (Sideload)

Si Stremio n'est pas disponible sur le Play Store dans votre région :

**Option A : Avec Downloader (plus simple)**

1. Installez l'application **"Downloader"** depuis le Play Store
2. Dans les paramètres de votre Android TV :
   - Allez dans **Paramètres** → **Sécurité & Restrictions**
   - Activez **"Sources inconnues"** pour l'application Downloader
3. Ouvrez l'application Downloader
4. Entrez l'URL : `https://stremio.com/downloads`
5. Téléchargez le fichier **APK ARM64** (pour la plupart des box TV)
6. Une fois téléchargé, cliquez sur **"Installer"**
7. Lancez Stremio et connectez-vous

**Option B : Avec Send Files to TV**

1. Sur votre smartphone, téléchargez **"Send Files to TV"**
2. Sur votre TV, installez également **"Send Files to TV"**
3. Sur votre smartphone, téléchargez l'APK Stremio depuis [stremio.com/downloads](https://www.stremio.com/downloads) (choisissez ARM64)
4. Utilisez "Send Files to TV" pour transférer le fichier sur votre TV
5. Sur votre TV, installez le fichier APK reçu
6. Lancez Stremio et connectez-vous

#### Configuration recommandée sur Android TV

1. Ouvrez Stremio sur votre TV
2. Allez dans **Paramètres**
3. Section **"Streaming Server"** :
   - **Cache Size** : Réglez sur **10GB**
   - **Torrent Profile** : Réglez sur **"Ultra Fast"** ou **"Fast"** selon votre connexion
4. Section **"Performance & Stability"** :
   - Activez **"Run as foreground service"** (Cela évite que Stremio se ferme en arrière-plan)

---

### Installation sur Smart TV

#### Samsung TV (2019 et plus récent)

1. Ouvrez l'**App Store** Samsung sur votre TV
2. Recherchez **"Stremio"**
3. Cliquez sur **"Installer"**
4. Lancez l'application
5. Connectez-vous avec votre compte

#### LG TV (2020 et plus récent)

1. Ouvrez le **LG Content Store**
2. Si Stremio n'apparaît pas dans la recherche, allez dans la section **"Entertainment"**
3. Vous devriez y trouver Stremio
4. Installez l'application
5. Lancez-la et connectez-vous

---

### Installation sur Smartphone Android

#### Via le Play Store

1. Ouvrez le **Google Play Store**
2. Recherchez **"Stremio"**
3. Installez l'application
4. Lancez Stremio
5. Connectez-vous

#### Installation manuelle (si non disponible)

1. Téléchargez l'APK depuis [stremio.com/downloads](https://www.stremio.com/downloads)
2. Choisissez la version **ARM64** (pour la plupart des smartphones récents)
3. Dans les paramètres de votre téléphone :
   - Allez dans **Sécurité**
   - Autorisez l'installation depuis des **sources inconnues**
4. Ouvrez le fichier APK téléchargé
5. Installez-le
6. Lancez Stremio et connectez-vous

---

## Real-Debrid : Pourquoi et comment ?

### Qu'est-ce que Real-Debrid ?

Real-Debrid est un service de **debrid** (ou de "dérestriction"). C'est un service qui télécharge des torrents sur ses serveurs ultra-rapides, puis vous permet de les streamer directement en HTTPS, comme sur Netflix.

### Pourquoi utiliser Real-Debrid avec Stremio ?

#### ✅ Avantages majeurs :

1. **Streaming sans buffering :** 
   - Real-Debrid dispose de serveurs très rapides (jusqu'à 1 Gbps)
   - Vous n'êtes plus dépendant du nombre de seeders d'un torrent
   - Vous pouvez regarder du contenu 4K, HDR, Dolby Vision sans aucun ralentissement

2. **Sécurité et confidentialité :**
   - Vous ne téléchargez plus directement des torrents
   - Tout passe par HTTPS (connexion sécurisée)
   - Votre FAI ne peut pas voir que vous utilisez des torrents
   - **Pas besoin de VPN** avec Real-Debrid

3. **Accès à plus de contenu :**
   - Accès à des torrents qui n'auraient plus assez de seeders
   - Énorme cache de torrents déjà téléchargés (instantané)
   - Qualité maximale disponible (remux, 4K, etc.)

4. **Polyvalence :**
   - Utilisable aussi pour télécharger des fichiers depuis des hébergeurs
   - Fonctionne avec d'autres applications (pas que Stremio)

#### ❌ Inconvénients :

1. **Coût :** Service payant (environ 16€ pour 6 mois, soit ~2,60€/mois)
2. **Restriction IP :** Un seul appareil/connexion à la fois par compte
3. **Pas de contribution :** Vous ne participez pas au partage des torrents (pas de seed)

### Est-ce que Real-Debrid est nécessaire ?

**Non, mais c'est fortement recommandé.** Voici quand vous en avez vraiment besoin :

- ✅ Si vous voulez regarder du contenu en haute qualité (4K, remux, etc.)
- ✅ Si vous voulez du streaming sans buffering
- ✅ Si votre FAI bloque ou limite les torrents
- ✅ Si vous ne voulez pas utiliser de VPN
- ✅ Si vous regardez du contenu ancien ou peu populaire (peu de seeders)

**Vous pouvez vous en passer si :**
- ❌ Vous êtes dans un pays où le torrenting n'est pas problématique
- ❌ Vous regardez uniquement du contenu très populaire et récent
- ❌ Vous acceptez de potentiels problèmes de buffering
- ❌ Votre connexion Internet est lente (Real-Debrid ne l'améliorera pas)

### Comment s'inscrire à Real-Debrid ?

1. Rendez-vous sur [real-debrid.com](https://real-debrid.com/)
2. Cliquez sur **"Sign Up"**
3. Créez votre compte
4. Une fois connecté, allez sur la page **"Premium Offers"**
5. Choisissez une formule :
   - **15 jours :** ~3€ (pour tester)
   - **30 jours :** ~4€
   - **90 jours :** ~9€
   - **180 jours :** ~16€ (meilleur rapport qualité/prix)
6. Effectuez le paiement (carte bancaire, PayPal, crypto-monnaies)
7. Votre compte est maintenant Premium !

### Récupérer votre clé API Real-Debrid

Vous aurez besoin de cette clé pour configurer les addons Stremio :

1. Connectez-vous sur [real-debrid.com](https://real-debrid.com/)
2. Allez sur votre profil (cliquez sur votre nom en haut à droite)
3. Descendez jusqu'à la section **"API Key"**
4. Cliquez sur le bouton pour afficher votre clé
5. Copiez cette clé (vous en aurez besoin plus tard)

> **⚠️ Attention :** Ne partagez jamais votre clé API avec quelqu'un d'autre !

---

## Configuration des addons essentiels

Les addons sont le cœur de Stremio. Ils fournissent les liens de streaming pour les films et séries.

### Supprimer les addons pré-installés inutiles

Par défaut, Stremio installe quelques addons que vous n'utiliserez probablement pas :

1. Ouvrez Stremio
2. Cliquez sur l'icône **puzzle** (addons) dans le menu de gauche
3. Désinstallez ces addons :
   - **WatchHub** (recommandations de services de streaming payants)
   - **YouTube** (si vous ne voulez pas de vidéos YouTube)
   - **Public Domain Movies** (vieux films des années 1900)

### Installer Torrentio (addon principal)

**Torrentio est l'addon le plus populaire et le plus important.** Il recherche des liens torrents sur plusieurs trackers publics.

#### Configuration de Torrentio

1. Sur votre ordinateur, allez sur [torrentio.strem.fun/configure](https://torrentio.strem.fun/configure)

2. **Providers (Fournisseurs) :**
   - Laissez tous les fournisseurs cochés pour avoir le maximum de résultats
   - Vous pouvez décocher les fournisseurs étrangers si vous voulez éviter le contenu en langue étrangère

3. **Sorting (Tri) :**
   - **Avec Real-Debrid :** Choisissez **"By quality then size"** (Par qualité puis taille)
   - **Sans Real-Debrid :** Choisissez **"By quality then seeders"** (Par qualité puis seeders)

4. **Priority foreign language (Langue étrangère prioritaire) :**
   - Laissez vide si vous voulez du contenu en anglais par défaut
   - Sélectionnez "French" si vous voulez prioriser le contenu en français

5. **Exclude qualities (Exclure des qualités) :**
   - Cochez **"Screener"** et **"CAM"** (qualité très mauvaise)
   - Si votre connexion est lente, cochez aussi **"4K"**

6. **Max results per quality :**
   - Laissez vide pour voir tous les résultats
   - Ou mettez "5" pour limiter et accélérer le chargement

7. **Video size limit :**
   - Laissez vide si votre connexion le permet
   - Sinon, mettez une limite (ex: 40 pour 40 GB max)

8. **Debrid provider (si vous en avez un) :**
   - Sélectionnez **"Real-Debrid"**
   
9. **API Key :**
   - Cliquez sur le lien pour être redirigé vers Real-Debrid
   - Copiez votre clé API
   - Collez-la dans le champ

10. **Debrid options :**
    - **Don't show download to debrid :** Laissez **décoché**
      - Ces liens ne sont pas en cache mais peuvent être ajoutés
      - Avec Real-Debrid, certains liens "non cachés" fonctionnent quand même
    - **Don't show debrid catalog :** Cochez si vous voulez cacher le catalogue de vos téléchargements

11. Cliquez sur **"Install"**
    - Stremio s'ouvre automatiquement
    - Cliquez sur **"Install"** à nouveau pour confirmer

### Installer des addons de catalogues

Les catalogues vous permettent d'avoir une belle page d'accueil avec du contenu à découvrir.

#### TMDB Addon (recommandé)

TMDB est meilleur que le catalogue par défaut de Stremio.

1. Allez sur [94c8cb09f068-tmdb-addon.baby-beamup.club](https://94c8cb09f068-tmdb-addon.baby-beamup.club/)
2. Sélectionnez votre langue (Français ou English)
3. Cliquez sur **"Install"** dans le menu de gauche
4. Confirmez l'installation dans Stremio

#### IMDB Catalogs (optionnel)

1. Allez sur [1fe84bc728af-imdb-catalogs.baby-beamup.club](https://1fe84bc728af-imdb-catalogs.baby-beamup.club/)
2. Cliquez sur **"Install"**
3. Confirmez dans Stremio

---

## Configuration des sous-titres

Les sous-titres sont essentiels, surtout pour le contenu en anglais !

### Installer OpenSubtitles

**OpenSubtitles** est le meilleur addon de sous-titres.

1. Dans Stremio, allez dans **Addons**
2. Recherchez **"OpenSubtitles"**
3. Installez **"OpenSubtitles v3"**

### Configurer OpenSubtitles Pro (pour plus d'options)

Si vous voulez plus de contrôle :

1. Allez sur [opensubtitles-v3.strem.io](https://opensubtitles-v3.strem.io/)
2. Sélectionnez vos langues préférées :
   - Ajoutez **French**
   - Ajoutez **English** (beaucoup de contenu)
3. Options recommandées :
   - **From :** Sélectionnez "All" ou "Trusted"
   - **Include AI Translated :** Cochez si vous voulez des sous-titres traduits par IA
   - **MovieHash + Auto Adjustment :** Cochez (synchronise mieux les sous-titres)
4. Cliquez sur **"Install"**

### Activer les sous-titres dans Stremio

1. Lancez un film ou une série
2. Cliquez sur l'icône de sous-titres (CC)
3. Sélectionnez la langue voulue
4. Les sous-titres s'affichent !

---

## Conseils et astuces

### Optimiser votre expérience sur Android TV / Mi Box

1. **Activez le service en premier plan :**
   - Paramètres → Performance & Stability
   - Cochez "Run as foreground service"
   - Cela évite que Stremio se ferme

2. **Utilisez une télécommande avec navigation facile :**
   - L'interface de Stremio fonctionne bien avec une télécommande classique
   - Vous pouvez aussi utiliser l'application mobile Stremio comme télécommande

3. **Configurez le cache :**
   - 10GB minimum recommandé
   - Plus de cache = moins de buffering

### Accélérer le chargement des résultats

1. **Limitez le nombre de résultats par addon :**
   - Dans la configuration de Torrentio, réglez "Max results" à 5-10

2. **Installez un seul addon principal :**
   - Trop d'addons ralentissent le chargement
   - Torrentio seul suffit la plupart du temps

3. **Désactivez les catalogues inutiles :**
   - Moins de catalogues = interface plus rapide

### Utiliser Stremio sur plusieurs appareils

Votre compte Stremio synchronise :
- ✅ Vos addons installés et leur configuration
- ✅ Votre bibliothèque (films/séries ajoutés)
- ✅ Votre progression de visionnage
- ✅ Vos paramètres

**Synchronisation automatique :** Connectez-vous simplement avec le même compte sur chaque appareil !

---

## Dépannage

### Problème : Stremio plante pendant la lecture

**Solution :**
1. Activez le décodage matériel accéléré :
   - Paramètres → Hardware Accelerated Decoding → ON
2. Baissez la qualité vidéo (choisissez 1080p au lieu de 4K)

### Problème : Aucun résultat ne s'affiche

**Solutions :**
1. Vérifiez que vous avez bien installé Torrentio
2. Vérifiez votre connexion Internet
3. Réinstallez l'addon Torrentio
4. Sur Android TV : Redémarrez l'application

### Problème : Buffering constant

**Solutions :**
1. Vérifiez votre vitesse de connexion Internet
   - 4K nécessite au moins 50 Mbps
   - 1080p nécessite au moins 10 Mbps
2. Choisissez des fichiers plus petits (moins de qualité)
3. Augmentez la taille du cache dans les paramètres
4. Si vous avez Real-Debrid, le problème vient probablement de votre connexion

### Problème : Erreur "Infringing file" avec Real-Debrid

Cela signifie que le fichier est bloqué par Real-Debrid (restrictions légales).

**Solution :**
- Essayez un autre lien
- Ce problème arrive surtout avec du contenu français ou certains hébergeurs

### Problème : L'application ne s'installe pas sur Android TV

**Solution :**
1. Vérifiez que vous avez activé les sources inconnues
2. Téléchargez la bonne version d'APK (ARM64 pour la Mi Box)
3. Essayez une autre méthode d'installation (Downloader vs Send Files)

### Problème : Les sous-titres ne se chargent pas

**Solutions :**
1. Vérifiez que vous avez installé un addon de sous-titres (OpenSubtitles)
2. Essayez un autre fichier (certains n'ont pas de sous-titres)
3. Réinstallez l'addon OpenSubtitles

### Problème : L'addon Torrentio ne trouve rien

**Solutions :**
1. Vérifiez votre configuration Torrentio
2. Assurez-vous que vous n'avez pas exclu trop de qualités
3. Si vous utilisez Real-Debrid, vérifiez que votre clé API est correcte :
   - Allez sur real-debrid.com
   - Vérifiez que votre abonnement est actif
   - Régénérez une nouvelle clé API si besoin

---

## Pour aller plus loin

### Addons supplémentaires recommandés

- **Comet :** Alternative à Torrentio (backup)
- **MediaFusion :** TV en direct et sports
- **Anime Kitsu :** Catalogues d'animes

### Services Debrid alternatifs

Si Real-Debrid ne vous convient pas, vous pouvez essayer :
- **Premiumize :** Plus cher mais très fiable
- **AllDebrid :** Moins cher mais moins performant
- **TorBox :** Nouveau service prometteur

### Ressources utiles

- [Guide officiel Stremio](https://www.stremio.com/help)
- [Reddit r/StremioAddons](https://www.reddit.com/r/StremioAddons/)
- [Liste complète des addons](https://stremio-addons.net/)

---

## Conclusion

Vous avez maintenant une configuration complète de Stremio ! Avec Real-Debrid, vous disposez d'une des meilleures solutions de streaming disponibles, avec :

- 🎬 Accès à un catalogue quasi-illimité de films et séries
- 🚀 Streaming en haute qualité sans buffering
- 📱 Synchronisation entre tous vos appareils
- 🔒 Connexion sécurisée (avec Real-Debrid)
- 💰 Coût très faible comparé aux abonnements multiples

**Profitez-en bien et bon visionnage ! 🍿**

---

## Questions fréquentes (FAQ)

**Q : Est-ce légal ?**
R : Stremio en lui-même est légal. L'utilisation que vous en faites dépend du contenu que vous streamez. Real-Debrid est également un service légal.

**Q : Ai-je besoin d'un VPN ?**
R : Non, si vous utilisez Real-Debrid. Oui, si vous utilisez des torrents directement sans service debrid.

**Q : Combien coûte Real-Debrid ?**
R : Environ 16€ pour 6 mois, soit environ 2,60€ par mois. C'est très abordable pour le service fourni.

**Q : Puis-je partager mon compte Stremio ?**
R : Vous pouvez utiliser votre compte sur plusieurs appareils, mais Real-Debrid n'autorise qu'un seul appareil/IP à la fois.

**Q : Ça fonctionne vraiment bien sur une Mi Box ?**
R : Oui ! La Mi Box 3e gen gère très bien Stremio. Assurez-vous simplement d'avoir une bonne connexion Internet.

**Q : Où trouver du contenu en français ?**
R : Configurez Torrentio avec "French" en langue prioritaire. Vous pouvez aussi installer des addons spécialisés français comme ceux de StremioFR.

---

**Guide réalisé avec ❤️ pour la communauté**
