# 🔌 O que é um *Socket*?  

Um **Socket** é uma interface de comunicação que permite a troca de dados entre processos, seja dentro de um mesmo computador (LocalHost) ou através de uma rede de comunicação (Processos Remotos). Ele funciona como um ponto de extremidade para a comunicação, permitindo que aplicações enviem e recebam informações de forma estruturada e independente da tecnologia de rede subjacente. A figura Abaixo, apresenta um diagrama simples mostrando como cliente e servidor interagem usando *Sockets* :  
<div align="center">
  <img src="/IMG/Socket.png" alt="Primitivas Socket" width="50%"/>
</div>
Em resumo, conforme pode ser observado na figura acima, o socket atua como uma interface que permite aos desenvolvedores criar aplicações em rede sem a necessidade de se preocupar com os detalhes de implementação da arquitetura TCP/IP.

---

## 📜 Origem no UNIX  
O conceito de *Socket* surgiu em **1983**, com a distribuição **4.2BSD do UNIX de Berkeley**.  
Na época, era necessário um mecanismo que integrasse as aplicações à camada de transporte da pilha TCP/IP, de forma padronizada e simples.  

Os *Sockets* foram projetados para:  
- Fornecer uma interface uniforme para protocolos de rede (TCP, UDP, etc.);  
- Permitir comunicação entre processos distribuídos em máquinas diferentes;  
- Ser compatíveis com diferentes protocolos de transporte.  

---

## 🌐 Importância Atual  
Apesar de terem surgido há mais de 40 anos, os *Sockets* continuam sendo **fundamentais para a comunicação em redes modernas**. Hoje, eles são a base para inúmeras aplicações e serviços, incluindo:  

- **Web**: navegadores e servidores utilizam *sockets* TCP para enviar e receber páginas, imagens e dados.  
- **Aplicativos de mensagens**: comunicação em tempo real depende de *sockets* para envio instantâneo de dados.  
- **Jogos online**: sincronização entre jogadores e servidores acontece por meio de *sockets* de baixa latência.  
- **IoT e sistemas distribuídos**: dispositivos conectados utilizam *sockets* para compartilhar dados na nuvem.  

---
## 🛠️ Primitivas de um *Socket*  

Os *Sockets* são manipulados por meio de um conjunto de **primitivas** (funções de sistema) que controlam a criação, configuração e troca de dados. As principais são:  

### 📌 Criação e Configuração  
- **`socket()`** → Cria um novo *socket* e retorna um descritor.  
- **`bind()`** → Associa o *socket* a um endereço (IP e porta).  
- **`listen()`** → Coloca o *socket* no modo passivo, pronto para aceitar conexões.  

### 📌 Conexão  
- **`connect()`** → Usado pelo cliente para solicitar conexão com o servidor.  
- **`accept()`** → Usado pelo servidor para aceitar uma conexão de um cliente.  

### 📌 Comunicação  
- **`send()` / `recv()`** → Envio e recebimento de dados em sockets orientados a conexão (TCP).  
- **`sendto()` / `recvfrom()`** → Envio e recebimento em sockets sem conexão (UDP).  

### 📌 Encerramento  
- **`close()`** → Fecha o *socket* e libera recursos.

  Em resumo temos a seguintes primitivas Socket:
<img src="/IMG/Primitivas_Socket.png" alt="Primitivas Socket" width="50%"/>  
---


