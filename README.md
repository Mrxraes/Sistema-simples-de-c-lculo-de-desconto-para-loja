# Sistema-simples-de-calculo-de-desconto-para-loja
Recebe os valores de input e retorna saídas para o fim de calcular o desconto para um cliente com base nas condições.
nome = input('Qual o seu nome?')    
preco = float(input('Qual o valor gasto no produto?'))
preco_form = format_currency(preco, "BRL", locale='pt_BR')
if preco > 199.90:
    print(f'Olá {nome},  valor sua compra é de {preco_form}, o que lhe dá direito a 20% de desconto!')
    resposta = input('Você gostaria?').strip().lower()
    if resposta == 'sim':
        product_descont = abs((preco * 20/ 100) - preco)
        product_form = format_currency(product_descont, "BRL", locale='pt_BR')
        print(f'Parabéns! O novo valor do seu produto é agora de {product_form}')
    elif resposta == 'não' or resposta == 'nao':
        print('Que pena, caso mude de ideia é só voltar o formulário e digitar sim!')
    else:
        print("Resposta inválida [ERRO]")
else:
    print('O valor informado não tem direito a nenhum desconto.')

    
