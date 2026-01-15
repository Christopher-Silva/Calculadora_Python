# Calculadora_Python
Calculadora de expressões com tratamento de erros em Python.

Este é um projeto de uma calculadora dinâmica para processamento de expressões matemáticas completas. Diferente de calculadoras simples que aceitam apenas dois números, este projeto utiliza a função 'eval()' para processar sentenças matemáticas inteiras. O foco principal deste projeto foi aplicar conceitos de robustez de código e experiência do usuário no terminal. 

Funcionalidades: 
- Cálculos Dinâmicos: Processo soma, subtração, multiplicação, divisão e potências em uma única linha.
- Saída Inteligente: Reconhece o comando de independência de letras ou minúsculas (ex: "SAIR", "Sair", "sair").
- Realiza cálculos complexos em uma única linha. Exemplo: (10 + 5) * 2/4.
- Blocos 'Try/Except' para robustez do código.
- Tratamento de erro para divisão por zero ('ZeroDivisionError').
- Tratamento de erros para entradas inválidas. Exemplo: (abc + 2).
- Comando de saída amigável com '.lower()'.
- Identifica entradas inválidas ou ilógicas (letras, símbolos aleatórios) sem travar o programa.

Conceitos aplicados: 
- Loops Infinitos: Uso de 'while True' com controle de interrupção via 'break'.
- Tratamento de Exceções: Implementação de blocos 'try/except' para prevenir falhas críticas.
- Manipulação de Strings: Uso do método '.lower()' para padronização de comandos.
- Avaliação de Expressões: Uso da função 'eval()' para processamento de strings matemáticas.
