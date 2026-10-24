# Trabalho Projeto Integrador

## Sistema Web para Gestão de Pesquisas por Questionário

### Integrantes

- Giovanni Vieira Pereira da Silva
- Gustavo Martins da Silva Ilescas
- Matheus Gabriel dos Santos Silva
- Alex Marola Barbosa Junior
- Erick Gustavo Miller Dos Santos
- Wagner Alves de Sousa
- Gabriel Gonçalves Pereira

---

## Sumário

1. [Estudo de Caso](#estudo-de-caso)
2. [Requisitos Funcionais e Não Funcionais](#requisitos-funcionais-e-não-funcionais)
3. [Atores](#atores)
4. [User Stories](#user-stories)
5. [UML e Casos de Uso](#uml-e-casos-de-uso)
6. [Segurança da Informação](#segurança-da-informação)

---

# Estudo de Caso

## Apresentação

O projeto tem como objetivo proporcionar aos estudantes uma experiência prática de desenvolvimento de software, envolvendo análise de requisitos, modelagem de dados, desenvolvimento de aplicações web, usabilidade, segurança da informação e geração de relatórios analíticos. O sistema a ser desenvolvido deverá permitir a criação, aplicação e análise de pesquisas institucionais, garantindo anonimato dos participantes e organização das respostas por categorias de respondentes.

## Objetivo do Projeto

Desenvolver um Sistema Web para Gestão de Pesquisas por Questionários, permitindo:

- Cadastro e gerenciamento de pesquisas
- Definição de categorias de participantes
- Criação de questionários específicos por categoria
- Aplicação da pesquisa com acesso por senha anônima
- Coleta e armazenamento das respostas
- Monitoramento da participação
- Geração de relatórios estatísticos

> **O sistema deverá permitir a realização de pesquisas institucionais de forma organizada, segura e anônima.**

## Escopo do Sistema

O sistema deverá contemplar os seguintes módulos funcionais:

### Módulo de Cadastro de Pesquisa

Responsável pela criação e configuração das pesquisas.

**Funcionalidades mínimas:**

#### Cadastro de pesquisas

Definição de:

- título da pesquisa
- descrição
- período de aplicação (data início e fim)
- status (ativa/inativa)

#### Cadastro de categorias de participantes

Exemplo de categorias:

- Alunos
- Professores
- Colaboradores

> **Cada pesquisa poderá possuir uma ou mais categorias de participantes.**

### Módulo de Questionários

Responsável pela criação das perguntas da pesquisa.

**Funcionalidades:**

- Cadastro de questões
- Associação das questões a uma categoria de participante
- Cadastro de alternativas de resposta
- Tipos de questões sugeridos:
  - Múltipla escolha (uma resposta)
  - Múltipla escolha (várias respostas)
  - Escala (ex: 1 a 5)
  - Resposta aberta (texto)

Cada categoria poderá possuir seu próprio questionário.

### Módulo de Geração de Senhas

O sistema deverá permitir a geração de senhas de acesso anônimas.

**Características:**

- Senhas aleatórias
- Associadas a uma categoria de participante
- Não devem identificar o respondente
- Cada senha deve permitir apenas uma resposta

**Funcionalidades:**

- Gerar lote de senhas por categoria
- Exportar senhas (PDF ou CSV)
- Marcar senha como utilizada

### Módulo de Aplicação da Pesquisa (Coleta de Dados)

Interface para os participantes responderem a pesquisa.

**Fluxo de uso:**

1. Usuário acessa o sistema
2. Digita a senha recebida
3. Sistema identifica a categoria
4. Exibe o questionário correspondente
5. Usuário responde as perguntas
6. Sistema grava as respostas no banco de dados
7. Senha é marcada como utilizada

**Requisitos:**

- Interface simples e responsiva
- Validação de respostas obrigatórias
- Impedir múltiplas respostas com a mesma senha

### Módulo de Gestão (Dashboard)

Interface administrativa para acompanhamento da pesquisa.

**Indicadores sugeridos:**

- Total de senhas geradas
- Total de respostas recebidas
- Taxa de participação
- Participação por categoria

### Módulo de Relatórios

O sistema deverá permitir a geração de relatórios analíticos.

**Relatórios sugeridos:**

- Resultado por pergunta
- Resultado por categoria
- Comparação entre categorias
- Exportação de resultados (PDF, CSV)
- Visualização em tela com gráficos

---

# Requisitos Funcionais e Não Funcionais

## Requisitos Funcionais

O sistema deverá permitir:

### Gerenciamento de pesquisas e questionários

- Cadastrar e gerenciar pesquisas
- Associar questionários às categorias de participantes
- Definir limites de respostas por questão
- Cadastrar categorias de participantes
- Validar as respostas conforme o tipo de pergunta e as regras definidas

> **Comentário (Matheus):** a ideia é que o sistema permita resposta dissertativa, múltipla escolha e alternativa. Teoricamente, o único ajuste necessário seria a normalização 1FN do banco de dados.

### Acesso e participação

- Gerar senhas anônimas de acesso
- Permitir o acesso aos questionários por meio de senha
- Impedir o uso de uma mesma senha para registrar mais de uma participação
- Permitir pausar e retomar pesquisas

### Segurança e administração

- Autenticar administradores por meio de login
- Controlar o acesso às funcionalidades conforme o nível de permissão do administrador

### Armazenamento e análise de dados

- Registrar e armazenar as respostas dos participantes
- Exibir estatísticas das pesquisas ativas e encerradas em um painel
- Gerar relatórios estatísticos das pesquisas
- Exibir indicadores de participação atualizados durante a aplicação das pesquisas

## Requisitos Não Funcionais

O sistema deverá atender aos seguintes requisitos:

- **Usabilidade**
  - Interface web amigável
  - Layout responsivo
- **Segurança**
  - Senhas criptografadas no banco
  - Validação de acesso
  - Proteção contra múltiplas respostas
- **Performance**
  - Sistema capaz de suportar múltiplos acessos simultâneos
- **Portabilidade**
  - Navegação com funções de acessibilidade
  - Funcionamento em navegadores modernos

---

# Atores

## Alunos

Representa participantes da pesquisa pertencentes à categoria "alunos".

**Interações:**

- Acessar o sistema de pesquisa
- Inserir senha anônima
- Responder questionário
- Enviar respostas

## Professor

Representa participantes da pesquisa pertencentes à categoria "professores".

**Interações:**

- Acessar o sistema de pesquisa
- Inserir senha anônima
- Responder questionário específico
- Enviar respostas

## Gestor Educacional

Representa o usuário responsável pela gestão do sistema.

**Interações:**

- Realizar login no sistema
- Cadastrar e gerenciar pesquisas
- Cadastrar categorias de participantes
- Criar e editar questionários
- Cadastrar perguntas e alternativas
- Gerar senhas anônimas
- Monitorar participação (dashboard)
- Visualizar estatísticas
- Gerar relatórios
- Exportar dados (PDF/CSV)
- Ativar/desativar pesquisas

## Colaboradores

Representa participantes da pesquisa pertencentes à categoria "Colaboradores".

**Interações:**

- Acessar o sistema de pesquisa
- Inserir senha anônima
- Responder questionário específico
- Enviar respostas

---

# User Stories

| Atores | Requisitos do sistema | O que espera que aconteça |
| --- | --- | --- |
| Gestores educacionais | Manter pesquisas | Vai ser possível criar as pesquisas, colocando o nome da pesquisa, uma descrição, um período de aplicação e, por fim, seu status (ativa ou inativa). Poderá editar essas informações e também excluir caso desejado, tanto a pesquisa quanto as informações. |
| Gestores educacionais | Manter questionários | Aqui o usuário vai criar o questionário, colocando enunciados e respostas para as questões. Será possível editar e excluir perguntas também. |
| Gestores educacionais | Gerar senhas para o anonimato | Vai ser possível gerar senhas de acesso aos questionários por suas respectivas categorias. |
| Gestores educacionais | Baixar senhas | Vai ser possível baixar essas senhas. |
| Gestores educacionais | Criar Dashboard | O sistema vai criar um dashboard conforme as informações da pesquisa: total de senhas geradas, total de respostas recebidas, taxa de participação e participação por categoria. |
| Gestores educacionais | Criar Relatórios das pesquisas | O sistema criará relatórios analíticos com base nos resultados por pergunta, resultado por categoria e comparação entre categorias, além de permitir visualizar as informações em gráficos. |
| Gestores educacionais | Exportar os relatórios, gráficos e dashboards | Vai permitir que o usuário exporte esses dados. |
| Alunos | Responder o Questionário | O usuário vai colocar a senha que lhe foi passada no campo de senhas, assim aparecerá o questionário com as perguntas a serem respondidas. |
| Professores | Responder o Questionário | O usuário vai colocar a senha que lhe foi passada no campo de senhas, assim aparecerá o questionário com as perguntas a serem respondidas. |

---

# UML e Casos de Uso

## Manter Pesquisas

![Diagrama de casos de uso - Manter Pesquisas](imagens/manter-pesquisas.png)

### FP1 — Criar Pesquisa

1. Abre formulário para criar pesquisa
2. Opção para selecionar para qual grupo é a pesquisa aparece
   - 2.1 Opção 1 "Alunos"
   - 2.2 Opção 2 "Professores"
   - 2.3 Opção 3 "Alunos e Professores"
3. Gestor seleciona a opção
4. O Gestor preenche o nome, descrição e o período de aplicação da pesquisa.
5. Campo Status aparece
6. Se período de aplicação for igual ao dia em que a pesquisa está sendo criada, o sistema automaticamente deixa o status da pesquisa como "ATIVA"
7. O Gestor clica em "Finalizar Cadastro Pesquisa"
8. O sistema valida os dados inseridos (nome, descrição e consistência das datas)
9. Sistema salva a pesquisa e exibe uma notificação no canto superior direito "Pesquisa Cadastrada no Sistema"

### FA1

- **Inicia no FP1 – Criar, etapa 6**

1. Se período de aplicação for diferente do dia em que a pesquisa está sendo criada, o sistema automaticamente deixa o status da pesquisa como "INATIVA"
2. Fluxo retorna para etapa 7 do FP1 – Criar

### FP2 — Editar Pesquisa

1. Sistema exibe uma tela com todas as pesquisas cadastradas
2. Gestor seleciona uma pesquisa
3. Sistema retorna os dados do formulário referente à pesquisa
4. Gestor faz as alterações
5. Gestor seleciona o botão "concluir"
6. Sistema valida as informações inseridas
7. Sistema salva no banco de dados
8. Sistema retorna a seguinte mensagem "Pesquisa editada com êxito"

### FA2 — Cancelar Edição

- **Inicia no FP2 – Editar, etapa 4**

1. Gestor desiste de fazer alteração e aperta no botão "Cancelar"
2. Sistema descarta toda alteração que foi feita
3. Sistema retorna para etapa

### FP3 — Excluir Pesquisa

1. Gestor solicita a exclusão da pesquisa
2. O sistema exibe uma lista com as pesquisas cadastradas
3. Gestor seleciona a pesquisa que deseja remover
4. O sistema exibe os dados da pesquisa em modo leitura e exibe o botão "Excluir Pesquisa"
5. O sistema exibe uma mensagem de confirmação "Deseja excluir essas Pesquisa?" com a opção "Confirmar" e "Sair"
6. Gestor aperta em "Confirmar"
7. O sistema deleta a pesquisa com todas as questões cadastradas no banco de dados

### FA3 — Cancelar Exclusão da Pesquisa

- **Inicia no FP3 – etapa 6**

1. Gestor aperta em "Cancelar"
2. Sistema não faz nenhuma exclusão no banco de dados
3. Sistema retorna para etapa 2 do FP3 – Excluir

---

## Gerar Senhas para o Anonimato

![Diagrama de casos de uso - Gerar senhas para o anonimato](imagens/gerar-senhas.png)

### FP1

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

### FA1 — Exportação imediata das senhas

1. Após o passo 11 do fluxo principal, o Gestor decide baixar o lote gerado.
2. O Gestor seleciona o formato desejado (PDF ou CSV).
3. O sistema compila as senhas e inicia o download do arquivo.

### FA2 — Bloqueio por ausência de questionário

1. No passo 4 do fluxo principal, o Gestor seleciona uma categoria que ainda não possui perguntas cadastradas.
2. O sistema interrompe o fluxo e exibe um alerta informando que é necessário criar o questionário da categoria antes de gerar as senhas.
3. Nenhuma alteração é feita no banco de dados e os indicadores do Dashboard permanecem intactos.

### FA3 — Validação de quantidade (erro de input)

1. No passo 5 do fluxo principal, o Gestor insere um valor inválido (zero, negativo ou texto).
2. O sistema impede a geração e exibe uma mensagem solicitando um número válido.

---

## Responder Questionários

![Diagrama de casos de uso - Responder questionários](imagens/responder-questionarios.png)

### FP1 — Acesso à pesquisa (Alunos / Gestores educacionais / Professores)

1. Sistema carrega o app na interface padrão;
2. Interface solicita senha para acessar a pesquisa;
3. Ator insere a senha;
4. Sistema valida a senha;
5. Sistema identifica o ator;
6. Sistema exibe o questionário;
7. Ator responde às perguntas;
8. Sistema solicita ao ator validar respostas e salvar resposta;
9. Ator seleciona "Salvar respostas";
10. Sistema armazena as respostas no banco de dados;
11. Sistema marca senha como utilizada;
12. Sistema finaliza a pesquisa;
13. Sistema exibe mensagem "Obrigado por participar!"
14. Sistema exibe caixa de texto para reiniciar a pesquisa.
15. Sistema retorna à etapa 1

### FA1 — Ator insere senha inválida ou incorreta

- **Inicia no FP1 – Acesso à pesquisa, etapa 4**

1. Caso a senha digitada esteja incorreta ou em formato inválido, o sistema exibirá a mensagem "A senha digitada não confere".
2. Sistema contabiliza uma (1) tentativa mal sucedida de acesso.
3. O sistema retornará à etapa 2.

### FA2 — Ator insere senha incorreta diversas vezes

- **Inicia no FP1 – Acesso à pesquisa, FA1 etapa 2**

1. Caso o sistema contabilize 5 tentativas incorretas, ficará temporariamente indisponível para novas tentativas de acesso por 5 minutos.
2. Se a contagem chegar a 10, o sistema bloqueia permanentemente a caixa de texto para inserir a senha.
3. O sistema retornará à etapa 2 e exibe a mensagem "Tentativas de acesso excedidas".

### FA3 — Ator sai da pesquisa sem responder todas as perguntas

- **Inicia no FP1 – Acesso à pesquisa, etapa 7**

1. Caso o usuário saia da pesquisa, o sistema salvará localmente as respostas e guardará num arquivo de cache.
2. Para acessar novamente a pesquisa de onde parou, o sistema retornará à etapa 1.

### FA4 — Ator não finaliza a pesquisa na etapa 8

- **Inicia no FP1 – Acesso à pesquisa, etapa 8**

1. Sistema salvará localmente as respostas e guardará num arquivo de cache.
2. Para acessar novamente a pesquisa de onde parou, o sistema retornará à etapa 1.

---

## Criar Dashboard

![Diagrama de casos de uso - Criar dashboard](imagens/dashboard.png)

### FP1 — Dashboard

1. O Gestor Educacional realiza login no sistema.
2. O sistema valida as credenciais de acesso.
3. O sistema exibe o Dashboard Administrativo.
4. O Gestor seleciona os filtros desejados:
   - Pesquisa;
   - Categoria;
   - Período;
   - Status.
5. O sistema processa os filtros informados.
6. O sistema calcula e exibe os indicadores principais (KPIs):
   - Total de Pesquisas;
   - Senhas Geradas;
   - Respostas Recebidas;
   - Taxa de Participação;
   - Pesquisas Ativas;
   - Pesquisas Encerradas.
7. O sistema exibe o gráfico de Participação por Categoria.
8. O sistema exibe o gráfico de Utilização das Senhas.
9. O sistema exibe o gráfico de Evolução das Respostas.
10. O sistema exibe o gráfico de Status das Pesquisas.
11. O sistema exibe os Resultados das Perguntas.
12. O sistema exibe a Comparação entre Categorias.
13. O sistema exibe os Comentários das Questões Abertas.
14. O sistema exibe os Indicadores de Segurança:
    - Total de Logins Administrativos;
    - Tentativas de Acesso Inválidas;
    - Senhas Reutilizadas Bloqueadas;
    - Usuários Ativos.
15. O Gestor analisa as informações apresentadas.
16. O Gestor pode solicitar a geração de relatórios.
17. O caso de uso é encerrado.

### FA01 — Alterar Filtros

1. Inicia em "Selecionar Filtros".
2. Gestor altera filtros.
3. Sistema recarrega todos os gráficos e indicadores.
4. Retorna para etapa 3.

### FA02 — Atualização Automática

1. Inicia após a exibição dos indicadores.
2. Sistema atualiza os dados em tempo real.
3. Retorna para etapa 3.

### FA03 — Visualizar Detalhes

1. Inicia em qualquer gráfico.
2. Gestor seleciona um gráfico.
3. Sistema apresenta informações detalhadas.
4. Retorna para etapa 3.

### FE01 — Nenhum dado encontrado

1. Inicia em "Aplicar Filtros".
2. Sistema não encontra registros.
3. Exibe mensagem: "Nenhum resultado encontrado para os filtros selecionados."
4. Retorna para etapa 4.

### FE02 — Erro ao carregar indicadores

1. Inicia em "Carregar Indicadores".
2. Sistema detecta falha na consulta.
3. Exibe mensagem de erro.
4. Retorna para etapa 3.

### FE03 — Falha na exportação

1. Inicia em "Exportar PDF/CSV".
2. Sistema não consegue gerar o arquivo.
3. Exibe mensagem de erro.
4. Retorna para a etapa 16.

---

# Segurança da Informação

## Confidencialidade

- AES

## Integridade

- Senha – somente números, caracteres e símbolos

## Disponibilidade

- Vercel
- Netlify
- Wix

## Autenticação

Senha de 10 dígitos, sendo:

| Perfil | Números | Caracteres | Símbolos |
| --- | :---: | :---: | :---: |
| Gestores Educacionais | 5 | 3 | 2 |
| Aluno | 7 | 2 | 1 |
| Professor | 8 | 1 | 1 |

## Autorização

- **Gestores Educacionais:** acesso a toda interface das pesquisas, questionários, dados e relatórios.
- **Aluno:** acesso somente para responder questionário.
- **Professor:** acesso somente para responder questionário.
