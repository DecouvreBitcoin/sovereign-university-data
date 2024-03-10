---
name: NOSTR

description: Descubre y comienza a usar NOSTR
---

Al final de esta guía, comprenderás qué es Nostr, habrás creado una cuenta y podrás utilizarla.

![Un nuevo retador ha llegado](assets/1.webp)

## ¿Qué es Nostr?

Nostr es un protocolo que tiene el poder de reemplazar a Twitter, Telegram y otras redes sociales. Es un protocolo abierto y simple que puede crear una red social global resistente a la censura de una vez por todas.

## ¿Cómo funciona?

Nostr se basa en tres componentes: pares de claves, clientes y relés.

Cada usuario tiene una o varias identidades, cada identidad está determinada por un par de claves criptográficas.

Para acceder a la red, es necesario utilizar un software cliente y conectarse a relés para recibir y emitir contenido.

![Sistema de claves](assets/2.webp)

## 1. Las claves criptográficas

A diferencia de Facebook o Twitter, donde el usuario debe proporcionar una dirección de correo electrónico y una gran cantidad de información a una empresa privada, Nostr funciona sin una autoridad central. El usuario genera un par de claves criptográficas, una clave secreta (también conocida como clave privada) y una clave pública.

La clave secreta, nsec, conocida solo por el usuario, se utiliza para autenticarse y publicar contenido.

La clave pública, npub, es un identificador único al que se adjunta todo el contenido publicado por un usuario. Tu clave pública es una especie de nombre de usuario que permite a otros usuarios encontrarte y suscribirse a tu feed de Nostr.

## 2. Los clientes

Los clientes son software que permiten interactuar con Nostr. Los principales clientes son:

> iOS: damus
> Android: amethyst
> Web: iris.to; snort.social; astral.ninja

Los clientes permiten a un usuario generar un nuevo par de claves (equivalente a crear una cuenta) o autenticarse con un par de claves existente.

## 3. Los relés

Los relés son servidores simples que puedes abandonar en cualquier momento si no te gusta el contenido que te envían. También puedes ejecutar tu propio relé si lo deseas.

> 💡 Consejo profesional: Los relés de pago suelen ser más eficientes para filtrar el spam y el contenido no deseado.

# Guía

Ahora que conoces lo suficiente sobre Nostr, puedes comenzar y crear tu primera identidad en este protocolo.

Para los fines de esta guía, utilizaremos iris.to (https://iris.to/) ya que este cliente web funciona en cualquier plataforma.

## Paso 1: Generación de claves

ris creará un juego de claves para ti sin que tengas que hacer nada más que ingresar un nombre (real o ficticio) para tu perfil. Luego haz clic en GO y ¡listo!

![Menú principal](assets/3.webp)

> ⚠️ ¡Atención! Deberás guardar un registro de tus claves si quieres poder acceder nuevamente a tu perfil una vez que cierres tu sesión. Te mostraré cómo hacerlo al final de esta guía.

## Paso 2: Publicar contenido

Para publicar contenido, simplemente escribe algunas palabras en el campo de publicación.

![Publicación](assets/4.webp)

¡Listo! Has publicado tu primer nota en Nostr.

![Publicación](assets/5.webp)

## Paso 3: Encontrar un amigo

Encuéntrame en Nostr y nunca más estarás solo. Me suscribiré a todos aquellos que se suscriban a mi feed. Para hacerlo, simplemente ingresa mi clave pública

npub1hartx53w6t3q5wv9xdqdwrk7h6r5866t8u775q0304zedpn5zgssasp7d3 en la barra de búsqueda.

![Mi perfil](assets/6.webp)

Haz clic en "seguir" y en unos días, también me suscribiré a tu feed. Seremos amigos. También me encantará leerte si quieres escribirme un mensaje.

Finalmente, asegúrate de suscribirte al feed de Agora256 para recibir una nota cada vez que publiquemos algo nuevo: npub1ag0rawstycy7nanuc6sz4v287rneen2yapcq3fd06972f8ncrhzqx

## Paso 4: Personaliza tu perfil

Aún tienes un poco de trabajo por hacer para personalizar tu perfil. Para ello, haz clic en el avatar que Iris ha generado automáticamente para ti en la esquina superior derecha de la pantalla y luego haz clic en "editar perfil".

![Perfil](assets/7.webp)

Solo tienes que indicarle a Iris dónde encontrar tu imagen y tu banner de perfil en la web. Te recomiendo que alojes tu propio contenido: protege lo que es tuyo.

![Otra opción](assets/8.webp)

Si lo prefieres, también puedes descargar imágenes, Iris las almacenará por ti en nostr.build, un servicio gratuito de alojamiento de contenido visual para Nostr.

Como puedes ver, también puedes configurar tu cliente para poder recibir y enviar sats. Así podrás recompensar a los autores de contenido que te gusten o, mejor aún, acumular sats por el contenido increíble que publiques.

## Paso 5: Respaldo del par de claves

Este paso es crucial si quieres mantener el acceso a tu perfil una vez que te desconectes del cliente o que tu sesión haya expirado.
'D'abord, clique sur l'icône "settings" représentée par un engrenage
![Setting](assets/9.webp)

Puis, copie-colle à tour de rôle tes npub, npub hex, nsec et nsec hex dans un fichier texte que tu garderas en sécurité. Je te recommande de crypter ce fichier, si tu sais comment le faire.

![Clef](assets/10.webp)

> ⚠️ Remarque bien l'avertissement que te donne iris. Si tu peux partager ta clé publique sans crainte, il en est tout autrement de ta clé privée. Quiconque possède cette dernière pourra accéder à ton compte.

## Conclusion

Ça y est, petite autruche, tu as fait tes premiers pas sur Nostr. Maintenant, il te faudra apprendre à courir à la vitesse de l'éclair. Nous publierons prochainement des guides qui te montreront à gérer tes clés et comment intégrer lightning à ton expérience Nostr à l'aide de getalby.
