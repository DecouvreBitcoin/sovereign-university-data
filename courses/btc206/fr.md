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

Nous n'avons pas de certitudes sur la continuité d'Ordinals. Il se peut que ce protocole devienne obsolète à long terme. 
Ceci reste une expérimentation en version alpha (au 25/06/24) et peut subir des modifications majeures. 

La version actuelle est : `ord 0.19`. 

Au vue de l'arrivée récente du protocole il n'y a pas encore de personne formée à ce sujet. J'ai découvert Ordinals en février 2023 et je ne suis qu'un explorateur de ce protocole.

Ce qui est partagé ici est une synthèse de mes connaissances et de mes expériences, et peut être amené à évoluer. Comme dans le cas de Bitcoin il est important de se tenir à jour des évolutions du/des protocole(s).

# I/ Introduction

Ordinals a été proposé par Casey Rodarmor ([Casey (@rodarmor) | Twitter](https://twitter.com/rodarmor/), [R O D A R M O R](https://rodarmor.com/), [casey (Casey Rodarmor) | Github](https://github.com/casey/)). 
En 2015, il travailla activement sur Bitcoin Core où il réalisa une série de mises-à-jours et le remaniement d'une partie des tests de Bitcoin Core ([Casey Rodarmor's Resume](https://rodarmor.com/resume/index.html)). Il fit cela en tant que développeur pour ChainCode Labs ([Chaincode Labs](https://chaincode.com/)).
Le protocole Oridnals a connu sa première inscription le 14 décembre 2022 [Inscription #0](https://ordiscan.com/inscription/0).

Ordinals est un protocole qui permet d'inscrire facilement des données sur Bitcoin et de les retrouver. 

Dans *L'élégance de Bitcoin* (Les contrats autonomes, l'inscription de données arbitraires et métaprotocoles pp.332-340), **Ludovic Lars** retrouve des trésors cachés dans Bitcoin comme l'hommage à Len Sassaman en art ASCII ![hommage_len](./assets/hommage_len.jpg) [source image](https://hellotoken.io/dordinals/) et bien d'autres[^1]. 

On voit ici que l'on sait inscrire des données sur Bitcoin depuis longtemps, mais qu'il nous est difficile de les retrouver. On dit alors que ces éléments ne sont pas indexés nativement[^2].
Ordinals est entre-autre une réponse à ceci en permettant de facilement retrouver tout ce qui est inscrit par cette méthode en utilisant un indexer[^3] ou un [explorer](https://ordinals.com).

Ordinals est une protocole qui permet l'écriture de larges données sur Bitcoin et d'en tracer la possession. 
On parle d'**enveloppe**, d'**index** (ou d'indexer^[1]) et de **satoshis** (les unités de Bitcoin) pour tracer la propriété.

Nous allons donc voir comment cela fonctionne, comment on peut utiliser ce protocole et présenter quelques projets important de l'écosystem Ordinals.

Avant cela on peut se demander si Ordinals est unique ?

## Ordinals est-il unique ?
Il existe d'autres protocoles à enveloppe sur Bitcoin (comme Atomicals) ou sur d'autres blockchain (comme Dogecoin).

### Atomicals

Ce protocole fut proposé fin 2023 sous forme de ligne de commande construite en javascript [atomicals-js](https://github.com/atomicals/atomicals-js). Comme pour Ordinals étant un protocole il doit être indexé. Pour ce faire ils ont proposés un indexer basé sur ElectrumX : [Electrumx Atomicals Indexer Server](https://github.com/atomicals/atomicals-electrumx).

Ce protocole utilise des messages plus compact qu'Ordinals avec une enveloppe plus élémentaire. De plus, au lieu d'écrire les données uniquement en hexadecimal sur Bitcoin il les transcrit d'abord en CBOR (Concise Binary Object Representation) puis en hexadécimal.
Atomicals a également la possibilité de faire des tokens, des nfts et des noms de domaine (appelé *realms*) nativement. 

<!--La différence majeure entre Atomicals et Ordinals est que Atomicals est un protocole de type *stateful* alors qu'Ordinals est un protocole de type *stateless*.-->

Une des attentes actuelles concernant Atomicals est l'Atomicals Virtual Machin (AVM) qui permettrait de faire des contrats autonomes sur Bitcoin.

A l'heure actuelle l'AVM n'est pas encore sortie.

Ce protocole est également très intéressant et permet de faire de nombreuses choses sur Bitcoin. Cela fera l'objet de cours futurs. 
Nous pouvons noter que la communauté atomicals est bien moindre que la communauté Ordinals. Ce protocole peine à se faire connaître et à être utilisé.

Pour vous plonger dans ce protocole je vous invite à consulter [la documentation faites par la communauté](https://atomicals-community.github.io/atomicals-guide/).

### Doginals

Doginals est une copie du protocole Ordinals qui utilise exactement la même enveloppe mais sur la blockchain Dogecoin. 

On y retrouve alors l'univers Ordinals avec souvent quelques mois de retard. 
Un avantage d'avoir Ordinals sur Dogecoin (via Doginals) est le coup indéniablement moindre des inscriptions ainsi que la rapidité des transactions.
De plus, on y trouve une culture différente de celle d'Ordinals. Les volumes sont évidemment dérisoire comparé à ceux d'Ordinals mais il y a tout de même un peu de trafic.
Doginals souffre néanmoins de mauvais indexers et d'outils encore peu développés aussi bien pour inscrire que pour intéragir avec le protocole.

L'intégration annoncée des Doginals dans [mydoge wallet](https://www.mydoge.com/) peut être une étape vers une utilisation plus simple et plus répandue de ce protocole.  

Le site web principal à propos de doginals est [doggy.market](https://doggy.market), un site d'achat/vente de doginals et de DRC-20[^4].


Les protocoles de type inscriptions sont encore balbutiant et peuvent être à la manière d'Atomicals assez différent d'Ordinals. Néanmoins, ce travail d'apprentissage sur Ordinals sera toujours bénéfique pour comprendre les évolutions futures. 

# II/ Le cœur d'Ordinals
**Ici nous regardons les détails de l'enveloppe et des tags du protocole.**

Dans une transaction Bitcoin on peut mettre un message. Ce message doit respecter une certaine structure et utiliser des "fonctions" du protocole Bitcoin.
Ces "fonctions" sont appelées des <u>opérations</u> et sont nommé `OP_CODE` où `CODE` désigne le nom de l'opération en jeu (par exemple `OP_ADD` pour l'opération d'addition). 
Ces opérations sont envoyées au *réseau Bitcoin*[^5] dans des transactions.

Via des `OP_CODEs` on peut réaliser des opérations algorithmique sur le réseau Bitcoin, on appelle cela un `script`. Pour plus de détail : [Opcodes used in Bitcoin Script - Bitcoin Wiki](https://wiki.bitcoinsv.io/index.php/Opcodes_used_in_Bitcoin_Script)

Ordinals peut alors être vu comme une proposition de standardisation de script Bitcoin pour permettre l'écriture de larges données sur Bitcoin et en tracer la possession. On voit ici apparaître le lien fort entre le script Bitcoin et les protocoles de type inscription sur Bitcoin. 
Les protocoles seront appelés de type Inscription lorsqu'ils utilisent la forme de script suivant :
```
OP_FALSE
OP_IF
    OP_PUSHDATA <ID_DU_PROTOCOLE>
    OP_PUSHDATA <REGLE_APPLIQUEE>
    ...
    OP_PUSHDATA <DONNEES>
OP_ENDIF
```
Evidemment, la forme exacte varie d'un protocole à l'autre, mais les protocoles à inscription sont tous, actuellement, basés sur cette structure.
On appelle alors ce script une **enveloppe**, servant à envelopper les données sur Bitcoin.

Comme ce cours concerne Ordinals nous nous bornerons à l'enveloppe Ordinals mais vous pourrez aisément trouver l'enveloppe d'Atomicals dans la documentation fournie par la communauté Atomicals.

## 1. L'enveloppe

Basiquement on pousse les informations suivantes via l'enveloppe : 
```
"ord"

"Type" (MIME format) 

"Données"
```

Autrement dit on envoie le script suivant sur Bitcoin : 
```
OP_FALSE
OP_IF
    OP_PUSHDATA "ord"
    OP_PUSH 1
    OP_PUSHDATA <TYPE MIME>
    OP_PUSH 0
    OP_PUSHDATA <DONNEES>
OP_ENDIF
```
Les opérations `OP_PUSH 1` et `OP_PUSH 0` sont des opérations qui permettent de séparer les champs de l'enveloppe. On appelle cela les **tags** et nous détailleront cela par la suite. 

La question qui peut se poser est : qu'est-ce que le format [MIME](https://developer.mozilla.org/fr/docs/Web/HTTP/Basics_of_HTTP/MIME_types/Common_types) ?

Le format MIME est un standard d'Internet initialement prévu pour détailler le type de fichier envoyé dans courrier électronique. Il permet d'indiquer le type de contenu d'un message.
La plupart des extensions de fichier (`.jpg`, `.pdf`, `.mp3`, ...) ont un type MIME associé. 
Pour Ordinals en fonction du fichier que l'on souhaite inscrire le type MIME est sélectionné puis écrit en conséquence. 

Cela a deux fonctions :
- Permettre de retrouver les données inscrites en fonction de leur type.
- Afficher correctement les données contenues dans l'enveloppe. Cela vaut surtout pour les explorers qui pourront afficher le contenu convenablement. 

Pouvant mettre n'importe quel format MIME, on peut aisément stocker du HTML, du CSS, du javascript ou encore de l'audio ou de la vidéo sur Bitcoin.

Quelques exemples sont disponibles dans l'article [{In-On}-Chain](https://6120.eu/posts/in-on-chain/).
Un exemple plutôt sympa est l'inscription 466 : [Yet Another Doom Clone](https://ordinals.com/content/521f8eccffa4c41a3a7728dd012ea5a4a02feed81f41159231251ecf1e5c79dai0). Publiée assez rapidement et codée entièrement en HTML, cette inscription fait que DOOM sera toujours disponible, on aura simplement à récupérer les données sur Bitcoin pour y jouer. Vous pouvez consulter le code source via [Inscription #466 | Ordiscan](https://ordiscan.com/inscription/466) en cliquant sur **view source code** en haut de la fenêtre d'affichage. 

Vous pouvez avoir un détail du nombre d'inscriptions par type MIME sur [ordinals.com/status](https://ordinals.com/status).

### Activité
Trouver une inscription de type MIME `text/html;charset=utf-8`, `image/jpeg`, `image/webp`, `video/mp4`, `image/gif` et `text/javascript`.

Pour cela trouver un explorer Ordinals qui vous permet de filtrer les inscriptions pour obtenir ces types MIME.
<!--Explorer possible : ord.io-->

### Activité avancée
Créer le script de création d'une transaction depuis `createrawtransaction` avec une librairie ou langage quelconque. (Sympa en bitcoin-cli, mais pas de copier-coller du Rust de [./src/subcommand/wallet/inscribe.rs](https://github.com/ordinals/ord))

**Détails sur les inscriptions brc-20**
Comme on l'a vu pour faire une inscription simple on a juste besoin de specifier le type de notre fichier et de l'envoyer sur Bitcoin.

En mars 2023 [domodata](https://domo-2.gitbook.io/brc-20-experiment) a proposé un standard permettant de créer et échanger des tokens sur Bitcoin via l'enveloppe Ordinals. On appelle ce standard **brc-20** et nous allons quel est-il et comment fonctionne-t-il. 

Le nom du standard est une référence au standard ERC-20 d'Ethereum. Le but de ce standard est d'être facile et de fonctionner. Il s'agit en effet de la première expérimentation dans cette direction. Loin d'être parfait et optimiser il a le mérite de fonctionner. 

Mais, comment ?
 
Pour créer un token brc-20 il suffit de créer une inscription avec le type MIME `application/json` et de respecter la structure suivante : 
```json
{
    "p": "brc-20",
    "op": "deploy",
    "tick": "TICK",
    "supply": "xx",
    "lim": 1000000
}
```
- `p` est le protocole utilisé, ici brc-20.
- `op` est l'opération à réaliser, ici deploy pour déployer un token.
- `tick` est le ticker du token, il doit faire 4 caractères pour être indexé.
- `supply` est la quantité totale de token possible.
- `lim` est le nombre maximum de token pouvant être minté par opération *mint*.

On voit ici qu'on est une fois de plus face à un protocole. Ce protocole possède 3 opérations : *deploy* (détaillé ci-dessus), *mint* (pour créer des tokens) et *transfer* (pour échanger des tokens).
Chaque opération prend des paramètres particuliers et doit respecter la structure attendue pour être indexée.

Comme pour Ordinals il faut un indexer, qui à l'instar d'Ordinals fait un peu plus que simplement permettre de retrouver les tokens. 
L'indexer brc-20, permet non seulement de tenir à jour les tokens existants mais tiens également une balance pour chaque wallet ayant minté ou transféré des tokens. 

Le *mint* est assez simple, il suffit d'inscrire le fichier suivant : 
```json
{
    "p": "brc-20",
    "op": "mint",
    "tick": "TICK",
    "amt": "xx"
}
```
Si le montant (amount : `amt`) est supérieur à la limite (`lim`) définie dans l'inscription de `deploy` alors l'opération est refusée et les tokens ne sont pas ajoutés à l'adresse ayant effectué l'opération. Si le montant est inférieur ou égal à la limite alors l'adresse est crédité d'autant de token. 

Le *transfer* est un peu plus complexe, il faut inscrire le fichier suivant puis transférer ce fichier fraîchement inscrit à l'adresse de destination.

```json
{
    "p": "brc-20",
    "op": "transfer",
    "tick": "TICK",
    "amt": "xx"
}
```

On voit donc qu'avec des fichiers JSON simples on peut créer des tokens en utilisant l'enveloppe Ordinals moyennant un indexer du protocole brc-20.

D'autres expérimentations plus poussées sont en cours du côté de [Trac ecosystem](https://trac.network/).
**Trac** se définit comme un ecosystème avec plusieurs protocoles permettant de créer des tokens, réalisés des swap, du staking ou encore des tokens d'authentification. Le développement est en cours et si vous voulez en savoir plus en français je vous invite à écouter l'[OP_SPACE 006: Tap Protocol -> TOUT !](https://x.com/i/spaces/1lPJqbbnzwmxb). 


## 2. Les *tags*
Les *tags* ou étiquette en français permettent une spécification des messages protocolaires. Cela permet d'ajouter du contexte à l'inscription brute vue en partie 1.

Ci-dessous un détail des *tags* possibles :
```
content_type, avec le tag 1, sa valeur est le type MIME du corps.
pointer, avec le tag 2, [pointer docs](https://docs.ordinals.com/inscriptions/pointer.html).
parent, avec le tag 3, [provenance](https://docs.ordinals.com/inscriptions/provenance.html).
metadata, avec le tag 5, [metadata](https://docs.ordinals.com/inscriptions/metadata.html).
metaprotocol, avec le tag 7, dont la valeur est l'identifiant du metaprotocol.
content_encoding, avec le tag 9, dont la valeur est l'encodage utilisé pour le corps.
delegate, avec le tag 11, [delegate](https://docs.ordinals.com/inscriptions/delegate.html).
```
Le tag 1 a été longuement détaillé dans la partie précédente. 

Les autres tags permettent de donner des informations supplémentaires sur l'inscription. Regardons quelques tags importants dans l'écosystème actuel. 

- Le tag 2 est utilisé pour donner un pointeur vers une autre inscription. Cela permet de lier des inscriptions entre elles.
- Le tag 3 est utilisé pour créer ce que l'on appelle des *parent/enfant*. Cela permet de tracer la provenance d'une inscription et de créer des "arbres d'inscriptions". En effet, dans le cadre d'une collection d'art par exemple il peut être intéressant d'inscrire l'image représentative de la collection puis d'inscrire chaque oeuvre de la collection en tant qu'enfant de l'inscription de la collection. Ex : [Manifesto parent](https://ordinals.com/inscription/2914e780bb7272612b97517af3dfe8fc604b6f8661645eedad226eef181df06bi0), les enfants sont appelés *children* dans l'interface d'[ordinals.com](https://ordinals.com).
- Le tag 5 est utilisé pour donner des informations supplémentaires sur l'inscription. Cela peut être des informations sur l'auteur, la date de création, le lieu de création, etc.
- Le tag 7 est utilisé pour donner l'identifiant du metaprotocol. Cela permet de spécifier quel protocole est utilisé pour l'inscription. Dans l'exemple donné pour le tag 3 le metaprotocol est `OP_SPACE`. 
- Le tag 9 est utilisé pour donner l'encodage du corps. Cela permet de savoir comment lire les données inscrites.
- Le tag 11 est utilisé pour donner un délégué. Cela permet de donner des droits à une autre adresse sur l'inscription.


### Activité possible
Chercher "à la main" des inscriptions exemples pour chacun des tags.
Attention : cet exercice peut être très difficile compte tenu de la mauvaise gestion des explorers actuels des filtres par *tags*. Un fork de [ord](https://github.com/ordinals/ord) a été proposé pour permettre de filtrer par tag metaprotocol : [xord](https://github.com/cyb-ord/xord) mais repose sur une ancienne version d'`ord`.

### Activité avancée

Proposer un script permettant de filtrer les inscriptions par leur tag. 
Cela pourra être publier et donner lieu à du soutient par la communauté Ordinals. 

On voit ici que les tags apportent de nouveaux cas d'usage d'Ordinals. Un exemple de l'utilisation avancée des tags est le protocole [cbrc-20](https://ordinals.com/preview/130c79034450163f36fcde8e27f96904dc42e535f28aacd5af3b9a18d0b1c7f9i0) aujourd'hui en cours d'abandon. Ce protocole utilisait le champ metaprotocol et metadata pour créer, minter et transférer des tokens. 

De nombreux uses-cases sont encore à explorer avec tout ceci.

### Activité
Trouver un ou deux projets utilisant certains tags avancées et expliquer comment ils les utilisent.

<!--Un exemple de très grosse transaction : [Creation des Quantum Cats](https://mempool.space/tx/4b31771df21656d2a77e6fa18720a6dd94b04510b9065a7c67250d5c89ad2079).-->
<!--Cette inscription contient par exemple un module javascript recursif : [cat0001](https://ordiscan.com/inscription/53785861).-->
<!--La collection Blob : [ex : blob01](https://ordiscan.com/inscription/67285792)-->
<!--La collection Bitcoin Puppet : [ex : puppet #6060](https://ordinals.com/inscription/e4520773d3d7a182ed4bd8875626419db5db3ec73fcacd4cc48ad060afb02a30i0).-->

### Récusivité

Pour aller plus loin on peut également parler de récursivité. Comme on l'a vu précédemment on peut inscrire des fichiers javascript ou html. 
Un tel fichier peut alors accéder à la mémoire interne de son lieu de stockage. Mais... Où est-il stocké ? 
Sur Bitcoin ! Il a donc accès à des éléments propre à Bitcoin. Cela se fait via l'accès à ce que l'on appelle des *endpoints* décrit dans la [documentation officielle](https://docs.ordinals.com/inscriptions/recursion.html). 

Les chemins sont de la forme : `/r/<OPTION>/<ID>` où `OPTION` est le nom d'une catégorie à laquelle on souhaite accéder et `ID` est l'identifiant de l'inscription. Une description complète est donnée dans le lien ci-dessus. 

Cela nous permet d'écrire du code qui utilise d'autres inscriptions. Par exemple, le code exact de React@18.2.0 est [on-chain](https://ordinals.com/content/7f403153b6484f7d24f50a51e1cdf8187219a3baf103ef0df5ea2437fb9de874i0). 
Ainsi, on peut créer un site web React utilisant cette librairie entièrement on-chain : [Psyop website](https://ordiscan.com/inscription/25949479).

La récursivité est aujourd'hui très utilisée dans Ordinals. 

### Activité 

Trouver une collection importante utilisant la recursivité. 

<!--Ex : [RSIC METAPROTOCOL](https://www.ord.io/56718386)-->

## 3. L'interprétation des satoshis et l'`index` pour la propriété ?

Le protocole Ordinals a été proposé par Casey avec une théorie de la propriété. Cette théorie originellement appelée Théorie des Ordinals défini une numérotation de chaque satoshi (sat) produit par le réseau Bitcoin.

Une fois la numérotation effectuée (qui continue à mesure que de nouveaux blocs sont minés) il a déclaré que l'inscription se faisait sur un sat, le premier de l'UTXO.
Ainsi, on peut tracer la propriété d'une inscription par la propriété du sat qui la contient.

> Cela se fait par l'information de la localisation *location* donnée par l'indexer à propos du sat.  

L'accès à ces informations peuvent se faire de plusieurs manières en fonction des usages et des besoins. 
De l'interface web [ordinals.com](https://ordinals.com) à la manipulation directe via le fichier `index.redb`.

De plus, une fois la numérotation effectuée, il y a des sats qui sont considérés comme rares. Par exemple, le premier sat miné par Satoshi est légendaire, le premier sat miné lors de chaque halving est rare ou encore le premier sat de chaque bloc est considéré comme *uncommon* (pas commun). 
Ces sats tout comme la numismatic (étude des pièces de monnaie) sont des éléments de collection et peuvent être échangés. De nouveaux niveau de raretés sont créés par les utilisateurs d'Ordinals. Par exemple, les sats ayant servi à payer la Pizza (du Bitcoin pizza day) sont identifiés comme les *pizza sats*.

### Activité 
En prenant connaissance des [points d'accès](https://docs.ordinals.com/guides/explorer.html) donné dans la documentation et des explorers trouvés précédemment donner des sats rares et/ou vérifier la rareté de certains sats. 
![API Endpoints](./assets/endpoints_ordinals.png)

Trouver une collection ayant été entièrement inscrite sur des sats particuliers. 
<!--Pizza Ninja-->

Un bon thread au sujet de la rareté réalisé par [@Besbtc](https://x.com/Besbtc) : [Sat rarity](https://x.com/Besbtc/status/1739987968922632240). 
<!--Proposer à Besbtc de faire un tuto sats rares.-->

#### Pour aller plus loin

La ligne de commande `ord` permet également d'étudier les sats. Pour cela il faut avoir l'index qui est convenanblement configuré. 
> Donner la configuration pour chasser les sats.

> Discuter du format redb. 

<!--Proposer à Crypto9ine de faire un tuto sur la chasse aux sats en cli.-->

# III/ L'utilisation & les projets

On a passé du temps pour bien comprendre ce qu'il se passe on-chain et quelles sont les idées derrière Ordinals. Maintenant on va voir comment on peut utiliser tout cela et quels sont les projets qui ont construit sur Ordinals.

## 1. Les outils

Pour utiliser Ordinals il faut des outils. 
Si vous êtes un développeur ou familier des lignes de commandes vous pouvez utiliser directement la ligne de commande [`ord`](https://github.com/ordinals/ord) pour inscrire et indexer Ordinals. Pour cela il vous faudra ~1To de disponible pour avoir un full node Bitcoin avec l'option `txindex=1` activée.
Pour l'installation de `ord` vous pouvez suivre la très bonne vidéo [@pazNGMI: How To Setup A Bitcoin Node & Ord Wallet](https://www.youtube.com/watch?v=tdC8kmjn5N0). Pour la partie node Bitcoin je vous invite à consulter directement PlanB Network [Tutoriels nodes](https://planb.network/fr/tutorials/node).

Pour un usage plus user friendly voici quelques outils que j'utilise ou dont j'ai entendu parler [^6]:

- Explorers : [ordinals.com](https://ordinals.com), [ordiscan.com](https://ordiscan.com), [ordpool.space](https://ordpool.space), [ord.io](https://ord.io), ...

- Quelques wallets : [Unisat](https://unisat.io), [Xverse](https://xverse.app), [Magic Eden](https://wallet.magiceden.io/), ...

- Outils d'inscriptions : [Unisat](https://unisat.io), [ordinals bot](https://ordinalsbot.com), [looksordinals.com](https://looksordinals.com), [Chisel](https://chisel.xyz) [Cool pour faire des inscriptions parent/enfants], ...

## 2. Les Projets

La propriété sur Ordinals est définit consensuellement comme étant le premier à écrire un fichier (vu comme "message" au sein du protocole). 
Idée importante dans la définition de sous-protocoles pour créer le consensus. 

Dans cett idée de propriété on a : 
[Bitmap](https://bitmap.community/) -> consensus produisant une propriété sur les blocs Bitcoin. Crée l’idée d’un metaverse Bitcoin dont les biens de propriétés sont les blocs. 
Le premier à inscrire : NumeroDeBloc.bitmap possède alors le bloc NumeroDeBloc au regard du protocole Bitmap.

Comme parlé précédemment brc-20, cbrc-20,… applique le principe du : premier arrivé premier servi. 

Un projet important à mentionner est : 
**Taproot Wizard** 🧙 
Histoire et indexation des informations. 

[^1]: Pour un peu d'histoire cypherpunk : [Len Sassaman and Satoshi: a Cypherpunk history | Medium](https://evanhatch.medium.com/len-sassaman-and-satoshi-e483c85c2b10).

[^2]: En effet, il est possible de retrouver ces données sur Internet par exemple mais très difficile on-chain (depuis Bitcoin).

[^3]: En français on prononce indexeUr et non indexé, comme explorer (exploreUr et non exploré).

[^4]: Standard basé sur brc-20 pour Doginals. Nous détaillerons plus tard ce qu'est le standard brc-20.

[^5]: On appelle <u>réseau Bitcoin</u>, l'ensemble des machines exécutant le protocole Bitcoin. On trouvera un détail des clients utilisés pour accéder au réseau Bitcoin sur [Coin Dance | Bitcoin Nodes Summary](https://coin.dance/nodes/share).

[^6]: Attention, ces outils peuvent être obsolètes ou ne pas être sécurisés. Il est important de bien se renseigner avant d'utiliser un outil et de ne pas mettre tout son argent dans un seul outil !
