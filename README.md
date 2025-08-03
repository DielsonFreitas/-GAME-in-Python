# -GAME-in-Python
Jogo para passar o tempo linguagem python !! progressão do curso ..

import random
from time import sleep


lista =['papel', 'pedra', 'tesoura']
jogador = str (input('Escolha entre papel, pedra ou tesoura: ')).strip()
computador = random.choice(lista)
print ('\033[35m O jogador escolheu:\033[m \033[32m {} \033[m'.format(jogador))
print ('\033[35m O computador escolheu:\033[35m \033[1;33m {} \033[33m'.format(computador))
sleep(1)

if jogador == computador:
    print ('\033[1;31m EMPATE !!\033[m')
elif (jogador == 'papel' and computador == 'pedra') or \
     (jogador == 'tesoura' and computador == 'papel') or \
     (jogador == 'pedra' and computador == 'tesoura'):
    print ('\033[32m O jogador GANHOU !!\033[m')
elif jogador in lista:
    print ('\033[7;31m O computador GANHOU !!\033[m')
else:
    print ('\033[7;31m computador GANHOU !!\033[m')
    
