# **Trabalho Projeto Integrador**

**Integrantes:**

**Giovanni Vieira Pereira da Silva Gustavo Martins da Silva Ilescas Matheus Gabriel dos Santos Silva Alex Marola Barbosa Junior**  
**Erick Gustavo Miller Dos Santos**  
**Wagner Alves de Sousa**  
**Gabriel Gonçalves Pereira**

**Sistema Web para Gestão de Pesquisas por Questionário**

# **Estudo de Caso**

1. ## **Apresentação**

O projeto tem como objetivo proporcionar aos estudantes uma experiência prática de desenvolvimento de software, envolvendo análise de requisitos, modelagem de dados, desenvolvimento de aplicações web, usabilidade, segurança da informação e geração de relatórios analíticos. O sistema a ser desenvolvido deverá permitir a criação, aplicação e análise de pesquisas institucionais, garantindo anonimato dos participantes e organização das respostas por categorias de respondentes.

2. ## **Objetivo do Projeto**

Desenvolver	um	Sistema	Web	para	Gestão	de	Pesquisas	por Questionários, permitindo:

* Cadastro e gerenciamento de pesquisas

* Definição de categorias de participantes

* Criação de questionários específicos por categoria

* Aplicação da pesquisa com acesso por senha anônima

* Coleta e armazenamento das respostas

* Monitoramento da participação

* Geração de relatórios estatísticos

**O sistema deverá permitir a realização de pesquisas institucionais de forma organizada, segura e anônima.**

3. ## **Escopo do Sistema**

   O sistema deverá contemplar os seguintes módulos funcionais:

   1. ## **Módulo de Cadastro de Pesquisa**

   ### **Responsável pela criação e configuração das pesquisas.**

Funcionalidades mínimas:

### **Cadastro de pesquisas**

Definição de:

* título da pesquisa

  * descrição

    * período de aplicação (data início e fim)

    * status (ativa/inativa)

  ### **Cadastro de categorias de participantes**

Exemplo de categorias:

* Alunos

  * Professores

    * Colaboradores

**Cada	pesquisa	poderá	possuir	uma	ou	mais	categorias	de participantes.**

2. ## **Módulo de Questionários**

   Responsável pela criação das perguntas da pesquisa.

Funcionalidades:

* Cadastro de questões

  * Associação das questões a uma categoria de participante

    * Cadastro de alternativas de resposta

    * Tipos de questões sugeridos:

    * Múltipla escolha (uma resposta)

    * Múltipla escolha (várias respostas)

    * Escala (ex: 1 a 5\)

    * Resposta aberta (texto)

Cada categoria poderá possuir seu próprio questionário

3. ## **Módulo de Geração de Senhas**

### **O sistema deverá permitir a geração de senhas de acesso anônimas.**

Características:

* Senhas aleatórias

  * Associadas a uma categoria de participante

    * Não devem identificar o respondente

    * Cada senha deve permitir apenas uma resposta

    * Funcionalidades:

    * Gerar lote de senhas por categoria

    * Exportar senhas (PDF ou CSV)

    * Marcar senha como utilizada

  4. ## **Módulo de Aplicação da Pesquisa (Coleta de Dados)**

### **Interface para os participantes responderem a pesquisa.**

* Fluxo de uso:

  * Usuário acessa o sistema

    * Digita a senha recebida

    * Sistema identifica a categoria

    * Exibe o questionário correspondente

    * Usuário responde as perguntas

    * Sistema grava as respostas no banco de dados

    * Senha é marcada como utilizada Requisitos:

    * Interface simples e responsiva

    * Validação de respostas obrigatórias

    * Impedir múltiplas respostas com a mesma senha

  5. ## **Módulo de Gestão (Dashboard)**

  ### **Interface administrativa para acompanhamento da pesquisa.**

Indicadores sugeridos:

* Total de senhas geradas

  * Total de respostas recebidas

    * Taxa de participação

    * Participação por categoria

  6. ## **Módulo de Relatórios**

  ### **O sistema deverá permitir a geração de relatórios analíticos.**

Relatórios sugeridos:

* Resultado por pergunta

  * Resultado por categoria

    * Comparação entre categorias

    * Exportação de resultados (PDF, CSV)

    * Visualização em tela com gráficos

# **Requisitos Funcionais e Não Funcionais**

4. ## **Requisitos Funcionais**

O sistema deverá permitir:

1. ##  **Gerenciamento de pesquisas e questionários**

* Cadastrar e gerenciar pesquisas

* Associar questionários às categorias de participantes

* Definir limites de respostas por questão

* Cadastrar categorias de participantes

* Validar as respostas conforme o tipo de pergunta e as regras definidas


  2. ## **Acesso e participação**

* Gerar senhas anônimas de acesso

* Permitir o acesso aos questionários por meio de senha

* Impedir o uso de uma mesma senha para registrar mais de uma participação

* Permitir pausar e retomar pesquisas

  3. ## **Segurança e administração**

* Autenticar administradores por meio de login

* Controlar o acesso às funcionalidades conforme o nível de permissão do administrador

  4. ## **Armazenamento e análise de dados**

* Registrar e armazenar as respostas dos participantes

* Exibir estatísticas das pesquisas ativas e encerradas em um painel

* Gerar relatórios estatísticos das pesquisas

* Exibir indicadores de participação atualizados durante a aplicação das pesquisas


5. ## **Requisitos Não Funcionais**

O sistema deverá atender aos seguintes requisitos:

* Usabilidade

* Interface web amigável

* Layout responsivo

* Segurança

* Senhas criptografadas no banco

* Validação de acesso

* Proteção contra múltiplas respostas

* Performance

* Sistema capaz de suportar múltiplos acessos simultâneos

* Portabilidade

* Navegação com funções de acessibilidade

* Funcionamento em navegadores modernos

**ATORES:**

**Alunos**

Representa participantes da pesquisa pertencentes à categoria

“alunos”.

### **Interações:**

* Acessar o sistema de pesquisa

* Inserir senha anônima

* Responder questionário

* Enviar respostas

## **Professor**

Representa participantes da pesquisa pertencentes à categoria

“professores”.

### **Interações:**

* Acessar o sistema de pesquisa

* Inserir senha anônima

* Responder questionário específico

* Enviar respostas

## **Gestor Educacional**

Representa o usuário responsável pela gestão do sistema.

### **Interações:**

* Realizar login no sistema

* Cadastrar e gerenciar pesquisas

* Cadastrar categorias de participantes

* Criar e editar questionários

* Cadastrar perguntas e alternativas

* Gerar senhas anônimas

* Monitorar participação (dashboard)

* Visualizar estatísticas

* Gerar relatórios

* Exportar dados (PDF/CSV)

* Ativar/desativar pesquisas

* **COLABORADORES**  
  Representa participantes da pesquisa pertencentes à categoria

“Colaboradores”.

### **Interações:**

* Acessar o sistema de pesquisa

* Inserir senha anônima

* Responder questionário específico

* Enviar respostas

**User Stories**

| Atores | Requisitos do sistema | O que espera que acontece |
| ----- | :---- | :---- |
| Gestores educacionais | Manter pesquisas | Vai ser possível criar as pesquisas, colando o nome da pesquisa, uma descrição para a pesquisa, um período de aplicação para a pesquisa e por fim, seu status, se ela está ativa ou inativa.Podera editar essas informações e também excluir caso desejado, tanto a pesquisas quanto informações |
| Gestores educacionais | Manter questionários | Aqui o usuário vai criar ao questionário, vai colocar enunciados e respostas para as questões do questionário. Será possível editar perguntas e excluir também.  |
| Gestores educacionais | Gerar senhas para o anonimato | Vai ser possível gerar senhas de acesso aos questionários por suas respetivas categorias |
| Gestores educacionais | Baixar senhas | Vai ser possível baixar essas senhas |
| Gestores educacionais | Criar Dashboard | O sistema vai criar um dashboard conforme as informações da pesquisa: Qual o total de senhas geradas, o total de respostas recebidas, a taxa de participação e a participação por categoria |
| Gestores educacionais | Criar Relatórios das pesquisas | O sistema criara relatórios analíticos com base nos resultados por perguntas, resultado por categoria, comparação entre categoria e visualizar em gráficos as informações também |
| Gestores educacionais | Exportar os relatórios, gráficos e dashboards | Vai permitir que o usuário exporte esses dados |
| Alunos | Responder o Questionário | O usuário vai colocar senha que lhe foi passada no campo de senhas, assim aparecera o questionário com as perguntas a serem respondidas |

| Professores | Responder o Questionário | O usuário vai colocar a senha que lhe foi passada no campo de senhas, assim aparecera o questionário com as perguntas a serem respondidas |
| :---- | :---- | :---- |

**UML**  
**Manter Pesquisas**  
![][image1]  
**FP1:**

1. Abre formulário para criar pesquisa  
   2. Opção para selecionar para qual grupo é a pesquisa aparece  
   3. 2.1 Opção 1 “Alunos”  
   4. 2.2 Opção 2 “Professores”  
   5. 2.3 Opção 3 “Alunos e Professores”  
   6. Gestor seleciona a opção  
   7. O Gestor preenche o nome, descrição e o período de aplicação da pesquisa.  
   8. Campo Status aparece   
   9. Se período de aplicação for igual dia o dia que a pesquisa está sendo criada, o sistema Automaticamente deixe o status da pesquisa como “ATIVA”  
   10. O Gestor clica em "Finalizar Cadastro Pesquisa"  
   11. O sistema valida os dados inseridos (nome, descrição e consistência das datas)  
   12. Sistema salva a pesquisa e exibe uma notificação no canto superior direito “Pesquisa Cadastrada no Sistema”

**FA1:**

* **INICIA NO FP1 – CRIAR etapa 6**  
  1. Se período de aplicação for diferente do dia que a pesquisa está sendo criada, sistema Automaticamente deixe o status da pesquisa como “INATIVA”  
  2.  Fluxo retorna para etapa 7 do FP1 – criar

**FP2. Editar Pesquisa**

1. Sistema exibe uma tela com todas as pesquisas cadastradas 	  
   2. Gestor seleciona uma pesquisa  
   3. Sistema retorna os dados do formulário referente a pesquisa  
   4. Gestor faz as alterações   
   5. Gestor seleciona o botão “concluir”  
   6. Sistema valida as informações inseridas  
   7. Sistema salva no banco de dados  
   8. Sistema retorna a seguinte mensagem “Pesquisa editada com êxito”  
      

**FA2. Cancelar Editar**

* **INICIA NO FP2 – Editar etapa 4**  
  1. Gestor desiste de fazer alteração e aperta no botão “Cancelar”  
  2. Sistema descarta toda alteração que foi feita  
  3. Sistema retorna para etapa 

**FP3: Excluir Pesquisa**

1. Gestor solicita a exclusão da pesquisa  
   2. O sistema exibe uma lista com as pesquisas cadastradas   
   3. Gestor seleciona a pesquisa que deseja remover   
   4. O sistema exibe os dados da pesquisa em modo leitura e exibe o botão “Excluir Pesquisa”  
   5. O sistema exibe uma mensagem de confirmação “Deseja excluir essas Pesquisa?” com a opção “Confirmar” e “Sair”  
   6. Gestor aperta em “Confirmar”  
   7. O sistema deleta a pesquisa com todas as questões cadastradas no banco de dados 

**FA3. Cancelar Exclusão da Pesquisa**

* **Inicia no FP3 – etapa 6**  
1. Gestor aperta em “Cancelar”  
2. Sistema não faz nenhuma exclusão no banco de dados  
3. Sistema retorna para etapa 2 do FP3 – Excluir

   

   **Gerar senhas para o anonimato**

![][image2]  
**FP1:**

1. O Gestor Educacional realiza o login no sistema.  
2. O Gestor acessa o Módulo de Geração de Senhas.  
3. O Gestor seleciona uma pesquisa previamente cadastrada e ativa.  
4. O Gestor seleciona a categoria de participantes desejada (ex: Alunos, Professores).  
5. O Gestor informa a quantidade de senhas que deseja gerar (geração em lote).  
6. O sistema processa a requisição e gera as senhas aleatórias.  
7. O sistema associa as senhas à categoria escolhida e as configura para uso único.  
8. O sistema salva as senhas no banco de dados com o status inicial de "não utilizada".   
9. O sistema atualiza a base de dados do Módulo de Gestão (Dashboard), somando a nova quantidade ao indicador de "Total de senhas geradas" daquela pesquisa.   
10. O sistema registra o universo amostral para aquela categoria específica, estabelecendo a base matemática que o Módulo de Relatórios usará futuramente para calcular a "Taxa de participação" e a "Participação por categoria".   
11. O sistema exibe uma mensagem de sucesso na tela para o Gestor e disponibiliza os botões para exportação (PDF/CSV). 

**FA1. Exportação imediata das senhas**

1. Após o passo 11 do fluxo principal, o Gestor decide baixar o lote gerado.  
2. O Gestor seleciona o formato desejado (PDF ou CSV).   
3. O sistema compila as senhas e inicia o download do arquivo.

**FA2. Bloqueio por ausência de questionário**

1. No passo 4 do fluxo principal, o Gestor seleciona uma categoria que ainda não possui perguntas cadastradas.  
2. O sistema interrompe o fluxo e exibe um alerta informando que é necessário criar o questionário da categoria antes de gerar as senhas.  
3. Nenhuma alteração é feita no banco de dados e os indicadores do Dashboard permanecem intactos.

**FA3. Validação de quantidade (Erro de Input)**

1. No passo 5 do fluxo principal, o Gestor insere um valor inválido (zero, negativo ou texto).  
2. O sistema impede a geração e exibe uma mensagem solicitando um número válido.  
   

   **Responder Questionários**

![][image3]  
**FP1: Acesso à pesquisa (Alunos/Gestores educacionais/Professores)**

1\. Sistema carrega o app na interface padrão;

2\. Interface solicita senha para acessar a pesquisa;  
3\. Ator insere a senha;  
4\. Sistema válida a Senha;  
5\. Sistema Identifica o ator;  
6\. Sistema exibe o questionário;  
7\. Ator responde às perguntas;  
8\. Sistema solicita ao ator validar respostas e salvar resposta;

9\. Ator seleciona “Salvar respostas”;  
10\. Sistema armazena as respostas no banco de dados;  
11\. Sistema marca senha como utilizada;  
12\. Sistema Finaliza a Pesquisa;

13\. Sistema exibe mensagem “Obrigado por participar\!”

14\. Sistema exibe caixa de texto para reiniciar a pesquisa.

15\. Sistema retorna a etapa 1

**FA1. Ator insere senha invalida ou incorreta**

* INICIA NO FP1 – Acesso à pesquisa etapa 4

1. Caso senha digitada estiver incorreta ou no formato inválido o sistema exibirá a mensagem “A senha digitada não confere”.

2. Sistema contabiliza uma (1) tentativa não sucedida de acesso.

3. O sistema retornará a etapa 2\.

**FA2. Ator insere senha incorreta diversas vezes** 

* **INICIA NO FP1 – Acesso à pesquisa FA1 etapa 2**

4. Caso sistema contabilizar 5 tentativas incorretas, se tornará temporariamente indisponível para realizar novas tentativas de acesso por 5 minutos.

5. Se a contagem chegar a 10 o sistema bloqueia permanentemente a caixa de texto para inserir a senha.

6. O sistema retornará a etapa 2 e exibe a mensagem “Tentativas de acesso excedidas**”**

**FA3. Ator sai da pesquisa sem responder todas as perguntas**

* **INICIA NO FP1 \- Acesso à pesquisa FP1 etapa 7**

1. Caso usuário saia da pesquisa, o sistema salvará localmente as respostas e guardará num arquivo de cache.

2. Para acessar novamente a pesquisa de onde parou, o sistema retornará a etapa 1\.

**FA4. Ator não finaliza a pesquisa na etapa 8**

* **INICIA NO FP1 \- Acesso à pesquisa FP1 etapa 8**

1. Sistema salvará localmente as respostas e guardará num arquivo de cache.  
2. Para acessar novamente a pesquisa de onde parou, o sistema retornará a etapa 1\.  
     
     
     
     
     
     
   **Criar Dashboard**

![][image4]  
**FP1: Dashboard**

1. O Gestor Educacional realiza login no sistema. 

2. O sistema valida as credenciais de acesso. 

3. O sistema exibe o Dashboard Administrativo. 

4. O Gestor seleciona os filtros desejados: 

* Pesquisa;   
* Categoria;   
* Período;   
* Status. 

5. O sistema processa os filtros informados. 

6. O sistema calcula e exibe os indicadores principais (KPIs): 

* Total de Pesquisas;   
* Senhas Geradas;   
* Respostas Recebidas;   
* Taxa de Participação;   
* Pesquisas Ativas;   
* Pesquisas Encerradas. 

7. O sistema exibe o gráfico de Participação por Categoria. 

8. O sistema exibe o gráfico de Utilização das Senhas. 

9. O sistema exibe o gráfico de Evolução das Respostas. 

10. O sistema exibe o gráfico de Status das Pesquisas. 

11. O sistema exibe os Resultados das Perguntas. 

12. O sistema exibe a Comparação entre Categorias. 

13. O sistema exibe os Comentários das Questões Abertas. 

14. O sistema exibe os Indicadores de Segurança: 

* Total de Logins Administrativos;   
* Tentativas de Acesso Inválidas;   
* Senhas Reutilizadas Bloqueadas  
* Usuários Ativos. 

15. O Gestor analisa as informações apresentadas. 

16. O Gestor pode solicitar a geração de relatórios. 

17. O caso de uso é encerrado.

**FA01 – Alterar Filtros**

1. Inicia em "Selecionar Filtros". 

2. Gestor altera filtros. 

3. Sistema recarrega todos os gráficos e indicadores. 

4. Retorna para etapa 3\. 

**FA02 – Atualização Automática**

1. Inicia após a exibição dos indicadores. 

2. Sistema atualiza os dados em tempo real. 

3. Retorna para etapa 3\. 

**FA03 – Visualizar Detalhes**

1. Inicia em qualquer gráfico. 

2. Gestor seleciona um gráfico. 

3. Sistema apresenta informações detalhadas. 

4. Retorna para etapa 3\. 

**FE01 – Nenhum dado encontrado**

1. Inicia em "Aplicar Filtros". 

2. Sistema não encontra registros. 

3. Exibe mensagem:  
   "Nenhum resultado encontrado para os filtros selecionados." 

4. Retorna para etapa 4\. 

**FE02 – Erro ao carregar indicadores**

1. Inicia em "Carregar Indicadores". 

2. Sistema detecta falha na consulta. 

3. Exibe mensagem de erro. 

4. Retorna para etapa 3\. 

**FE03 – Falha na exportação**

1. Inicia em "Exportar PDF/CSV". 

2. Sistema não consegue gerar o arquivo. 

3. Exibe mensagem de erro. 

4. Retorna para a etapa 16\.

**Confidencialidade**

* AES

### **Integridade**

* Senha – Somente números, caracteres e símbolos 

### 

### **Disponibilidade**

* Vercel

* Netlify

* Wix

**Autenticação**  
Senha numérica de 10 dígitos, sendo:  
Gestores Educacionais: 5 números, 3 caracteres e 2 simbolos  
Aluno: 7 números, 2 caracteres e 1 símbolo  
Professor: 8 números, 1 carácter e 1 símbolo   
**Autorização**  
Gestores Educacionais: Acesso a toda interface das pesquisas, questionários, dados e relatórios.  
Aluno: Acesso somente para responder questionário.  
Professor: Acesso somente para responder questionário.

### 

[image1]: <data:image/png;base64,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>

[image2]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjcAAAGNCAYAAADtkVAgAABZx0lEQVR4XuzdB1QUV98GcHaXBUQQbIiiWKJYYwmoxBaxm9hLNLGLsUeNPdGoscZeY9fYxRZbLG/sBQXlS+zlTd6YGKPG2KIQQNg839y7hWUWjSjgsj6/c/5H3Zmdmd3FvQ937sx1AhEREZEDcVI/QERERJSZMdwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiIiJyKAw3RERE5FAYboiIiMihMNwQERGRQ2G4ISIiIofCcENEREQOheGGiIiIHArDDRERETkUhhsiInqtPXr0CGfPnsXMmTPRv39/tG7dGhUr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KcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJxC3AAAAKcQNwAAwCnEDQAAcApxAwAAnELcAAAApxA3AADAKcQNAABwCnEDAACcQtwAAACnEDcAAMApxA0AAHAKcQMAAJzybyNfhmX3Z3JrAAAAAElFTkSuQmCC>

[image3]: <data:image/png;base64,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>

[image4]: <data:image/png;base64,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YP7lPQg77viLgyB0ZhoNP+OGeznYy+FeDvZyuM92sJfDfb4Huw/3cQEoD/Zxw70MP+VwL8PPuOFeDvZyuJeDvRzuw8G+YsVn08te1h9jp+UHcualvbF6Rctseg6x9763f8+c3CeTbSSM65Fxe3/KPil7pOyTqD+m65GyTzZHj3ifzBR+JumRsk/K8FP2yTVdn+TbTJ844P2ReyS/OACjPLtE11GdbowXkajQlk6fs6MPOdXfq5TtHnjgge7vXrNGDTm5fAdWSlcNzD99VIC2jvJ1/dBDGpDRcN/StmzLwT7b4V4O9nK4z2aw+4Df+C3bhx76+tTtpNvs7//+76eGuS9t1epfDurceLoO83uaaR100IHWJzP1yLiNhM3dI94nUY+U/THbADTJRkIUfrxHxm0k1D2ideih7xjpE+8NLYUfemQ8zy66nlydbowXkajQli7f2aKXD+opL/3Nev+N2XrooYfSi1/84q72xz/+8epVY5g/p59+enrBC14wdVueccZpKd6yLYd7GX4m2bIth3s52MvhvqkGuw/31cWaabD7cB8XgGYa7mX4Gbdle21atuz4kYFefsCpL20s8GZuC0PX6ec+97mp22L77V8w6JNT0/Q94n0SBaCyPybpkXF7SMs+WSw94n0SBaA++Oy443B+jQs+WuoRLX2NmGeX6Lqq043xIhIV2tLpFRP6SAung8r0927s+/royP1PfepTXS0OVFs4Tz75ZPfJ2PrspDxI9trrN9KKFV9JcxvsPtznumU7brf+JMO9HOzjtmxXFysPda1ysI/bsl2Ywb5+vT7S4nVTt8P++++fLr744q4HoqWnu3S8j97HRK+0xMJQj+g6/upXvzr1/jha6pH163V/31w94n0S9UjZH7MNQKttRT0ySfgp+2Tje+Sii/7X1G2g20N94r1R9og2DvTvE088kTCeZxddf65ON8aLSFRoSzfuJbb6W/WOzxt7cJmO0NdL4vMdGQtHYVW35+6795+Vk9exxx6d1q3TYJ3rcC8Hezncy8E+bst2XAAqw0854Gcz2H2458GuNdvhPlMAGrdbf3S4n3jih0e2ZvURDfm+P25pd/4NN9zQPc3M20csLPWIrvOzzjqr+/iefDtpj9DG9Yj3SRSAyvAzyUZC1B/eJ/O1kTAfPeJ9EvXIdenxx7850iNa5513XtUXeeWDnTXbZnso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CgEAALTAs0uUW+p0Y7yIRIUAAABa4Nklyi11ujFeRKJCAAAALfDsEuWWOt0YLyJRIQAAgBZ4dolyS51ujBeRqBAAAEALPLtEuaVON8aLSFQIAACgBZ5dotxSpxvjRSQqBAAA0ALPLlFuqdON8SISFQIAAGiBZ5cot9TpxngRiQoBAAC0wLNLlFvqdGNUhMVisVgsFmtLWqU5BaBIVAgAAKBFUW4hAAEAgEUtyi0EIAAAsKhFuYUABAAAFrUot8wpAAEAAGzJCEAAAGDJIQABAIAlhwAEAACWHAIQAABYcghAAABgySEAAQCAJYcABAAAlhwCEAAA2KKtv+n4qfXEDcd3p6277riR07VKBCAAAFC56KKL/KTutOj0mdx9990TXfYHP/hBWrVqlZ88Iqrx5HXHpx99u1/rVh3XnfbYNf33+r8nBuvxawlAAABgBlHQmCTERK677rp0ww03zHjZSepH///wN49Lj189CDqD9chVx6Un130/PXrVIPRcf4qfdQoBCACAzSg/6Of1/e9/vzv9wQcfHDl97dq16fbbb58KANdff323cg39n19Ge1T8Z0S1o/Pl85b8/9esWZNuvPHGqfPq+5tuumnkMvfff//U/ysI6Xu54oorpup885vf7E4ra0ff59PKy8r9K49Ld154TLrj/x6THr1iEISu/HR6fLDu/dqx6f5LjkuPfOP49NgV7AECAKAZ5QP5rbfeOhUG9FSQTv/JT37S/XvVVVelhx9+eOq8l156abrkkkumauj/dJ78//q3DEjf+c53uq9F51MIis6n30Er1ynptHy6znPllVd2gS2fpjo54GQKRPn/FZDyz7r44ovT448/XpxztL6fXn59yy23dIEwn/74Nz6d1l16fPrB149LPxz8+8hlx6enHvl+evjrg+Bz+afTE9/oV4kABADAZlQ+6D/xxBPp3/7t37qvv/a1r02drn/z6QoUea+Llr5XICgvk5dCRr58abrz/fjHP+6CiV8m/38+vfxdFYQUbqa7TLlEwe7aa69NX//616eO+yn/P39f7vXKp/nXT1zy6bT28s+lW5d/Kt1y7qe60+694Nip86372vHp8ZUEIAAAmpEf9PN64IEHutPzU0d5PfTQQyOXyU+B6ess743J65prrpk6f2m685XL+f/nvT3l7+p0Wt7blL+Xb33rW1OX0deiPVr6vtwjpaWgpWBWXr78+rELR8ON3PPVY9Mj//f47l+56/8cM/L/BCAAADaj/CCvPSH5Ka1MQUV7a8oAITr/nXfeme66666RQCD33HNPt0dHe4V+9KMfTZ3f6TgaP58uu3Llyu7f6DLl76rzZU899VR3un7XkurqdO0tyvS9nq7Le5B0mfz/+rmqnQORfkf9/2OPPTb1FF75e+WvH72gD0DfOv2v0x1n90HnnnOPTY8NTn/k/NFjfzICEAAAm1EOFVuyfJySAszm8OhXh3uAblrWf73mK8d2p2v94Nw6BBGAAADYjLSHw/ecbGm0J0cHRW8uj5776XT/l49L3z3zmPS9Lx6T7vqnY9Pas47rTtd65JxPp/u+3L8/UEYAAgAASw4BCAAALDkEIAAAsOT8//kIq4Wos7oRAAAAAElFTkSuQmCC>