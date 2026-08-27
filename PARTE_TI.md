# 📚 Estudos de TI: Computadores e Arquitetura

Resumo prático e direto ao ponto focado em concursos públicos (Padrão VUNESP).

---

## 🏗️ 1. Arquitetura de Computadores

### Modelo de Von Neumann (5 Unidades)
* **Unidade de Entrada:** Responsável por obter instruções e dados para o sistema (ex: clique do mouse, uso do teclado, webcam).
* **Unidade de Controle (UC):** Gerencia e coordena os recursos do computador.
* **Unidade Lógica e Aritmética (ULA):** Executa operações aritméticas (soma, subtração, divisão) e lógicas (comparações como maior, menor, igual, além de trabalhar com letras e números).
* **Unidade de Memória:** Dispositivos eletrônicos que armazenam informações e as fornecem quando solicitadas.
* **Unidade de Saída (E/S):** Disponibiliza ao usuário a informação processada (ex: monitor, impressora, caixa de som).

### Processo de Execução de um Programa (Ciclo de Instrução)
O processador repete este ciclo infinitamente até o programa encerrar:
1. **Busca:** A Unidade de Controle busca a instrução armazenada no endereço de memória atual.
2. **Decodificação:** O processador lê a instrução e descobre o código de operação (o que ele deve fazer).
3. **Execução:** O processador realiza a ordem da instrução.
4. **Armazenamento:** Se necessário, o resultado é guardado nos registradores.

*Resumo final:* O ciclo (busca -> decodifica -> executa) se repete continuamente até que chegue uma instrução de encerrar o programa.

---

## 📊 2. Hierarquia de Memórias
1-Mais rapida / 5-Mais lenta
> **Regra de Ouro para a Prova:**
> * Quanto mais perto da CPU $\rightarrow$ Mais rápida, mais cara e menor capacidade.
> * Quanto mais longe (base) $\rightarrow$ Mais lenta, mais barata e maior capacidade.

### 1. Registradores
* **Onde fica:** Dentro da CPU.
* **O que é:** A mais rápida e menor de todas. Guarda os dados na hora em que o processador está calculando.

### 2. Memória Cache (L1, L2, L3)
* **Onde fica:** Dentro ou muito perto da CPU.
* **O que é:** Muito rápida. Guarda os programas mais utilizados para evitar buscar na RAM.

### 3. Memória RAM
* **Onde fica:** Na placa-mãe.
* **O que é:** Volátil (apaga ao desligar). É a mesa de trabalho: os aplicativos abertos rodam aqui temporariamente.

### 4. Memória Flash
* **Onde fica:** Pendrives, cartões de memória e nos SSDs.
* **O que é:** Não volátil, sem peças móveis. Mais rápida que o HD tradicional, fica entre a RAM e o armazenamento de massa.

### 5. HD / SSD (Armazenamento de Massa)
* **Onde fica:** Conectado à placa-mãe.
* **O que é:** Não volátil. Guarda tudo de forma permanente até ser apagado. É a mais lenta e a de maior capacidade.

## 3. Barramentos
Os barramentos são as "rodovias" digitais que conectam o processador (CPU), a memória e os periféricos do computador:

* **Barramento de Dados (O quê):** Transporta a informação real que está sendo processada ou armazenada (números, textos, imagens, instruções).

* **Barramento de Endereços (Onde):** Indica a localização exata na memória de onde o dado deve ser lido ou onde deve ser gravado.

* **Barramento de Controle (Como/Quando):** Envia os sinais de comando e sincronização (ex.: "leia agora", "escreva agora", "espere").


## 💻 Resumo Técnico: Microprocessador

* **Clock (GHz):** Velocidade do processador. Mede quantos ciclos de instrução ele consegue executar por segundo (quanto maior o GHz, mais rápido).
* **Núcleos (Cores):** Divisões físicas independentes na CPU. Permitem a execução de múltiplas tarefas simultaneamente (multitarefa real).
* **Arquitetura 32 vs 64 bits:** Capacidade de processamento de dados por ciclo e limite de endereçamento de memória RAM:
  * **32 bits:** Suporta no máximo **4 GB de RAM**.
  * **64 bits:** Suporta muito mais de 4 GB de RAM (vários GBs/TBs) e lida com blocos maiores de dados.

## 💾 Resumo Técnico: Memória ROM, BIOS e UEFI

* **ROM (Read-Only Memory):** Memória **não-volátil** (os dados não se apagam quando o computador é desligado). Vem gravada de fábrica na placa-mãe.
* **Função Principal:** Armazena o firmware de inicialização do sistema (**BIOS** ou **UEFI**), responsável por fazer o autoteste do hardware (POST) e carregar o sistema operacional na memória RAM.
* **BIOS (Basic Input/Output System):** É o primeiro software que roda ao ligar o PC. Ele testa os componentes físicos (POST) e dá o "pontapé inicial" para carregar o Sistema Operacional (Windows/Linux).
* **UEFI:** É a **evolução da BIOS**. Faz a mesma coisa, mas é muito mais moderna: tem interface gráfica (dá para usar o mouse), é mais rápida, suporta HDs/SSDs maiores e é mais segura (possui o *Secure Boot*).

* ## 🔌 Resumo Técnico: Chipset e Portas de E/S

* **Chipset (Arquitetura Tradicional):** O conjunto de chips da placa-mãe dividido em duas pontes principais:
  * **Ponte Norte (Northbridge):** O lado "rápido". Conecta diretamente a CPU, a memória RAM e a placa de vídeo de alto desempenho. *(Nota moderna: hoje em dia, boa parte disso foi integrada diretamente dentro do próprio processador).*
  * **Ponte Sul (Southbridge):** O lado "lento". Gerencia os periféricos de menor velocidade e dispositivos de entrada/saída, como portas USB, discos (SATA/IDE), rede e áudio.
* **Portas de Comunicação:**
  * **Serial:** Transmite os dados de forma sequencial, **bit a bit** (um após o outro por um único canal). É mais lenta e usada antigamente para modems ou mouses seriais.
  * **Paralela:** Transmite **múltiplos bits simultaneamente** em paralelo (vários fios lado a lado). Era muito usada antigamente para impressoras legadas.
  * **USB (Universal Serial Bus):** O padrão atual, rápido, universal e *hot-swappable* (permite conectar/desconectar com o PC ligado).

---
⚠️ **Alerta de Casca de Banana (VUNESP):** Cuidado com alternativas que usam **"nunca"**, **"sempre"**, **"exclusivamente"** ou **"totalmente"**. Elas costumam ser falsas devido à generalização indevida!

## 🖥️ Resumo Técnico: Placas de Expansão e GPU

* **Placas de Expansão:** Placas de circuito impresso encaixadas nos slots da placa-mãe (como slots PCIe) para adicionar novas funcionalidades ou melhorar o desempenho do computador.
* **Placa de Vídeo (GPU):**
  * **GPU Integrada:** Vem embutida no próprio processador (CPU) ou na placa-mãe. Usa uma parcela da memória RAM principal como memória de vídeo. É mais econômica e ideal para tarefas do dia a dia (navegação, escritório).
  * **GPU Dedicada (Placa de Vídeo Offboard):** É um componente separado com seu próprio chip gráfico poderoso e sua própria memória de vídeo dedicada (VRAM). Oferece alto desempenho para jogos pesados, edição de vídeo e modelagem 3D.
* **Placa de Rede (NIC - Network Interface Card):** O componente responsável por conectar o computador a uma rede local (LAN) ou à internet. Pode ser cabeada (Ethernet/RJ45) ou sem fio (Wi-Fi), permitindo o envio e recebimento de pacotes de dados.
