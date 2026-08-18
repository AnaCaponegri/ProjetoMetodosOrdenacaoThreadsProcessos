Servidor de Hospedagem de Arquivos — Java

Projeto de estudos desenvolvido em Java com interface gráfica Swing, utilizando comunicação em rede para criar um sistema cliente-servidor de hospedagem e transferência de arquivos em uma rede local.

📌 O que o projeto faz

O sistema é dividido em duas aplicações:

Servidor: disponibiliza arquivos para download e recebe conexões dos clientes.
Cliente: localiza o servidor na rede, visualiza os arquivos disponíveis e realiza os downloads.

A comunicação entre cliente e servidor utiliza TCP e UDP.

🛠️ Tecnologias usadas
Java
Swing
Sockets (java.net)
TCP
UDP
Threads
SwingWorker

📋 Funcionalidades
🖥️ Servidor
Mapear uma pasta local para disponibilizar arquivos
Exibir os arquivos disponíveis
Exibir nome, tamanho e quantidade de downloads
Receber solicitações de download via TCP
Responder à descoberta de servidores via UDP
Atualizar a interface durante as operações

💻 Cliente
Localizar automaticamente o servidor na rede
Listar os arquivos disponíveis
Solicitar arquivos ao servidor
Realizar downloads
Executar downloads em segundo plano sem travar a interface

🌐 Comunicação em rede
O projeto utiliza dois protocolos de comunicação:

TCP: utilizado para realizar a transferência dos arquivos.
UDP: utilizado para localizar o servidor na rede local.

🧵 Concorrência
Foram utilizados conceitos de concorrência para permitir que o sistema realize operações sem bloquear a interface gráfica.

Thread para atender múltiplas conexões no servidor
SwingWorker para realizar downloads em segundo plano
Atualização da interface gráfica de forma segura utilizando a EDT do Swing

📂 Estrutura de pacotes

| Pacote/Classe | O que faz |
|---|---|
| `br.edu.servidor` | Classes relacionadas ao servidor |
| `ServidorApp` | Interface gráfica do servidor |
| `ServidorTCP` | Comunicação TCP do servidor |
| `ServidorUDP` | Comunicação UDP do servidor |
| `TratadorClienteTCP` | Trata as conexões dos clientes utilizando Threads |
| `GerenciadorArquivos` | Gerencia os arquivos disponibilizados pelo servidor |
| `br.edu.cliente` | Classes relacionadas ao cliente |
| `ClienteApp` | Interface gráfica do cliente |
| `ClienteTCP` | Comunicação TCP do cliente |
| `ClienteUDP` | Comunicação UDP do cliente |
| `DownloadWorker` | Realiza os downloads em segundo plano |

📚 O que estou praticando

Neste projeto estou praticando principalmente:
Programação em Java
Comunicação entre aplicações
Sockets
Protocolos TCP e UDP
Programação concorrente
Threads
SwingWorker
Desenvolvimento de interfaces gráficas com Swing
Comunicação em rede local
Transferência de arquivos
