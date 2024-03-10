---
name: Tails

description: Instalar Tails en una memoria USB
---

![image](assets/cover.jpeg)

Un sistema operativo portátil y amnésico que te protege contra la vigilancia y la censura.

## ¿Por qué tener una memoria USB con Tails instalado?

Tails (https://tails.boum.org/) es la forma más fácil de tener a tu disposición, en todo momento, una computadora segura que no dejará rastro en la computadora en la que la utilices.

Para usar Tails, apaga la computadora que tengas disponible (en casa de tus padres, en casa de tus amigos, en un cibercafé...) y arráncala desde tu memoria USB Tails en lugar de Windows, macOS o Linux.

Después de eso, tendrás un espacio de trabajo y comunicación que es independiente del sistema operativo habitual y que nunca utiliza el disco duro.

Tails nunca escribe en el disco duro y solo utiliza la memoria RAM de la computadora para funcionar. Esta memoria se borra por completo al apagar Tails, eliminando así cualquier rastro posible.

## Algunos casos concretos de uso

Para darte ideas concretas sobre la utilidad de tener siempre contigo una memoria USB con Tails, aquí tienes una pequeña lista no exhaustiva compilada por el equipo de Agora256:

- Conectarse a Internet y a Tor de forma no censurada y anónima para consultar sitios sin dejar rastro;
- Abrir un PDF desde un sitio web sospechoso;
- Probar tu copia de seguridad de la clave privada de Bitcoin con la billetera Electrum;
- Utilizar una suite de oficina (LibreOffice) y trabajar en una computadora que no te pertenece;
- Dar los primeros pasos en un entorno Linux para aprender a salir del mundo de Microsoft y Apple.

## ¿Cómo confiar en Tails?

Siempre hay un grado de confianza en el uso de software, pero esta no tiene por qué ser ciega. Una herramienta como Tails debe intentar proporcionar a sus usuarios medios para ser digna de confianza. Para Tails, esto significa:

- Un código fuente público: https://gitlab.tails.boum.org/;
- Un proyecto basado en proyectos reputados: Tor y Debian;
- Descargas verificables y reproducibles;
- Recomendaciones de diferentes personas y organizaciones.

## Guía de instalación y uso

Esta guía de instalación tiene como objetivo guiarte en cada paso de la instalación, no describiremos más acciones de las que se encuentran en la guía oficial, pero te señalaremos en la dirección correcta y te daremos consejos y trucos.

Por razones de experiencia práctica, estos consejos se centrarán en las plataformas de macOS y Linux.
🛠️
Antes de comenzar este procedimiento, asegúrese de tener en su posesión una memoria USB con una velocidad de lectura de al menos 150 MB/s y un tamaño de al menos 8 GB, idealmente de tipo USB 3.0.

## Requisitos previos

- 1 memoria USB, solo para Tails, de al menos 8 GB
- Un ordenador conectado a Internet con Linux, macOS (o Windows)
- Aproximadamente una hora de tiempo total, dependiendo de la velocidad de su conexión a Internet, incluyendo media hora para la instalación (archivo para descargar de 1.3 GB)

## Paso 1: Descargar Tails desde su ordenador

![imagen](assets/1.webp)

> 🔗 Sección oficial de Tails: https://tails.boum.org/install/linux/index.fr.html#download

Descargar el archivo de instalación con la extensión img puede llevar algún tiempo dependiendo de la velocidad de descarga de su Internet, así que asegúrese de hacerlo con anticipación. Con una línea moderna y rápida, esto tomará menos de 5 minutos.

Guarde el archivo en una carpeta conocida, como "Descargas", ya que será necesario para pasar al siguiente paso.

## Paso 2: Verificar su descarga

![imagen](assets/2.webp)

> 🔗 Sección oficial de Tails: https://tails.boum.org/install/linux/index.fr.html#verify

Verificar la descarga le permite asegurarse de que proviene de los desarrolladores de Tails y que no ha sido corrompida o interceptada durante la descarga.

Es posible verificar manualmente que el archivo que acaba de descargar es el correcto utilizando PGP, pero sin conocimientos avanzados, esta verificación ofrece el mismo nivel de seguridad que la verificación JavaScript en la página de descarga, aunque es mucho más complicada y propensa a errores.

¡Para verificar el archivo, utilice el botón "Seleccionar su descarga..." proporcionado en la sección oficial!

## Paso 3: Instalar Tails en su memoria USB

![imagen](assets/3.webp)

> 🔗 Sección oficial de Tails:
>
> - Linux: https://tails.boum.org/install/linux/index.fr.html#install
> - macOS: https://tails.boum.org/install/mac/index.fr.html#etcher y https://tails.boum.org/install/mac/index.fr.html#install

Este paso de instalación de Tails en su memoria USB es el más difícil de toda la guía, especialmente si nunca lo ha hecho antes. El punto más importante es elegir correctamente el procedimiento en la sección oficial para su sistema operativo: Linux o macOS.

Una vez que haya instalado y preparado las herramientas como se recomienda, podrá copiar el archivo con la extensión img en su memoria USB (borrando todos los datos existentes) para que sea "arrancable" de forma independiente.

¡Buena suerte! Nos vemos en el paso 4.

## Paso 4: Reiniciar con su memoria USB Tails

![imagen](assets/4.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.fr.html#restart
> Es hora de iniciar uno de tus ordenadores usando tu nuevo USB. ¡Inserta el USB en uno de los puertos USB y reinicia!

> 💡 La mayoría de los ordenadores no arrancan automáticamente desde el USB de Tails, pero puedes presionar la tecla del menú de arranque para mostrar una lista de dispositivos posibles desde los cuales arrancar.

Para determinar qué tecla debes presionar para asegurarte de tener el menú de arranque que te permita seleccionar el USB en lugar de tu disco duro habitual, aquí tienes una lista no exhaustiva por fabricante:

| Fabricante | Tecla              |
| ---------- | ------------------ |
| Acer       | F12, F9, F2, Échap |
| Apple      | Option             |
| Asus       | Échap              |
| Clevo      | F7                 |
| Dell       | F12                |
| Fujitsu    | F12, Échap         |
| HP         | F9                 |
| Huawei     | F12                |
| Intel      | F10                |
| Lenovo     | F12                |
| MSI        | F11                |
| Samsung    | Échap, F12, F2     |
| Sony       | F11, Échap, F10    |
| Toshiba    | F12                |
| otros…     | F12, Échap         |

Una vez seleccionado el USB, deberías ver esta nueva pantalla de inicio, es una muy buena señal, así que deja que el ordenador continúe su arranque...

![image](assets/5.webp)

## Paso 5: ¡Bienvenido a Tails!

![image](assets/6.webp)

> 🔗 Official Tails section: https://tails.boum.org/install/linux/index.fr.html#tails

Uno o dos minutos después del cargador de arranque y la pantalla de carga, aparecerá la Pantalla de bienvenida.

![image](assets/7.webp)

En la Pantalla de bienvenida, selecciona tu idioma y distribución de teclado en la sección Idioma y región. Haz clic en Iniciar Tails.

![image](assets/8.webp)

Si tu ordenador no está conectado a una red por cable, consulta las instrucciones oficiales de Tails para ayudarte a conectarte a una red sin Wi-Fi (sección "Prueba tu Wi-Fi").

Una vez conectado a la red local, aparecerá el Asistente de Conexión a Tor para ayudarte a conectarte a la red Tor.

![image](assets/9.webp)

Puedes comenzar a navegar de forma anónima, explorar las opciones y los programas incluidos en Tails. Disfruta, tienes total libertad para cometer errores, ya que nada se modifica en el USB... ¡Tu próximo reinicio habrá olvidado todas tus experiencias!

## En una próxima guía...

Una vez que hayas experimentado un poco más con tu propio USB de Tails, exploraremos otros temas más avanzados en otro artículo, como:

> Actualizar una clave con la última versión de Tails; Configurar y utilizar el almacenamiento persistente; Instalar software adicional.
> D'ici là, comme toujours, si vous avez des questions, n'hésitez pas à les partager à la communauté Agora256, nous apprenons ensemble, pour être meilleur demain que nous ne le sommes aujourd'hui!
