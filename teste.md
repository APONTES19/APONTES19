## Em construção! #versão 1.0
# Projeto Monitoring
42 Labs 3º Edição
## Monitoring
Aplicação de monitoramento de serviços web <br>
[itens necessário pra funcionar](#ambiente-de-Desenvolvimento)
### Protocolos Suportados
HTTP<br>
PING<br>
DNS
### imagens de funcionamento
[link da imagem do programa funcionando]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
Como observado na imagem acima, o monitoring é capaz de
analisar os serviços de acordo com as [configurações](#arquivo-monitoringdb)definidas e te fornece um acompanhamento em tempo real de acordo com os parametros, além de gerar um relatorio com todos os logs para que possa acompanhar os monitoramentos passados de seus registros.
### Modo de usar
utilizando um terminal unix
1. baixe o repositório em sua máquina<br>
[link imagem baixando o programa]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
2. acesse a pasta onde foi criado o repósitorio<br>
[link imagem cd na pasta]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
3. com o terminal aberto utilize o comando `make`<br>
[link imagem rodando o make]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
4. vai no arquivo[link para a pagina em Arquivo] monitorin e altere com os serviços e protocolos que deseja monitorar.
5. novamente no terminal execute agora o comando `./monitoring` veja flag especiais[link para as flags na página]<br>
[link rodando o programa]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
6. no primeiro acesso o programa vai de pedir algumas informação<br> de configuração, não se preoculpe pois ele vai identificar caso seja <br>o segundo acesso ao programa monitoring<br>
[link imagem fazendo o primeiro acesso ao programa]
<img src="https://raw.githubusercontent.com/APONTES19/APONTES19/main/lib/img/BANNER%20GITHUB.png" width="100%">
7. Pronto agora é só analizar os logs recebidos<br>
8. Para sair do programa utilize `ctrl + c`.


#### Arquivo `monitoring.db`
Observe que é necessário alterar o arquivo [`monitoring.db`](https://imgs.xkcd.com/comics/networking_problems.png)[link para o arquivo] que está na parta ./config de acordo com suas perferência de monitoramento para isso siga a
tabela de orientação abaixo conforme o protocolo que desejar
veja que é possivel monitorar quantos serviços quizer desde que
seja os [protocolos](#protocolos-suportados) suportados.

As configurações para cada protocolo são:

| Protocolo   | Configurações                                                           |
|-------------|-------------------------------------------------------------------------|
| HTTP        | nome, protocolo, endereço, método HTTP, código HTTP esperado, intervalo |
| PING        | nome, protocolo, endereço, intervalo                                    |
| DNS         | nome, protocolo, endereço, intervalo, servidor DNS                      |

#importante os argumentos devem ser separados por um tab<br>
`site	HTTP	www.meusite.com.br	GET	200`
#### Flags de uso
`--config`<br>
ex: `./monitoring -- config`<br>
está opção de leva as configurações iniciais de uso do programa, caso queira modificar o email e caminho do monitoring.db<br>
`--simplify`<br>
ex: `./monitoring.db --simplify`<br>
está opção faz um leitura no arquivo `monitoring.log` e te traz na tela os monitoramentos  já obtidas anteriormente de forma resumida, veja que assim não é um monitoramento em tempo real e sim o historico resumido.

## Experiencia de Desenvolvimento
### fluxo grama do projeto
[link imagem do miro]<br>
Estratégia utilizada inicialmente foi olhar o projeto com um sistema funcional qual eu nunca tinha desenvolvido, então quiz simular uma situação onde o produto fosse ofertado ao publico em geral tornando partes de configurações e parametros ajustaveis e o programa como um todo com bastante monitoramento dos possiveis erros, então confesso que perdi um tempo tentando elaborar isso de forma melhor mais tive que simplificar e partir para o cor do projeto, fiz a validação do documento monitoring.db depois a validação dos protocolos e por fim a validação dentro do protocolo
assim garantindo o bom funcionamento das requisições,depois trabalhei uma forma de mostrar as requisições ao usuaria e está não fou uma parte facil
pois não conseguir gerar um monitoring.log da forma que desejava e devido ao tempo tive de abandonar a ideia e seguir da maneira que foi possivel.<br><br>
Ao desenvolver este projeto me desafie a ir além dos meus conhecimentos, confesso que não foi nada facil e em especial pelo
prazo de 7 dias para entregar uma solução e também pelo fato de ser
um mundo novo o tema de redes que não conhecia.<br><br>
Pude aprender sobre requisições em http sobre o protocolo PING sobre o que é DNS e muita coisa sobre a poderosa feramenta curl que roda em diversas aplicações de nosso cotidiano a qual não fazia a minima ideia que existia.
<br><br>
Pude aprender gerenciar melhor o tempo e ter mais foco a solução principal, também não menos importante a lidar com as distrações, pois para se desenvolver algo que não conhece tem que começar a conhecer e logo em seguida tentar executar uma versão mais simples, mais se não tiver foco acaba tentando achar soluções diferentes e complexas que demanda tempo para entendelas,gostei de trabalhar em dupla para o entendimento do projeto ao inves de trabalhar em grupo pois nos deu a possibilidade de trocar mais experiencias de implementações que deram errado e isso fez econimizar um tempo.




## Ambiente de Desenvolvimento
### Sistema Operacional:
Windowns 11 WSL2 com Distro Ubunto
### Programas:
Sistema operacional Linux, Terminal unix, Curl, Ping
### [Bibliotecas:](www.google.com)
<stdio.h><br>
<stdlib.h><br>
<string.h><br>
<sys/wait.h><br>
<unistd.h><br>
<fcntl.h><br>
<stddef.h><br>
<ctype.h><br>
### Desenvolvido por [Lucas Martins](https://github.com/APONTES19) data de desenvolvimento 03/08/2022 #versão 1.0
