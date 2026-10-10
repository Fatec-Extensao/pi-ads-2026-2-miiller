🔐 Gerador de Senhas em C
📋 Sobre o projeto

Este projeto consiste em um gerador de senhas aleatórias desenvolvido em linguagem C, capaz de criar 50 senhas únicas de 8 caracteres com base no perfil selecionado pelo usuário.

O programa foi desenvolvido para gerar senhas destinadas a três tipos de usuários de um ambiente educacional: alunos, professores e gestores educacionais.

Cada senha possui um prefixo que identifica o perfil selecionado, além de caracteres minúsculos, números, caracteres especiais e uma combinação aleatória de diferentes tipos de caracteres.

🎯 Funcionalidades
Seleção do perfil: permite escolher entre Aluno, Professor e Gestor Educacional.
Prefixo identificador: cada senha começa com uma letra correspondente ao perfil selecionado.
Geração aleatória: utiliza a função rand() para gerar combinações de caracteres.
Variedade de caracteres: inclui letras maiúsculas, letras minúsculas, números e caracteres especiais.
Reorganização dos caracteres: embaralha os caracteres gerados para variar a composição das senhas.
Prevenção de duplicatas: verifica se uma senha já foi gerada e cria outra caso encontre uma repetição.
Geração em lote: produz 50 senhas por execução.
🛠️ Tecnologias utilizadas
Linguagem: C
Bibliotecas padrão:
stdio.h — entrada e saída de dados.
stdlib.h — geração de números pseudoaleatórios.
string.h — comparação de strings.
time.h — inicialização da semente aleatória com base no horário atual.
⚙️ Requisitos

Para compilar e executar o programa, é necessário ter:

Um compilador C, como o GCC.
Um terminal ou ambiente de desenvolvimento compatível.
Um sistema operacional que suporte a execução de programas em C.
🚀 Como executar
1. Salve o código

Salve o código-fonte em um arquivo chamado main.c.

2. Compile o programa

Se estiver utilizando o GCC, execute no terminal:

gcc main.c -o gerador_senhas

3. Execute o programa

No Linux ou macOS:

./gerador_senhas


No Windows:

gerador_senhas.exe

💻 Como utilizar

Ao iniciar o programa, será apresentado um menu para selecionar o tipo de usuário.

--- Gerador de senhas ---
Escolha o tipo de senha:
A - Aluno
P - Professor
G - Gestor Educacional
Opcao:


Digite a letra correspondente ao perfil desejado:

Opção	Perfil	Prefixo
A	Aluno	A
P	Professor	P
G	Gestor Educacional	G

O programa aceita letras maiúsculas ou minúsculas. Após a seleção, serão geradas e exibidas 50 senhas diferentes.

📌 Exemplo de execução

Exemplo ilustrativo de saída ao selecionar o perfil de aluno:

--- SENHAS GERADAS ---

01 - A7#m2Kp!
02 - A@4vT8#q
03 - A6&xP1!z
04 - A9$kR3?b
05 - A2*L5w#n
...
50 - A8!cM4%y


Observação: as senhas apresentadas são exemplos fictícios. A saída real será diferente a cada execução.

🧠 Como funciona o código

O programa utiliza algumas etapas principais para gerar as senhas:

Inicialização: define a quantidade de senhas (TOTAL = 50) e o tamanho de cada senha (TAM = 8).
Seleção do perfil: solicita ao usuário uma opção e define o prefixo correspondente.
Geração dos caracteres: adiciona o prefixo, um caractere minúsculo, um número e um caractere especial.
Preenchimento: completa os caracteres restantes com elementos selecionados aleatoriamente do conjunto disponível.
Embaralhamento: reorganiza os caracteres após o prefixo para variar a composição da senha.
Verificação de duplicatas: compara a senha atual com as anteriores e repete a geração se encontrar uma senha idêntica.
Exibição: apresenta as 50 senhas numeradas no terminal.
📁 Estrutura do projeto
gerador-de-senhas/
├── main.c
└── README.md

⚠️ Observações importantes
As senhas geradas possuem 8 caracteres, incluindo o prefixo identificador.
O prefixo permanece na primeira posição, enquanto os outros caracteres são embaralhados.
O código utiliza rand() e srand() para gerar números pseudoaleatórios. Esse método é adequado para fins didáticos, mas não é recomendado para gerar senhas destinadas a sistemas reais que exijam alta segurança.
A inicialização com time(NULL) não garante resultados imprevisíveis ou criptograficamente seguros.
Caso o usuário digite uma opção inválida, o programa termina sem gerar as senhas.
🔮 Possíveis melhorias
Permitir que o usuário escolha a quantidade de senhas.
Permitir a configuração do tamanho das senhas.
Salvar as senhas geradas em um arquivo de texto.
Implementar um gerador criptograficamente seguro.
Melhorar o tratamento de entradas inválidas, exibindo uma mensagem de erro.
Adicionar testes automatizados para verificar o tamanho, a composição e a unicidade das senhas.
👨‍💻 Autor

Desenvolvido como projeto de estudo da linguagem C, com foco em lógica de programação, manipulação de strings, estruturas de repetição e geração de números pseudoaleatórios.