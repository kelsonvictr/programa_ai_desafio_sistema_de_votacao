# 🎬 Desafio 1 — Sistema de Votação de Filme

Um guia passo a passo para construir um sistema de votação de filmes em Python, cobrindo conceitos fundamentais da linguagem.

## 📋 Sobre o Projeto

Este desafio consiste em criar um programa que simula uma sessão de votação de filmes. Os participantes escolhem entre três filmes, e ao final o programa exibe o vencedor com base na contagem de votos.

## 🚀 Como Executar

```bash
python votacao.py
```

## 🧠 Conceitos Abordados

- **Funções** — organização do código com `def`
- **Loop `while True`** — repetição contínua até o encerramento
- **Listas** — armazenamento dos votos com `.append()`
- **Contagem** — uso do método `.count()` para totalizar votos
- **Condicionais** — `if / elif / else` para determinar o vencedor

## 💻 Código Completo

```python
def mostrar_menu():
    print("🎬 Votação de Filme")
    print("1 - Filme A")
    print("2 - Filme B")
    print("3 - Filme C")
    print("0 - Encerrar")

votos = []

while True:
    mostrar_menu()
    opcao = int(input("Digite seu voto: "))
    if opcao == 0:
        break
    elif opcao in [1, 2, 3]:
        votos.append(opcao)
        print("✅ Voto registrado!")
    else:
        print("⚠️ Opção inválida!")

v1 = votos.count(1)
v2 = votos.count(2)
v3 = votos.count(3)

if v1 > v2 and v1 > v3:
    print(f"🏆 Filme A ganhou com {v1} voto(s)!")
elif v2 > v1 and v2 > v3:
    print(f"🏆 Filme B ganhou com {v2} voto(s)!")
else:
    print(f"🏆 Filme C ganhou com {v3} voto(s)!")
```

## 🗺️ Passo a Passo

1. **Criar o menu** — função `mostrar_menu()` exibe as opções disponíveis
2. **Loop de votação** — `while True` mantém o programa rodando até digitar `0`
3. **Guardar os votos** — cada voto válido é adicionado à lista `votos`
4. **Contar e decidir** — `.count()` totaliza os votos de cada filme e o `if/elif/else` determina o vencedor

## 🌐 Guia Interativo

Abra o arquivo `index.html` no navegador para acessar o tutorial visual completo com animações, exemplos interativos e demonstração do programa em execução.

## 🔧 Desafios Extras

- Troque os nomes "Filme A/B/C" por filmes reais
- Mostre o percentual de votos de cada filme
- Trate o caso de empate entre dois ou mais filmes
