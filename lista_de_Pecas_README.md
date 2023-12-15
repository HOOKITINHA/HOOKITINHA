lista_peca = []
codigo_peca = 0

def cadastrar_peca(codigo):
    print('----- Bem Vindo ao MENU de Cadastrar Peças -----')
    print('Código da Peça: {}'.format(codigo))
    nome = input('Digite o Nome da peça: ')
    fabricante = input('Digite o Fabricante da peça: ')
    preco = int(input('Digite o Preço (R$) da peça: '))
    
    dicionario_peca = {'codigo': codigo,
                       'nome': nome,
                       'fabricante': fabricante,
                       'preco': preco}
    
    lista_peca.append(dicionario_peca.copy())

def consultar_peca():
    print('----- Bem Vindo ao MENU de Consultar Peça -----')
    opcao_consultar = input('\nEscolha a opção:\n'+
                            '1 - Consultar todas as Peças\n'+
                            '2 - Consultar peças por Código\n'+
                            '3 - Consultar peças por Fabricante\n'+
                            '4 - Retornar\n>> ')
    if opcao_consultar == '1':
        print('Você escolheu a opção Consultar Todas as peças')
        for peca in lista_peca:
            for key, value in peca.items():
                print('{}: {}'.format(key, value))
            print('--------------------')
    elif opcao_consultar == '2':
        print('Você escolheu a opção Consultar peça por Código')
        valor_desejado = input('Digite o Código desejado: ')
        for peca in lista_peca:
            if int(peca['codigo']) == int(valor_desejado):
                print('--------------------')
                for key, value in peca.items():
                    print('{}: {}'.format(key, value))
                print('--------------------')
    elif opcao_consultar == '3':
        print('Você escolheu a opção Consultar peça por Fabricante')
        valor_desejado = input('Entre com o Fabricante desejado: ')
        for peca in lista_peca:
            if peca['fabricante'] == valor_desejado:
                print('--------------------')
                for key, value in peca.items():
                    print('{}: {}'.format(key, value))
                print('--------------------')
    elif opcao_consultar == '4':
        print('Você escolheu a opção Retornar ao MENU anterior')
        return
    else:
        print('Opção Inválida. Tente novamente.')

def remover_peca():
    print('----- Bem Vindo ao MENU de Remover Peça -----')
    valor_desejado = int(input('Digite o código da peça que deseja remover: '))
    for peca in lista_peca:
        if peca['codigo'] == valor_desejado:
            lista_peca.remove(peca)
            print('Peça Removida')

print('----- Bem Vindo ao Controle de Estoque da Bicicletaria do Lucas De Barros Santos -----')

while True:
    opcao_principal = input('\nEscolha a opção desejada:\n'+
                            '1 - Cadastrar peça\n'+
                            '2 - Consultar peça\n'+
                            '3 - Remover peça\n'+
                            '4 - Sair\n>> ')
    
    if opcao_principal == '1':
        codigo_peca += 1
        cadastrar_peca(codigo_peca)
    elif opcao_principal == '2':
        consultar_peca()
    elif opcao_principal == '3':
        remover_peca()
    elif opcao_principal == '4':
        break
    else:
        print('Opção Inválida. Tente novamente')


<!---
HOOKITINHA/HOOKITINHA is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
