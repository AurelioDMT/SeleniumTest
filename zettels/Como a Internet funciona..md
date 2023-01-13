tags: #web
status: #zettel/fleeting

# Resumo do que eu entendi
- Basicamente a ==internet== é uma ==rede **centralizada** composta por vários computadores, seguindo um protocolo específico==.

- Composta por três tipos de computadores:
	- Computador normal.
	- Computador especial (roteador). Tem a única função de certificar que o conteúdo do computador A, foi pro computador B.
	- Modem, que transforma a informação em uma informação gerenciável pela linha telefônica.
---
# Site (minhaconexao)
- Conectar-se a internet é tão fácil que a maioria das pessoas nunca parou para pensar o que está por trás dessa tecnologia. Provavelmente você fica mais preocupado com a velocidade da internet, fazendo constantemente um teste de velocidade, do que como ela chega até você.

- Mas afinal de contas, o que faz a internet que você utiliza na sua casa, escritório ou qualquer outro lugar com conexão funcionar? No post de hoje vamos ==responder== essa pergunta e mostrar ==como funciona a internet que chega à sua casa==.

## Veja como funciona a internet que chega para você
- A verdade é que o funcionamento da internet não é tão simples e fácil quanto conectar-se a ela. Ao mesmo tempo em que você está conectado, outras bilhões de pessoas também estão conectadas a bilhões de outras coisas. E isso tudo acontece na base do acordo, que é como funciona a internet: todos precisam concordar em seguir as mesmas regras. Há anos, o Brasil já faz parte dessa rede mundial de redes de computadores, que no ==total==, liga quase ==40 milhões de pessoas no país==.

- Quando você conecta dois computadores, você tem ==uma rede (network)==. Se um amigo seu conecta mais outros dois computadores, ele cria ==outra rede (network)==. Se vocês concordam em funcionar sob as ==mesmas regras==, vocês podem conectar ==ambas as redes==. ==Duas networks conectadas representam uma internetwork==, ou internet. As ==regras== são chamadas de ==protocolo internet==. E, entrando em acordos, várias redes são formadas, até que todo o planeta esteja conectado. A internet é, portanto, uma rede de redes compartilhadas.

- O ==acesso à internet== de modo externo se dá quando a ==sua rede local== se conecta a ==outra rede maior==, no caso, o ==seu provedor de internet==, por meio da tecnologia ==TCP/IP==, um modo de ==comunicação baseado no endereço de IP (Internet Protocol)==. Este IP é o endereço de cada um dos pontos de uma rede, e cada ponto da rede consiste em um computador que, por sua vez, se interliga a outros computadores, formando o que se chama de “==teia de redes==”.

## Como as redes se conectam
- Para ==conectar as redes==, existem milhões de ==cabos de fibra óptica espalhados pelo mundo==. Existem cabos instalados até embaixo dos oceanos, ligando um continente a outro. ==Antes de chegar ao seu computador a informação passa por diversos pontos==, literalmente dá a volta ao mundo em alguns casos, dependendo de onde o servidor com as informações está localizado. Nesse caminho, ==elas são quebradas em diversas partes== e, no ==fim do percurso==, o seu ==computador== se encarrega de ==reunir todos os pedaços para formar o conteúdo== que você vê aí no seu monitor.

- Para entender melhor, quando você ==envia== uma mensagem qualquer (imagem, vídeo, áudio ou texto) do ==seu dispositivo para outro==, essa mensagem é ==dividida== em várias partes e essas partes são ==chamadas de pacotes de dados==. Cada um desses pacotes toma um ==caminho diferente== para chegar ao seu destino. ==Por conta do protocolo==, o dispositivo que recebe a mensagem ==sabe como juntar tudo de novo e formar a mensagem original==.

- Mas como as mensagens vão de uma rede para outra, ou seja, de ==dispositivos localizados em provedores diferentes==? Algumas companhias fazem ligações privadas entre si, mas o mais comum atualmente é que as mensagens trafeguem ==entre plataformas== compartilhadas de serviço, chamadas de pontos de troca de tráfego (==PTTs==), onde várias ==empresas diferentes== podem ==interligar-se e compartilhar suas tecnologias==. ==Qualquer empresa==, como provedores, redes sociais, empresas de comunicação e ainda outras ==podem se conectar nesses pontos e se beneficiar da troca de tráfego==, além de reduzir custos e ter um tráfego mais rápido.

- No ==mundo inteiro== são enviados cerca de ==90 trilhões de e-mails por dia==. São aproximadamente 234 milhões de sites e 126 milhões de blogs. ==Para que tanta informação possa continuar existindo e se expandindo==, foi ==criado um novo formato de identificação de cada conteúdo e usuário na web==, o chamado ==IPv6==, pois o atual formato, o ==Ipv4==, está ==quase sem combinações possíveis==. Deu para perceber que o funcio

# Site (mdnwebdocs)
## Resumo
- A Internet é a ==espinha dorsal da Web==, a ==infraestrutura técnica que faz a Web possível==. Mas basicamente, a ==Internet é uma gigantesca rede de computadores que se comunicam juntos==.

-  A história da internet é um pouco obscura. ==Ela começou nos anos 60== como um projeto de pesquisa consolidado pelo ==exército norte americano==, e tornou-se uma ==infraestrutura pública== nos ==anos 80== com o suporte dado por diversas ==universidades públicas== e ==companhias privadas==. As várias tecnologias que suportam a internet evoluíram através do tempo, mas a forma de funcionamento não mudou muito: ==Internet é uma forma de conectar computadores e garantir, em qualquer situação, que eles encontrem uma forma de se manter conectados==.
## Mergulho profundo
### Uma rede simples
- Quando ==dois computadores precisam se comunicar==, você precisa ==conectá-los==, seja ==fisicamente== (normalmente com um Cabo de rede) ou de uma forma ==sem fio== (por exemplo com sistemas WiFi ou Bluetooth). Todos os ==computadores modernos== suportam alguma(s) ==dessas conexões==.

- Nota: Até o final deste artigo nós estaremos falando ==apenas a respeito de cabos físicos==, ==mas redes sem fio funcionam da mesma forma==
- ![[Pasted image 20221223150704.png]]

- Uma ==rede não é limitada a dois computadores==. Você pode conectar ==quantos computadores desejar==. Mas isto se torna complicado. Se você está ==tentando conectar==, digamos, ==dez computadores==, você irá precisar de ==45 cabos==, com ==9 conexões por computador!==
- ![[Pasted image 20221223150732.png]]

- ==Para resolver este problema==, cada computador na rede está conectado a um pequeno ==computador especial chamado de roteador==. Este roteador tem um ==único trabalho==: como um sinalizador em uma estação de trem, ==ter certeza de que a mensagem enviada por um determinado computador chegue ao computador destinatário corretamente==. Para ==enviar uma mensagem== para o ==computador B==, o ==computador A== deve ==enviar a mensagem== para o ==roteador==, que por sua vez ==encaminha a mensagem== para o ==computador B== e tem a ==certeza== de que a mensagem não foi entregue ao ==computador C==.

- Uma vez que nós ==adicionamos um roteador no sistema==, nossa rede de ==10 computadores apenas necessitará de 10 cabos==: uma ==única conexão== para cada ==computador== e um ==roteador com 10 conexões==.
- ![[Pasted image 20221223150801.png]]

### Uma rede de redes
- Por enquanto, tudo bem. Mas ==como conectar centenas, milhares, bilhões de computadores?== Claro que um ==único roteador não pode se adaptar para tanto==, mas, se você ler com cuidado, nós dissemos que ==um roteador é um computador como qualquer outro==, então o que nos impede de ==conectar dois roteadores juntos?== Nada, então façamos isto.
- ![[Pasted image 20221223150850.png]]

- Conectando ==computadores a roteadores==, e então ==roteadores a roteadores== nós podemos ==escalar nossa rede infinitamente==.
- ![[Pasted image 20221223150919.png]]

- Esta ==rede== é ==muito parecida com o que chamamos de Internet==, mas ==alguma coisa está faltando==. Nós construímos tais redes para nossos próprios fins. ==Existem outras redes além das nossas ligadas em outros lugares==: nossos amigos, vizinhos, qualquer pessoa pode ter uma rede de computadores. Mas é ==inviável== ligarmos cabos entre nossas casas e o resto do mundo, então ==como nos podemos lidar com isso?== Muito bem, já existem cabos ligados a sua casa, como por exemplo, cabos de eletricidade e telefone. A estrutura do telefone já conecta nossa casa com o resto do mundo, então é exatamente o que nós precisamos. Para conectar nossa rede a rede telefônica, precisamos de um equipamento especial chamado ==modem==. Este modem ==transforma a informação da nossa rede== em uma informação ==gerenciável pela rede telefônica e vice-versa==.
- ![[Pasted image 20221223150939.png]]

- Então nós estamos ==conectados à infraestrutura telefônica==. O próximo passo ==é enviar mensagens da nossa rede para a rede que nós desejamos alcançar==. Para fazer isto, vamos precisar conectar nossa rede a um ==Provedor de Serviço de Internet (ISP, em inglês)==. Um ISP é uma ==companhia== que ==gerencia alguns roteadores especiais que são conectados e podem também acessar roteadores de outros ISPs==. Então a mensagem da nossa rede é transportada para a rede de redes do ISP e então para a rede de destino. ==A Internet é composta por toda esta infraestrutura de redes==.
- ![[Pasted image 20221223151012.png]]

### Encontrando computadores
- Se você quer enviar uma ==mensagem para um computador==, você precisa ==especificar== qual é este computador. Por isso, qualquer computador conectado à uma rede possui um ==único endereço de identificação==, chamado de "==Endereço IP==" (onde IP, do inglês Internet Protocol, significa Protocolo de Internet). Este é um endereço composto por uma série de 4 números separados por pontos, por exemplo: `192.168.2.10`.

- Isto é perfeito para computadores, mas nós seres humanos temos dificuldades para lembrar estes endereços. Para tornar as coisas mais fáceis, nós podemos dar apelidos aos endereços IP que nós humanos podemos compreender, chamados nome de ==domínio==. Por exemplo, google.com é um nome de domínio usado para "apelidar" o endereço `142.250.190.78` (no momento em que este artigo foi escrito. Endereços de IP podem mudar). Então, usando o nome de domínio é uma forma mais simples de encontrar um computador na Internet.
- ![[Pasted image 20221223151142.png]]

### A internet e a Web
- Como você deve ter notado, quando navegamos na Web com nossos navegadores, normalmente utilizamos os ==nomes de domínios== para chegar a um website. Isto significa que a ==Internet e a Web são a mesma coisa?== Não é tão simples assim. Como vimos, a Internet é uma ==infraestrutura técnica que permite conectar bilhões de computadores==. Entre estes computadores, ==alguns computadores (chamados de servidores Web) podem enviar mensagens inteligíveis para navegadores Web==. A ==Internet== é a ==infraestrutura==, enquanto a ==Web== é um ==serviço construído sob esta infraestrutura==. Vale a pena notar que existem diversos outros serviços que funcionam na Internet, tais como email e IRC.

### Intranets e Extranets
- ==Intranets são redes privadas restritas aos membros de uma organização particular==. Elas são geralmente usadas para ==prover um portal para que tais membros tenham acesso a recursos compartilhados==, possam colaborar e ==comunicarem-se entre si de forma segura==.

- Por exemplo, a ==intranet== de uma organização pode ==hospedar páginas da web para compartilhar informações== de departamentos ou equipes, unidades compartilhadas para gerenciamento de documentos e ==arquivos importantes==, portais para executar tarefas de administração de negócios e ferramentas de colaboração como wikis, quadros de discussão e sistemas de mensagens.

- Extranets são bastante ==semelhantes== às Intranets, exceto pelo fato de que abrem toda ou parte de uma rede privada para permitir o compartilhamento e a ==colaboração com outras organizações==.

- Elas são ==normalmente usadas para compartilhar informações de forma segura com clientes== e partes interessadas que trabalham em estreita colaboração com uma empresa. Frequentemente, suas ==funções são semelhantes às fornecidas por uma intranet==: informações e compartilhamento de arquivos, ferramentas de colaboração, fóruns de discussão, etc.

- Tanto as ==intranets== quanto as ==extranets== são executadas no mesmo tipo de ==infraestrutura== que a Internet e ==usam os mesmos protocolos==. Eles podem, portanto, ser acessados por membros autorizados de diferentes locais físicos.
- ![[Pasted image 20221223151247.png]]

# References
- https://www.minhaconexao.com.br/blog/internet/como-funciona-internet
- https://developer.mozilla.org/pt-BR/docs/Learn/Common_questions/How_does_the_Internet_work
