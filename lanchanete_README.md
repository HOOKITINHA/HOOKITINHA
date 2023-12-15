# EXERCICIO 2 DE 4 LOGICA DE PROGRAMAÇÃO E ALGORITIMO
print(' Bem Vindo a Lanchonete do Lucas De Barros Santos')
print('*****************Cardápio******************')
print('CODIGO |        DESCRIÇÃO        | VALOR R$')
print('    100|    CACHORRO - QUENTE    |     9,00')
print('    101| CACHORRO - QUENTE DUPLO |    11,00')
print('    102|         X-Egg           |    12,00')
print('    103|       X-Salada          |    13,00')
print('    104|        X-Bacon          |    14,00')
print('    105|         X-Tudo          |    17,00')
print('    200|     Refrigerante Lata   |     5,00')
print('    201|        Chá Gelado       |     4,00')
print('*******************************************')
valor = 0
while True:
    cod = input('Digite o Pedido desejado  (100/101/102/103/104/105/200/201):')
    if cod != '100' and cod != '101' and cod != '102' and cod != '103' and cod != '104' and cod != '105' and cod != '200' and cod !=  '201':
        print('codigo digitado invalido')
        continue
    if cod == '100':
        print('Você escolheu, Cachorro - Quente valor R$ 9,00')
        valor = valor + 9
    elif cod == '101':
        print('Você escolheu, Cachorro - Quente Duplo valor R$ 11,00')
        valor = valor + 11
    elif cod == '102':
        print('Você escolheu, X-Egg valor R$ 12,00')
        valor = valor + 12
    elif cod == '103':
        print('Você escolheu, X-Salada valor R$ 13,00')
        valor = valor + 13
    elif cod == '104':
        print('Você X-Bacon valor R$ 14,00')
        valor = valor + 14
    elif cod == '105':
        print('Você X-Tudo valor R$ 17,00')
        valor = valor + 17
    elif cod == '200':
        print('Você Refrigerante Lata valor R$ 5,00')
        valor = valor + 5
    elif cod == '201':
        print('Você escolheu, Chá Gelado R$ 4,00')
        valor = valor + 4
    print('Deseja mais alguma coisa?')
    print('1-Sim')
    print('0- NÃO')
    deseja_algo_mais = input()
    if deseja_algo_mais == '1':
        continue
    else:
        print('Pedido finalizado total a ser pago é R${:.2f}'.format(valor))
        break


<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
