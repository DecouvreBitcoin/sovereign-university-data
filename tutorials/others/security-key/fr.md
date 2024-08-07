---
name: YUBIKEY 2FA
description: Comment utiliser une clé de sécurité physique ?
---
![cover](assets/cover.webp)

De nos jours, l'authentification à deux facteurs (2FA) est devenue indispensable pour renforcer la sécurité des comptes en ligne face aux accès non autorisés. Avec l'augmentation des attaques informatiques, se reposer uniquement sur un mot de passe pour sécuriser vos comptes est parfois insuffisant.

Le 2FA introduit une couche de sécurité supplémentaire en requérant une seconde forme d'authentification en plus du mot de passe traditionnel. Cette vérification peut prendre plusieurs formes, comme un code envoyé par SMS, un code dynamique généré par une application dédiée, ou encore l'utilisation d'une clé de sécurité physique. L'utilisation du 2FA diminue grandement les risques de compromission de vos comptes, même en cas de vol de votre mot de passe.

Dans un autre tutoriel, je vous expliquais comment mettre en place et utiliser une application de 2FA TOTP :

https://planb.network/tutorials/others/authy

Ici, nous allons voir comment utiliser une clé de sécurité physique comme second facteur d'authentification pour tous vos comptes.

## C'est quoi une clé de sécurité physique ?

Une clé de sécurité physique est un dispositif utilisé pour renforcer la sécurité de vos comptes en ligne grâce à l'authentification à deux facteurs (2FA). Ces appareils ressemblent souvent à de petites clés USB que l'on doit insérer dans un port de l'ordinateur pour vérifier que c'est bien l'utilisateur légitime qui tente de se connecter.
![SECURITY KEY 2FA](assets/notext/01.webp)
Lorsque vous vous connectez à un compte protégé par 2FA et que vous utilisez une clé de sécurité physique, vous devez non seulement entrer votre mot de passe habituel, mais aussi insérer la clé de sécurité physique dans votre ordinateur et appuyer sur un bouton pour valider l'authentification. Cette méthode ajoute donc une couche de sécurité supplémentaire, car même si quelqu'un parvient à obtenir votre mot de passe, il ne pourra pas accéder à votre compte sans posséder physiquement la clé.

La clé de sécurité physique est particulièrement efficace car elle combine deux facteurs d'authentification de nature différente : la preuve de connaissance (le mot de passe) et la preuve de possession (la clé physique).

Toutefois, cette méthode de 2FA présente aussi des inconvénients. Premièrement, vous devez toujours avoir la clé de sécurité à disposition si vous souhaitez accéder à vos comptes. Il faudra peut-être l'ajouter à votre trousseau de clés. Secondement, contrairement à d'autres méthodes de 2FA, l'utilisation d'une clé de sécurité physique implique un coût initial puisqu'il faut acheter le petit appareil. Le prix des clés de sécurité varie généralement entre 30 € et 100 € en fonction des fonctionnalités choisies.

## Quelle clé de sécurité physique choisir ?

Pour choisir votre clé de sécurité, plusieurs critères sont à prendre en compte.

Tout d'abord, vous devez vérifier les protocoles pris en charge par l'appareil. Au minimum, je vous conseille de choisir une clé qui prend en charge OTP, FIDO2 et U2F. Ces informations sont généralement mises en avant par les fabricants dans les descriptions de produits. Pour vérifier les compatibilités de chaque clé, vous pouvez également consulter le site [dongleauth.com](https://www.dongleauth.com/dongles/).

Vérifiez également que la clé est compatible avec votre système d'exploitation, même si les marques connues comme Yubikey supportent généralement tous les systèmes largement utilisés.

Il faut également choisir la clé en fonction du type de ports disponibles sur votre ordinateur ou votre smartphone. Par exemple, si votre ordinateur n'a que des ports USB-C, choisissez une clé avec une connectique USB-C. Certaines clés offrent également des options de connexion via Bluetooth ou NFC.
![SECURITY KEY 2FA](assets/notext/02.webp)
Vous pouvez aussi comparer les appareils en fonction de leurs caractéristiques supplémentaires comme la résistance à l'eau et à la poussière, ainsi que la forme et la taille de la clé.

Concernant les marques de clés de sécurité, Yubico est la plus connue avec ses [appareils YubiKey](https://www.yubico.com/), que j'utilise personnellement et que je vous recommande. Google propose également un appareil avec la [clé de sécurité physique Titan](https://store.google.com/fr/product/titan_security_key). Pour des alternatives open-source, [SoloKeys](https://solokeys.com/) (non OTP) et [NitroKey](https://www.nitrokey.com/products/nitrokeys) sont des options intéressantes, mais je n'ai jamais eu l'occasion de les tester.

## Comment utiliser une clé de sécurité physique ?

Une fois que vous avez reçu votre clé de sécurité, aucune configuration spécifique n'est nécessaire. La clé est normalement prête à l'emploi dès sa réception. Vous pouvez immédiatement l'utiliser pour sécuriser vos comptes en ligne qui supporte ce type d'authentification. Pour l'exemple, je vais vous montrer comment sécuriser ma boîte mail Proton avec cette clé de sécurité physique.
![SECURITY KEY 2FA](assets/notext/03.webp)
Vous trouverez l'option pour activer le 2FA dans les paramètres de votre compte, souvent sous la section "*Password*" ou "*Security*". Cliquez sur la coche ou le bouton vous permettant d'activer le 2FA avec clé physique.
![SECURITY KEY 2FA](assets/notext/04.webp)
Branchez votre clé sur votre ordinateur.
![SECURITY KEY 2FA](assets/notext/05.webp)
Touchez le bouton de votre clé de sécurité pour valider.
![SECURITY KEY 2FA](assets/notext/06.webp)
Entrer un nom pour vous souvenir de la clé utilisée.
![SECURITY KEY 2FA](assets/notext/07.webp)
Et voilà, votre clé de sécurité a bien été ajoutée pour l'authentification 2FA de votre compte.
![SECURITY KEY 2FA](assets/notext/08.webp)
Dans mon exemple, si je tente de me reconnecter à ma boite mail Proton, on va d'abord me demander de renseigner mon mot de passe avec mon identifiant. C'est le premier facteur d'authentification.
![SECURITY KEY 2FA](assets/notext/09.webp)
Puis, on me demande de brancher ma clé de sécurité pour le second facteur d'authentification.
![SECURITY KEY 2FA](assets/notext/10.webp)
Il faut ensuite toucher le bouton de la clé physique pour valider l'authentification, et je suis de nouveau connecté à ma boite mail Proton.
![SECURITY KEY 2FA](assets/notext/11.webp)
Répétez cette opération pour tous les comptes en ligne que vous souhaitez sécuriser de cette manière, particulièrement pour les comptes critiques tels que vos boîtes mail, vos gestionnaires de mots de passe, vos services de cloud et de stockage en ligne ou encore vos comptes financiers.
