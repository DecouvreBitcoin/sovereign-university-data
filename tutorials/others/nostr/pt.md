---
name: NOSTR

description: Descubra e comece a usar o NOSTR
---

No final deste guia, você entenderá o que é o Nostr, terá criado uma conta e estará apto a usá-lo.

![Um novo desafiante chegou](assets/1.webp)

## O que é o Nostr?

O Nostr é um protocolo que tem o poder de substituir o Twitter, o Telegram e outras redes sociais. É um protocolo aberto simples e capaz de criar uma rede social global resistente à censura.

## Como funciona?

O Nostr é baseado em três componentes: pares de chaves, clientes e relés.

Cada usuário possui uma ou várias identidades, sendo que cada identidade é determinada por um par de chaves criptográficas.

Para acessar a rede, é necessário usar um software cliente e se conectar a relés para receber e emitir conteúdo.

![Sistema de chaves](assets/2.webp)

## 1. Chaves criptográficas

Ao contrário do Facebook ou do Twitter, onde o usuário precisa fornecer um endereço de e-mail e uma série de informações para uma empresa privada, o Nostr funciona na ausência de uma autoridade central. O usuário gera um par de chaves criptográficas, uma chave secreta (também chamada de chave privada) e uma chave pública.

A chave secreta, nsec, conhecida apenas pelo usuário, é usada para autenticação e publicação de conteúdo.

A chave pública, npub, é um identificador único ao qual todo o conteúdo publicado por um usuário está vinculado. Sua chave pública é uma espécie de nome de usuário que permite que outros usuários o encontrem e se inscrevam em seu feed Nostr.

## 2. Clientes

Os clientes são softwares que permitem interagir com o Nostr. Os principais clientes são:

> iOS: damus
> Android: amethyst
> Web: iris.to; snort.social; astral.ninja

Os clientes permitem que um usuário gere um novo par de chaves (equivalente a criar uma conta) ou se autentique com um par de chaves existente.

## 3. Relés

Os relés são servidores simplificados que você pode abandonar a qualquer momento se não gostar do conteúdo que eles estão transmitindo. Você também pode executar seu próprio relé, se desejar.

> 💡 Dica profissional: Relés pagos geralmente são mais eficientes para filtrar spam e conteúdo indesejado.

# Guia

Agora você já sabe o suficiente sobre o Nostr para começar e criar sua primeira identidade neste protocolo.

Para fins deste guia, usaremos o iris.to (https://iris.to/), pois este cliente web funciona em qualquer plataforma.

## Etapa 1: Geração de chaves

O ris criará um conjunto de chaves para você sem que você precise fazer mais nada além de digitar um nome (real ou fictício) para o seu perfil. Em seguida, clique em GO e pronto!

![Menu principal](assets/3.webp)

> ⚠️ Atenção! Você precisará manter um registro de suas chaves se quiser acessar seu perfil novamente após fechar sua sessão. Eu mostrarei como fazer isso no final deste guia.

## Etapa 2: Publicar conteúdo

Para publicar conteúdo, é tão simples e intuitivo quanto escrever algumas palavras no campo de publicação.

![Publicação](assets/4.webp)

Pronto, você publicou sua primeira nota no Nostr.

![Post](assets/5.webp)

## Etapa 3: Encontrar um amigo

Encontre-me no Nostr e nunca mais fique sozinho. Eu também me inscrevo em todos que se inscrevem no meu feed. Para fazer isso, basta digitar minha chave pública

npub1hartx53w6t3q5wv9xdqdwrk7h6r5866t8u775q0304zedpn5zgssasp7d3 na barra de pesquisa.

![Meu perfil](assets/6.webp)

Clique em "seguir" e em alguns dias, também me inscreverei no seu feed. Seremos amigos. Também ficarei feliz em ler sua mensagem se você quiser me escrever.

Por fim, certifique-se de se inscrever no feed do Agora256 para receber uma nota sempre que publicarmos algo novo: npub1ag0rawstycy7nanuc6sz4v287rneen2yapcq3fd06972f8ncrhzqx

## Etapa 4: Personalize seu perfil

Ainda há um pouco de trabalho a ser feito para personalizar seu perfil. Para fazer isso, clique no avatar que o iris gerou automaticamente para você no canto superior direito da tela e clique em "editar perfil".

![Perfil](assets/7.webp)

Agora, basta informar ao iris onde encontrar sua imagem e banner de perfil na internet. Eu recomendo que você hospede seu próprio conteúdo: proteja o que é seu.

![Outra opção](assets/8.webp)

Se preferir, você também pode fazer o download de imagens, elas serão armazenadas para você pelo iris no nostr.build, um serviço gratuito de hospedagem de conteúdo visual para o Nostr.

Como você pode ver, você também pode configurar seu cliente para poder receber e enviar sats. Assim, você poderá recompensar os autores de conteúdo que você gostou ou, melhor ainda, acumular sats para o ótimo conteúdo que você vai publicar.

## Etapa 5: Backup do par de chaves

Esta etapa é crucial se você quiser manter o acesso ao seu perfil depois de desconectar do cliente ou quando sua sessão expirar.
'D'abord, clique sur l'icône "settings" représentée par un engrenage
![Setting](assets/9.webp)

Puis, copie-colle à tour de rôle tes npub, npub hex, nsec et nsec hex dans un fichier texte que tu garderas en sécurité. Je te recommande de crypter ce fichier, si tu sais comment le faire.

![Clef](assets/10.webp)

> ⚠️ Remarque bien l'avertissement que te donne iris. Si tu peux partager ta clé publique sans crainte, il en est tout autrement de ta clé privée. Quiconque possède cette dernière pourra accéder à ton compte.

## Conclusion

Ça y est, petite autruche, tu as fait tes premiers pas sur Nostr. Maintenant, il te faudra apprendre à courir à la vitesse de l'éclair. Nous publierons prochainement des guides qui te montreront à gérer tes clés et comment intégrer lightning à ton expérience Nostr à l'aide de getalby.
