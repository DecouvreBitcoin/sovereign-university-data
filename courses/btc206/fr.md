---
name: Les Inscriptions sur Bitcoin au travers d'Ordinals
goal: Comprendre le fonctionnement technique et effectif d'Ordinals
objectives:
  - Définir les notions théoriques d'Ordinals
  - Savoir comment les données sont inscrites sur Bitcoin 
  - Utiliser des outils pour explorer les inscriptions.
  - Comprendre les projets qui utilisent Ordinals
---


# 0/ Précautions

Avertissement : Risques.

D'où je parles ?

# I/ Introduction

-> Inscription de données arbitraires. 

-> Histoire: *L'élégance de Bitcoin* de **Ludovic Lars** (Les contrats autonomes, l'inscription de données arbitraires et métaprotocoles pp.332-340).

-> Premières définitions. 
Ordinals est une proposition de standardisation de script Bitcoin pour permettre l'écriture de larges données sur Bitcoin et en tracer la possession. On parle d'**enveloppe** et d'**index** (ou d'indexer^[1]).

^[1]: En français on prononce indexeUr et non indexé.

## Ordinals est-il unique ?

Il existe d'autres protocoles à enveloppe sur Bitcoin (comme Atomicals) ou sur d'autres blockchain (comme Dogecoin).


# II/ Le cœur d'Ordinals
Ici nous regardons les détails de l'enveloppe et des tags du protocole. 

## 1. L'enveloppe

Basiquement: 

"ord"

"Type" (MIME format) 

"Data"

Détailler le type MIME et ce qu'il peut en être fait. 
Exemples: [{In-On}-Chain](https://6120.eu/posts/in-on-chain/)


### Activité possible
Créer le script de création d'une transaction depuis `createrawtransaction` avec une librairie ou langage quelconque. (Sympa en bitcoin-cli, mais pas de copier-coller du Rust de [./src/subcommand/wallet/inscribe.rs](https://github.com/ordinals/ord))

**Détails sur les inscriptions brc-20**
On ne fait qu'utiliser le type MIME `application/json` pour les inscriptions brc-20 avec un indexer qui vient s'ajouter à celui Ordinals. 

Discuter de tap qui utilise uniquement des json via l’enveloppe ord pour son propre indexer. 

## 2. Les *tags*
Spécification des messages protocolaires. Permet d'ajouter du context au message brut.

```
content_type, with a tag of 1, whose value is the MIME type of the body.
pointer, with a tag of 2, [pointer docs](https://docs.ordinals.com/inscriptions/pointer.html).
parent, with a tag of 3, [provenance](https://docs.ordinals.com/inscriptions/provenance.html).
metadata, with a tag of 5, [metadata](https://docs.ordinals.com/inscriptions/metadata.html).
metaprotocol, with a tag of 7, whose value is the metaprotocol identifier.
content_encoding, with a tag of 9, whose value is the encoding of the body.
delegate, with a tag of 11, [delegate](https://docs.ordinals.com/inscriptions/delegate.html).
```

Détails.


### Activité possible
Chercher "à la main" des inscriptions vérifiant certains critères.

Avec ceci amener le concept de parent/enfant (et potentielles utilisations), cbrc-20 et explorer les potentialités.


## 3. L'interprétation des satoshis et l'`index` pour la propriété ?

> L'inscription se fait sur un satoshi. On trace la propriété d'une inscription par la propriété du sat qui la contient.

> Cela se fait par l'information de la localisation *location* donné l'indexeur à propos du satoshi.  

L'accès à ces informations peuvent se faire de plusieurs manières en fonction des usages et des besoins. 

De l'interface web [ordinals.com](https://ordinals.com) à la manipulation directe via le fichier `index.redb`.

### Activité 

En prenant connaissance des [points d'accès](https://docs.ordinals.com/guides/explorer.html) donné dans la documentation trouver des sats rares et/ou vérifier la rareté de certains sats. 

![API Endpoints](./assets/endpoints_ordinals.png)

#### Pour aller plus loin

La ligne de commande `ord` permet également d'étudier les sats. Pour cela il faut avoir l'index qui est convenanblement configuré. 
> Donner la configuration pour chasser les sats.

> Discuter du format redb. 

>> Discuter de l'impact des satoshis et comment sont-ils concrétement représentés ?

Prendre de la hauteur sur les enveloppes. 


# III/ L'utilisation & les projets

## 1. Les outils

- Explorers : ordinals.com, ordiscan.com, ordpool.space, ord.io, ...

- Quelques wallets : Unisat, Xverse, Magic Eden, Leather

- Outils d'inscriptions : unisat, ordinals bot, looksordinals.com, ...


## 2. Les Projets

La propriété sur Ordinals est définit consensuellement comme étant le premier à écrire un fichier (vu comme "message" au sein du protocole). 
Idée importante dans la définition de sous-protocoles pour créer le consensus. 

Dans cett idée de propriété on a : 
Bitmap -> consensus produisant une propriété sur les blocs Bitcoin. Crée l’idée d’un metaverse Bitcoin dont les biens de propriétés sont les blocs. 
Le premier à inscrire : NumeroDeBloc.bitmap

Comme parlé précédemment brc-20, cbrc-20,… applique le principe du : premier arrivé premier servi. 

Un projet important à mentionner est : 
**Taproot Wizard** 🧙 
Histoire et indexation des informations. 
