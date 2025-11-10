# Python Descomplicado

### Introdução

Seja bem-vindo ao mundo da programação! Se você sempre quis aprender como "conversar" com computadores, mas achava tudo muito complicado ou técnico, este guia foi feito para você.

Escolhemos o Python como seu ponto de partida por um motivo simples: é a linguagem perfeita para quem está começando. Ela é famosa por ser fácil de ler (quase como escrever em inglês), poderosa (usada por empresas como Google, Netflix e Instagram) e incrivelmente versátil.

Esqueça os manuais densos e os exemplos que não fazem sentido. O objetivo deste ebook é ir direto ao ponto. Vamos focar nos pilares essenciais que você *realmente* precisa para construir seus primeiros programas funcionais.

Em vez de teoria abstrata, usaremos exemplos do dia a dia — como verificar a idade de um usuário, calcular o preço de um produto ou organizar uma lista de tarefas. Nosso compromisso é usar uma linguagem simples e mostrar o código em contextos reais.

Prepare-se para descobrir que programar pode ser intuitivo e muito recompensador. Vamos começar?

---

### 1. Variáveis: As "Caixinhas" para Guardar Seus Dados

**Explicação Simples:**
Pense em variáveis como caixas etiquetadas. Você dá um nome à caixa (a variável) e usa o sinal de igual (`=`) para guardar algo dentro dela. Isso permite que você armazene informações para usar (ou modificar) depois. O nome da variável deve ser claro, como `nome_cliente` em vez de apenas `n`.

**Exemplo em Contexto Real (Cadastro de Loja):**
Imagine que você precisa guardar os dados básicos de um novo cliente para usar mais tarde no programa.

```python
# Armazenando o nome e a idade de um cliente
nome_cliente = "Ana Sousa"
idade_cliente = 29
email_cliente = "ana.sousa@email.com"

# Agora podemos usar essas "caixas" em outro lugar
# Por exemplo, para imprimir uma mensagem de boas-vindas:
print(f"Boas-vindas, {nome_cliente}!")
print(f"Enviaremos sua fatura para: {email_cliente}")

1.1 Dando Nomes: As Regras Para Etiquetar Suas "Caixinhas"
Explicação Simples: Você não pode dar qualquer nome para uma variável. Existem regras simples:

Sem espaços: Use o underline (ou "traço baixo") _ no lugar. Ex: nome_cliente (isso é chamado de "snake_case" e é o padrão do Python).

Comece certo: Variáveis devem começar com uma letra ou com _. Elas não podem começar com um número.

Sem acentos ou símbolos: Evite ç ou &, $ (use apenas letras, números e _).

Diferencia maiúsculas: Nome é uma variável DIFERENTE de nome.

Exemplo em Contexto Real (Nomes Bons vs. Ruins): Vamos tentar nomear as variáveis para um cadastro de produto.

Python

# BOM (Padrão Python)
nome_produto = "Camiseta Branca"
preco_custo = 49.90
estoque_loja_sp = 150

# MAU (Evite isso!)
# 1produto = "Camiseta"      # ERRO: Começa com número
# nome produto = "Camiseta"  # ERRO: Tem espaço
# preço-custo = 49.90        # ERRO: Usa hífen (Python acha que é subtração)
# @estoque = 150             # ERRO: Usa símbolo especial
2. Tipos de Dados: O Que Você Está Realmente Guardando?
Explicação Simples: O Python gosta de saber que tipo de informação está na "caixa". Se você guardar o número 5, ele sabe que pode fazer contas. Se guardar o texto "5", ele tratará apenas como um caractere.

Os tipos básicos são:

Texto (string ou str): Sempre entre aspas. Ex: "Olá", "R$ 19,90"

Números Inteiros (int): Sem casas decimais. Ex: 10, 42, -5

Números Decimais (float): Usam ponto para separar. Ex: 19.99, 1.5

Lógico (boolean ou bool): Só pode ser True (Verdadeiro) ou False (Falso).

Exemplo em Contexto Real (Ficha de Produto): Vamos definir um produto em um e-commerce. Cada informação tem o tipo certo para que o sistema funcione (por exemplo, usar o preco para calcular o total e o em_estoque para saber se pode vender).

Python

# Diferentes tipos de dados descrevendo um produto
nome_produto = "Fone de Ouvido Sem Fio" # str (Texto)
quantidade_estoque = 50                # int (Inteiro)
preco_unitario = 149.90                # float (Decimal)
em_estoque = True                      # bool (Lógico)
2.1 A Mágica da Conversão: Quando Texto Vira Número
Explicação Simples: O Python é muito rígido com tipos. Ele não deixa você somar o número 10 com o texto "5". O problema é que o comando input() (que usamos para perguntar coisas ao usuário) sempre retorna TEXTO.

Se você pede a idade e o usuário digita 30, o Python não guarda o número 30, ele guarda o texto "30". Precisamos "converter" manualmente esse texto para um número antes de fazer contas.

Exemplo em Contexto Real (Calculando Ano de Nascimento): Vamos perguntar a idade do usuário e calcular (aproximadamente) o ano em que ele nasceu.

Python

# 1. O input() SEMPRE retorna um TEXTO (str)
idade_texto = input("Digite sua idade: ") # O usuário digita "25"

# 2. Se tentarmos fazer contas com o texto, dará erro!
# ano_nascimento = 2024 - idade_texto # ISSO DARIA ERRO!

# 3. A Conversão Correta (usando int() para converter para Inteiro)
idade_numero = int(idade_texto)

# 4. Agora sim podemos calcular
ano_nascimento = 2024 - idade_numero
print(f"Legal! Você nasceu por volta de {ano_nascimento}.")
3. Condicionais (If/Else): Ensinando Seu Código a Tomar Decisões
Explicação Simples: É aqui que seu programa ganha "inteligência". Usamos if (se), elif (senão se) e else (senão) para que o código execute blocos diferentes dependendo de se uma condição é True ou False. A sintaxe usa : (dois pontos) e indentação (o espaço antes da linha) para definir o que está "dentro" da condição.

Exemplo em Contexto Real (Controle de Acesso): Vamos verificar se um usuário tem idade suficiente para entrar em uma área restrita de um site ou aplicativo.

Python

# Definimos a idade mínima permitida
idade_minima = 18

# Imagine que esta variável veio de um cadastro (como no Capítulo 1)
idade_do_usuario = 22

# O programa agora toma uma decisão:
if idade_do_usuario >= idade_minima:
    # Este bloco SÓ executa se a condição for Verdadeira
    print("Acesso permitido. Bem-vindo!")
else:
    # Este bloco SÓ executa se a condição for Falsa
    print("Acesso negado. Você deve ter 18 anos ou mais.")
3.1 O Caminho do Meio: Usando elif para Múltiplas Escolhas
Explicação Simples: Às vezes, "sim" ou "não" (o if/else) não é suficiente. E se você tiver 3 ou 4 opções?

Imagine um semáforo:

Se (if) o sinal estiver "Verde" -> Siga.

Senão Se (elif) o sinal estiver "Amarelo" -> Atenção.

Senão (else) -> Pare (pois só pode ser o "Vermelho").

O elif (abreviação de "else if") permite adicionar quantas verificações extras você precisar antes de chegar ao else final.

Exemplo em Contexto Real (Calculando Desconto por Valor): Uma loja dá descontos diferentes dependendo do valor da compra.

Python

valor_da_compra = 210.00
desconto = 0

if valor_da_compra >= 500.00:
    # 1ª Verificação (Valor mais alto)
    print("Desconto de 15% aplicado!")
    desconto = 0.15
elif valor_da_compra >= 200.00:
    # 2ª Verificação (O "caminho do meio")
    # Só entra aqui se for >= 200 E < 500
    print("Desconto de 10% aplicado!")
    desconto = 0.10
else:
    # 3ª Opção (Se nenhuma das anteriores for verdade)
    print("Sem desconto para esta faixa de valor.")
    desconto = 0

valor_final = valor_da_compra - (valor_da_compra * desconto)
print(f"Valor final a pagar: R$ {valor_final:.2f}")
