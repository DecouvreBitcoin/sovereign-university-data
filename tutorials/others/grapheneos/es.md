---
name: GrapheneOS

description: Tutorial de Graphene OS
---

> "[GrapheneOS](https://grapheneos.org/) es un sistema operativo móvil centrado en la privacidad y la seguridad, con compatibilidad de aplicaciones de Android, desarrollado como un proyecto de código abierto sin fines de lucro."

GrapheneOS, fundado originalmente en 2014 como 'CopperheadOS', se basa en el código tradicional de Android (AOSP), pero con muchos cambios y mejoras destinados a mejorar la privacidad y seguridad del usuario. GrapheneOS pone al usuario en control de su teléfono, no a las grandes empresas tecnológicas.

### Resumen:

- Introducción
- Preparación
- Instalación
- Alternativas de aplicaciones
- Desventajas
- Información útil

Guía de https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md

## ¿Por qué usar GrapheneOS?

Los teléfonos modernos son dispositivos de seguimiento y recolección de datos de $500 a $1000. Cada aspecto de nuestra vida pasa por ellos y, desafortunadamente, gran parte de estos datos se comparte con terceros de alguna forma u otra. GrapheneOS está diseñado específicamente para reducir esta compartición de datos y mejorar la seguridad de su dispositivo frente a posibles vectores de ataque. No existe tal cosa como una cuenta de GrapheneOS. No necesitas una para descargar aplicaciones o interactuar con el sistema operativo. En pocas palabras, tú no eres el producto.

GrapheneOS proporciona seguridad adicional a tu experiencia de Android a través de algunos principios básicos.

1. **Reducción de la superficie de ataque** - Elimina código innecesario (o software innecesario).
2. **Prevención de exposición a vulnerabilidades** - Permite al usuario suficiente granularidad para elegir los compromisos con los que se sienten cómodos.
3. **Contención de sandbox** - GrapheneOS fortalece los sandbox existentes de Android, limitando aún más la capacidad de cada aplicación para comunicarse con el resto de tu teléfono.

Obtén más información sobre los detalles técnicos del conjunto de funciones de GrapheneOS [aquí](https://grapheneos.org/features).

### Facilitando la transición

Si has estado inmerso en el ecosistema de Google o Apple durante años, la idea de perder toda esa comodidad de la noche a la mañana puede ser aterradora. Pero con algunas decisiones cuidadosas sobre la instalación de aplicaciones (que se tratarán más adelante), gran parte de esta dificultad esperada se puede reducir o eliminar.

Aunque las alternativas están mejorando, la idea de un cambio así todavía puede resultar desalentadora. Si te encuentras en esta situación, mi mejor consejo es que utilices tu nuevo dispositivo GrapheneOS junto con tu teléfono actual durante un tiempo. A partir de ahí, puedes ir reduciendo gradualmente el uso de 2-3 aplicaciones por semana hasta que te encuentres usando solo tu dispositivo GrapheneOS.

Si adoptas este enfoque, sé estricto contigo mismo y corta tu dependencia de las alternativas vigiladas lo más rápido posible. Los humanos somos perezosos y a menudo elegimos el camino de menor resistencia. Recuerda por qué hiciste el cambio en primer lugar.

**En lugar de pagar con tus datos personales, elegiste pagar con tu tiempo y, a veces, con tu dinero ganado con esfuerzo (dependiendo de las aplicaciones alternativas que instales).**

## Empezando

Actualmente, GrapheneOS solo está disponible para la gama de teléfonos [Google Pixel](https://grapheneos.org/faq#supported-devices) (lo cual es irónico). Sin embargo, esto no es sin una buena razón. Los Pixel ofrecen la mejor seguridad basada en hardware para complementar el trabajo realizado para fortalecer el sistema operativo. Esto incluye cosas como aislamientos de componentes específicos y arranque verificado.

### Elegir un dispositivo

Al elegir el Pixel en el que deseas instalar GrapheneOS, asegúrate de verificar durante cuánto tiempo el dispositivo seguirá recibiendo [actualizaciones de seguridad](https://support.google.com/pixelphone/answer/4457705?hl=en#zippy=%2Cpixel-xl-a-a-g-a-g) predeterminadas.
En el momento de escribir este texto, el Pixel 6a es el modelo más económico disponible con un buen soporte a largo plazo, garantizado hasta julio de 2027. Si eliges este modelo, la desbloqueo OEM no funcionará con la versión del sistema operativo original de fábrica. Debes actualizarlo a la versión de junio de 2022 o posterior a través de una actualización por aire. Después de actualizarlo, también deberás restablecer los valores de fábrica del dispositivo para solucionar el desbloqueo OEM. Todos los demás modelos que estén desbloqueados por el operador estarán listos para GrapheneOS directamente desde la caja.

Al elegir un dispositivo, también debes asegurarte de comprar una versión desbloqueada. Ciertos operadores como Verizon envían sus unidades con el gestor de arranque bloqueado, lo que impide por completo el siguiente proceso.

### Instalación de GrapheneOS

El instalador web de GrapheneOS [web installer](https://grapheneos.org/install/web) hace que todo el proceso sea muy sencillo y puede ser completado por cualquier persona en menos de 10 minutos.
Las siguientes instrucciones son una versión resumida tomada del enlace mencionado anteriormente.

Todo lo que necesitas tener a mano es:

- El Pixel
- Un cable USB para conectar el teléfono a tu computadora
- Una computadora para ejecutar un navegador web (cualquier navegador basado en Chromium: Chrome, Edge, Brave, etc.)

1. El primer paso es ir a **Configuración** > **Acerca del teléfono** y tocar repetidamente el número de compilación hasta que veas que se activa **'Modo desarrollador'**.
2. A continuación, ve a **Configuración** > **Sistema** > **Opciones de desarrollador** y activa **'Desbloqueo OEM'**.
3. Reinicia el dispositivo y mantén presionado el botón de volumen hacia abajo mientras el teléfono se enciende nuevamente.
4. Conecta el teléfono a tu computadora portátil y, si se solicita autorización, permite la conexión.
5. En la página del instalador web, haz clic en 'Desbloquear el gestor de arranque'.
6. Luego verás que cambian las opciones del teléfono. Usa el botón de volumen para cambiar la selección a `desbloquear` y usa el botón de encendido para aceptar.
7. A continuación, haz clic en descargar versión en la página del instalador web.
8. Una vez que se haya descargado por completo, pasa al siguiente paso y haz clic en 'Flashear versión'. Esto tomará uno o dos minutos y no necesitas tocar el teléfono en absoluto.
9. Por último, pasa al siguiente paso del instalador web y haz clic en **Bloquear gestor de arranque**. Deberás cambiar la selección y confirmar con el botón de encendido de la misma manera que hiciste anteriormente en el proceso.
10. Cuando veas la palabra `Iniciar`, confírmala con el botón de encendido y el dispositivo se iniciará en tu nuevo sistema operativo sin Google.

![image](assets/2.webp)

Pantalla de inicio de GrapheneOS

_Después del inicio y la configuración inicial, es buena práctica desactivar el desbloqueo OEM desde Configuración > Sistema > Opciones de desarrollador._

_También puedes considerar el paso adicional, opcional pero recomendado, de verificar la instalación a través de la aplicación Auditor. Necesitarás un teléfono Android separado con la aplicación instalada para completar este paso. Las instrucciones se pueden encontrar [aquí](https://attestation.app/tutorial)._


![video](https://www.youtube.com/embed/L1KZWjZVnAw)

Video que detalla los sencillos pasos mencionados anteriormente

Si esos sencillos pasos parecen demasiado complicados, puedes considerar comprar un Pixel con el software GrapheneOS [preinstalado](https://ronindojo.io/en/roninmobile). Solo ten en cuenta que estás depositando una pequeña cantidad de confianza en el proveedor.

### Aplicaciones preinstaladas

Ahora que estás configurado, es posible que notes lo básico que parece GrapheneOS después de la primera instalación. Por defecto, tendrás estas aplicaciones instaladas:

![image](assets/3.webp)

Aplicaciones predeterminadas
Los únicos dos términos con los que es posible que no estés familiarizado son 'Auditor' y 'Vanadium'.
- 'La [aplicación Auditor](https://play.google.com/store/apps/details?id=app.attestation.auditor) utiliza características de seguridad basadas en hardware para validar la identidad de un dispositivo junto con la autenticidad y la integridad del sistema operativo. Verificará que el dispositivo esté ejecutando el sistema operativo original con el gestor de arranque bloqueado y que no se haya producido ninguna manipulación del sistema operativo.'
- [Vanadium](https://github.com/GrapheneOS/Vanadium) es una variante del navegador web Chromium con mayor privacidad y seguridad.

## Personalización

La configuración del teléfono es algo personal, pero aquí hay algunos de los primeros elementos que cambio al instalar GrapheneOS para sentirme más cómodo.

### Establecer un fondo de pantalla y actualizar el tema

Ve a Configuración > Fondo de pantalla y estilo. Desde aquí:

- Actualizo los fondos de pantalla de la pantalla de inicio y de bloqueo con imágenes descargadas de la web.
- Elijo los colores de acento que se utilizan en toda la interfaz de usuario.
- Habilito el tema oscuro.

### Mostrar el porcentaje de batería

Ve a **Configuración** > **Batería**, luego habilita **Mostrar porcentaje de batería** en la barra de estado.

### Importar contactos

**Desde otro teléfono Android** - Ve a la aplicación Contactos y busca la opción Exportar a VCF.

**Desde iOS** - Utiliza una aplicación como Export Contact y utiliza la opción de exportar 'vCard' para exportar un archivo VCF.
Una vez que tengas el archivo VCF, puedes transferirlo a tu dispositivo GrapheneOS con una opción de almacenamiento externo como una tarjeta microSD o una unidad USB. Si no tienes ninguna de esas opciones a mano, puedes optar por compartirlo a través de una de las muchas aplicaciones que se enumeran a continuación.

![image](assets/4.webp)

Pantalla de inicio personalizada


## Aplicaciones alternativas

¡Para hacer que tu teléfono sea útil, querrás instalar algunas aplicaciones! Las opciones que se mencionan a continuación están incluidas porque las he utilizado personalmente o porque reciben fuertes recomendaciones de la comunidad de privacidad en general. Hay muchas otras excelentes alternativas disponibles que no se mencionan, y [Awesome Privacy](https://awesome-privacy.xyz) ofrece una lista increíblemente extensa de aplicaciones para preservar la privacidad para todo tipo de dispositivos.

El hecho de que una aplicación sea software libre y de código abierto (FOSS) no significa que esté libre de posibles filtraciones de privacidad. Utiliza [Exodus](https://reports.exodus-privacy.eu.org/en/) para ver cómo se desempeñan tus aplicaciones preferidas en sus auditorías de privacidad.

### F-Droid

[F-Droid](https://f-droid.org/) es un catálogo instalable de aplicaciones FOSS para Android. El cliente facilita la navegación, instalación y actualización de aplicaciones en tu dispositivo. Vale la pena mencionar que las actualizaciones a través de F-Droid a veces pueden ser más lentas que con otras tiendas de aplicaciones. Esto depende principalmente de si la aplicación se encuentra en el repositorio principal de F-Droid o en uno personalizado.

Para instalar F-Droid, simplemente ve a su sitio web a través de un navegador en tu teléfono GrapheneOS y toca descargar. Esto descargará un archivo `.apk`. Luego se te preguntará si deseas instalar la aplicación.

Además de las aplicaciones que se encuentran dentro del repositorio predeterminado de F-Droid, muchos proyectos de código abierto también alojarán su propio repositorio que se puede agregar en la configuración de la aplicación F-Droid. Si este es el caso, el proyecto en cuestión te guiará a través de los pasos muy sencillos requeridos para lograr esto en su sitio web.

![image](assets/5.webp)

Pantalla de inicio de F-Droid

### Aurora Store
[Aurora Store](https://auroraoss.com/) es una versión de código abierto de la tienda de Google Play. Aurora se ve y se siente muy similar a la tradicional Play Store y te permite descargar y actualizar cualquier aplicación que normalmente encontrarías a través de la opción de Google.
La característica destacada de Aurora es el inicio de sesión anónimo. Esto significa que puedes descargar cualquiera de tus aplicaciones favoritas que no estén disponibles a través de F-Droid o APK directo, sin tener que iniciar sesión en tu cuenta de Google.

Antes de apresurarte a hacer de esto tu opción de instalación predeterminada, recuerda que muchas de las aplicaciones de las que estamos tratando de alejarnos se instalaron desde la Play Store. El hecho de que sean accesibles desde Aurora no cambia el hecho de que algunas pueden tener funciones de seguimiento incorporadas. No siempre será posible, pero siempre que puedas, busca una alternativa en F-Droid antes de descargar a través de Aurora.

Para instalar Aurora, simplemente busca 'Aurora Store' en F-Droid.

Aurora también tiene algunos posibles vectores de ataque, ya que las "cuentas anónimas" son realmente creadas y controladas por Aurora. En teoría, podrían ofrecer actualizaciones maliciosas o enviar aplicaciones a tu teléfono, aunque aún tendrías que aceptar la solicitud de instalación en el dispositivo. Aurora también a veces tiene problemas con las aplicaciones que no aparecen debido a errores de región y lectura incorrecta del dispositivo. Esto generalmente se puede solucionar con los siguientes pasos.

**Consejo principal** - A veces, Aurora Store experimentará limitación de velocidad que limita tu capacidad para buscar e instalar aplicaciones. Para solucionar esto, ve a **Configuración** > **Aplicaciones** > **Aurora** > **Abrir por defecto**, luego agrega el dominio `play.google.com`. Ahora, cada vez que navegues por el sitio web de un producto o servicio que tenga el enlace 'Descargar a través de Play Store', al tocarlo se abrirá esa aplicación dentro de Aurora para que la descargues.

![image](assets/6.webp)

Pantalla de inicio de Aurora Store

### Descarga de APK

Las aplicaciones en Android también se pueden descargar e instalar a través de un archivo `.apk`. Esta es una excelente alternativa que no requiere tiendas de aplicaciones de terceros, simplemente descarga el archivo directamente desde el sitio web o repositorio de GitHub del proyecto o servicio.

La desventaja de este enfoque es que no obtienes actualizaciones automáticas, por lo que deberás estar pendiente de los canales de comunicación de ese servicio para conocer las nuevas versiones. Sin embargo, hay un gran proyecto llamado Obtanium que tiene como objetivo solucionar esto. [Obtainium](https://github.com/ImranR98/Obtainium) te permite instalar y actualizar aplicaciones de código abierto directamente desde sus páginas de lanzamiento, y recibir notificaciones cuando se publiquen nuevas versiones.

![image](assets/7.webp)

Vista previa de Obtanium

### Aplicaciones web

En ocasiones en las que quieras usar un servicio de forma poco frecuente y no quieras descargar una aplicación nativa, simplemente puedes acceder a la versión web. Muchos sitios web ofrecen actualmente soporte para Progressive Web App (PWA). Esto te permite agregar un sitio web específico (por ejemplo, Twitter.com) a la pantalla de inicio de tu teléfono. Luego, al tocar el icono, se abrirá como una aplicación de pantalla completa sin las distracciones habituales que vienen con la experiencia típica del navegador. A continuación, puedes ver un ejemplo de cómo se ve esto.

Para lograr esto en Vanadium, el navegador nativo de GrapheneOS, simplemente navega al sitio web de tu elección, toca los tres puntos verticales en la esquina superior derecha de la pantalla y luego toca **'Agregar a la pantalla de inicio'**.

La única desventaja de este enfoque es que, debido a que es solo una página web marcada, no recibirás ningún tipo de notificaciones. ¡Aunque algunos podrían ver eso como algo positivo!

![image](assets/8.webp)

PWA de Twitter

### Navegadores web
No puedes equivocarte con la opción preempaquetada, Vanadium. La aplicación se comporta de manera idéntica a cualquier otro navegador móvil que haya probado y nunca he tenido problemas de compatibilidad.
Para cuando necesites acceder a sitios nativos `.onion` de Tor, puedes descargar el APK del Navegador Tor directamente desde su [sitio web](https://www.torproject.org/download/#android) o a través de F-Droid.

### VPNs

Para proteger tu actividad en línea de tu proveedor de servicios de internet (ISP) que espía, una aplicación de Red Privada Virtual (VPN) es una buena opción. Una VPN envía tu tráfico de internet a través de un túnel encriptado hacia una dirección IP compartida controlada por el proveedor de servicios de VPN para asegurar que la actividad de tu dispositivo no pueda ser vinculada contigo.

Las siguientes son 3 opciones respetadas que te permiten pagar por el servicio con Bitcoin y sin proporcionar información personal. Las 3 opciones están disponibles a través de F-Droid.

- [Mullvad](https://f-droid.org/packages/net.mullvad.mullvadvpn/)
- [Proton](https://f-droid.org/en/packages/ch.protonvpn.android/)
- [iVPN](https://f-droid.org/en/packages/net.ivpn.client/)

### Mensajería

En los últimos años, las soluciones de mensajería encriptada se han vuelto abundantes. Sin embargo, el problema sigue siendo que puedes tener la mejor y más privada opción instalada en tu teléfono, pero si no tienes contactos que la usen, ¿cuál es el punto?

La mayoría de las personas que no tienen interés en la privacidad probablemente estén usando WhatsApp o iMessage. El primero se puede descargar a través de Aurora Store, pero el último no funcionará en GrapheneOS (¡obviamente!).

- [Signal](https://signal.org/) es uno de los mensajeros con encriptación de extremo a extremo (E2EE) más populares que tiene un sólido historial y un conjunto de funciones completo. Signal requiere un número de teléfono para registrarse, por lo que si planeas chatear con personas a las que preferirías que no conocieran tu número de teléfono, tal vez deberías considerar algunas de las alternativas. Signal debe descargarse a través de Aurora Store.
- [Simplex](https://f-droid.org/en/packages/chat.simplex.app/) es un mensajero E2EE bastante nuevo. No tiene un ID de usuario, no requiere número de teléfono ni información personal. Las personas te encuentran escaneando tu código QR personal o visitando tu enlace único. Simplex también permite a los usuarios avanzados ejecutar su propio servidor para reducir aún más la dependencia de cualquier entidad centralizada. Simplex no tiene un cliente de escritorio, por lo que puede que no sea adecuado si la capacidad de usar múltiples dispositivos es una prioridad para ti. Simplex para Android está disponible a través de F-Droid.
- [Threema](https://threema.ch/en/faq/libre_installation) ofrece una experiencia similar a Simplex, pero ha estado disponible por más tiempo y, como resultado, se siente un poco más pulido. Threema no es gratuito, una licencia de por vida cuesta $4.99 y se puede comprar con Bitcoin. Threema ofrece un cliente web y aplicaciones de escritorio nativas. La aplicación de Android está disponible a través de F-Droid.
- [Telegram FOSS](https://f-droid.org/en/packages/org.telegram.messenger/) es una bifurcación no oficial de código abierto del Telegram oficial para Android. Telegram tiene 'chats secretos' con E2EE, pero la opción predeterminada no es privada. Telegram FOSS se puede descargar desde F-Droid.

![image](assets/9.webp)
Izquierda: Threema
Derecha: Simplex

### Medios

- [Spotube](https://f-droid.org/packages/oss.krtirtho.spotube/) es un cliente de Spotify multiplataforma que no requiere una cuenta Premium. Spotube está disponible a través de F-Droid.
- [Nextcloud](https://nextcloud.com/) is a self-hosted productivity platform that allows you to store, sync, and share your files, calendars, contacts, and more. Nextcloud can be downloaded from the Aurora Store.
- [Joplin](https://f-droid.org/en/packages/net.cozic.joplin/) is an open source note-taking and to-do app with synchronization capabilities. Joplin supports end-to-end encryption and can be downloaded from F-Droid.
- [LibreOffice Viewer](https://f-droid.org/en/packages/org.documentfoundation.libreoffice/) allows you to view and edit documents, spreadsheets, and presentations on your Android device. It is compatible with Microsoft Office formats and can be downloaded from F-Droid.

![image](assets/17.webp)

Left: Nextcloud
Right: Joplin
- [KDE Connect](https://f-droid.org/packages/org.kde.kdeconnect_tp/) conecta todos tus dispositivos para que puedan comunicarse fácilmente entre sí cuando están conectados a tu red doméstica. Puedes enviar fácilmente archivos, fotos y datos del portapapeles a través de todos tus dispositivos (¡incluso en iOS!). KDE Connect se puede descargar desde F-Droid.
- [Notesnook](https://f-droid.org/en/packages/com.streetwriters.notesnook/) es una aplicación de notas con cifrado de extremo a extremo que sincroniza tus pensamientos y listas de tareas en todos tus dispositivos. Su plan gratuito debería cubrir la mayoría de los casos de uso personal. Notesnook está disponible en F-Droid.
- [Standard Notes](https://f-droid.org/en/packages/com.standardnotes/) es muy similar a Notesnook, pero requiere un plan de pago para igualar el conjunto de funciones. Standard Notes está disponible a través de F-Droid.
- [Anysoft Keyboard](https://f-droid.org/packages/com.menny.android.anysoftkeyboard/) es una aplicación de teclado que te permite personalizar prácticamente todo lo que puedas imaginar en cuanto a tu experiencia de escritura en el teléfono. Se puede descargar a través de F-Droid.
- [GBoard](https://play.google.com/store/apps/details?id=com.google.android.inputmethod.latin&hl=en&gl=US) es la aplicación de teclado predeterminada de Google. En mi experiencia, ofrece la mejor experiencia de escritura y deslizamiento. Si descargas esta aplicación, asegúrate de desactivar por completo todos los permisos relacionados con la red. Se puede descargar a través de Aurora.

![image](assets/17.webp)

Izquierda: Notesnook
Derecha: KDE Connect

### Estilo de vida

- [Geometric Weather](https://f-droid.org/en/packages/wangdaye.com.geometricweather/) es una aplicación de pronóstico del tiempo de código abierto y bellamente diseñada disponible en F-Droid. También admite diferentes tamaños de widgets para que puedas ver el clima en la ubicación que elijas directamente desde tu pantalla de inicio.
- [Translate You](https://f-droid.org/packages/com.bnyro.translate/) es una aplicación de traducción de código abierto y que respeta la privacidad que admite más de 200 idiomas. Translate You está disponible a través de F-Droid.
- [Proton Calendar](https://proton.me/calendar/download) es una aplicación de calendario fácil de usar con cifrado de extremo a extremo que interactúa perfectamente con tus cuentas de correo electrónico de Proton. Proton Calendar se puede descargar como un archivo APK o a través de la tienda Aurora.
- [PassAndroid](https://f-droid.org/en/packages/org.ligi.passandroid/) es una aplicación para mostrar y almacenar tarjetas de embarque, cupones, entradas de cine y tarjetas de membresía, entre otras cosas. Simplemente descarga el archivo `pkpass` o `espass` relevante y ábrelo con la aplicación. PassAndroid está disponible a través de F-Droid.

![image](assets/19.webp)
Izquierda: Geometric Weather
Derecha: Proton Calendar

### Seguridad/Privacidad

- [Bitwarden](https://mobileapp.bitwarden.com/fdroid/) ofrece una solución gratuita de gestión de contraseñas de plataforma cruzada y con cifrado de extremo a extremo para todos tus dispositivos. Su servicio de pago te permite integrar códigos de autenticación de dos factores en la aplicación. El servidor de Bitwarden se puede alojar de forma independiente y la aplicación de Android está disponible a través de F-Droid.
- [Proton Pass](https://proton.me/pass/download) ofrece un servicio gratuito similar a Bitwarden, pero los clientes de [Proton Unlimited](https://proton.me/pricing) pueden acceder a funciones avanzadas adicionales. Proton Pass está disponible a través de APK o Aurora.
- [FreeOTP](https://f-droid.org/packages/org.fedorahosted.freeotp/) es una aplicación de autenticación de dos factores para sistemas que utilizan protocolos de contraseñas de un solo uso. Los tokens se pueden agregar fácilmente escaneando un código QR. FreeOTP está disponible a través de F-Droid.
- [Aegis](https://f-droid.org/es/packages/com.beemdevelopment.aegis/) es una aplicación gratuita, segura y de código abierto para Android que te permite gestionar tus tokens de verificación en dos pasos para tus servicios en línea. Aegis está disponible a través de F-Droid.
- [Cryptomator](https://f-droid.org/es/packages/org.cryptomator.lite/) es un servicio de pago multiplataforma que cifra tus datos localmente para que puedas subirlos de forma segura a tu servicio de almacenamiento en la nube favorito. Cryptomator se puede descargar a través de F-Droid.

![imagen](assets/21.webp)
Izquierda: Proton Pass
Derecha: Bitwarden

### Soluciones en la nube

- [Proton Drive](https://proton.me/drive/download) es una solución en la nube de pago con cifrado de extremo a extremo para hacer copias de seguridad y almacenar todos tus archivos. En el momento de escribir esto, acaban de anunciar un cliente de escritorio para Windows, pero los usuarios de Mac y Linux deben seguir utilizando la versión web para sincronizar desde sus computadoras (por ahora). El cliente de Android está disponible como APK o a través de Aurora.
- [Skiff](https://skiff.com/download) también ofrece almacenamiento en la nube de pago con cifrado de extremo a extremo y herramientas de colaboración de archivos. Ofrecen un cliente de escritorio para Mac y Windows (además de una aplicación web) y sus clientes de Android deben descargarse desde Aurora.
- [Nextcloud](https://f-droid.org/es/packages/com.nextcloud.client/) ofrece una solución en la nube completa para la colaboración, sincronización entre dispositivos y almacenamiento de archivos. Los usuarios más avanzados pueden optar por alojar su software libre y de código abierto en cualquier hardware que deseen. Los clientes de Android se pueden descargar a través de F-Droid.
- [Cryptpad](https://cryptpad.fr/) ofrece una alternativa gratuita basada en la web y con cifrado de extremo a extremo a Google Docs.

![imagen](assets/23.webp)

Proton Drive

## Las desventajas

Las alternativas de código abierto y respetuosas con la privacidad a las aplicaciones de los conglomerados tecnológicos a las que estás acostumbrado/a a usar son numerosas, y algunas de ellas suelen ser mejores que las alternativas de código cerrado y llenas de spyware.

Sin embargo, al cambiar a GrapheneOS, hay algunas comodidades a las que tendrás que renunciar debido a la falta de alternativas. Estas incluyen:

- **Apple CarPlay/Android Auto**: Tendrás que conformarte con la buena y antigua conexión Bluetooth, USB o Auxiliar.
- **Apple/Google Pay**: ¡La mayoría de las personas llevan su billetera consigo de todos modos!
- **Aplicaciones bancarias**: No es que estas no funcionen en absoluto. Algunas funcionan perfectamente, de hecho. Otras solo funcionan con los Servicios de Google Play habilitados (lee más al respecto a continuación) y otras simplemente no funcionan en absoluto. Lee el informe de tu banco [aquí](https://privsec.dev/posts/android/banking-applications-compatibility-with-grapheneos/) para ver el estado actual. No te preocupes si el tuyo está en la lista de los que no funcionan, recuerda que puedes guardar la URL como una aplicación web en la pantalla de inicio.
- **Notificaciones push**: La mayoría de las aplicaciones que te envían actualizaciones cuando no estás usando una aplicación específica lo hacen a través de los Servicios de Google Play. Estos no están instalados de forma predeterminada en GrapheneOS, por lo que si te encuentras sin recibir notificaciones inmediatas cuando un amigo te envía un correo electrónico, es probable que sea por eso. La buena noticia es que algunas de las aplicaciones mencionadas anteriormente han implementado su propia conexión en segundo plano para verificar periódicamente las actualizaciones y luego enviarte una notificación cuando sea necesario.

### Google Play en un entorno seguro
GrapheneOS tiene una capa de compatibilidad que ofrece la opción de instalar y utilizar las versiones oficiales de Google Play en el sandbox de aplicaciones estándar. Google Play no tiene ningún acceso especial o privilegios en GrapheneOS en comparación con eludir el sandbox de la aplicación y recibir un gran cantidad de acceso altamente privilegiado.

Si descubres que simplemente no puedes vivir sin esas notificaciones push de tu aplicación favorita o que una cierta aplicación "imprescindible" es inútil sin los Servicios de Google Play, GrapheneOS te permite [instalar](https://grapheneos.org/usage#sandboxed-google-play-installation) estos servicios en un entorno completamente aislado. Una vez instalados, estos servicios no requieren una cuenta de Google para funcionar y los permisos de cada uno se pueden controlar de forma estricta.

Antes de apresurarte a instalarlos el primer día, te insto a que veas hasta dónde llegas sin ellos. Probablemente te sorprenderás de cuántas aplicaciones funcionan perfectamente normalmente sin ellos.

Si deseas instalarlos, simplemente toca la aplicación preinstalada "Apps" seguida de "Google Play Services". Considera instalarlos junto con esas aplicaciones menos privadas de las que no puedes prescindir, dentro de un perfil de usuario completamente separado para proporcionar una capa adicional de segregación del resto de tu teléfono.

![image](assets/24.webp)

Pantalla de instalación de Play Services

### Perfiles

GrapheneOS te permite tener una experiencia telefónica separada dentro de tu teléfono. Los perfiles adicionales pueden instalar sus propias aplicaciones y servicios y no pueden acceder a ningún archivo o dato de la cuenta del propietario.
Si solo tienes una o dos de esas aplicaciones imprescindibles que requieren Play Services, pero solo se usan muy ocasionalmente, instalarlas junto con Play Services en un perfil separado podría ser una gran idea para fortalecer aún más cualquier implicación mínima de privacidad que quede al tenerlas en ejecución en el perfil del propietario.

Puedes leer más sobre este caso de uso [aquí](https://discuss.grapheneos.org/d/168-ideas-for-user-profiles/2).

Si decides agregar un perfil separado para adaptarse a tu caso de uso, la aplicación [Insular](https://f-droid.org/en/packages/com.oasisfeng.island.fdroid/) puede ser útil para ti. Insular te permite clonar fácilmente cualquiera de tus aplicaciones existentes en el nuevo perfil sin necesidad de pasar por ninguna de las rutas de instalación tradicionales mencionadas anteriormente en esta guía. Insular también te permite "congelar" rápidamente cualquiera de esas aplicaciones para desactivar por completo todos los servicios en segundo plano de esa aplicación.

![image](assets/24.webp)

Pantalla de gestión de perfiles de usuario

### e-Sims

Si deseas llevar tu privacidad telefónica al siguiente nivel y tener un servicio celular que esté separado de tu identidad en el mundo real, es posible que te interese una eSIM. Una eSIM es una tarjeta SIM virtual que puedes comprar en línea y agregar a tu teléfono mediante un código QR. Empresas que ofrecen este tipo de servicios que se pueden pagar de forma anónima con Bitcoin incluyen [Silent.Link](https://silent.link/) y [Bitrefill](https://www.bitrefill.com/gb/en/esims/).

Las eSIM no deben considerarse como una panacea completa para la privacidad telefónica. Pueden ser una herramienta útil en manos adecuadas, pero por favor investiga los [compromisos](https://grapheneos.org/faq#cellular-tracking) de utilizar cualquier tipo de servicio celular si tu intención es estar completamente "fuera de la red".

Es necesario instalar los Servicios de Google Play en un entorno aislado para la provisión de eSIM en GrapheneOS.

## Copias de seguridad

Después de configurar tu nuevo teléfono Pixel sin Google, es una buena idea crear una copia de seguridad. Esta copia de seguridad te permitirá restaurar el teléfono a un estado idéntico en caso de que pierdas tu teléfono o te lo roben.
Puedes optar por almacenar el archivo de respaldo en cualquier medio de almacenamiento externo, o en una solución de nube autohospedada como Nextcloud, aunque algunos usuarios informan niveles variables de éxito con esta última opción.
Para crear tu primer respaldo:

1. Ve a **Configuración** > **Sistema** > **Respaldo**, luego anota tu código de recuperación de 12 palabras. Este código es necesario para descifrar el archivo de respaldo en una fecha posterior. Si pierdes el código, perderás el acceso a tu respaldo telefónico.
2. A continuación, elige la ubicación de almacenamiento. Recomendaría una unidad USB externa o una tarjeta microSD de grado industrial.
3. Elige los datos que se respaldarán. Si tienes suficiente espacio en tu medio de almacenamiento especificado, te aconsejaría seleccionar todo.
4. Toca los tres puntos en la parte superior derecha y elige **Respaldar ahora**.

![imagen](assets/26.webp)

Pantalla de respaldo

Recuerda que si estás haciendo respaldos sin conexión en medios de almacenamiento externo, tiene sentido completar este paso regularmente para asegurarte de que no se pierdan las actualizaciones importantes recientes de tu teléfono en caso de que ocurra lo peor.

![video](https://www.youtube.com/embed/eyWmcItzisk)

Video que detalla el proceso de respaldo

## Conclusión

En los últimos años, el software GrapheneOS ha madurado significativamente. Es más estable y compatible que nunca. Combinado con el floreciente ecosistema de aplicaciones de código abierto y preservación de la privacidad, GrapheneOS se convierte en una alternativa realmente viable a Android o iOS de fábrica, incluso para personas "normales" como tú.

Las violaciones de datos y la vigilancia masiva son tan comunes en el mundo actual que apenas hacen titulares. Depende de ti protegerte. Habrá ajustes y sacrificios que hacer en el camino, pero reducir tu exposición a tales infracciones no es tan difícil como crees que será.

Espero que esta guía te ayude en tu camino. Si encontraste útil esta guía y te gustaría apoyar mi trabajo, considera enviar una [donación](/tips).

Si eres un usuario existente de GrapheneOS, o te conviertes en uno como resultado de esta guía, considera [donar](https://grapheneos.org/donate) para apoyar su importante trabajo.

### Obtén más información

GrapheneOS es una madriguera de conejo en la que cualquiera podría pasar fácilmente semanas explorando. Hay tanto que puedes aprender y experimentar para adaptar la experiencia a tus necesidades y modelos de amenazas. A continuación, se presentan algunos enlaces donde puedes continuar tu viaje:

- [Guía oficial de uso de GrapheneOS](https://grapheneos.org/usage) - Sitio web oficial
- [Foro de GrapheneOS](https://discuss.grapheneos.org/) - Sitio web oficial
- [Masterclass de configuración de GrapheneOS](https://www.youtube.com/watch?app=desktop&v=GLJyD9MJgIQ) - Video de 'The Privacy Wayfinder'
- [Podcast general de GrapheneOS](https://www.youtube.com/watch?app=desktop&v=UCPX0mFFRNA) - Podcast de 'Watchman Privacy'

Crédito completo a: https://github.com/BitcoinQnA/Bitcoiner.Guide/blob/main/grapheneos.md