# jogos
Criação de jogos

Nome jogo: Jokenpô


from random import randint


cores = {'term':'\033[m', 
        'azul': '\033[34m',
        'branco': '\033[30m',
        'vermelho': '\033[31m',
        'verde': '\033[32m',
        'amarelo': '\033[32m',
        'rosa': '\033[35m],',
        'azulC': '\033[36',
        'cinza': '\033[37' }
cond = 0
while cond == 0:
    
    valor = str(input('Você escolhe Papel, Pedra ou Tesoura: '))
    papel = int(1)
    pedra = int(2)
    tesou = int(3)
    valor = valor.upper()
    if valor == 'PAPEL':
        valor = int(papel)
    elif valor == 'PEDRA':
        valor = int(pedra)
    else:
        valor = int(tesou)

    sorte = randint(1,3)

    if sorte == 1 and valor == 1 :
        print('{}Os dois escolheram papel Deu empate{}'.format(cores['azul'],cores['term']))
    elif sorte == 2 and valor == 2 :
        print('{}Os dois escolheram pedra Deu empate{}'.format(cores['azul'],cores['term']))
    elif sorte == 3 and valor == 3 :
        print('{}Os dois escolheram pedra Deu empate{}'.format(cores['azul'],cores['term']))
    elif sorte == 3 and valor == 2 :
        print('Você escolheu pedra e o computador escolheu tesoura')
        print('{}Pedra ganha de Tesoura, parabéns você ganhou{}'.format(cores['verde'],cores['term']))
    elif sorte == 2 and valor == 3 :
        print('Você escolheu tesoura e o computador escolheu pedra')
        print('{}Pedra ganha de Tesoura, que pena você perdeu{}'.format(cores['vermelho'],cores['term']))
    elif sorte == 2 and valor == 1 :
        print('Você escolheu papel e o computador escolheu pedra')
        print('{}papel ganha de pedra, parabéns você ganhou{}'.format(cores['verde'],cores['term']))
    elif sorte == 1 and valor == 2 :
        print('Você escolheu pedra e o computador escolheu papel')
        print('{}papel ganha de pedra, que pena você perdeu{}'.format(cores['vermelho'],cores['term']))
    elif sorte == 1 and valor == 3 :
        print('Você escolheu tesoura e o computador escolheu papel')
        print('{}tesoura ganha de papel, parabéns você ganhou{}'.format(cores['verde'],cores['term']))
    elif sorte == 3 and valor == 1 :
        print('Você escolheu papel e o computador escolheu tesoura')
        print('{}tesoura ganha de papel, que pena você perdeu{}'.format(cores['vermelho'],cores['term']))
    else:
        print('Por gentileza, da proxima vez escolher Papel, tesoura ou pedra')

    y = str(input('''Deseja jogar de novo? Sim ou não
    Resposta: '''))
    y = y.upper()

    if y == 'SIM' or y == 'S':
        print('Então vamos lá novamente!')
        cond = 0
    elif y == 'NÃO' or y == 'NAO' or y =='N':
        print('Que pena, foi bom jogar com você')
        cond = 1
    else:
        print('Não entendemos oque Você digitou mas vou considerar que sim, bora lá')
        cond = 0
