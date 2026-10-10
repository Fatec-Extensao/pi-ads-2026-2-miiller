# 🔐 Gerador de Senhas em C

## 📋 Sobre o projeto

Este projeto consiste em um gerador de senhas aleatórias desenvolvido em linguagem C. O programa gera 50 senhas únicas, com 8 caracteres cada, de acordo com o perfil selecionado pelo usuário.

As senhas são destinadas a três tipos de usuários de um ambiente educacional: alunos, professores e gestores educacionais.

## ✨ Funcionalidades

- 👤 Seleção do perfil do usuário:
  - 🎓 `A` - Aluno
  - 👨‍🏫 `P` - Professor
  - 🏫 `G` - Gestor Educacional
- 🔢 Geração de 50 senhas por execução.
- 🔠 Senhas com 8 caracteres.
- 🔡 Utilização de letras maiúsculas e minúsculas.
- 🔢 Inclusão de números.
- 🔣 Inclusão de caracteres especiais.
- 🔀 Embaralhamento dos caracteres das senhas.
- 🛡️ Verificação para evitar senhas duplicadas.
- 🖥️ Exibição das senhas numeradas no terminal.

## 🛠️ Tecnologias utilizadas

- 💻 Linguagem C.
- `stdio.h` - entrada e saída de dados.
- `stdlib.h` - geração de números pseudoaleatórios.
- `string.h` - comparação de strings.
- `time.h` - inicialização da semente aleatória.

## 📌 Requisitos

- Compilador C, como o GCC.
- Terminal ou ambiente de desenvolvimento compatível.

## 🚀 Como executar

### 1. 📄 Salvar o código

Salve o código-fonte em um arquivo chamado `main.c`.

### 2. ⚙️ Compilar o programa

Execute o seguinte comando no terminal:

```bash
gcc main.c -o gerador_senhas
```

### 3. ▶️ Executar o programa

No Linux ou macOS:

```bash
./gerador_senhas
```

No Windows:

```bash
gerador_senhas.exe
```

## 👥 Como utilizar

Ao iniciar o programa, será exibido o seguinte menu:

```text
--- Gerador de senhas ---
Escolha o tipo de senha:
A - Aluno
P - Professor
G - Gestor Educacional
Opcao:
```

O usuário deverá selecionar uma das opções abaixo:

| 🔑 Opção | 👤 Perfil | 🏷️ Prefixo |
|----------|-----------|------------|
| A        | 🎓 Aluno | A |
| P        | 👨‍🏫 Professor | P |
| G        | 🏫 Gestor Educacional | G |

O programa aceita letras maiúsculas e minúsculas. Após a seleção, serão geradas 50 senhas diferentes.

## 💻 Exemplo de execução

Exemplo ilustrativo de saída para o perfil Aluno:

```text
--- SENHAS GERADAS ---

01 - A7#m2Kp!
02 - A@4vT8#q
03 - A6&xP1!z
04 - A9$kR3?b
05 - A2*L5w#n
...
50 - A8!cM4%y
```

> ⚠️ As senhas apresentadas são exemplos fictícios. Os resultados reais serão gerados aleatoriamente a cada execução.

## 🧠 Como funciona o código

1. **Inicialização:** define a quantidade de senhas com `TOTAL = 50` e o tamanho com `TAM = 8`.
2. **Seleção do perfil:** define o prefixo correspondente ao usuário.
3. **Geração dos caracteres:** adiciona o prefixo, uma letra minúscula, um número e um caractere especial.
4. **Preenchimento:** completa os caracteres restantes com elementos selecionados aleatoriamente.
5. **Embaralhamento:** reorganiza os caracteres das posições seguintes ao prefixo.
6. **Verificação de duplicatas:** compara cada senha com as anteriores e gera outra caso encontre uma repetição.
7. **Exibição:** apresenta as 50 senhas numeradas no terminal.

## 📁 Estrutura do projeto

```text
gerador-de-senhas/
├── gerador-de-senhas.cpp
└── README.md
```

## ⚠️ Observações importantes

- Cada senha possui 8 caracteres, incluindo o prefixo.
- O primeiro caractere identifica o perfil selecionado.
- O programa evita senhas duplicadas na mesma execução.
- A função `rand()` gera números pseudoaleatórios, e `srand()` inicializa sua sequência.
- O uso de `rand()` não é recomendado para gerar senhas que exigem alta segurança.
- Se o usuário informar uma opção inválida, o programa será encerrado sem gerar as senhas.

## 🔮 Possíveis melhorias

- ⚙️ Permitir que o usuário escolha a quantidade de senhas.
- 📏 Permitir a configuração do tamanho das senhas.
- 💾 Salvar as senhas geradas em um arquivo.
- 🔒 Implementar um gerador criptograficamente seguro.
- ❌ Melhorar o tratamento de entradas inválidas.
- 🧪 Desenvolver testes automatizados.

## 👨‍💻 Autor

Projeto desenvolvido para fins educacionais, com foco nos seguintes conceitos da linguagem C:

- 🧩 Lógica de programação.
- 🔁 Estruturas de repetição.
- 📝 Manipulação de strings.
- 📚 Vetores e matrizes.
- 🎲 Geração de números pseudoaleatórios.
- 🔍 Comparação de strings.

---
