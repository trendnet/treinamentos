# TRENDnet Brasil
## Projeto para Estação de Embalagem de Fábrica

### Solução solicitada pelo cliente

    From: Jose Luis

	Bom dia!
    Preciso de uma solução de gravação por ip.
    
    Uma câmera IP e gravação no HD do computador local sendo iniciada a gravação de vídeo quando houver movimento.
    
    ele quer que customize o nome do arquivo isso é:
    Se a câmera gravar c:\Videos\grav01.avi
    para C:\videos\codigo_grav01.avi
    
    Existe alguma solução que atenda essa solicitação??
    
    att

### Estação de embalagem da fábrica

Em contato com José Luís, foram obtidas informações a respeito do trabalho a ser realizado. Trata-se de uma estação de embalagem da linha de produção de uma fábrica que precisa monitorar e gravar as imagens da operação, através de uma câmera IP. A estação contém uma mesa onde será embalado o produto. A câmera IP está iluminando a mesa, de forma a registrar a embalagem do produto final. Equipando a estação há um micro acoplado a uma balança.

### Sequência de operação

- Uma EMBALAGEM numerada, ou seja, identificada por um CÓDIGO, é colocada na mesa;
- O micro tem conhecimento prévio do CÓDIGO da EMBALAGEM no início da operação;
- A câmera IP deve iniciar a gravação das imagens, associando-as ao CÓDIGO;
- O produto final é acondicionado dentro da EMBALAGEM pelo operador;
- O micro é acionado para registrar o peso total da EMBALAGEM;
- A EMBALAGEM é retirada da estação ao final da operação;
- O vídeo da operação fica acessível através do CÓDIGO;

### Diagrama da Rede Local
O diagrama abaixo mostra a arquitetura utilizada na Estação de Embalagem. O micro está conectado à câmera através da rede local. O switch da rede está representado pela barra horizontal, com endereços IP na faixa 192.168.10.X. 

![Estação Embalagem](http://i.imgur.com/wXC1dxz.png)

Para efeito deste exemplo, os endereços IP da rede são portanto:

    192.168.10.35  TV-IP302PI
    192.168.10.101 Micro

### Solução sugerida

A detecção de movimento é o melhor gatilho para disparar a gravação das imagens. Esse método é bastante preciso, sensível a qualquer movimentação na área iluminada pela câmera. A câmera TRENDnet TV-IP302 possui ainda portas de entrada e saída que podem ser utilizadas com sensores de presença para detetar o início da operação. Contudo, a introdução de mais hardware sempre pode comprometer a confiabilidade da solução.

![TV-IP302PI](http://i.imgur.com/hI7TiNT.jpg)

Utilizaremos o micro para armazenar os vídeos gerados pela câmera IP. Supondo que há possibilidade de acionar um software no micro para gerenciar a operação, podemos executar os passos descritos a seguir.

#### 1. Criar área compartilhada no micro  

Com o Windows Explorer, criar a pasta `c:/_public/cam` no micro para armazenar os vídeos, como visto abaixo:

![Share 1](http://i.imgur.com/8EmRwsy.png)

Clicar com botão direito do mouse na pasta criada e selecionar `Share with Specific People`.

![Share 2](http://i.imgur.com/CFSoimG.png)

Selecionar `Everyone` como visto a seguir.

![Share 3](http://i.imgur.com/Gna4IbR.png)

Habilitar permissão de `Leitura/Escrita`, conforme mostrado a seguir e clicar no botão `Share`. 

![Share 4](http://i.imgur.com/COP3MNT.png)

Para verificar que a pasta está realmente disponível em rede, acessar pelo Windows Explorer, utilizando o endereço baseado no nome do micro (`\\CANOAS22`) e constatar que a pasta compartilhada aparece. 

![Share 5](http://i.imgur.com/a42q5OL.png)

#### 2. Configuração da câmera TV-IP302PI

Não iremos detalhar toda a configuração da câmera, somente as telas principais relacionadas ao acionamento da detecção de movimento. Utilizaremos um comando CGI que permite configurar a câmera através do protocolo `http`.

Para esta aplicação, a câmera IP pode ser configurada em 2 passos:

- Configura-se o endereço do folder compartilhado para gravação do vídeo.
- Configura-se a área desejada para deteção de movimento;

##### 2.1. Configuração da pasta compartilhada

Com um navegador Internet, acessar o endereço da câmera e selecionar `Setup | Network | Event Server`. Na seção `Samba` digitar o endereço da pasta compartilhada no campo `Location`. Os campos `Workgroup`, `Username` e `Password` se referem à autenticação de um usuário válido do micro.

![Samba 1](http://i.imgur.com/SX03Sly.png)

##### 2.2. Configuração da zona de deteção de movimento

Navegar para `Setup | Event Configuration | Motion Detection` e demarcar a área desejada onde se quer detectar o movimento.

![Deteção de Movimento](http://i.imgur.com/V0TZDp8.png)

Reparar que a `Area 1` (em azul) selecionada está associada ao Samba, ou seja, gravação de vídeo em uma pasta compartilhada de disco, utilizando o padrão Samba. Veja mais detalhes no [Projeto Gravando no NAS](http://trend.net.br/c/108/gravando-no-nas "Gravando no NAS").

#### 3. Gravação de vídeos

Observe na pasta compartilhada que a câmera ira gravar os vídeos assim que forem detectados movimentos na zona azul pré-configurada.

![Gravação vídeos](http://i.imgur.com/9m2l5Qc.png)

Os nomes dos arquivos incluem a data e a hora em que o vídeo foi gravado, como abaixo:

    \\CANOAS22\cam\20150428\161956m.avi

#### 4. Introdução do CÓDIGO da EMBALAGEM

Para completar a especificação do projeto, é preciso associar os vídeos gravados com o CÓDIGO de cada EMBALAGEM montada na linha de produção. Para isso, utilizaremos dois comandos CGI suportados pela câmera TRENDnet TV-IP302PI.

Estes comandos deverão ser executados a partir de um software do micro, em sincronismo com a linha de produção. Uma opção seria o próprio micro já saber o CÓDIGO da EMBALAGEM a ser montada. Outra opção seria, por exemplo, um leitor de código de barras no micro que fosse acionado para ler a etiqueta da EMBALAGEM. De qualquer forma, o micro deve saber de antemão, antes da operação iniciar, qual o CÓDIGO da EMBALAGEM a ser montada.

Para simular o software do micro utilizaremos um navegador Internet nesse exemplo.

##### 4.1 Comando GetSamba

Através do navegador Internet, digitaremos o comando CGI abaixo na linha de endereço:

    http://192.168.10.35/GetSamba.cgi

O resultado surge na tela do navegador, visto abaixo:

![GetSamba](http://i.imgur.com/MXI1kwM.png)

Repare que a câmera retornou com o parâmetros de configuração do Samba:

    SMB_URL=\\192.168.10.104\cam
	SMB_Group=workgroup
	SMB_User=studio
	SMB_Pwd=tnet
	SMB_Isaddfolder=0

##### 4.2 Comando SetSamba

Como precisamos introduzir o CÓDIGO da EMBALAGEM para criar uma área customizada para armazenamento dos vídeos, vamos primeiro criar um novo folder com um CODIGO, por exemplo, `SKU-1234`, dentro da pasta `cam`.

![Codigo 1](http://i.imgur.com/jh2AFKv.png)

Agora utilizaremos o comando abaixo para configurar a câmera para gravar na nova pasta:

    http://192.168.10.35/SetSamba.cgi?SMB_URL=\\192.168.10.104\cam\SKU-1234&SMB_Group=workgroup&SMB_User=studio&SMB_Pwd=tnet&SMB_Isaddfolder=0

![SetSamba](http://i.imgur.com/QQgw5FF.png)

Repare que ao acessarmos novamente a câmera pelo navegador, a nova configuração será exibida no menu `Setup | Network | Event Server`.

![New Samba](http://i.imgur.com/7k4bM5R.png)

A partir deste momento, assim que for detectado movimento, vídeos serão gravados na pasta que inclui o CÓDIGO da EMBALAGEM, ou seja, `SKU-1234`, acrescida das informações de data e hora:

    \\CANOAS22\cam\SKU-1234\20150428

![Código OK](http://i.imgur.com/zAKCSsb.png)

Desta forma, temos uma pasta compartilhada na rede com os videos gravados em função dos CÓDIGOS das EMBALAGENS montadas na linha de produção.

![Pasta com CÓDIGO da EMBALAGEM](http://i.imgur.com/tGA9r2j.png) 
