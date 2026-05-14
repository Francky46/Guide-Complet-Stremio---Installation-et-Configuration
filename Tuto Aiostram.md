# Tuto Stremio — AIOStreams + Real-Debrid + TorBox

> **Contexte** : Depuis le 10 mai 2026, Real-Debrid bloque une large partie des torrents cachés (WEB-DL, WEBRip, AMZN, NF, YTS, RARBG...). Ce tuto explique comment patcher sa config Stremio avec AIOStreams et TorBox pour contourner le problème.

---

## C'est quoi le problème ?

Real-Debrid a commencé à retourner des erreurs **"File was removed from debrid service due to copyright infringement"** sur une grande partie des streams. Ce n'est **pas** un ban de compte, et RD n'est **pas** en panne. C'est un filtre par mots-clés sur les noms de fichiers. Ton abonnement fonctionne toujours.

---

## La solution : AIOStreams + TorBox en complément de RD

**AIOStreams** est un addon Stremio qui agrège plusieurs scrapers (Comet, MediaFusion...) en une seule liste unifiée, filtrée et triée automatiquement.  
**TorBox** est un service debrid alternatif à RD, sans filtre keyword pour l'instant, qui sert de fallback quand RD bloque.

---

## Étape 1 — S'abonner à TorBox

1. Va sur [torbox.app](https://torbox.app)
2. Crée un compte
3. Souscris au plan **Essential** (~3$/mois ou ~18$/an)
4. Va dans **Settings** → copie ta **clé API**

---

## Étape 2 — Choisir une instance AIOStreams

Il existe plusieurs instances publiques gratuites. Les plus recommandées :

- **Midnight's instance** — hébergée par le TorBox community manager
- **Viren070's instance** — hébergée par le développeur (nightly)

> ⚠️ Évite l'instance ElfHosted pour un usage public gratuit — Torrentio n'y fonctionne pas.
> J'ai personnellement choisi l'instance du développeur : [https://aiostreams.viren070.me](https://aiostreams.viren070.me)

Consulte la liste complète et le statut en temps réel sur : [status.dinsden.top](https://status.dinsden.top)

---

## Étape 3 — Configurer les services debrid

Dans l'onglet **Services** :

1. Clique sur la roue dentée à côté de **TorBox** → entre ta clé API (disponible sur [https://torbox.app/settings?section=account](https://torbox.app/settings?section=account)
2. Clique sur la roue dentée à côté de **Real-Debrid** → entre ta clé API (disponible sur [real-debrid.com/apitoken](https://real-debrid.com/apitoken))
3. **Ordre de priorité** : mets TorBox en premier (pas de filtre), RD en second

---

## Étape 4 — Installer les scrapers (onglet Addons > Marketplace)

### Comet
| Paramètre | Valeur |
|---|---|
| Timeout | `15000` ms |
| Resources | `Stream` uniquement |
| URL | `https://comet.feels.legal` |
| Include P2P | **OFF** |
| Remove Trash | **ON** |
| Search Debrid Library | OFF |
| Use Multiple Instances | OFF |
| Services | vide |
| Media Types | vide |

### MediaFusion
| Paramètre | Valeur |
|---|---|
| Timeout | `15000` ms |
| Resources | `Stream` uniquement (retire Catalog et Metadata) |
| URL | `https://mediafusion.elfhosted.com` |
| Use Cached Searches Only | **ON** |
| Enable Watchlist Catalogs | OFF |
| Download via Browser | OFF |
| Contributor Streams | OFF |
| Services | vide |
| Media Types | vide |

### Torrentio
> ⚠️ Torrentio bloque les IPs de la plupart des instances publiques. Si tu vois "Our server is blocked from accessing", passe à l'étape suivante — Comet + MediaFusion suffisent.

### Addon Fetching Strategy
Laisse sur **Default** — interroge tous les scrapers simultanément.

---

## Étape 5 — Configurer les filtres

### Cache
- Exclude Uncached → **OFF**
- Exclude Cached → **OFF**
- Tout le reste → vide

### Resolution
- **Required** → vide
- **Excluded** → `720p`, `576p`, `480p`, `360p`, `240p`, `144p`
- **Included** → vide
- **Preference Order** → `2160p` → `1440p` → `1080p` → `Unknown`

### Quality
- **Excluded** → `CAM`, `TS`, `TC`, `SCR` *(déjà configuré par défaut)*
- **Preference Order** → `BluRay REMUX` → `BluRay` → `WEB-DL` → `WEBRip` → `HDRip` → `HC HD-Rip` → `DVDRip` → `HDTV` → `Unknown`  
  *(Supprime CAM, TS, TC, SCR de la preference order)*

### Language
- **Required** → vide *(ne jamais bloquer sur la langue)*
- **Excluded** → vide
- **Included** → vide
- **Preferred** → `French`, `Multi`  
  *(Preference Order : French → Multi)*

> 💡 Ne pas mettre French en Required — tu perderais les séries sans piste française comme les séries anglophones et allemandes en VOSTFR.

### Subtitle
- Tout vide

---

## Étape 6 — Configurer le tri (Sorting)

Dans la section **Sorting**, onglet **Global**, réorganise la **Preference Order** dans cet ordre :

1. Cached
2. Language
3. Resolution
4. Quality
5. Stream Type
6. Size
7. Visual Tag
8. Audio Tag
9. Audio Channel
10. Encode
11. Library
12. Regex Patterns
13. Stream Expression Score
14. Subtitle

> L'ordre **Cached → Language → Resolution → Quality** garantit : lecture immédiate, français en priorité, meilleure résolution disponible, meilleure qualité disponible.

---

## Étape 7 — Sauvegarder et installer dans Stremio

1. Clique sur **Save** dans AIOStreams
2. Entre ton mot de passe et sauvegarde ce dernier
3. Sauvegarde ton UUID
4. Si erreur "Failed to fetch manifest" sur un addon → désactive-le temporairement, sauvegarde, réactive-le plus tard
5. Clique sur **Install** → **Copy URL**
6. Sur ta box dans Stremio : Addons → colle l'URL → Install

---

## Étape 8 — Nettoyer Stremio

Supprime les anciens addons dans Stremio :
- ~~Comet~~ (géré par AIOStreams)
- ~~MediaFusion~~ (géré par AIOStreams)
- ~~Torrentio~~ (géré par AIOStreams)

Les garder en doublon pollue ta liste de streams.

---

## Résumé

| Avant | Après |
|---|---|
| 3 addons séparés, sélection manuelle | 1 addon, liste unifiée et triée |
| RD seul → erreurs sur WEB-DL/WEBRip | RD + TorBox → fallback automatique |
| Pas de filtre langue | Français/Multi prioritaire automatiquement |
| Scroll pour trouver le bon stream | Le meilleur stream est en tête de liste |

---

*Tuto rédigé en mai 2026 — situation RD susceptible d'évoluer.*
