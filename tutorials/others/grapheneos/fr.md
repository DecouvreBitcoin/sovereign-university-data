---
name: GrapheneOS
description: Tutoriel Graphene OS
---

> "[GrapheneOS](https://grapheneos.org/) est un système d'exploitation mobile axé sur la confidentialité et la sécurité, compatible avec les applications Android, développé en tant que projet open source à but non lucratif."

GrapheneOS, initialement fondé en 2014 sous le nom de 'CopperheadOS', est basé sur le code Android traditionnel (AOSP), mais avec de nombreux changements et améliorations visant à améliorer la confidentialité et la sécurité des utilisateurs. GrapheneOS permet à l'utilisateur de contrôler son téléphone, et non les grandes entreprises technologiques.

### Sommaire :

- Introduction
- Préparation
- Installation
- Alternatives d'applications
- Inconvénients
- Informations utiles

Guide disponible sur https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md

## Pourquoi utiliser GrapheneOS ?

Les téléphones modernes sont des appareils de suivi et de collecte de données coûtant entre 500 et 1000 dollars. Chaque aspect de notre vie passe par eux, et malheureusement, une grande partie de ces données est partagée avec des tiers d'une manière ou d'une autre. GrapheneOS est conçu spécifiquement pour réduire ce partage de données et améliorer la sécurité de votre appareil contre les vecteurs d'attaque potentiels. Il n'y a pas de compte GrapheneOS. Vous n'avez pas besoin d'un compte pour télécharger des applications ou interagir avec le système d'exploitation. En d'autres termes, vous n'êtes pas le produit.

GrapheneOS offre une sécurité supplémentaire à votre expérience Android grâce à quelques principes fondamentaux simples.

1. **Réduction de la surface d'attaque** - Suppression du code inutile (ou des logiciels superflus).
2. **Prévention de l'exposition aux vulnérabilités** - Permettre à l'utilisateur de choisir les compromis avec lesquels il est à l'aise.
3. **Containement des applications** - GrapheneOS renforce les sandbox Android existantes, limitant davantage la capacité de chaque application à communiquer avec le reste de votre téléphone.

Pour en savoir plus sur les détails techniques de l'ensemble des fonctionnalités de GrapheneOS, cliquez [ici](https://grapheneos.org/features).

### Faciliter la transition

Si vous êtes depuis des années dans l'écosystème Google ou Apple, l'idée de perdre toute cette commodité du jour au lendemain peut être effrayante. Mais avec des décisions d'installation d'applications soigneusement réfléchies (abordées plus tard), une grande partie de cette difficulté attendue peut être réduite ou éliminée.

Aussi bonnes que deviennent les alternatives, le changement peut encore être rebutant. Si vous vous trouvez dans cette situation, mon meilleur conseil est d'utiliser votre nouvel appareil GrapheneOS en parallèle avec votre téléphone actuel pendant un certain temps. À partir de là, vous pouvez progressivement vous passer de 2 à 3 applications par semaine jusqu'à ce que vous ne vous serviez plus que de votre appareil GrapheneOS.

Si vous adoptez cette approche, soyez strict avec vous-même et abandonnez rapidement votre dépendance aux alternatives surveillées. Nous, les humains, sommes paresseux et nous choisissons souvent le chemin de moindre résistance. N'oubliez pas pourquoi vous avez effectué ce changement en premier lieu.

**Au lieu de payer avec vos données personnelles, vous avez choisi de payer avec votre temps, et parfois avec votre argent durement gagné (selon les applications alternatives que vous installez).**

## Premiers pas

GrapheneOS est actuellement uniquement disponible pour la gamme de téléphones [Google Pixel](https://grapheneos.org/faq#supported-devices) (ce qui est plutôt ironique). Cela n'est pas sans raison. Les Pixel offrent la meilleure sécurité basée sur le matériel pour compléter le travail effectué pour renforcer le système d'exploitation. Cela inclut des isolations de composants spécifiques et un démarrage vérifié.

### Choix d'un appareil

Lorsque vous choisissez le Pixel sur lequel vous souhaitez installer GrapheneOS, assurez-vous de vérifier pendant combien de temps l'appareil continuera à recevoir les [mises à jour de sécurité](https://support.google.com/pixelphone/answer/4457705?hl=fr#zippy=%2Cpixel-xl-a-a-g-a-g) par défaut.
Au moment de la rédaction, le Pixel 6a est le modèle le moins cher disponible avec une bonne prise en charge à long terme, garantie jusqu'en juillet 2027. Si vous choisissez ce modèle, le déverrouillage OEM ne fonctionnera pas avec la version du système d'exploitation d'origine. Vous devez le mettre à jour vers la version de juin 2022 ou ultérieure via une mise à jour over-the-air. Après l'avoir mis à jour, vous devrez également réinitialiser l'appareil aux paramètres d'usine pour résoudre le problème de déverrouillage OEM. Tous les autres modèles déverrouillés par l'opérateur seront prêts pour GrapheneOS dès la sortie de la boîte.

Lors du choix d'un appareil, vous voudrez également vous assurer d'acheter une version déverrouillée. Certains opérateurs comme Verizon expédient leurs unités avec un bootloader verrouillé, ce qui empêche complètement le processus suivant.

### Installation de GrapheneOS

L'installateur web de GrapheneOS rend l'ensemble du processus très simple et peut être réalisé par n'importe qui en moins de 10 minutes. Les instructions suivantes sont une version simplifiée tirée du lien ci-dessus.

Tout ce dont vous avez besoin est :

- Le Pixel
- Un câble USB pour relier le téléphone à votre ordinateur
- Un ordinateur exécutant un navigateur web (n'importe quel navigateur basé sur Chromium : Chrome, Edge, Brave, etc.)

1. La première étape consiste à aller dans **Paramètres** > **À propos du téléphone** et à taper plusieurs fois sur le numéro de build jusqu'à ce que vous voyiez que le **"Mode développeur"** est activé.
2. Ensuite, allez dans **Paramètres** > **Système** > **Options pour les développeurs** et activez **"Déverrouillage OEM"**.
3. Redémarrez ensuite l'appareil et maintenez le bouton de volume bas enfoncé pendant que le téléphone se rallume.
4. Connectez le téléphone à votre ordinateur portable et si vous êtes invité à autoriser la connexion, acceptez-la.
5. Sur la page de l'installateur web, cliquez sur **"Déverrouiller le bootloader"**.
6. Vous verrez ensuite les options du téléphone changer. Utilisez le bouton de volume pour changer la sélection en `déverrouiller` et utilisez le bouton d'alimentation pour accepter.
7. Ensuite, cliquez sur **"Télécharger la version"** sur la page de l'installateur web.
8. Une fois le téléchargement terminé, passez à l'étape suivante et cliquez sur **"Flasher la version"**. Cela prendra une minute ou deux et vous n'aurez pas besoin de toucher au téléphone.
9. Enfin, passez à l'étape suivante de l'installateur web et cliquez sur **"Verrouiller le bootloader"**. Vous devrez changer la sélection et confirmer avec le bouton d'alimentation de la même manière que vous l'avez fait précédemment dans le processus.
10. Lorsque vous voyez le mot `Démarrer`, confirmez cela avec le bouton d'alimentation et l'appareil démarrera sur votre nouveau système d'exploitation sans Google.

![image](assets/2.webp)

Écran de démarrage de GrapheneOS

_Après le démarrage initial et la configuration, il est recommandé de désactiver le déverrouillage OEM depuis Paramètres > Système > Options pour les développeurs._

+Vous voudrez peut-être également effectuer l'étape supplémentaire, facultative mais recommandée, de vérifier l'installation via l'application Auditor. Vous aurez besoin d'un autre téléphone Android avec l'application installée pour effectuer cette étape. Les instructions à cet effet se trouvent [ici](https://attestation.app/tutorial)._

![video](https://www.youtube.com/embed/L1KZWjZVnAw)

Vidéo détaillant les étapes simples décrites ci-dessus

Si ces étapes simples vous semblent trop compliquées, vous pouvez envisager d'acheter un Pixel avec le logiciel GrapheneOS pré-installé. Cependant, veuillez noter que vous devez accorder une certaine confiance au fournisseur.

### Applications pré-installées

Maintenant que vous êtes prêt, vous remarquerez peut-être à quel point GrapheneOS est dépouillé lors de la première installation. Par défaut, vous aurez ces applications installées :

![image](assets/3.webp)

Applications par défaut
Les seuls termes avec lesquels vous pourriez ne pas être familiers sont "Auditor" et "Vanadium".
- "L'application [Auditor](https://play.google.com/store/apps/details?id=app.attestation.auditor) utilise des fonctionnalités de sécurité basées sur le matériel pour valider l'identité d'un appareil ainsi que l'authenticité et l'intégrité du système d'exploitation. Elle vérifiera que l'appareil exécute le système d'exploitation d'origine avec le chargeur de démarrage verrouillé et qu'aucune altération du système d'exploitation n'a eu lieu."
- [Vanadium](https://github.com/GrapheneOS/Vanadium) est une variante du navigateur web Chromium renforcée en termes de confidentialité et de sécurité.

## Personnalisation

Les paramètres du téléphone sont une affaire personnelle, mais voici quelques-uns des premiers éléments que je modifie lors de l'installation de GrapheneOS pour me sentir plus chez moi.

### Définir un fond d'écran et mettre à jour le thème

Accédez à Paramètres > Fond d'écran et style. À partir de là, je :

- Met à jour les arrière-plans de l'écran d'accueil et de verrouillage avec des images téléchargées depuis le web.
- Choisis les couleurs d'accentuation utilisées dans l'interface utilisateur.
- Active le thème sombre.

### Afficher le pourcentage de la batterie

Accédez à **Paramètres** > **Batterie**, puis activez **Afficher le pourcentage de la batterie** dans la barre d'état.

### Importer des contacts

**Depuis un autre téléphone Android** - Accédez à l'application Contacts et recherchez l'option Exporter vers VCF.

**Depuis iOS** - Utilisez une application comme Export Contact et utilisez l'option d'exportation 'vCard' pour exporter un fichier VCF.
Une fois que vous avez le fichier VCF, vous pouvez le transférer sur votre appareil GrapheneOS avec une option de stockage externe comme une carte microSD ou une clé USB. Si vous n'en avez pas sous la main, vous pouvez choisir de le partager via l'une des nombreuses applications répertoriées ci-dessous.

![image](assets/4.webp)

Écran d'accueil personnalisé


## Applications alternatives

Pour rendre votre téléphone utile, vous voudrez installer certaines applications ! Les options suivantes sont incluses parce que je les ai toutes utilisées personnellement ou parce qu'elles reçoivent de fortes recommandations de la part de la communauté de la vie privée. Il existe de nombreuses autres excellentes alternatives disponibles qui ne sont pas mentionnées, et [Awesome Privacy](https://awesome-privacy.xyz) propose une liste incroyablement exhaustive d'applications préservant la vie privée pour tous types d'appareils.

Le fait qu'une application soit un logiciel libre et open source (FOSS) ne signifie pas qu'elle est exempte de fuites potentielles de confidentialité. Utilisez [Exodus](https://reports.exodus-privacy.eu.org/en/) pour voir comment vos applications préférées se comportent par rapport à leurs audits de confidentialité.

### F-Droid

[F-Droid](https://f-droid.org/) est un catalogue installable d'applications FOSS pour Android. Le client facilite la navigation, l'installation et la mise à jour des applications sur votre appareil. Il convient de mentionner que les mises à jour via F-Droid peuvent parfois être plus lentes qu'avec d'autres magasins d'applications. Cela dépend principalement de la disponibilité de l'application dans le référentiel principal de F-Droid ou dans un référentiel personnalisé.

Pour installer F-Droid, il suffit de se rendre sur leur site web via un navigateur sur votre téléphone GrapheneOS et de cliquer sur Télécharger. Cela téléchargera un fichier `.apk`. Vous serez ensuite invité à installer l'application.

En plus des applications disponibles dans le référentiel par défaut de F-Droid, de nombreux projets open source hébergent également leur propre référentiel qui peut être ajouté dans les paramètres de l'application F-Droid. Si tel est le cas, le projet en question vous guidera à travers les étapes très simples nécessaires pour y parvenir sur leur site web.

![image](assets/5.webp)

Écran d'accueil de F-Droid

### Aurora Store
[Aurora Store](https://auroraoss.com/) est une version FOSS de la boutique Google Play. Aurora ressemble beaucoup à la boutique Play traditionnelle et vous permet de télécharger et de mettre à jour n'importe quelle application que vous trouveriez normalement via l'option Google.
La fonctionnalité phare d'Aurora est la connexion anonyme. Cela signifie que vous pouvez télécharger n'importe quelle de vos applications préférées qui ne sont pas disponibles via F-Droid ou APK direct, sans avoir à vous connecter à votre compte Google.

Avant de vous précipiter pour en faire votre option d'installation par défaut, rappelez-vous que bon nombre des applications que nous essayons d'éviter ont été installées à partir de la boutique Play. Le fait qu'elles soient accessibles depuis Aurora ne change pas le fait que certaines peuvent comporter des fonctionnalités de suivi intégrées. Ce ne sera pas toujours possible, mais chaque fois que vous le pouvez, recherchez une alternative F-Droid avant de télécharger via Aurora.

Pour installer Aurora, il vous suffit de rechercher 'Aurora Store' dans F-Droid.

Aurora présente également quelques vecteurs d'attaque potentiels, car les "comptes anonymes" sont réellement créés et contrôlés par Aurora. Ils pourraient, en théorie, fournir des mises à jour malveillantes ou pousser des applications sur votre téléphone, bien que vous deviez toujours accepter la demande d'installation sur l'appareil. Aurora a également parfois des problèmes avec les applications qui n'apparaissent pas en raison de lectures erronées de la région et de l'appareil. Cela peut généralement être contourné avec les étapes ci-dessous.

**Top conseil** - Parfois, Aurora Store sera soumis à des limites de taux qui limitent votre capacité à rechercher et installer des applications. Pour contourner cela, allez dans **Paramètres** > **Applications** > **Aurora** > **Ouvrir par défaut**, puis ajoutez le domaine `play.google.com`. Maintenant, chaque fois que vous accédez au site web d'un produit ou d'un service qui a le lien 'Télécharger via Play Store', en le touchant, l'application s'ouvrira dans Aurora pour que vous puissiez la télécharger.


![image](assets/6.webp)

Écran d'accueil d'Aurora Store

### Téléchargement APK

Les applications sur Android peuvent également être téléchargées et installées via un fichier `.apk`. Il s'agit d'une excellente alternative qui ne nécessite aucune boutique d'applications tierce, il vous suffit de télécharger le fichier directement depuis le site web ou le dépôt GitHub du projet ou du service.

L'inconvénient de cette approche est que vous ne bénéficiez pas de mises à jour automatiques, vous devrez donc surveiller les canaux de communication de ce service pour connaître les nouvelles versions. Cependant, il existe un excellent projet appelé Obtanium qui vise à résoudre ce problème. [Obtainium](https://github.com/ImranR98/Obtainium) vous permet d'installer et de mettre à jour des applications open-source directement depuis leurs pages de versions, et de recevoir des notifications lorsque de nouvelles versions sont disponibles.

![image](assets/7.webp)

Aperçu d'Obtanium

### Applications Web

Pour les moments où vous souhaitez utiliser occasionnellement un service et ne pas télécharger d'application native, vous pouvez simplement accéder à la version web. De nombreux sites web proposent également une prise en charge des Progressive Web Apps (PWA). C'est là que vous pouvez ajouter un signet vers un site web spécifique (par exemple Twitter.com) sur l'écran d'accueil de votre téléphone. Ensuite, lorsque vous appuyez sur l'icône, il s'ouvre comme une application en plein écran, sans les distractions habituelles de l'expérience de navigation classique. Vous pouvez voir un exemple de ce à quoi cela ressemble ci-dessous.

Pour réaliser cela dans Vanadium, le navigateur natif de GrapheneOS, il vous suffit de vous rendre sur le site web de votre choix, d'appuyer sur les trois points verticaux dans le coin supérieur droit de l'écran, puis de toucher **'Ajouter à l'écran d'accueil'**.

Le seul inconvénient de cette approche est que, parce qu'il s'agit simplement d'une page web mise en favori, vous ne recevrez aucune forme de notifications. Cependant, certains pourraient voir cela comme un avantage !

![image](assets/8.webp)

PWA Twitter

### Navigateurs Web
Vous ne pouvez vraiment pas vous tromper avec l'option pré-emballée, Vanadium. L'application se comporte de la même manière que n'importe quel autre navigateur mobile que j'ai essayé et je n'ai jamais eu de problèmes de compatibilité.

Pour les moments où vous avez besoin d'accéder aux sites natifs `.onion` de Tor, vous pouvez télécharger directement l'APK du navigateur Tor depuis leur [site web](https://www.torproject.org/download/#android) ou via F-Droid.

### VPN

Pour protéger votre activité en ligne de votre fournisseur de services Internet (FSI) qui espionne, une application de réseau privé virtuel (VPN) est une bonne option. Un VPN envoie votre trafic Internet dans un tunnel chiffré vers une adresse IP partagée contrôlée par le fournisseur de services VPN pour garantir que l'activité de votre appareil ne peut pas être liée à vous.

Voici 3 options respectées qui vous permettent de payer le service en Bitcoin et sans fournir d'informations personnelles. Les 3 options sont disponibles via F-Droid.

- [Mullvad](https://f-droid.org/packages/net.mullvad.mullvadvpn/)
- [Proton](https://f-droid.org/en/packages/ch.protonvpn.android/)
- [iVPN](https://f-droid.org/en/packages/net.ivpn.client/)

### Messagerie

Ces dernières années, les solutions de messagerie chiffrée sont devenues nombreuses. Le problème reste cependant que vous pouvez avoir la meilleure et la plus privée des options installée sur votre téléphone, mais si vous n'avez aucun contact qui l'utilise, à quoi bon ?

La plupart des personnes qui ne s'intéressent pas à la vie privée utilisent probablement WhatsApp ou iMessage. Le premier peut être téléchargé via Aurora Store, mais le second ne fonctionnera pas sur GrapheneOS (évidemment !).

- [Signal](https://signal.org/) est l'un des messagers chiffrés de bout en bout (E2EE) les plus populaires, avec un solide historique et un ensemble de fonctionnalités riches. Signal nécessite un numéro de téléphone pour l'inscription, donc si vous prévoyez de discuter avec des personnes à qui vous ne souhaitez pas divulguer votre numéro de téléphone, envisagez peut-être certaines des alternatives. Signal doit être téléchargé via Aurora Store.
- [Simplex](https://f-droid.org/en/packages/chat.simplex.app/) est un messager E2EE assez récent. Il n'a pas d'identifiant d'utilisateur, ne nécessite pas de numéro de téléphone ni d'informations personnelles. Les gens vous trouvent en scannant votre code QR personnel ou en visitant votre lien unique. Simplex permet également aux utilisateurs avancés de faire fonctionner leur propre serveur pour réduire davantage la dépendance à une entité centralisée. Simplex n'a pas de client de bureau, il peut donc ne pas convenir si la prise en charge de plusieurs appareils est une priorité pour vous. Simplex pour Android est disponible via F-Droid.
- [Threema](https://threema.ch/en/faq/libre_installation) offre une expérience similaire à Simplex, mais existe depuis plus longtemps et, par conséquent, semble un peu plus abouti. Threema n'est pas gratuit, une licence à vie coûte 4,99 $ et peut être achetée avec Bitcoin. Threema propose un client web et des applications de bureau natives. L'application Android est disponible via F-Droid.
- [Telegram FOSS](https://f-droid.org/en/packages/org.telegram.messenger/) est un fork FOSS non officiel de l'application Telegram officielle pour Android. Telegram dispose de "chats secrets" E2EE, mais l'option par défaut n'est pas privée. Telegram FOSS peut être téléchargé depuis F-Droid.

![image](assets/9.webp)
Gauche : Threema
Droite : Simplex

### Médias

- [Spotube](https://f-droid.org/packages/oss.krtirtho.spotube/) est un client Spotify multiplateforme qui ne nécessite pas de compte Premium. Spotube est disponible via F-Droid.
- [ViMusic](https://f-droid.org/en/packages/it.vfsfitvnm.vimusic/) est une application fantastique pour diffuser gratuitement de la musique à partir de YouTube Music. ViMusic est disponible sur F-Droid.
- [Newpipe](https://f-droid.org/packages/org.schabi.newpipe/) offre une expérience YouTube sans publicités ennuyeuses et sans autorisations douteuses. Avec NewPipe, vous pouvez vous abonner à des chaînes, écouter en arrière-plan et même télécharger pour une visualisation hors ligne. NewPipe est accessible via F-Droid.
- [AntennaPod](https://f-droid.org/packages/de.danoeh.antennapod/) est un lecteur de podcast qui vous permet de vous abonner et de gérer tous vos émissions préférées. AntennaPod est disponible via F-Droid.

![image](assets/11.webp)

Gauche : Spotube
Droite : ViMusic

### Cartes

Si vous souhaitez bénéficier d'une assistance vocale lors de la conduite et de l'utilisation d'une application de cartes sur GrapheneOS, vous devrez installer [RHVoice](https://rhvoice.org/installation/) et [le configurer](https://discuss.grapheneos.org/d/2488-organic-maps-app-voice-instructions-are-not-available).

- [Magic Earth](https://www.magicearth.com/) est une alternative aux cartes qui prend en charge la navigation étape par étape, la 3D et les cartes hors ligne. Magic Earth peut être téléchargé depuis l'Aurora Store.
- [Organic Maps](https://f-droid.org/en/packages/app.organicmaps/) est une alternative aux cartes pour les voyageurs, les touristes, les randonneurs et les cyclistes, basée sur les données OpenStreetMap contribuées par la communauté. Il s'agit d'une application axée sur la confidentialité, open-source et dérivée de l'application Maps.me (anciennement connue sous le nom de MapsWithMe). Elle prend en charge 100% des fonctionnalités sans connexion Internet active et peut être téléchargée depuis F-Droid.
- [OsmAnd](https://f-droid.org/en/packages/net.osmand.plus/) est une autre excellente alternative aux cartes qui prend en charge toutes les fonctionnalités mentionnées ci-dessus.

![image](assets/13.webp)

Gauche : Magic Earth
Droite : Organic Maps

### Email

- [Proton Mail](https://proton.me/mail) propose un service de messagerie privée gratuit prenant en charge le chiffrement de bout en bout vérifié. Proton propose également une version payante prenant en charge les domaines personnalisés et [l'aliasing](https://proton.me/support/creating-aliases). Proton Mail peut être téléchargé sous forme d'APK direct ou via Aurora.
- [Tutanota](https://tutanota.com/) propose les mêmes fonctionnalités que Proton Mail, y compris des services payants optionnels, et peut être téléchargé sous forme d'APK direct ou via F-Droid.
- [K-9 Mail](https://f-droid.org/en/packages/com.fsck.k9/) est un client de messagerie open source qui fonctionne avec pratiquement tous les fournisseurs de messagerie. Il prend en charge plusieurs comptes, une boîte de réception unifiée et la norme de chiffrement OpenPGP.

![image](assets/15.webp)

Gauche : Proton Mail
Droite : Tutanota

### Productivité

- [Syncthing](https://f-droid.org/packages/com.nutomic.syncthingandroid/) est un programme de synchronisation de fichiers. Il synchronise les fichiers entre deux appareils ou plus en temps réel, en les protégeant en toute sécurité des regards indiscrets. Vos données vous appartiennent et vous méritez de choisir où elles sont stockées, si elles sont partagées avec des tiers et comment elles sont transmises sur Internet. Syncthing est disponible via F-Droid.
- [KDE Connect](https://f-droid.org/packages/org.kde.kdeconnect_tp/) permet à tous vos appareils de communiquer facilement entre eux lorsqu'ils sont connectés à votre réseau domestique. Vous pouvez facilement envoyer des fichiers, des photos et des données du presse-papiers sur tous vos appareils (même sur iOS !). KDE Connect peut être téléchargé depuis F-Droid.
- [Notesnook](https://f-droid.org/en/packages/com.streetwriters.notesnook/) est une application de prise de notes E2EE qui permet de synchroniser vos pensées et vos listes de tâches sur tous vos appareils. Leur plan gratuit devrait couvrir la plupart des cas d'utilisation personnels. Notesnook est disponible sur F-Droid.
- [Standard Notes](https://f-droid.org/en/packages/com.standardnotes/) est très similaire à Notesnook, mais nécessite un abonnement payant pour correspondre à l'ensemble des fonctionnalités. Standard Notes est disponible via F-Droid.
- [Anysoft Keyboard](https://f-droid.org/packages/com.menny.android.anysoftkeyboard/) est une application de clavier qui vous permet de personnaliser à peu près tout ce que vous pouvez imaginer en ce qui concerne votre expérience de saisie sur téléphone. Il peut être téléchargé via F-Droid.
- [GBoard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin&hl=en&gl=US) est l'application de clavier Google par défaut. D'après mon expérience, il offre de loin la meilleure expérience de saisie et de balayage. Si vous téléchargez cette application, assurez-vous de désactiver complètement toutes les autorisations liées au réseau. Elle peut être téléchargée via Aurora.

![image](assets/17.webp)

Gauche : Notesnook
Droite : KDE Connect

### Style de vie

- [Geometric Weather](https://f-droid.org/en/packages/wangdaye.com.geometricweather/) est une application météo Open Source au design magnifique, disponible via F-Droid. Elle prend également en charge de nombreux formats de widgets différents, vous permettant ainsi de voir la météo dans l'emplacement de votre choix directement depuis votre écran d'accueil.
- [Translate You](https://f-droid.org/packages/com.bnyro.translate/) est une application de traduction Open Source respectueuse de la vie privée qui prend en charge plus de 200 langues. Translate You est disponible via F-Droid.
- [Proton Calendar](https://proton.me/calendar/download) est un calendrier simple à utiliser et E2EE qui interagit parfaitement avec vos comptes de messagerie Proton. Proton Calendar peut être téléchargé sous forme d'APK ou via le magasin Aurora.
- [PassAndroid](https://f-droid.org/en/packages/org.ligi.passandroid/) est une application permettant d'afficher et de stocker des cartes d'embarquement, des coupons, des billets de cinéma et des cartes de membre, etc. Il vous suffit de télécharger le fichier `pkpass` ou `espass` correspondant et de l'ouvrir avec l'application. PassAndroid est disponible via F-Droid.

![image](assets/19.webp)
Gauche : Geometric Weather
Droite : Proton Calendar

### Sécurité/Vie privée

- [Bitwarden](https://mobileapp.bitwarden.com/fdroid/) propose une solution de gestionnaire de mots de passe gratuite et E2EE multiplateforme pour tous vos appareils. Leur service payant vous permet d'intégrer des codes 2FA dans l'application. Le serveur de Bitwarden peut être auto-hébergé et l'application Android est disponible via F-Droid.
- [Proton Pass](https://proton.me/pass/download) propose un service gratuit similaire à Bitwarden, mais les clients [Proton Unlimited](https://proton.me/pricing) peuvent accéder à des fonctionnalités avancées supplémentaires. Proton Pass est disponible via APK ou Aurora.
- [FreeOTP](https://f-droid.org/packages/org.fedorahosted.freeotp/) est une application d'authentification à deux facteurs pour les systèmes utilisant des protocoles de mots de passe à usage unique. Les jetons peuvent être ajoutés facilement en scannant un code QR. FreeOTP est disponible via F-Droid.
- [Aegis](https://f-droid.org/en/packages/com.beemdevelopment.aegis/) est une application gratuite, sécurisée et open source pour Android qui permet de gérer vos jetons de vérification en deux étapes pour vos services en ligne. Aegis est disponible via F-Droid.
- [Cryptomator](https://f-droid.org/en/packages/org.cryptomator.lite/) est un service payant multiplateforme qui chiffre vos données localement afin que vous puissiez les télécharger en toute sécurité sur votre service cloud préféré. Cryptomator peut être téléchargé via F-Droid.

![image](assets/21.webp)
À gauche : Proton Pass
À droite : Bitwarden

### Solutions cloud

- [Proton Drive](https://proton.me/drive/download) est une solution cloud payante avec chiffrement de bout en bout pour sauvegarder et stocker tous vos fichiers. Au moment de la rédaction, ils viennent d'annoncer un client de bureau pour Windows, mais les utilisateurs Mac et Linux doivent continuer à utiliser la version web pour synchroniser depuis leurs ordinateurs (pour le moment). Le client Android est disponible en tant qu'APK ou via Aurora.
- [Skiff](https://skiff.com/download) propose également un stockage cloud payant avec chiffrement de bout en bout et des outils de collaboration sur les fichiers. Ils proposent un client de bureau pour Mac et Windows (ainsi qu'une application web) et leurs clients Android doivent être téléchargés depuis Aurora.
- [Nextcloud](https://f-droid.org/en/packages/com.nextcloud.client/) offre une solution cloud complète pour la collaboration, la synchronisation entre appareils et le stockage de fichiers. Les utilisateurs plus avancés peuvent choisir d'héberger eux-mêmes leur logiciel libre et open source sur n'importe quel matériel de leur choix. Les clients Android peuvent être téléchargés via F-Droid.
- [Cryptpad](https://cryptpad.fr/) propose une alternative gratuite et basée sur le web à Google Docs avec chiffrement de bout en bout.

![image](assets/23.webp)

Proton Drive

## Les inconvénients

Les alternatives open source et respectueuses de la vie privée aux applications des conglomérats technologiques auxquelles vous avez l'habitude d'utiliser sont nombreuses, et certaines d'entre elles sont souvent meilleures que les alternatives à code source fermé et remplies de logiciels espions.

Cependant, lorsque vous passez à GrapheneOS, il y a certains conforts auxquels vous devez renoncer en raison de l'absence d'alternatives. Il s'agit notamment de :

- **Apple CarPlay/Android Auto** - Vous devrez vous en tenir au bon vieux Bluetooth, USB ou Aux.
- **Apple/Google Pay** - Presque tout le monde porte son portefeuille de toute façon !
- **Applications bancaires** - Ce n'est pas que cela ne fonctionne pas du tout. Certaines fonctionnent parfaitement. D'autres ne fonctionnent qu'avec les services Google Play activés (lire plus à ce sujet ci-dessous) et d'autres ne fonctionnent tout simplement pas du tout. Consultez le rapport sur votre banque [ici](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/) pour connaître l'état actuel. Ne vous inquiétez pas si la vôtre est sur la liste des applications qui ne fonctionnent pas, rappelez-vous que vous pouvez simplement enregistrer l'URL en tant qu'application web sur votre écran d'accueil.
- **Notifications push** - La plupart des applications qui vous envoient des mises à jour lorsque vous n'utilisez pas une application spécifique le font via les services Google Play. Ceux-ci ne sont pas installés par défaut avec GrapheneOS, donc si vous constatez que vous n'êtes pas immédiatement notifié lorsque votre ami vous envoie un e-mail, c'est probablement la raison. La bonne nouvelle, c'est que certaines des applications mentionnées ci-dessus ont mis en place leur propre connexion en arrière-plan pour vérifier périodiquement les mises à jour et vous envoyer une notification si nécessaire.

### Google Play en mode sandbox
GrapheneOS dispose d'une couche de compatibilité offrant la possibilité d'installer et d'utiliser les versions officielles de Google Play dans l'environnement d'application standard. Google Play n'a absolument aucun accès spécial ou privilèges sur GrapheneOS, contrairement à la possibilité de contourner l'environnement d'application et d'obtenir un accès très privilégié.

Si vous constatez que vous ne pouvez tout simplement pas vous passer de ces notifications push pour votre application préférée ou si une certaine application "indispensable" est inutile sans les services Google Play, GrapheneOS vous permet d'installer ces services dans un environnement complètement isolé. Une fois installés, ces services ne nécessitent aucun compte Google pour fonctionner, et les autorisations de chaque service peuvent être étroitement contrôlées.

Avant de vous précipiter pour les installer dès le premier jour, je vous encourage à voir jusqu'où vous pouvez aller sans eux. Vous serez probablement surpris de voir combien d'applications fonctionnent parfaitement normalement sans eux.

Si vous souhaitez les installer, il vous suffit de toucher l'application préinstallée "Applications", puis "Services Google Play". Pensez à les installer aux côtés de ces applications moins privées dont vous ne pouvez pas vous passer, dans un profil utilisateur complètement séparé pour fournir une couche supplémentaire de ségrégation par rapport au reste de votre téléphone.

![image](assets/24.webp)

Écran d'installation des services Play

### Profils

GrapheneOS vous permet d'avoir une expérience téléphonique distincte au sein de votre téléphone. Les profils supplémentaires peuvent installer leurs propres applications et services et n'ont pas accès aux fichiers ou aux données du compte propriétaire.
Si vous n'avez qu'une ou deux de ces applications indispensables qui nécessitent les services Google Play, mais qui sont utilisées très rarement, l'installation de ces applications aux côtés des services Google Play dans un profil séparé pourrait être une excellente idée pour renforcer davantage les éventuelles implications de confidentialité laissées par leur exécution dans le profil propriétaire.

Vous pouvez en savoir plus sur ce cas d'utilisation [ici](https://discuss.grapheneos.org/d/168-ideas-for-user-profiles/2).

Si vous décidez d'ajouter un profil séparé pour répondre à votre cas d'utilisation, l'application [Insular](https://f-droid.org/en/packages/com.oasisfeng.island.fdroid/) pourrait vous être utile. Insular vous permet de cloner facilement l'une de vos applications existantes vers le nouveau profil sans passer par les méthodes d'installation traditionnelles mentionnées précédemment dans ce guide. Insular vous permet également de "geler" rapidement l'une de ces applications pour désactiver complètement tous les services en arrière-plan de cette application.

![image](assets/24.webp)

Écran de gestion des profils utilisateur

### e-SIM

Si vous souhaitez pousser votre confidentialité téléphonique à un niveau supérieur et disposer d'un service cellulaire détaché de votre identité réelle, une e-SIM pourrait vous convenir. Une e-SIM est une carte SIM virtuelle que vous pouvez acheter en ligne et ajouter à votre téléphone via un code QR. Les entreprises proposant de tels services, pouvant être payés de manière anonyme avec Bitcoin, incluent [Silent.Link](https://silent.link/) et [Bitrefill](https://www.bitrefill.com/gb/en/esims/).

Les e-SIM ne doivent pas être considérées comme une panacée complète pour la confidentialité téléphonique. Elles peuvent être un outil utile entre de bonnes mains, mais veuillez faire des recherches sur les [compromis](https://grapheneos.org/faq#cellular-tracking) liés à l'utilisation de tout type de service cellulaire si votre intention est de rester complètement "hors réseau".

Les services Google Play isolés doivent être installés pour la provision de l'e-SIM dans GrapheneOS.

## Sauvegardes

Après avoir configuré votre nouveau téléphone Pixel sans Google, il est conseillé de créer une sauvegarde. Cette sauvegarde vous permettra de restaurer le téléphone dans un état identique en cas de perte ou de vol de votre téléphone.
Vous pouvez choisir de stocker le fichier de sauvegarde sur n'importe quel support de stockage externe, ou sur une solution cloud auto-hébergée comme Nextcloud, bien que certains utilisateurs signalent des niveaux de réussite variables avec cette dernière option.
Pour créer votre première sauvegarde :

1. Allez dans **Paramètres** > **Système** > **Sauvegarde**, puis notez votre code de récupération de 12 mots. Ce code est nécessaire pour décrypter le fichier de sauvegarde ultérieurement. Perdez ce code, perdez l'accès à la sauvegarde de votre téléphone.
2. Ensuite, choisissez l'emplacement de stockage. Je recommande un disque USB externe ou une carte microSD de qualité industrielle.
3. Choisissez les données à sauvegarder. Si vous avez de l'espace sur votre support de stockage spécifié, je vous conseille de tout sélectionner.
4. Appuyez sur les trois points en haut à droite, puis choisissez **Sauvegarder maintenant**.

![image](assets/26.webp)

Écran de sauvegarde

N'oubliez pas que si vous effectuez des sauvegardes hors ligne sur des supports de stockage externes, il est judicieux de réaliser cette étape régulièrement pour vous assurer que toutes les mises à jour importantes récentes de votre téléphone ne sont pas perdues en cas de problème.

![video](https://www.youtube.com/embed/eyWmcItzisk)

Vidéo détaillant le processus de sauvegarde

## Conclusion

Ces dernières années, le logiciel GrapheneOS a considérablement évolué. Il est plus stable et compatible que jamais. Associé à l'écosystème d'applications Open Source et respectueuses de la vie privée en plein essor, GrapheneOS constitue une véritable alternative viable à Android ou iOS d'origine, même pour des personnes "normales" comme vous !

Les violations de données et la surveillance de masse sont si courantes dans le monde d'aujourd'hui qu'elles ne font presque plus les gros titres. C'est à vous de vous protéger. Des ajustements et des sacrifices devront être faits en cours de route, mais réduire votre exposition à de telles atteintes n'est pas aussi difficile que vous le pensez.

J'espère que ce guide vous aidera dans votre parcours. Si vous avez trouvé ce guide utile et souhaitez soutenir mon travail, veuillez envisager d'envoyer un [don](/tips).

Si vous êtes déjà utilisateur de GrapheneOS, ou si vous le devenez grâce à ce guide, envisagez de [faire un don](https://grapheneos.org/donate) pour soutenir leur travail important.

### En savoir plus

GrapheneOS est un véritable labyrinthe dans lequel n'importe qui pourrait facilement passer des semaines. Il y a tellement de choses à apprendre et à expérimenter pour personnaliser l'expérience en fonction de vos besoins et de vos modèles de menace. Voici quelques liens pour poursuivre votre voyage :

- [Guide d'utilisation officiel de GrapheneOS](https://grapheneos.org/usage) - Site officiel
- [Forum GrapheneOS](https://discuss.grapheneos.org/) - Site officiel
- [Cours magistral sur les paramètres de GrapheneOS](https://www.youtube.com/watch?app=desktop&v=GLJyD9MJgIQ) - Vidéo par 'The Privacy Wayfinder'
- [Podcast général sur GrapheneOS](https://www.youtube.com/watch?app=desktop&v=UCPX0mFFRNA) - Podcast par 'Watchman Privacy'

Crédit complet à : https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md
