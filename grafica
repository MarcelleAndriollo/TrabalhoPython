print("Bem-vindo(a) a gráfica da Marcelle Tiemi Suzuki Andriollo")

def escolha_servico():
    #Lista de serviços disponíveis com custo por página
    servicos_validos = {
        "dig": 1.10,
        "ico": 1.00,
        "ipb": 0.40,
        "fot": 0.20
        }

    while True:
        #Pedindo ao cliente qual serviço ele deseja realizar
        print("\nEscolha o serviço desejado:")
        print("DIG - Digitalização")
        print("ICO - Impressão Colorida")
        print("IPB - Impressão Preto e Branco")
        print("FOT - Fotocópia")
        servico = input("Digite o serviço desejado (dig/ico/ipb/fot): ").strip().lower()
        if servico in servicos_validos:
            return servicos_validos[servico]
        else:
            #Informa ao cliente que a opção escolhida não é válida
            print("Opção inválida. Por favor, escolha uma opção válida (dig/ico/ipb/fot).")

def num_pagina():
    while True:
        try:
            #Pergunta ao cliente o número de páginas
            num_paginas = int(input("Digite o número de páginas: "))
            if num_paginas >= 20000:
                #Verifica se o número de páginas está dentro do permitido
                print("Quantidade de páginas não aceita. Tente novamente.")
                continue

            #Aplicação os descontos
            if num_paginas < 20:
                return num_paginas
            elif num_paginas < 200:
                return num_paginas * 0.85
            elif num_paginas < 2000:
                return num_paginas * 0.80
            else:
                return num_paginas * 0.75
        except ValueError:
            print("Por favor, insira um número válido.")

def servico_extra():
    #Serviços extras com valor
    extras_validos = {
        "1": 15.00,
        "2": 40.00,
        "3": 0.00
    }

    while True:
        #Pergunta ao cliente qual serviço deseja adicionar
        print("\nEscolha um serviço adicional:")
        print("1 - Encadernação Simples (R$ 15,00)")
        print("2 - Encadernação Capa Dura (R$ 40,00)")
        print("3 - Nenhum adicional")
        extra = input("Digite o serviço adicional (1 para encadernação simples, 2 para encadernação de capa dura, 3 para nenhum): ").strip()
        if extra in extras_validos:
            return extras_validos[extra]
        else:
            #Informa ao cliente que a opção é inválida e vai repetir a pergunta
            print("Opção inválida. Por favor, escolha uma opção válida 1,2,3")

#Seleção do serviço
custo_servico = escolha_servico()
#Número de páginas com desconto
num_paginas_com_desconto = num_pagina()
#Seleção do serviço adicional
custo_extra = servico_extra()


#Cálculo do total a pagar
total = (custo_servico * num_paginas_com_desconto) + custo_extra
print(f"\nO valor total a pagar é: R${total:.2f}")
