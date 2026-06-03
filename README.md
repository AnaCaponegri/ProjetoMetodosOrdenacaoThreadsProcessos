# Resumo do Projeto: Servidor de Hospedagem de Arquivos

* **O que é:** Um sistema cliente-servidor em **Java** com interface gráfica **Swing** para gerir e transferir arquivos em rede local.
* **Tecnologias:** Sockets (`java.net`), Concorrência (`Thread`, `SwingWorker`) e Interface Gráfica (Swing).

### 🛠️ Funcionalidades Principais
* **Servidor (`br.edu.servidor`):** Mapeia uma pasta local, exibe os metadados dos arquivos (nome, tamanho e downloads) numa `JTable`, atende requisições de download via **TCP** e responde a broadcasts de descoberta via **UDP**. Atualiza a interface em tempo real usando a EDT de forma segura.
* **Cliente (`br.edu.cliente`):** Localiza o servidor automaticamente na rede (UDP), lista os arquivos disponíveis e realiza o download em background através de um **`SwingWorker`** (evitando o travamento da interface).

### 📂 Estrutura de Pacotes
* **Servidor:** `ServidorApp` (GUI), `ServidorTCP`, `ServidorUDP`, `TratadorClienteTCP` (Thread por cliente) e `GerenciadorArquivos`.
* **Cliente:** `ClienteApp` (GUI), `ClienteTCP`, `ClienteUDP` e `DownloadWorker` (Concorrência).
