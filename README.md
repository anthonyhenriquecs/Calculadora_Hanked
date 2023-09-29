# Calculadora_Hanked

def calcular_rankeadas(vitorias, derrotas):
    saldoVitorias = vitorias - derrotas

    if vitorias < 10:
        nivel = "Ferro"
    elif 11 <= vitorias <= 20:
        nivel = "Bronze"
    elif 21 <= vitorias <= 50:
        nivel = "Prata"
    elif 51 <= vitorias <= 80:
        nivel = "Ouro"
    elif 81 <= vitorias <= 90:
        nivel = "Diamante"
    elif 91 <= vitorias <= 100:
        nivel = "Lendário"
    else:
        nivel = "Imortal"

    return saldoVitorias, nivel


# Solicitar dados do usuário
vitorias = int(input("Digite a quantidade de vitórias: "))
derrotas = int(input("Digite a quantidade de derrotas: "))

saldoVitorias, nivel = calcular_rankeadas(vitorias, derrotas)

print(f"O Herói tem de saldo de {saldoVitorias} e está no nível de {nivel}.")

