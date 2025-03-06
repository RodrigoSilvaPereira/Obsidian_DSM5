## 🔹 1. Introdução ao TCP/IP  
O **TCP/IP (Transmission Control Protocol / Internet Protocol)** é um conjunto de protocolos que possibilita a comunicação entre dispositivos em redes de computadores. Ele é composto por diversas camadas:  

 Protocolo TCP/IP e Enderecamento de Redes  

### 🏗 **Camadas do Modelo TCP/IP**  
1. **Camada de Aplicação** → Define como os aplicativos utilizam a rede (Ex: HTTP, FTP, SMTP).  
2. **Camada de Transporte** → Garante a comunicação confiável entre dispositivos (Ex: TCP, UDP).  
3. **Camada de Rede** → Responsável pelo roteamento dos pacotes entre redes (Ex: IP, ICMP).  
4. **Camada de Enlace** → Cuida da transmissão física dos dados na rede (Ex: Ethernet, Wi-Fi).  

## 🔹 2. Endereçamento IP  
O **Endereço IP (Internet Protocol)** identifica de forma única um dispositivo dentro de uma rede. Ele é composto por 32 bits (IPv4) ou 128 bits (IPv6).  

### ✨ **Exemplo de um IP IPv4:**  
**192.168.1.10** → Representação decimal de 4 blocos de 8 bits cada.  

### 📌 **Divisão do Endereço IP**  
Um IP é dividido em duas partes:  
- **Parte de Rede** → Identifica a rede onde o dispositivo está.  
- **Parte de Host** → Identifica um dispositivo específico dentro dessa rede.  

## 🔹 3. Classes de IP  
Os endereços IPv4 são divididos em classes, conforme mostrado abaixo:  

| Classe | Intervalo de IP        | Máscara Padrão        | Uso                |
|--------|------------------------|-----------------------|--------------------|
| A      | 1.0.0.0 - 126.255.255.255 | 255.0.0.0             | Grandes redes     |
| B      | 128.0.0.0 - 191.255.255.255 | 255.255.0.0           | Redes médias      |
| C      | 192.0.0.0 - 223.255.255.255 | 255.255.255.0         | Pequenas redes    |
| D      | 224.0.0.0 - 239.255.255.255 | —                     | Multicast         |
| E      | 240.0.0.0 - 255.255.255.255 | —                     | Uso experimental  |

### 🛑 **Exemplo:**  
Um IP **192.168.1.15** pertence à **Classe C**, pois está dentro do intervalo **192.0.0.0 - 223.255.255.255** e usa a máscara padrão **255.255.255.0**.  

## 🔹 4. Máscara de Rede  
A **Máscara de Rede** define quantos bits do endereço IP pertencem à rede e quantos pertencem ao host.  

### 🔍 **Exemplo de Máscaras Padrão**  
- Classe A → **255.0.0.0** (8 bits para rede, 24 para hosts)  
- Classe B → **255.255.0.0** (16 bits para rede, 16 para hosts)  
- Classe C → **255.255.255.0** (24 bits para rede, 8 para hosts)  

## 🔹 5. Gateway Padrão  
O **Gateway** é o roteador que permite a comunicação entre diferentes redes. Ele atua como um intermediário para que os pacotes possam ser encaminhados corretamente.  

### 🔄 **Exemplo de Configuração de Rede**  
| Dispositivo | IP               | Máscara de Rede  | Gateway        |
|-------------|-----------------|-----------------|----------------|
| PC1         | 192.168.1.10    | 255.255.255.0  | 192.168.1.1    |
| PC2         | 192.168.1.20    | 255.255.255.0  | 192.168.1.1    |
| Roteador    | 192.168.1.1     | 255.255.255.0  | 192.168.1.254  |

## 🔹 6. Cálculo de IP e Sub-redes  
### 🔢 **Exemplo de Cálculo de IP**  
Dado o endereço **192.168.1.34/27**, vamos calcular:  
- **Máscara de Sub-rede:**  
  - /27 significa que há **27 bits para a rede** → **255.255.255.224**  
- **Número de hosts possíveis:**  
  - 2⁵ - 2 = **30 hosts** utilizáveis.  
- **Endereço da rede:**  
  - 192.168.1.32  
- **Primeiro IP utilizável:**  
  - 192.168.1.33  
- **Último IP utilizável:**  
  - 192.168.1.62  
- **Broadcast:**  
  - 192.168.1.63  

O **broadcast** é uma técnica de comunicação em redes de computadores onde uma mensagem é enviada de um único dispositivo para **todos os dispositivos** na mesma rede. Ou seja, um pacote de dados é transmitido para todos os endereços dentro de uma sub-rede, sem a necessidade de especificar um destino único.

### 📎 **Resumindo:**  
Se tivermos um IP **192.168.1.34/27**, podemos usar os endereços de **192.168.1.33 até 192.168.1.62** para dispositivos.  

## 📌 Conclusão  
Compreender o **TCP/IP, Classes de IP, Máscara de Rede, Gateway e Cálculo de IP** é essencial para o funcionamento e gerenciamento de redes. Esses conceitos são a base da comunicação na internet e dentro de redes locais (LANs).  

---

Esse material te ajudará a ir bem na prova (Manda um Pix pro Rodrigo de agradecimento)! 🚀  
