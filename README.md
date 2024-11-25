# Gerenciador_de_pagamentos
Exercício de um Gerenciador de pagamentos em Python, programa ainda ser interface, somente a lógica.

#Elabore um programa que calcule o valor a ser pago por um produto

#Considerando que o seu preço normal e as condição de pagamento abaixo:

#Á vista dinheiro/cheque: 10% de desconto

#Á vista no cartão: 5% de desconto 

#Em até 2x no cartão: Preço normal

#3x ou mais no cartão: 20% de juros 

    print('Sua compra será parcelada em {}x de R${:.2f} COM JUROS'.format(quantidade_parcelas,parcela))
    valor_final = total
else:
    total = 0
    print(' \033[4;31;41m Opção inválida de pagamento, FAVOR TENTE NOVAMENTE \033[m')

print('Fim do programa')
