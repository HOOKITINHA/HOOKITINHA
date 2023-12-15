total = 0
dinheiro = 0

while True:
    idade = input('Qual a sua idade? (Digite "sair" para encerrar) ')

    if idade.lower() == 'sair':
        break

    idade = int(idade)
    total += 1

    if idade < 3:
        ingresso = 0
    elif idade > 12:
        ingresso = 30
    else:
        ingresso = 15

    dinheiro += ingresso
    media = dinheiro / total

print('Total de pessoas: {}'.format(total))
print('Total arrecadado: {}'.format(dinheiro))
print('Média arrecadada: {}'.format(media))
<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
