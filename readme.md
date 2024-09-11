# Calculadora Assembly

Desenvolvido no primeiro semestre na curso de engenharia da computação na UFPEL, este repositório contém um programa em linguagem Assembly projetado para realizar operações aritméticas básicas: adição, subtração, multiplicação, divisão e cálculo de fatorial. 

## Visão Geral do Programa

O programa é baseado em um sistema simples de entrada e saída que lê entradas do usuário, processa operações aritméticas e retorna o resultado. Ele usa endereços de memória específicos e segue um fluxo estruturado para lidar com diferentes operações.

### Mapeamento de Memória

- `OPE (255)`: Operação a ser realizada.
- `OP1 (254)`: Primeiro operando.
- `OP2 (253)`: Segundo operando.
- `C (252)`: Contador usado em loops.
- `R (251)`: Registrador temporário para resultados intermediários.
- `ESPERA (0)`: Atraso entre operações.
- `UM (1)`: Valor constante usado para decrementos e comparações.

### Fluxo de Execução

1. **Entrada do Menu:**
   O programa começa lendo uma entrada para determinar a operação (`SOMA`, `SUBT`, `MUL`, `DIV`, ou `FAT`).
   
2. **Entrada dos Operandos:**
   Aguarda-se a entrada de dois operandos (`OP1` e `OP2`) para as operações.

3. **Processamento da Operação:**
   Com base na operação selecionada, o programa pula para o subprograma correspondente:
   
   - **SOMA**: Adiciona `OP1` e `OP2`, e então exibe o resultado.
   - **SUBT**: Subtrai `OP2` de `OP1`, e então exibe o resultado.
   - **MUL**: Multiplica `OP1` por `OP2` usando adição repetida, simulando a multiplicação.
   - **DIV**: Realiza a divisão inteira de `OP1` por `OP2`, contando o número de subtrações.
   - **FAT**: Calcula o fatorial de `OP1` usando multiplicação repetida.

4. **Saída:**
   O resultado da operação é armazenado e exibido. O programa retorna ao menu para aguardar a próxima operação.

5. **Saída:**
   Se uma operação não reconhecida for inserida, o programa encerra a execução.

### Operações em Detalhe

- **Adição (SOMA)**: Adiciona dois operandos e exibe a soma.
  
- **Subtração (SUBT)**: Subtrai o segundo operando do primeiro e exibe a diferença.
  
- **Multiplicação (MUL)**: Multiplica os operandos usando adição repetida. Lida com casos em que um dos operandos é zero.
  
- **Divisão (DIV)**: Realiza a divisão inteira usando subtração repetida, contando o número de subtrações.
  
- **Fatorial (FAT)**: Calcula o fatorial de um número por meio de um loop que multiplica a sequência decrescente de números.
