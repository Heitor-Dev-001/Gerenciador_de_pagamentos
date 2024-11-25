# Gerenciador_de_pagamentos
Exercício de um Gerenciador de pagamentos em Python, programa ainda ser interface, somente a lógica.

#Elabore um programa que calcule o valor a ser pago por um produto

#Considerando que o seu preço normal e as condição de pagamento abaixo:

#Á vista dinheiro/cheque: 10% de desconto

#Á vista no cartão: 5% de desconto 

#Em até 2x no cartão: Preço normal

#3x ou mais no cartão: 20% de juros 

#Entrada do usuário
print('{:=^40}'.format('Lojas do Heitor'))

preco_normal = float (input ('Digite o preço normal do produto: R$'))
print('''Formas de pagamento: 
[1] À vista dinheiro/cheque 
[2] À vista no cartão
[3] Em até 2x no cartão 
[4] 3x ou mais no cartão''')
opcao = int (input('Digite a opção de pagamento:'))

#Calcula o valor a ser pago

if opcao == 1:
    valor_final = preco_normal * 0.90 #10 % de desconto
elif opcao == 2:
    valor_final = preco_normal *0.95 #5% de desconto
elif opcao == 3:
    valor_final = preco_normal #preço normal
    parcela = valor_final / 2
    print('Sua compra será parcelada em 2x de {:.2f} SEM JUROS'.format(parcela))
elif opcao == 4:
    total = preco_normal *1.20 #20 % de juros
    quantidade_parcelas = int(input('Quantas parcelas?'))
    parcela = total / quantidade_parcelas
    print('Sua compra será parcelada em {}x de R${:.2f} COM JUROS'.format(quantidade_parcelas,parcela))
    valor_final = total
else:
    total = 0
    print(' \033[4;31;41m Opção inválida de pagamento, FAVOR TENTE NOVAMENTE \033[m')

print('Fim do programa')
