# EXERCICIO 1 DE 4 LOGICA DE PROGRAMAÇÃO E ALGORITIMO
print(' Bem Vindo a Loja do Lucas De Barros Santos ')
valor = float(input('Digite o valor desejado:'))
qnt = int(input('Digite a quantidade de produto desejada:'))
desconto = 0
if qnt <=9:
    desconto = 0.00
elif qnt >= 10 and (qnt <=99):
    desconto = 0.05
elif qnt >= 100 and (qnt <=999):
    desconto = 0.10
else:
    desconto = 0.15
valor_compra_sem_desconto = valor * qnt
print('O valor sem desconto é de: R$ {:.2f}'.format(valor_compra_sem_desconto))
valor_com_desconto = valor_compra_sem_desconto - valor_compra_sem_desconto * desconto
print('O valor total com desconto é de: R${:.2f}'.format(valor_com_desconto))
<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
