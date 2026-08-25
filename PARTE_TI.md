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
