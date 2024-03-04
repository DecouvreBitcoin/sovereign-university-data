---
name: Linux Mint

description: Configuration d'un ordinateur pour les transactions Bitcoin
---

![image](assets/cover.jpeg)

## Qu'est-ce qui ne va pas si vous utilisez un ordinateur ordinaire ?

Lorsque vous effectuez des transactions Bitcoin, il est idéal que votre ordinateur ne contienne aucun logiciel malveillant. Évidemment.

Si vous gardez votre phrase de récupération Bitcoin (généralement composée de 12 ou 24 mots) hors de l'ordinateur avec un dispositif de signature (par exemple, un portefeuille matériel - son objectif principal), vous pourriez penser qu'il n'est pas si important d'avoir un ordinateur "propre" - ce n'est pas vrai.

Un ordinateur infecté par des logiciels malveillants peut lire vos adresses Bitcoin, exposant ainsi votre solde à un attaquant - ils ne peuvent pas prendre de bitcoins simplement en connaissant l'adresse, mais ils peuvent voir combien vous en avez et calculer à partir de là si vous êtes une cible intéressante. Ils peuvent également découvrir où vous habitez, par exemple, et vous extorquer de l'argent en vous menaçant de vous arracher les ongles ou de kidnapper vos enfants.

## Quelle est la solution ?

J'encourage la plupart des utilisateurs de Bitcoin à utiliser un ordinateur dédié exempt de logiciels malveillants (avec accès à Internet) pour effectuer des transactions Bitcoin. Je suggère aux gens d'utiliser un système d'exploitation open-source comme Linux Mint, mais utilisez Windows ou Mac si vous le devez - c'est mieux que d'utiliser un ordinateur ordinaire bien utilisé qui contient invariablement des logiciels malveillants cachés.

Un obstacle auquel les gens se heurtent est l'installation d'un nouveau système d'exploitation sur de tels ordinateurs. Ce guide est là pour vous aider.

Il existe de nombreuses variantes de Linux et j'en ai essayé plusieurs. Ma recommandation pour les utilisateurs de Bitcoin est Linux Mint, car il est facile à installer, très rapide (en particulier au démarrage et à l'arrêt), peu encombrant (chaque logiciel supplémentaire représente un risque) et il a rarement planté ou eu un comportement étrange (comparé à d'autres versions comme Ubuntu et Debian).

Certains peuvent être très réticents à utiliser un nouveau système d'exploitation, préférant Windows ou Mac OS. Je comprends, mais les systèmes d'exploitation Windows et Apple sont des logiciels propriétaires, nous devons donc faire confiance à ce qu'ils font ; je ne pense pas que ce soit une bonne politique, mais ce n'est pas tout ou rien. Je préférerais beaucoup plus que les gens utilisent un ordinateur Windows ou Mac OS fraîchement installé et dédié plutôt qu'un ordinateur bien utilisé (avec qui sait quels logiciels malveillants se sont accumulés dessus). Une étape de mieux est d'utiliser un ordinateur Linux fraîchement installé, ce que je vais vous montrer.

Si vous êtes nerveux à l'idée d'utiliser Linux en raison de l'inconnu, c'est normal, mais il est également normal de consacrer du temps à l'apprentissage. Tant d'informations sont disponibles en ligne. Voici une excellente courte vidéo qui présente les bases de la ligne de commande que je recommande vivement.
Choisissez un ordinateur

Je vais commencer par ce que je pense être la meilleure option. Ensuite, je donnerai mon avis sur les alternatives.

Option idéale :

Ma recommandation, si vous en avez les moyens et si la taille de votre portefeuille Bitcoin le justifie, est d'acheter un tout nouvel ordinateur portable d'entrée de gamme. Le modèle le plus basique construit de nos jours est suffisamment performant pour ce qu'il va être utilisé. Les spécifications du processeur et de la RAM ne sont pas pertinentes, car elles seront toutes suffisamment bonnes.

À éviter :

- Tout combo tablette, y compris le Surface Pro
- Les Chromebooks - souvent la capacité de stockage est trop faible
- Tout ordinateur avec un disque eMMC ; s'il a un disque SSD, c'est parfait
- Les Mac - ils sont chers et le matériel ne fonctionne pas bien avec les systèmes d'exploitation Linux d'après mon expérience
- Tout ce qui est reconditionné ou d'occasion (ce n'est pas un critère absolu pour rejeter l'option)
  Au lieu de cela, recherchez un ordinateur portable Windows 11 (actuellement, Windows 11 est la dernière version. Nous nous débarrasserons de ce logiciel, ne vous inquiétez pas.). J'ai cherché sur amazon.com un "ordinateur portable Windows 11" et j'ai trouvé cet bon exemple :
  ![image](assets/1.webp)

Le prix de celui-ci ci-dessus est bon. Les spécifications sont suffisantes. Il a une caméra intégrée que nous pouvons utiliser pour les transactions QR code PSBT (sinon, vous devriez acheter une caméra USB pour le faire). Ne vous inquiétez pas du fait que ce n'est pas une marque bien reconnue (c'est bon marché). Si vous voulez une meilleure marque, cela vous coûtera, par exemple :

![image](assets/2.webp)

Certains des moins chers n'ont que 64 Go d'espace de stockage ; je n'ai pas testé d'ordinateurs portables avec des disques aussi petits - il est probablement possible d'avoir 64 Go, mais cela pourrait être limite.

## Autres options - Tails

Tails est un système d'exploitation qui démarre à partir d'une clé USB et prend temporairement le contrôle du matériel de n'importe quel ordinateur. Il utilise uniquement des connexions Tor, donc vous devez être à l'aise avec l'utilisation de Tor. Aucune des données que vous écrivez en mémoire pendant votre session n'est enregistrée sur le disque (elle démarre à chaque fois à partir de zéro), sauf si vous modifiez les paramètres et créez une option de stockage permanente (sur la clé USB) - que vous verrouillez avec un mot de passe.

Ce n'est pas une mauvaise option et c'est gratuit, mais c'est un peu lourd pour notre objectif. L'installation de nouveaux logiciels n'est pas facile. Une bonne fonctionnalité est qu'il est livré avec Electrum, mais l'inconvénient est que vous ne l'avez pas installé vous-même. Assurez-vous que la clé USB que vous utilisez a au moins 8 Go.

Votre flexibilité est réduite si vous utilisez Tails. Vous ne pourrez peut-être pas suivre divers guides pour configurer ce dont vous avez besoin et le faire fonctionner correctement. Par exemple, si vous suivez mon guide pour installer Bitcoin Core, des modifications sont nécessaires pour le faire fonctionner. Je ne pense pas faire un guide spécifique pour Tails, donc vous devrez développer vos compétences et le faire seul.

Je ne suis pas non plus sûr de la compatibilité des portefeuilles matériels avec ce système d'exploitation.

Cela dit, un ordinateur Tails pour les transactions Bitcoin est une bonne option supplémentaire et vous aidera certainement à améliorer vos compétences en matière de confidentialité en apprenant à utiliser Tails.

## Autres options - Live OS Boot

C'est très similaire à Tails, sauf que le système d'exploitation n'est pas dédié à la confidentialité. La façon de l'utiliser de base est de flasher une clé USB avec le système d'exploitation Linux de votre choix et de faire démarrer l'ordinateur à partir de là au lieu du disque interne. Comment faire cela est expliqué plus tard.

L'avantage est que vous êtes moins restreint et que les choses fonctionneront sans réglages avancés.

Je ne suis pas sûr de la capacité d'un tel système à isoler les logiciels malveillants sur l'ordinateur existant de la clé USB de démarrage que vous utilisez pour le nouveau système d'exploitation. Il fait probablement du bon travail et n'est probablement pas aussi bon que Tails. Parce que je ne sais pas, ma préférence va vers l'ordinateur portable dédié.
Autres options - Votre propre ordinateur portable ou ordinateur de bureau d'occasion

Utiliser un ordinateur d'occasion n'est pas idéal, principalement parce que j'ignore le fonctionnement interne des logiciels malveillants sophistiqués, ni si le formatage d'un disque suffit à s'en débarrasser. C'est probablement le cas, mais je ne veux pas sous-estimer l'ingéniosité des pirates malveillants. Vous pouvez décider, je ne veux pas m'engager.
Si vous choisissez d'utiliser un ancien ordinateur de bureau plutôt qu'un ancien ordinateur portable, cela ira bien, sauf que cela occupera définitivement de l'espace pour vos transactions bitcoin probablement rares ; vous ne devriez pas l'utiliser pour autre chose. Alors qu'avec un ordinateur portable, vous pouvez simplement le ranger et même le cacher pour une sécurité supplémentaire.

## Installation de Linux Mint sur n'importe quel ordinateur

Voici les instructions pour effacer n'importe quel système d'exploitation de votre nouvel ordinateur portable et installer Linux Mint, mais vous pouvez les adapter pour installer à peu près n'importe quelle version de Linux sur à peu près n'importe quel ordinateur.

Nous allons utiliser n'importe quel ordinateur pour transférer le système d'exploitation sur une clé USB ou un autre support de stockage. Peu importe lequel, tant qu'il est compatible avec un port USB, et je suggère un minimum de 16 Go.

Obtenez l'un de ces éléments :

![image](assets/3.webp)

Ou vous pouvez utiliser quelque chose comme ceci :

![image](assets/4.webp)

Ensuite, rendez-vous sur linuxmint.com

![image](assets/5.webp)

Survolez le menu Téléchargement en haut, puis cliquez sur le lien "Linux Mint 20.3" ou quelle que soit la version recommandée la plus récente au moment où vous faites cela.

![image](assets/6.webp)

Il y aura quelques "saveurs" parmi lesquelles choisir. Optez pour "Cinnamon" pour suivre ce guide. Cliquez sur le bouton Télécharger.

![image](assets/7.webp)

Sur la page suivante, vous pouvez faire défiler vers le bas pour voir les miroirs (les miroirs sont différents serveurs qui contiennent une copie du fichier que nous voulons). Vous pouvez vérifier le téléchargement à l'aide de SHA256 et gpg (recommandé), mais je vais passer à expliquer cela ici car j'ai déjà rédigé des guides à ce sujet.

![image](assets/8.webp)

Choisissez un miroir qui est le plus proche de chez vous et cliquez sur son lien (le texte vert dans la colonne du miroir). Le fichier commencera à se télécharger - la version que je télécharge fait 2,1 gigaoctets.

Une fois le téléchargement terminé, vous pouvez transférer le fichier sur un support de stockage portable et le rendre bootable. Pour cela, la manière la plus simple est d'utiliser Balena Etcher. Téléchargez-le et installez-le si vous ne l'avez pas.

Ensuite, exécutez-le :

![image](assets/9.webp)

Cliquez sur "Flash from file" et sélectionnez le fichier LinuxMint que vous avez téléchargé.

Ensuite, cliquez sur "Select target". Assurez-vous que le support de stockage est branché et assurez-vous de sélectionner le bon lecteur, sinon vous risquez de détruire le contenu du mauvais lecteur !

Après cela, sélectionnez "Flash !" Vous devrez peut-être entrer votre mot de passe. Lorsque c'est terminé, le lecteur ne sera probablement pas lisible par votre ordinateur Windows ou Mac car il a été transformé en un périphérique Linux. Il suffit de le retirer.
Préparation de l'ordinateur cible

Allumez le nouvel ordinateur portable et, pendant qu'il démarre, maintenez enfoncée la touche du BIOS. Il s'agit généralement de F2, mais cela peut être F1, F8, F10, F11, F12 ou Suppr. Essayez chacune d'entre elles jusqu'à ce que vous l'obteniez, ou recherchez sur Internet le modèle de votre ordinateur et posez la bonne question.

Par exemple, "touche du BIOS pour les ordinateurs portables Dell".

Chaque ordinateur aura un menu BIOS différent. Explorez et trouvez le menu qui vous permet de configurer l'ordre de démarrage. Dans notre cas, nous voulons que l'ordinateur essaie de démarrer à partir d'un périphérique USB connecté (s'il y en a un connecté), avant de tenter de démarrer à partir du disque dur interne (sinon Windows se chargera). Une fois que vous avez défini cela, vous devrez peut-être enregistrer avant de quitter ou cela peut s'enregistrer automatiquement.

Redémarrez l'ordinateur et il devrait démarrer à partir du périphérique de stockage USB. Nous pouvons maintenant installer Linux sur le disque interne et Windows sera définitivement supprimé.
Lorsque vous arrivez à l'écran suivant, sélectionnez "Installation OEM (pour les fabricants)". Si vous choisissez plutôt "Démarrer Linux Mint", vous obtiendrez une session Linux Mint chargée à partir du périphérique mémoire, mais une fois que vous éteignez l'ordinateur, aucune de vos informations n'est enregistrée - c'est essentiellement une session temporaire pour que vous puissiez l'essayer.
![image](assets/10.webp)

Vous serez guidé à travers un assistant graphique qui vous posera plusieurs questions qui devraient être simples. L'une d'entre elles sera les paramètres de langue, une autre sera votre connexion Internet à domicile et votre mot de passe. Si on vous demande d'installer un logiciel supplémentaire, refusez. Lorsque vous arrivez à la question sur le type d'installation, certaines personnes peuvent hésiter - vous devez choisir "Effacer le disque et installer Linux Mint". De plus, ne chiffrez pas le disque et ne sélectionnez pas LVM.

Vous arriverez finalement sur le bureau. À ce stade, vous n'avez pas tout à fait terminé. Vous agissez en réalité en tant que fabricant (c'est-à-dire quelqu'un qui assemble un ordinateur et configure Linux pour le client). Vous devez double-cliquer sur l'icône du bureau, "Installer Linux Mint", pour finaliser l'installation.

![image](assets/11.webp)

N'oubliez pas de retirer la clé USB, puis redémarrez. Après le redémarrage, vous utiliserez le système d'exploitation pour la première fois en tant que nouvel utilisateur. Félicitations.

Une des premières choses à faire (et à faire régulièrement) est de maintenir le système à jour.

Ouvrez l'application Terminal et tapez ce qui suit :

```
    sudo apt-get update
```

appuyez sur <enter>, confirmez votre choix, puis cette commande :

```
    sudo apt-get upgrade
```

appuyez sur <enter> et confirmez votre choix.

Laissez-le faire son travail, cela peut prendre plusieurs minutes.

Ensuite, j'aime installer Tor (sensible à la casse) :

```
    sudo apt-get install tor
```

> _AJOUT : Vous pouvez également exécuter le démarrage de Linux Mint à partir de "l'installation OEM" (Assurez-vous d'être connecté à Internet, sinon vous pourriez rencontrer des erreurs). Si vous faites cela, vous devrez ensuite cliquer sur l'icône "envoyer à l'utilisateur final" qui devrait se trouver sur le bureau. Vous redémarrez ensuite et démarrez le système d'exploitation comme si vous ouvriez l'ordinateur pour la première fois._

Ce guide explique pourquoi vous pourriez avoir besoin d'un ordinateur dédié aux transactions Bitcoin et comment installer un système d'exploitation Linux Mint frais dessus.
