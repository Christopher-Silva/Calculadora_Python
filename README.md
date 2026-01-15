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

Segue o código: 

#Calculadora Python

print("\nCalculadora Python") #  Este print informa que o programa é uma calculadora
print("\nAo desejar encerrar a calculadora, digite 'sair'") #  Este print informa como encerrar a calculadora

while True: #  While True ficará aguardando uma expressão após a outra para executar enquanto a resposta não for 'sair'
  
  expressao = input("\nDigite a expressão:") #  Recebe a expressão a ser calculada
  
  if expressao.lower() == 'sair': #  if condiciona o encerramento da calculada a palavra 'sair', a função .lower() faz com que todas as letras fiquem em minusculo para que seja exatamente "sair" caso seja digitado "Sair ou SAIR"
                                  #  Se a preferência for que a palavra 'sair' fique em maiúsculo, basta alterar .lower() por .upper()
    print("Calculadora encerrada") #  informa que a calculadora está sendo encerrada
    break #  encerra o ciclo while e para a calculadora
  
  try: #  try seria "realize este código, caso dê errado, pule para except"
    resultado = eval(expressao) #  Eval transforma a entrada em string para uma conta matemática
    print("Resultado: ", resultado) #  imprime o resultado da operação

  except ZeroDivisionError: #  Em caso de divisão por zero, será enviado a mensagem de erro para tentar novamente
    print("Erro: Divisão por zero. Tente novamente")  
  
  except: #  Em caso de operações ilógicas, como "abc + 2" será exibido a mensagem de "Expressão inválida. Tente novamente"
    print("Expressão inválida. Tente novamente") 



