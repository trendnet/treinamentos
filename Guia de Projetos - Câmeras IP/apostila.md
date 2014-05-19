![logo](http://i.imgur.com/g21MEB0.png)

![capa](http://i.imgur.com/kfCeg3w.png)

##Treinamento de Projetos com Câmeras IP

Esta apostila foi gerada automaticamente, a partir do material de treinamento que se encontra publicado no site da TRENDnet Brasil. Você encontrará aqui os conceitos  básicos sobre redes locais, visando a capacitação de equipes envolvidas com projetos de monitoração de sons e imagens utilizando câmeras IP.

**Acompanhe os projetos completos contendo aplicação dos produtos em [trend.net.br](http://trend.net.br "TRENDnet Brasil").**

Estamos à disposição para quaisquer dúvidas e recomendamos consulta à rede Autorizada TRENDnet de todo o Brasil para auxiliá-lo em seus projetos.

#Projetos com Câmeras IP

A Série de Projetos IPCam apresenta para você e sua equipe artigos técnicos que irão mostrar como é simples e eficiente a utilização de Câmeras IP em projetos de monitoração de imagens e sons.
##Câmera IP x Câmera Analógica

Vantagens das Câmeras IP em relação às Câmeras Analógicas:

- Menor custo total da instalação

	Como a maioria das empresas e organizações já dispõe de uma rede local em operação, agregar um sistema de vigilância IP não requer maiores investimentos em infraestrutura. Opções cabeadas ou wireless são alternativas menos caras que cabos coaxiais dos  sistemas analógicos.

	Custos de equipamentos e gerenciamento são menores, pois soluções IP seguem padrões industriais, baseados em sistemas abertos e não em hardware proprietário como os sistemas DVR analógicos.

- Maior qualidade de imagem 

	Uma vez digitalizadas as imagens na câmera, não há mais necessidade de conversão analógico/digital, como no caso das câmeras analógicas. Também não há degradação das imagens em função de distância, outro aspecto crítico das soluções analógicas.

- Escalabilidade e flexibilidade

	Um sistema de vídeo-vigilância em rede local pode crescer conforme as necessidades do proprietário. No  caso de sistemas analógicos, o crescimento é limitado à capacidade disponível no DVR. Além disso, é preciso investir na aquisição de um novo DVR.

	O sistema IP permite a inclusão de câmeras, encoders e diversos outros dispositivos que compartilham a mesma rede cabeada ou wireless sem maiores investimentos em infraestrutura. Enquanto isso, a solução analógica requer um cabo coaxial exclusivo de cada câmera até a estação de visualização/gravação. Ainda pior, exige cabeamento exclusivo e separado para áudio, caso utilizado.

	Câmeras IP podem ser realocadas para qualquer outro ponto coberto pela rede IP, sem requerer maiores intervenções na infraestrutura. 

	Em soluções que a câmera tenha movimentação horizontal, vertical e de zoom - popularmente chamadas de PTZ (pan, tilt e zoom) - tais comandos são transmitidos pela rede existente.

- Maior confiabilidade

	Os modelos de câmeras PoE (Power over Ethernet)  dispensam tomada no local da instalação. Recebem alimentação elétrica pelo próprio cabo de rede, o que, em diversas situações, garante substancial redução de investimentos e mais qualidade no resultado final.




###Câmeras Digitais

O principal componente das câmeras digitais é o chip que mede a intensidade da luz. A lente da câmera digital projeta a imagem diretamente na área do chip de silício que contém os sensores dispostos em forma de matriz. São os pixels para os íntimos. De acordo com a luminosidade projetada em cada pixel, o sensor informa um número que corresponde à intensidade luminosa que chega àquele ponto da tela. Se a imagem é em preto e branco, basta usarmos um número no processo de digitalização. No entanto, para imagens coloridas, precisamos decompor a luz utilizando três sensores, que geram três números, respectivamente para a intensidade do vermelho, do verde e do azul. O comprimento do número, ou seja, o maior valor que ele pode alcançar, vai definir quantos níveis de cor poderemos ter. Com a palavra de 1 byte (8 bits) podemos ter 256 níveis de cor, com 2 bytes (16 bits) chegamos a 65.536 níveis e assim por diante. Isso significa que quanto mais cores tivermos, maior será a demanda de memória para armazenar a imagem digital. 

![exemplo-ccd](http://i.imgur.com/anGERJO.jpg)

Reparem que o custo de armazenar e transmitir as imagens digitais sofre uma dupla pressão. Por um lado, é desejável uma maior resolução, ou seja, pixels cada vez menores. Isso significa que iremos precisar de mais pixels para cobrir toda a imagem. Como cada pixel é um número, aumenta-se a quantidade de números. Por outro lado, também é desejável que tenhamos mais níveis de cor e para isso, precisamos utilizar palavras maiores. Com mais bits, cada número fica maior. Como as duas tendências se multiplicam, periga haver um aumento exponencial da demanda de memória e do tempo de transmissão das imagens digitais. Até agora, isso vem sendo compensado com algoritmos mais eficientes para compressão de imagens que reduzem significativamente o volume de dados.
 
Para analisar diferentes soluções envolvendo câmeras digitais, vamos considerar que quatro módulos, interligados conforme o diagrama abaixo, estarão sempre presentes nos sistemas digitais de captura e armazenamento de imagens.

![Módulos de uma Câmera Digital](http://i.imgur.com/WfQHDaY.png)

A luz é captada continuamente pelo sensor de cada pixel, gerando uma sequência de números que são passados para o processador de imagens. Este, por sua vez, realiza a preparação dos números, para gravá-los em um formato padrão, a ser reconhecido por quem vai ver as imagens, como MPEG4, JPEG, AVI, etc. Em seguida o processador de imagens escreve esses dados em um sistema de arquivos que irá persistir as imagens digitais de forma organizada em uma unidade de disco. Hoje em dia, os principais sistemas digitais funcionam desta forma. Como vamos ver a seguir, o que varia é a multiplicação destes módulos quando temos várias câmeras integradas em um único sistema.

###DVR - Digital Video Recorder

Considerando a necessidade de construir sistemas que suportassem diversas câmeras digitais, surgiram inicialmente os **DVRs (Digital Video Recorders)** que integram três módulos em um equipamento único. Utilizando tecnologia proprietária, oferecem aplicações completas para captar, gravar, armazenar e visualizar as imagens, acoplando-se a câmeras analógicas. Estes sistemas ainda existem no mercado, sendo mais explorados em nichos de soluções especializadas.

![exemplo-cftv-dvr](http://i.imgur.com/DtxkZb5.jpg)

###CFTV - Circuito Fechado de TV

Com o aumento da popularidade dos micros, e principalmente devido à sua padronização de hardware, surgiu um enorme mercado de componentes para sistemas digitais de imagens. A partir de um PC, basta instalar uma placa extensora no barramento do computador e um software proprietário no sistema operacional e temos um DVR barato, sem perda de qualquer funcionalidade. Veja abaixo um kit típico à venda no mercado atual incluindo uma placa com quatro conectores BNC, 4 sensores de imagem e respectivas fontes de alimentação e domes para proteção. Reparem que há bastante cabeamento no kit, pois cada câmera deve ser conectada ao micro por um cabo coaxial.

![exemplo-cftv-micro](http://i.imgur.com/wyhHqsk.jpg)

Esta tecnologia foi batizada de **CFTV (Circuito Fechado de Televisão)**, não que um DVR não possa ser enquadrado como tal, mas o jargão ficou popular para as soluções montadas a partir de PCs. Um Sistema CFTV com diversas câmeras seria representado pelo seguinte diagrama:

![Módulos de um Sistema CFTV (ou DVR)](http://i.imgur.com/39EX0Ie.png)

Os diversos sensores de luz são câmeras analógicas conectadas por cabos coaxiais à placa extensora instalada no micro. A placa realiza a função de Processador de Imagem, com auxílio eventual de um software aplicativo proprietário, instalado no sistema operacional do micro.  Este software aciona o Sistema de Arquivos do sistema operacional do micro para gravar as imagens digitais na Unidade de Disco.

 Uma grande desvantagem desta tecnologia está na utilização do cabeamento exclusivo, pois qualquer alteração no sistema implica em alterar também o cabeamento. Para inclusão de um novo ponto, é preciso antes passar mais um cabo, e eventualmente instalar mais uma placa extensora, para aí sim, conectarmos uma nova câmera. A tecnologia CFTV precisa ainda que um sinal analógico atravesse o cabo coaxial, estando sujeito a interferências externas que afetam a qualidade das imagens. Apesar destas limitações, este tecnologia é muito popular, possuindo uma enorme base instalada em aplicações de monitoração e segurança.

###IPCam - Câmeras IP

As Câmeras IP exploram a fraqueza do CFTV em que os cabos só servem para trafegar sinal analógico das câmeras e ainda assim estão sujeitos a interferência externa em ambientes hostis que comprometem a qualidade das imagens. As IPCams resolveram isso eliminando os cabos coaxiais e aumentando a inteligência na ponta do sistema, trazendo o Processador de Imagem para perto do Sensor de Luz. Como mostrado no diagrama a seguir, o processamento da câmera IP, além de digitalizar as imagens, utiliza um meio de comunicação digital altamente especializado, como veremos a seguir.

![Módulos de um Sistema IPCam](http://i.imgur.com/qtS9lDn.png)

O padrão **Ethernet**, que há [40 anos](http://www.theinquirer.net/inquirer/feature/2269647/ethernet-turns-40-years-old-today "Ethernet faz 40 anos em 2013") usava o [conector vampiro](http://en.wikipedia.org/wiki/Vampire_tap "Vampire tap"), hoje evoluiu para o conhecido RJ-45. Sendo largamente utilizado em residências e empresas,  interopera com vasta opção de fornecedores e meios de comunicação, trafegando dados em alta velocidade, com enorme confiabilidade e disponibilidade. A participação do Instituto de Engenheiros Elétricos e Eletrônicos, entidade  mundialmente reconhecida, foi fundamental na ratificação e aceitação de diversas variações do padrão IEEE 802.3 em cabos coaxiais e fibras óticas, depois em cabos de par trançado e rádios wireless. Nestes 40 anos, as velocidades de 10 cresceram para 10/100 e hoje temos 10/100/1000 Megabits por segundo, sempre mantendo a compatibilidade e interoperabilidade com o que já existe, chave para o sucesso de uma tecnologia que resiste por tanto tempo no topo, mesmo no mundo dinâmico atual.

No entanto, as Câmeras IP resolveram o problema da comunicação elevando o custo das pontas, pois o hardware da IPCam era, a princípio, mais caro que o da câmera analógica dos sistemas DVR e CFTV. Recentemente, a crescente popularização das IPCams reduziram seus preços, equilibrando a disputa com as câmeras analógicas. É preciso também levar em conta que a infraestrutura da rede local pode ser compartilhada entre aplicações diversas nas residências e empresas. Além de imagens, as redes podem trafegar dados e voz de forma altamente modular e flexível. O aproveitamento da rede local já existente amortiza os investimentos de instalação e manutenção do sistema de monitoramento de imagens. Basta se conectar ao switch de rede mais próximo para se acrescentar uma nova câmera, com opções que combinam conexões de par trançado, fibra ótica e/ou wireless. Uma extensão natural da rede local utiliza roteadores que se conectam à Internet para transmitir com segurança imagens digitalizadas de qualquer ponto para qualquer ponto do planeta.

O fato do tráfego na rede local ser inteiramente digital é fundamental para minimizar as interferências externas na qualidade das imagens. Um bit zero trafegando com ruído, continua sendo um bit zero, o mesmo vale para o 1. E os protocolos da rede local ainda incluem bits extras nas mensagens para correção e deteção de erros. Por exemplo, um bit de paridade que conta se é par (0) ou ímpar (1) a quantidade de bits 1 da mensagem, pode ser gerado na origem e conferido na chegada da mensagem. Com isso, detecta-se a troca de um bit qualquer da mensagem durante a transmissão, incluindo o bit de paridade. Nesse caso, o protocolo faz com que a mensagem seja repetida, ou seja, as imagens digitais que transitam na rede local tem garantia de qualidade, sem ruídos introduzidos durante o tráfego.

Nos próximos projetos mostraremos diferentes arquiteturas envolvendo Câmeras IP TRENDnet, procurando melhor explorar os recursos de software e hardware já disponíveis atualmente. Iremos configurar alguns modelos de câmera pra demonstrar como são simples e eficientes as soluções de rede com IPCams nos dias de hoje.

###O caminho percorrido pelas imagens

A figura abaixo mostra um caso típico de câmera digital colorida, em que filtros direcionam a luz de entrada para sensores que convertem em sinal elétrico a intensidade de luz vermelha, verde e azul (RGB) que chega em cada pixel. 

![Sensores captam a Imagem RGB](http://i.imgur.com/2rh8cPX.png "Sensores captam a Imagem RGB")

Conforme indicado no diagrama a seguir, o Processador de Imagem da Câmera IP realiza a conversão analógica/digital da intensidade de luz em cada pixel, gerando uma sequência de números que representa um quadro (ou "frame") da imagem. Estes números, por sua vez, são empacotados em mensagens, dentro do campo `DATA`, mostrado na figura abaixo.

![Câmera IP preenche dados de pacote de rede](http://i.imgur.com/oZRIMbv.png "Câmera IP preenche dados de pacote de rede")

Desta forma, os pacotes contendo sequências de imagens (ou "streams") podem agora percorrer a rede, seguindo por exemplo as regras do HTTP (Hypertext Transfer Protocol) que é um protocolo da camada de aplicação que utiliza outras camadas básicas, formada pelos protocolos TCP/IP e Ethernet. Abaixo um exemplo típico de pacotes que trafegam em rede. Não é preciso entender detalhes de sua formação, que inclui endereços de origem e destino da mensagem, número de portas e tamanho dos pacotes, entre outros.

![Pacotes de Rede](http://i.imgur.com/bT2SpAE.png "Pacotes de Rede")

Repare apenas como operam os protocolos modernos, oferecendo serviços em camadas. Desta forma, o campo de dados (`Data`) do pacote Ethernet é, na verdade, toda a mensagem do protocolo IP, incluindo cabeçalho e campo de dados. Por sua vez, o campo de dados do pacote IP contem a mensagem TCP e assim por diante. Isso permite que uma camada de protocolo ofereça seus serviços às camadas superiores, tornando os protocolos independentes e interoperáveis entre si.

O importante é que, ao chegar ao seu destino, a sequência de mensagens é desempacotada, recompondo novamente o quadro original da imagem, como vemos na figura a seguir, que retrata as mensagens recebidas em um micro dotado de sistema operacional com suporte a rede e navegadores Internet.

![Imagem reconstituída na tela do micro](http://i.imgur.com/HcVAduo.png)

Os pacotes que trafegam na Rede Ethernet são recebidos na placa (adaptador ou interface) de rede do micro, passam pelos "drivers" de rede e por outras camadas do sistema operacional. O resultado final é a reconstituição do "frame", ou seja, a mesma sequência de números que representa a intensidade de luz em cada pixel do quadro original da imagem. Finalmente estes dados são repassados, já desempacotados, ao navegador Internet que reproduz a imagem original na tela do micro.




###Codificação de Imagens Digitais

Vimos no projeto [Câmeras Cabeadas na LAN](http://trend.net.br/c/85/cabeada "Câmeras Cabeadas na LAN") que as câmeras IP digitalizam as imagens captadas, convertem a intensidade da luz de cada pixel em sequências de números para depois transmiti-los sob a forma de pacotes de mensagem na rede. Nada impede que as imagens digitalizadas sejam empacotadas *in natura*, tirando-se foto dos pixels e enfileirando-se uma sequência de quadros (ou *frames*) da imagem captada. Portanto, cada *frame* poderia ser transmitido sem alterações pela rede local e desempacotado no seu destino para recompor a imagem digitalizada original.

Contudo, foi comentado anteriormente na [Introdução às Câmeras IP](http://trend.net.br/c/79/introdu%C3%A7%C3%A3o "Introdução às Câmeras IP") que o armazenamento e transmissão de imagens digitais sofre uma dupla pressão. Em busca de imagens com cada vez mais definição, queremos tanto mais pixels quanto níveis de cor. Essas duas tendências se multiplicam, gerando um volume de dados cada vez maior em cada quadro da imagem.

Levando ainda em conta que 30 quadros por segundo podem ser captados pelas Câmeras IP, cria-se alta demanda por memória e velocidade de transmissão das imagens digitais. Como evitar o congestionamento, já que  todas as câmeras vão se utilizar da rede local para trafegar as imagens? Como reduzir o volume de dados das imagens digitalizadas? Qual a banda passante mínima para se trafegar imagens com qualidade ao vivo?

Seguindo a tendência das Câmeras IP em transferir para si  a inteligência, o diagrama a seguir adiciona um par de elementos que atua em sintonia: o codificador e o decodificador de imagens. 

![CODEC – Codificação e Decodificação das Imagens Digitais](http://i.imgur.com/LqAN9nt.png "CODEC – Codificação e Decodificação das Imagens Digitais.png")

O codificador é um **processamento** realizado pela câmera IP, visando compactar os quadros da imagem. Pacotes menores de mensagem economizam banda passante na rede e as mensagens chegam mais rapidamente ao destino. O decodificador realiza o **processamento inverso**, procurando restaurar as imagens o mais próximo possível da imagem original captada, antes da codificação. Este par de processadores é conhecido como [CODEC](http://pt.wikipedia.org/wiki/Codec "Codec"), onde são codificados e decodificados os frames. Sua ação é vital no sucesso atual da Câmeras IP, otimizando a transmissão e o armazenamento de imagens digitalizadas.

Os principais CODECs utilizados nas Câmeras IP foram herdados da indústria de entretenimento, envolvida com o armazenamento de filmes e músicas entre outros. Veja a seguir uma análise dos principais CODECs utilizados nas Câmeras IP.

####AVI

Audio Video Interleave ([AVI](http://pt.wikipedia.org/wiki/Audio_Video_Interleave "Audio Video Interleave")) é na verdade um formato encapsulador de áudio e vídeo criado pela Microsoft. É um dos formatos mais populares no mundo, nativamente reconhecido pelo Windows e por leitores de DVD. O formato AVI representa a imagem digitalizada *in natura*, ou seja sem compressão aplicada. Por essa razão, consome bem mais banda passante das redes. Em compensação, o padrão AVI proporciona maior nitidez, simplesmente porque a imagem decodificada é idêntica à imagem original. Os demais CODECs sempre introduzem alguma distorção nas imagens. 

####MJPG, MJPEG ou Motion JPG

No padrão Motion JPEG ([M-JPEG or MJPEG](http://en.wikipedia.org/wiki/Motion_JPEG "Motion JPEG")) cada quadro (ou *frame*) é individualmente compactado pelo JPEG, padrão pioneiro para compressão de imagens que surgiu com o QuickTime em 1990.

Veja na figura abaixo que a câmera reduz os frames originais na proporção de 1:20, aplicando o algoritmo de compressão JPEG. Os frames compactados seguem pela rede e o efeito, após a decodificação no navegador do micro, é semelhante a de um desenho animado, em que quadros superpostos em sequência criam a ilusão de movimento na tela.

![Codec Motion JPEG  envia pela rede frames originais compactados](http://i.imgur.com/c3XMSvo.png "Codec Motion JPEG  envia pela rede frames originais compactados")

####MJPEG over HTTP

O protocolo HTTP é então usado para transportar as sequências de quadros compactados, formando um HTTP *streaming*. Com isso, em resposta a um pedido `HTTP GET` para um arquivo ou *stream* JPEG, a Câmera IP enfileira uma sequência de *frames* via HTTP. Através de um `mime-type` especial no cabeçalho da mensagem, a Câmera IP sinaliza que enviará vários *frames* como resposta. As camadas de protocolo mantem a conexão TCP aberta, visto que o cliente (navegador Internet do micro) quer receber novos *frames* e o servidor (câmera IP) irá prover esses novos *frames*.

O protocolo [RTP ou Real-Time Transport Protocol](http://www.networksorcery.com/enp/protocol/rtp.htm "RTP") especifica o sequenciamento de imagens JPEG de forma a ser recebida por clientes utilizando QuickTime ou VLC. O codec MJPEG proporciona qualidade com compressão limitada, o que significa maior qualidade na imagem, ao custo de maior banda passante consumida. Em compensação, pela simplicidade do seu algoritmo, o codec MJPEG alivia tanto o processador da câmera quanto o do micro, liberando ambos para executar outras tarefas. 

####MPEG4

O [MPEG4](http://pt.wikipedia.org/wiki/MPEG-4 "MPEG-4") utiliza um algoritmo de compressão de dados baseado em blocos que foi utilizado inicialmente para compressão de áudio e vídeo digitais. Introduzido no final de 1998 para designar um grupo de padrões de codificação de som e vídeo, foi certificado pela indústria de entretenimento, através do ISO/IEC Moving Picture Experts Group (MPEG).

O algoritmo do MPEG4 leva em conta mais que cada *frame* individual, ou seja, a sequência de *frames* é analisada e são avaliadas as diferenças, tomando-se por base um *frame* chave. A partir daí, são codificados apenas blocos de imagem que apresentem diferenças em relação ao *frame* chave. Veja no diagrama abaixo que tudo começa com a transmissão do *frame* chave compactado. A partir daí, para os demais *frames*, são enviadas apenas mudanças em relação ao *frame* chave, também compactadas. Em função das mudanças na cena, pode-se eventualmente renovar o *frame* chave, visando otimizar a banda passante na rede.

![Codecs MPEG4 e H.264 analisam a sequência de frames e enviam só o que mudou](http://i.imgur.com/1bswCro.png "Codecs MPEG4 e H.264 analisam a sequência de frames e enviam só o que mudou")

####H.264

A abrangência do MPEG4 foi além da codificação multimídia e surgiu o [H.264](http://en.wikipedia.org/wiki/H.264/MPEG-4_AVC "H.264/MPEG-4 AVC"), baseado no MPEG-4 Parte 10 ou AVC (*Advanced Video Coding*). Tendo o transporte de vídeos sempre levado em conta,  desde a primeira versão em 2003, o algoritmo de compressão de dados baseado em blocos  recebeu extensões batizadas de *Fidelity Range Extensions*. É o conhecido codec de discos Blue-ray. 


###Qual o melhor codec?

Vimos a grande utilidade dos codecs e uma variedade de algoritmos que nos permite privilegiar a qualidade da imagem ou a compactação dos bits. Nesta disputa não há um vencedor único. Para se escolher o codec em uma aplicação de monitoramento de vídeo, há que se considerar a qualidade da imagem e a banda passante da rede.

Câmeras PTZ, ou *pan-tilt-zoom*, programadas em patrulha contínua, por exemplo, alternam o foco entre diferentes cenários do ambiente. Nesse caso, a opção pelo MPEG4 ou H.264 poderia fazer a câmera processar inutilmente complexos algoritmos, para sempre decidir pela renovação do *frame* chave. Por isso, se o cenário muda muito o tempo todo, é aconselhável aplicar o codec MJPEG. Caso seja necessário auditar posteriormente as imagens capturadas, como cada *frame* MJPEG transporta uma imagem completa, temos uma boa sequência de "instantâneos" de qualidade. 

O algoritmo de compactação MJPEG não exige tanto  processamento, pois cada *frame* é compactado de forma independente. Contudo, a falha em prever como serão os novos *frames* limita a eficiência deste codec à escala 1:20, ou seja, consegue-se reduzir no máximo 20 vezes o tamanho dos quadros originais da imagem digitalizada.

Veja na representação gráfica abaixo que o tamanho uniforme dos *frames* MJPEG permite prever a banda passante consumida, resultando em transmissões a taxas constantes, o que garante uma transição suave nas imagens.

![Comparando streams produzidos pelos codecs](http://i.imgur.com/zWOkSPw.png "Comparando streams produzidos pelos codecs")

Por sua vez, os codecs MPEG4 e H.264, foram desenvolvidos para dar qualidade à imagem, mesmo em situações de banda passante reduzida. Esta opção permitiu popularizar, de uma forma sem precedentes, o tráfego de imagens na rede mundial.

Recomendados para imagens ao vivo, são bem melhores na compactação dos bits, com alguma perda na qualidade. Veja no diagrama acima que, por causa da variação no tamanho dos pacotes, é  difícil prever a banda passante que os codecs MPEG4 e H.264 irão necessitar. Contudo, graças à compressão de 1:50 que eles proporcionam, vemos vídeos em profusão sendo transmitidos em conexões lentas, alimentando a explosão *mobile*. 

O ponto forte dos codecs MPEG4 e H.264 são algoritmos inteligentes que requerem potência de processamento para prever o comportamento das imagens na codificação e decodificação dos *frames*. Veja no [AVC Audio Video Standard](http://iphome.hhi.de/wiegand/assets/pdfs/DIC_H264_07.pdf "H.264/AVC Video Coding Standard") resultados comparativos como o mostrado abaixo em que o H.264 compacta 37% mais dados que o MPEG-4.

![Comparação H.264 & MPEG-4.png](http://i.imgur.com/zXXVF9r.png "Comparação H.264 & MPEG-4.png")

Aumentar a inteligência na ponta é a razão de ser e do sucesso da tecnologia que turbina os sistemas de monitoração de imagens baseados em Câmeras IP.
## Roteador conecta rede local à Internet

Os [roteadores](http://pt.wikipedia.org/wiki/Roteador "Roteador") são dispositivos equipados com diversas portas de comunicação que encaminham mensagens entre redes distintas de computadores. Quando uma das portas recebe um pacote de dados, o roteador lê o endereço contido na mensagem para determinar seu destino final. Em seguida, consultando informações armazenadas internamente e/ou seguindo as regras específicas do protocolo, é capaz de direcionar o pacote adequadamente na rede.

O exemplo abaixo mostra um diagrama típico empregado tanto em residências quanto em pequenas e médias empresas, onde um roteador está conectado na rede local e também a um provedor Internet.

![Roteador conecta rede local à Internet](http://i.imgur.com/BOIecDY.png "Roteador conecta rede local à Internet")

Estão realçados em vermelho dois endereços típicos do roteador:

- **privado**: o da porta conectada à rede local (endereço 192.168.10.1);
- **público**: o da porta conectada ao modem do provedor Internet (que disponibilizou por exemplo o endereço 200.175.30.110).

O roteador é responsável pelo tráfego entre os micros da rede local e a Internet,  transferindo informações como páginas web, e-mails, dados, imagens, vídeos, etc.

Na prática, os roteadores da atualidade não se limitam exclusivamente ao roteamento e  também incorporam funções como modem digital, switch, firewall, ponto de acesso wireless,  servidor DHCP e DNS dinâmico, integradas em um único dispositivo. Esta otimização reduz o custo das redes e populariza uma tecnologia que garante total interoperabilidade entre todos os fabricantes de hardware e software.


##IPv4 e IPv6

Cada dispositivo na Internet deve estar associado a um endereço IP para que possa se comunicar com os demais.  A versão 4 do protocolo Internet ([IPv4](http://en.wikipedia.org/wiki/IPv4 "IPv4")) surgiu no início da década de 80 e foi a primeira a ser largamente difundida em público, originada no projeto DARPA de defesa norte-americano que publicou a [RFC 791](http://tools.ietf.org/html/rfc791 "RFC 791").

O IPv4 inclui um esquema de endereçamento com identificadores numéricos com 32 bits. Estes endereços são tipicamente divididos em 4 partes, separadas por ponto, resultando em quatro octetos (ou bytes) na faixa de 0 a 255. Consequentemente o IPv4 proporciona uma capacidade de endereçamento de aproximadamente 4,3 bilhões de endereços.

A falta de endereços não era uma preocupação dos projetistas quando o IPv4 foi criado. Contudo, dez anos depois, após medidas paliativas  para economizar endereços, ficava claro que algo deveria ser feito para evitar a exaustão de endereços IPv4. Mudanças na infraestrutura da Internet seriam necessárias.

Iniciada em 1992 com uma chamada para artigos técnicos da IETF (Internet Engineering Task Force) iniciou-se um trabalho em cooperação unindo grandes empresas como  ATT, Microsoft, Digital, CERN, MIT, Xerox e Cisco, entre outras. Algum tempo depois, a tarefa de se mudar o endereçamento da Internet se mostrava complexa e uma versão 5 foi proposta mas nunca chegou a ser usada em público.

Com a publicação da [RFC 1883](http://tools.ietf.org/html/rfc1883 "RFC 1883"), bem no final de 1995 surgiu o [IPv6](http://en.wikipedia.org/wiki/IPv6 "IPv6"), última revisão do protocolo IP utilizada hoje em dia. Comparando com o IPv4, a vantagem mais óbvia do IPv6 é um espaço de endereçamento muito maior. Utilizando endereços com 128 bits, o IPv6 permite 7.9 x 10 elevado a 28! mais endereços que a quantidade atual do IPv4. Tem endereço para se ligar de tudo na face da Terra.

Os endereços IPv6 são representados por 8 grupos de quatro digitos hexadecimais separados por dois pontos, ver dois exemplos abaixo de endereços IPv4 e IPv6.

    IPv4:	192.168.10.30
    IPv6:	2001:0db8:85a3:0042:1000:8a2e:0370:7334

##Servidor DHCP

O [protocolo DHCP](http://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol "DHCP") foi criado em 1993 para configurar  automaticamente dispositivos conectados em rede, utilizando os protocolos da Internet. Normalmente instalado no roteador que está conectado ao provedor Internet, gerencia as informações de configuração da rede. O servidor DHCP é responsável por distribuir aos usuários da rede local  as seguintes informações:

- **endereço IP**: o servidor DHCP distribui aos usuários e mantém o gerenciamento sobre os endereços IP da rede local. Por esta razão, só pode haver um servidor DHCP ativo em uma rede;
- **endereço gateway default**: este endereço informa para onde devem ser enviadas as mensagens cujo endereço de destino estejam fora da rede local;
- **um ou mais endereços de servidores DNS**: são servidores que convertem nomes virtuais em endereços IP, utilizados em praticamente todos as operações de acesso à grande rede.

Assim que um cliente da rede local implementa essas configurações, está apto a navegar na Internet.

## Pontos de Acesso

Os pontos de acesso se comunicam através de enlaces de rádio com outros elementos da rede como adaptadores Wi-fi dos micros, roteadores wireless ou outros pontos de acesso. Na maioria dos casos o ponto de acesso possui uma porta Ethernet cabeada e um rádio para conexão wireless. 

Os modernos pontos de acesso podem ser configurados para operar em múltiplos modos de acordo com as necessidades do projeto. Seguem alguns exemplos de utilização de pontos de acesso.

### Modo AP (Access Point)

O modo AP, visto na figura abaixo, é o mais comum, também chamado de modo infraestrutura. O ponto de acesso atua como um *gateway*  que permite aos usuários acessar a Internet. De acordo com o modelo, há opções para incluir serviços como NAT (*Network Address Translation*) e DHCP.

![Operação em Modo Ponto de Acesso](http://i.imgur.com/wbba7yr.png)

###Modo AP com WDS (Wireless Distribution System)

Além de operar de operar em modo AP, o ponto de acesso pode ainda proporcionar um link no padrão [WDS (Wireless Distribution System)](http://en.wikipedia.org/wiki/Wireless_distribution_system "Wireless distribution system") que permite expansão da rede, conforme vemos a seguir.

![Operação em modo AP com WDS](http://i.imgur.com/EFYnROG.png) 

###Modo AP Multiponto com WDS

No modo AP Multiponto podem ser conectados diversos pontos de acesso para formar uma grande rede sem fio. Utilizando o padrão WDS, cada ponto de acesso pode fazer o papel de estação principal, repetidor ou estação remota.

A estação principal (Main) é tipicamente conectada a uma rede cabeada, através da porta Ethernet. Repetidores são pontos de acesso localizados entre a estação principal e a estação remota, repetindo mensagens com o objetivo de ampliar o  alcance da rede. A estação remota é o ponto final que aceita conexões de clientes wireless e/ou cabeados e trafega os dados para cima, na direção da Internet. Vejam um típico diagrama multiponto a seguir.

![Operação em Modo AP Multiponto com WDS](http://i.imgur.com/6PoUOTg.png)

###Modo CPE

Neste modo, o ponto de acesso é usado como um equipamento externo CPE (*Customer Premises Equipment*) que recebe o sinal wireless da *Main Base Station*, conforme visto a seguir. Este modo é largamente utilizado por provedores de Internet banda larga na última milha de acesso a residências e empresas. Neste caso, utiliza-se a porta Ethernet para proporcionar acesso cabeado aos clientes.

Neste caso, o sinal de rádio é usado exclusivamente para conexão entre a Main Base Station e o ponto de acesso do cliente, sem conexão Wi-fi para clientes wireless.

![Modo CPE (Customer Premises Equipment)](http://i.imgur.com/0ge9Hxj.png)

###Modo Combinado AP + CPE

Neste modo, o ponto de acesso é usado como um equipamento externo (CPE) como no caso anterior, adicionando ainda as funções de gateway com NAT e DHCP. Em consequência disto, clientes wireless passam também a ser aceitos. Diferentes opções de configuração dos pontos de acesso podem ainda determinar se os clientes devam ou não estar em diferentes sub-redes da estação principal (Main Base Station).

![Modo combinado AP + CPE](http://i.imgur.com/odx9N48.png)

## Som e imagens ao vivo

Como visto até agora, as câmeras IP são capazes de enviar uma sequência de mensagens para o navegador Internet, mostrando imagens/sons captados e digitalizados em tempo real. Vimos também que essas sequências de pacotes são baseadas em algoritmos de compactação de dados, mais conhecidos como codecs. Como mostra a figura abaixo, os pacotes contendo dados compactados das imagens digitalizadas trafegam pela rede utilizando o protocolo HTTP. Ao chegarem ao navegador Internet instalado em um micro, tablet ou smartphone, as imagens são decodificadas e apresentadas na tela ao usuário.

![Tráfego HTTP de imagens digitais  entre Câmera IP e navegador Internet](http://i.imgur.com/Y7bv5CP.png)

Uma característica das câmeras IP é que independente do meio físico empregado, seja par trançado de cobre, fibra ótica, sinal wireless ou  pela teia da Internet, as mensagens geradas seguem para o seu destino em um fluxo contínuo. O que mais podemos fazer com esse fluxo contínuo de dados digitais gerados pelas câmeras IP? Veremos a seguir como a inteligência das câmeras IP pode ir além dos codecs e do protocolo HTTP para monitoração em tempo real, permitindo a gravação de arquivos na rede.

## Servidor de Arquivos

O servidor de arquivos é responsável pelas operações com arquivos na rede local. Para que um servidor de arquivos possa operar, é necessário existir um protocolo de comunicação que acione as funções de criação/exclusão de arquivos, bem como de leitura e gravação de dados nos mesmos.

###Protocolo SMB (Server Message Block)

O protocolo SMB foi criado na IBM com o objetivo de equipar o antigo sistema operacional DOS com um sistema de arquivos para redes. Mais tarde, nos anos 90, a Microsoft fundiu o protocolo SMB com o gerenciador de redes do OS/2. A partir daí, as versões subsequentes do Windows continuaram sempre adicionando novas funções ao SMB.

O SMB foi originalmente projetado para operar no topo do protocolo Netbios, em um esquema cliente-servidor em que o cliente requisitava serviços específicos e o servidor respondia apropriadamente. A popularidade do Windows e dos PCs aumentou e a partir do Windows 2000 o SMB ganhou vida própria.  O projeto Samba, que teve como objetivo inicial a engenharia reversa do SMB, permitiu o acesso a arquivos em computadores que não utilizavam o sistema operacional Microsoft. Assim, o Samba tornou-se uma implementação gratuita do padrão SMB que ficou muito popular no mundo Unix.

Visando a interoperabilidade de equipamentos e programas, o protocolo SMB convergiu para uma especificação única, tornando-se hoje um padrão de fato e de direito, em se tratando de protocolo para sistemas de arquivos em rede. Portanto são equivalentes e compatíveis entre si as implementações hoje existentes do protocolo SMB:

- [Microsoft SMB](http://en.wikipedia.org/wiki/Server_Message_Block "Microsoft SMB"), embutido no Windows desde os primórdios tempos da IBM, esteve sempre presente nos sistemas operacionais Microsoft. É acionado, por exemplo, quando criamos um "share" no Windows, dando acesso compartilhado de uma pasta de nosso computador a outros usuários da rede;    
- [Samba SMB](http://www.samba.org/cifs/docs/what-is-smb.html "Samba SMB"), com presença obrigatória na família Linux, na verdade existe desde bem antes, no tempo em que se falava de variações do sistema Unix. Trouxe o grande benefício de compartilhar arquivos entre máquinas Windows e Linux. 

A figura abaixo mostra que as operações com arquivos em rede são realizadas pela interação de dois elementos: o Cliente SMB e o Servidor SMB.  Portanto, câmeras IP equipadas com Cliente SMB são capazes de criar e gravar dados em arquivos, através da rede local. Com isso, os dados gerados pelos codecs são encaminhados para armazenamento em disco, através do Servidor SMB.  

![Tráfego SMB entre Câmera IP com Cliente SMB e Servidor SMB.](http://i.imgur.com/dcw4li3.png "Tráfego SMB entre Câmera IP com Cliente SMB e Servidor SMB.")  


### NAS (Network Attached Storage)

O [NAS (Network Attached Storage)](http://pt.wikipedia.org/wiki/Network-Attached_Storage "NAS") é um equipamento especializado em serviços de armazenamento de dados em rede local. Precisa dispor internamente de um processador, um adaptador de rede, um disco e um sistema operacional que implemente o protocolo SMB. Desta forma, as chamadas oriundas de Clientes SMB, através da rede, irão operar diretamente nos arquivos gravados em disco.   

