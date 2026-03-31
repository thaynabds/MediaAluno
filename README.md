---

# Atividades Python - Thayná Batista da Silva

---

## Atividade 1 - Média do Aluno

```python
# Aluna: Thayná Batista da Silva
# Atividade 1 - Média do Aluno

notas = []

for i in range(4):
    nota = float(input(f"Digite a {i+1}ª nota: "))
    notas.append(nota)

media = sum(notas) / 4

print("\n=== RESULTADOS ===")
print(f"Notas: {notas}")
print(f"Média: {media:.1f}")
print(f"Menor nota: {min(notas)}")
print(f"Maior nota: {max(notas)}")

if media >= 7:
    print("SITUAÇÃO: APROVADO")
else:
    print("SITUAÇÃO: REPROVADO")
```

---

## Atividade 2 - Caixa Eletrônico Simplificado

```python
# Aluna: Thayná Batista da Silva
# Atividade 2 - Caixa Eletrônico

saldo = 1000.00

while True:
    print("\n=== CAIXA ELETRÔNICO ===")
    print("1 - Consultar saldo")
    print("2 - Sacar")
    print("3 - Depositar")
    print("4 - Sair")
    
    opcao = input("Escolha uma opção: ")
    
    if opcao == "1":
        print(f"Seu saldo é: R$ {saldo:.2f}")
    
    elif opcao == "2":
        valor = float(input("Valor para sacar: R$ "))
        if valor > saldo:
            print("Erro! Saldo insuficiente.")
        else:
            saldo -= valor
            print(f"Saque realizado! Novo saldo: R$ {saldo:.2f}")
    
    elif opcao == "3":
        valor = float(input("Valor para depositar: R$ "))
        if valor > 0:
            saldo += valor
            print(f"Depósito realizado! Novo saldo: R$ {saldo:.2f}")
        else:
            print("Valor inválido!")
    
    elif opcao == "4":
        print("Obrigado por usar nosso caixa!")
        break
    
    else:
        print("Opção inválida! Tente novamente.")
```

---

## Atividade 3 - Pesquisa sobre Tratamento de Erros

### Qual a diferença entre erro sintático e de semântica?

**Erro Sintático:** Ocorre quando a sintaxe do código está errada. O Python detecta e mostra mensagem de erro antes de executar. Exemplo: `print("oi"` (falta fechar parênteses).

**Erro Semântico:** Ocorre quando a sintaxe está correta, mas a lógica está errada. O programa roda, mas não faz o que deveria. Exemplo: `media = nota1 + nota2 / 2` (prioridade errada nas operações).

### Por que devemos implementar em Python o Try / Except?

O `try/except` é usado para evitar que o programa quebre quando ocorre um erro. Em vez de mostrar uma mensagem de erro feia e parar, o programa continua rodando e mostra uma mensagem amigável para o usuário. É útil quando o usuário digita letra em vez de número, quando tenta dividir por zero, ou quando tenta abrir um arquivo que não existe.

### Qual a finalidade de utilizarmos o Else e Finally juntamente com o Try / Except?

O `else` executa se nenhum erro aconteceu dentro do `try`. O `finally` executa sempre, aconteça erro ou não, sendo útil para fechar arquivos, conexões de banco de dados, etc.

```python
try:
    numero = int(input("Digite um número: "))
except:
    print("Erro! Digite apenas números.")
else:
    print(f"Você digitou {numero}")
finally:
    print("Fim da tentativa.")
```

### Dicas de quando utilizar tratamento de erros

**Quando usar:**
- Entrada de usuário (sempre use `try/except`)
- Divisões (proteja contra divisão por zero)
- Arquivos (ao abrir ou escrever em arquivos)
- Conversões (ao converter string para número)
- APIs e banco de dados (ao se conectar com serviços externos)

**Quando não usar:**
- Quando o erro é um erro de programação (deve ser corrigido, não tratado)
- Quando o erro é esperado e pode ser evitado com `if` antes

---

**Aluna:** Thayná Batista da Silva

---
