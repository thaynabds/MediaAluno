# MediaAluno
# Calculadora de Média de Notas

Programa simples em Python pra calcular média de 4 notas, mostrar menor/maior e se aprovou (média >=7)!

Feito por um iniciante pra iniciantes. 😊

## Como usar

1. Salva o código num arquivo `media_notas.py`
2. Abre no terminal/cmd
3. Roda: `python media_notas.py`
4. Digita as 4 notas!

## Código completo

```python
# notas do aluno - super simples!

nota1 = float(input("1 nota: "))
nota2 = float(input("2 nota: "))
nota3 = float(input("3 nota: "))
nota4 = float(input("4 nota: "))

notas = [nota1, nota2, nota3, nota4]  # lista com as notas

print("suas notas:", notas)

media = (nota1 + nota2 + nota3 + nota4) / 4
print("media:", media)

menor = min(notas)
maior = max(notas)
print("menor nota:", menor)
print("maior nota:", maior)

if media >= 7:
    print("APROVADO!")
else:
    print("REPROVADO!")
```

## Exemplo de saída

```
1 nota: 8
2 nota: 6
3 nota: 9
4 nota: 7
suas notas: [8.0, 6.0, 9.0, 7.0]
media: 7.5
menor nota: 6.0
maior nota: 9.0
APROVADO!
```

## Requisitos

- Python 3 (qualquer versão)

Pronto! Copia esse README.md pro teu repo GitHub. [canalqb.com](https://www.canalqb.com.br/2025/09/prompt-para-github-padrao-canalqb.html)
