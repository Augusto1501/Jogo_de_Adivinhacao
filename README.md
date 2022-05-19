// # Jogo_de_Adivinhacao
// Primeiro projeto em PYTHON

    import random

    num = 1
    facil = 10
    medio = 5
    dificil = 3
    pontos = 0
    while pontos < 50:
        num_secreto = random.randrange(1, 11)
        print("Digite qua nível você quer jogar")
        print("Sendo {1} facil, {2} médio e {3} dificil")
        print(" ")

        niveis = int(input("Defina o nível: "))

        if (niveis == 1):
            num_tentativas = 10
        elif (niveis == 2):
            num_tentativas = 5
        else:
            num_tentativas = 3

        for num_rum in range(1, num_tentativas + 1):
            print(" ")
            print("------------------------------------")
            print("Tentativa {1} de {0}".format(num_tentativas, num))
            print(" ")
            chute = int(input("Digite um número: "))

            correto = chute == num_secreto
            maior = chute > num_secreto
            menor = chute < num_secreto

            if (correto):
                print(" ")
                pontos = pontos + 10
                print("Você acertou! Está com {} pontos".format(pontos))
                break
            elif (menor):
                print(" ")
                print("Seu chute foi menor que o número secreto")
            elif (maior):
                print(" ")
                print("Seu chute foi maior que o número secreto")
            num = num + 1
            print("------------------------------------")
        num = 1
        print("_________________________________")
    print("***********************************")
    print("FIM!")
    print("***********************************")

