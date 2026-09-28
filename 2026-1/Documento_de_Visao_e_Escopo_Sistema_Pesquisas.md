CENTRO ESTADUAL DE EDUCAÇÃO TECNOLÓGICA PAULA SOUZA

FACULDADE DE TECNOLOGIA DE LINS PROF. ANTONIO SEABRA

CURSO SUPERIOR DE TECNOLOGIA EM ANÁLISE E DESENVOLVIMENTO DE SISTEMAS

RICHARD DE OLIVEIRA BARRA JUNIOR

GUSTAVO WILLIAN GODOY DA SILVA

MATHEUS SOARES GOMES

MARCELO CARDOSO VENDRAME

SISTEMA WEB PARA GESTÃO DE PESQUISAS POR QUESTIONÁRIOS

Documento de Visão e Escopo

LINS/SP

1º SEMESTRE/2026

SUMÁRIO

1. INTRODUÇÃO .......................................................................................... 3

1.1 OBJETIVO DO DOCUMENTO ................................................................... 3

1.2 DEFINIÇÃO DO PROBLEMA .................................................................... 3

1.3 OBJETIVOS DO SISTEMA ....................................................................... 4

2. VISÃO GERAL DO PROJETO .................................................................... 5

2.1 PRINCIPAIS USUÁRIOS ......................................................................... 5

2.2 AMBIENTE OPERACIONAL ..................................................................... 6

3. VISÃO DO PRODUTO E ESCOPO DO SISTEMA ....................................... 7

3.1 FUNCIONALIDADES ............................................................................... 7

4. REQUISITOS FUNCIONAIS ....................................................................... 9

5. REQUISITOS NÃO FUNCIONAIS ............................................................. 12

6. REQUISITOS DE SEGURANÇA ............................................................... 13

7. ARQUITETURA E TECNOLOGIAS ........................................................... 15

8. ANÁLISE COMPARATIVA ........................................................................ 16

9. CONSIDERAÇÕES FINAIS ...................................................................... 17

REFERÊNCIAS ........................................................................................... 18

1. INTRODUÇÃO

O Sistema Web para Gestão de Pesquisas por Questionários tem como proposta apoiar instituições na criação, aplicação e análise de pesquisas institucionais. A solução permite que diferentes grupos, como alunos, professores, funcionários e colaboradores, respondam questionários de forma organizada, segura e anônima.

O diferencial do projeto está na utilização de senhas anônimas geradas em lotes. Cada senha é aleatória, única e permite apenas um acesso ao questionário, evitando a identificação direta do respondente e reduzindo a possibilidade de respostas duplicadas. O sistema também prevê recursos administrativos para acompanhamento da participação e geração de relatórios com gráficos e exportações.

1.1 OBJETIVO DO DOCUMENTO

Este documento tem como objetivo apresentar a visão geral e o escopo do sistema, descrevendo seus usuários, funcionalidades, requisitos, restrições e limites. Ele servirá como base para a modelagem, desenvolvimento e validação do projeto nas próximas etapas da disciplina.

1.2 DEFINIÇÃO DO PROBLEMA

Instituições que aplicam pesquisas por questionários costumam enfrentar dificuldades para controlar participação, preservar o anonimato dos respondentes, evitar respostas duplicadas e consolidar resultados de maneira rápida. Em processos manuais ou pouco integrados, a distribuição de senhas, o acompanhamento de respostas e a geração de relatórios podem se tornar tarefas demoradas e sujeitas a falhas.

O sistema proposto busca resolver esse problema ao centralizar a gestão das pesquisas em uma plataforma web, com questionários organizados por categoria de participante, controle de senhas de uso único e relatórios estatísticos para análise dos resultados.

1.3 OBJETIVOS DO SISTEMA

O objetivo geral do sistema é oferecer uma plataforma web para criação, aplicação e análise de pesquisas por questionários com foco em anonimato e controle de participação.

Os objetivos específicos são:

- permitir o cadastro de pesquisas com período de validade;

- organizar participantes por categorias, como alunos, professores e funcionários;

- permitir a criação de questionários com diferentes tipos de questões;

- gerar senhas anônimas, aleatórias e de uso único;

- validar o acesso dos respondentes por senha;

- registrar respostas sem associá-las diretamente à identidade do respondente;

- acompanhar a participação por meio de indicadores;

- gerar relatórios estatísticos com gráficos e exportações em PDF ou CSV.

2. VISÃO GERAL DO PROJETO

O projeto consiste em uma aplicação web voltada à gestão completa de pesquisas institucionais. A plataforma será utilizada por perfis administrativos para cadastrar pesquisas, montar questionários, gerar senhas, acompanhar participação e consultar relatórios. Os respondentes acessam apenas a área de resposta, informando uma senha anônima válida.

2.1 PRINCIPAIS USUÁRIOS

| Usuário | Responsabilidades |

| --- | --- |

| Administrador | Usuário responsável pelo controle geral da plataforma. Pode gerenciar usuários, pesquisas, categorias, questionários, senhas, relatórios e permissões. |

| Coordenador/Pesquisador | Usuário responsável por criar e acompanhar pesquisas específicas. Pode cadastrar pesquisas, montar questionários, gerar senhas, acompanhar respostas e visualizar relatórios. |

| Respondente | Usuário que acessa a pesquisa de forma anônima por meio de uma senha válida e responde ao questionário. |

| Responsável pela Distribuição das Senhas | Usuário ou funcionário responsável por exportar, imprimir ou distribuir as senhas anônimas geradas pelo sistema. |

2.2 AMBIENTE OPERACIONAL

O sistema será utilizado em ambiente web, acessível por navegadores modernos em computadores, tablets e celulares. A solução deverá contar com servidor web, banco de dados relacional e conexão segura para proteger o acesso às áreas administrativas e aos dados coletados.

Como ambiente mínimo previsto, considera-se:

- navegadores como Google Chrome, Mozilla Firefox e Microsoft Edge;

- servidor web com suporte à linguagem de programação escolhida pela equipe;

- banco de dados relacional para armazenar pesquisas, questionários, senhas e respostas;

- interface responsiva para uso em dispositivos móveis;

- mecanismos de autenticação, autorização e validação de dados.

3. VISÃO DO PRODUTO E ESCOPO DO SISTEMA

O produto será uma solução simples, eficiente e segura para aplicação de pesquisas por questionários. O sistema deve priorizar o anonimato do respondente, a organização das pesquisas por categorias, a facilidade de uso e a análise dos resultados por meio de indicadores e relatórios.

Fazem parte do escopo do sistema:

- cadastro e gerenciamento de pesquisas;

- cadastro de categorias de participantes;

- criação de questionários e perguntas;

- definição de tipos de questões;

- geração e exportação de senhas anônimas;

- acesso do respondente por senha válida;

- registro anônimo das respostas;

- monitoramento de participação;

- geração e exportação de relatórios estatísticos.

Não fazem parte do escopo inicial: envio automático de senhas por e-mail ou SMS, integração com sistemas externos de autenticação institucional, aplicativo móvel nativo e análise avançada por inteligência artificial.

3.1 FUNCIONALIDADES

3.1.1 Módulo de pesquisas

Permite cadastrar, listar, editar e organizar pesquisas, definindo título, descrição e período de validade.

3.1.2 Módulo de categorias e questionários

Permite criar categorias de participantes e montar questionários específicos para cada grupo. As perguntas podem ser configuradas como múltipla escolha, escala de avaliação ou resposta aberta.

3.1.3 Módulo de geração de senhas

Permite gerar lotes de senhas aleatórias, únicas e anônimas. O módulo tem relação direta com o algoritmo desenvolvido em VisualG no projeto interdisciplinar, que gera senhas por categoria de usuário e utiliza validação, repetição, vetores e sorteio de caracteres.

3.1.4 Módulo de coleta de respostas

Permite que o respondente acesse a pesquisa por meio de senha válida, responda às perguntas e envie suas respostas sem identificação direta.

3.1.5 Módulo de relatórios

Permite acompanhar a participação, visualizar gráficos e exportar resultados em PDF ou CSV.

4. REQUISITOS FUNCIONAIS

Os requisitos funcionais descrevem as ações que o sistema deve executar para atender aos objetivos do projeto.

| Código | Requisito funcional | Descrição | Atores |

| --- | --- | --- | --- |

| RF01 | Cadastrar pesquisa | Permitir cadastrar uma pesquisa com título, descrição e período de validade. | Administrador; Coordenador/Pesquisador |

| RF02 | Gerenciar categorias de participantes | Permitir cadastrar, listar, editar e excluir categorias, como alunos, docentes, funcionários ou colaboradores. | Administrador; Coordenador/Pesquisador |

| RF03 | Criar questionário | Permitir criar questionários associados a uma pesquisa e a uma categoria de participante. | Administrador; Coordenador/Pesquisador |

| RF04 | Cadastrar perguntas | Permitir cadastrar perguntas que farão parte dos questionários. | Administrador; Coordenador/Pesquisador |

| RF05 | Definir tipo de questão | Permitir definir o tipo da questão, como múltipla escolha, escala de avaliação ou resposta aberta. | Administrador; Coordenador/Pesquisador |

| RF06 | Gerar senhas anônimas | Permitir gerar lotes de senhas aleatórias, únicas e anônimas para acesso às pesquisas. | Administrador; Coordenador/Pesquisador |

| RF07 | Exportar senhas | Permitir exportar as senhas geradas em PDF ou CSV para distribuição. | Administrador; Coordenador/Pesquisador; Responsável pela Distribuição das Senhas |

| RF08 | Acessar pesquisa com senha | Permitir que o respondente acesse a pesquisa utilizando uma senha válida. | Respondente |

| RF09 | Validar senha de acesso | Verificar se a senha informada existe, está válida, pertence à pesquisa e ainda não foi utilizada. | Respondente |

| RF10 | Responder questionário | Permitir que o respondente visualize e responda às perguntas do questionário. | Respondente |

| RF11 | Registrar respostas | Armazenar as respostas enviadas sem associá-las diretamente à identidade do respondente. | Respondente |

| RF12 | Impedir reutilização de senha | Marcar a senha como utilizada após o envio das respostas, impedindo novo acesso com o mesmo código. | Respondente |

| RF13 | Monitorar participação | Exibir dados de acompanhamento, como senhas geradas, senhas utilizadas, respostas recebidas e percentual de participação. | Administrador; Coordenador/Pesquisador |

| RF14 | Gerar relatórios estatísticos | Gerar relatórios com gráficos e informações estatísticas sobre os resultados das pesquisas. | Administrador; Coordenador/Pesquisador |

| RF15 | Exportar resultados | Permitir exportar os resultados das pesquisas em PDF ou CSV. | Administrador; Coordenador/Pesquisador |

5. REQUISITOS NÃO FUNCIONAIS

Os requisitos não funcionais descrevem características de qualidade e restrições que o sistema deve atender.

| Código | Requisito não funcional | Descrição |

| --- | --- | --- |

| RNF01 | Usabilidade | O sistema deve possuir interface amigável, intuitiva e responsiva, permitindo o uso em computadores, tablets e celulares. |

| RNF02 | Performance | O sistema deve suportar múltiplos acessos simultâneos durante o período de aplicação das pesquisas. |

| RNF03 | Portabilidade | O sistema deve ser compatível com navegadores modernos, como Google Chrome, Mozilla Firefox e Microsoft Edge. |

| RNF04 | Disponibilidade | O sistema deve permanecer disponível durante o período de validade das pesquisas cadastradas. |

6. REQUISITOS DE SEGURANÇA

Os requisitos de segurança são fundamentais para proteger o acesso administrativo, preservar o anonimato dos respondentes e impedir uso indevido das informações coletadas.

| Código | Requisito de segurança | Descrição |

| --- | --- | --- |

| RS01 | Autenticação administrativa | O sistema deve exigir login e senha para usuários administrativos antes de permitir acesso às funcionalidades de gerenciamento. |

| RS02 | Controle de acesso por perfil | O sistema deve limitar as funcionalidades conforme o perfil do usuário, como Administrador, Coordenador/Pesquisador e Responsável pela Distribuição das Senhas. |

| RS03 | Armazenamento seguro de senhas administrativas | As senhas dos usuários administrativos devem ser armazenadas utilizando hash seguro, impedindo visualização direta no banco de dados. |

| RS04 | Geração segura de senhas anônimas | As senhas de acesso às pesquisas devem ser aleatórias, únicas e difíceis de adivinhar. |

| RS05 | Uso único das senhas anônimas | Cada senha anônima deve permitir apenas uma resposta ao questionário e deve ser bloqueada após o uso. |

| RS06 | Preservação do anonimato | O sistema não deve associar as respostas diretamente à identidade do respondente. |

| RS07 | Validação da senha de acesso | O sistema deve verificar se a senha existe, pertence à pesquisa correta, está dentro do prazo de validade e ainda não foi utilizada. |

| RS08 | Proteção contra acesso não autorizado | O sistema deve impedir acesso direto às páginas administrativas sem autenticação. |

| RS09 | Proteção contra alteração indevida de dados | Somente usuários autorizados devem poder editar, excluir ou visualizar pesquisas, questionários, senhas e relatórios. |

| RS10 | Proteção contra SQL Injection | O sistema deve utilizar consultas preparadas para impedir comandos maliciosos no banco de dados. |

| RS11 | Proteção contra XSS | O sistema deve tratar dados exibidos nas páginas para impedir execução de scripts maliciosos. |

| RS12 | Validação de dados de entrada | O sistema deve validar campos obrigatórios, formatos e regras antes de salvar informações. |

| RS13 | Registro de ações administrativas | O sistema deve registrar ações importantes, como criação de pesquisas, geração de senhas e exportação de relatórios. |

| RS14 | Proteção dos relatórios exportados | Somente usuários autorizados devem poder gerar ou baixar relatórios e arquivos exportados. |

| RS15 | Encerramento automático de sessão | O sistema deve encerrar sessões administrativas após um período de inatividade. |

7. ARQUITETURA E TECNOLOGIAS

A arquitetura prevista é baseada em aplicação web, separando a interface do usuário, as regras de negócio e a persistência dos dados. Essa organização facilita manutenção, evolução e validação das funcionalidades.

| Camada | Descrição |

| --- | --- |

| Interface web | Telas de acesso administrativo, criação de questionários, resposta da pesquisa e visualização de relatórios. |

| Regras de negócio | Validação de dados, controle de perfis, geração de senhas, bloqueio de reutilização e cálculo de indicadores. |

| Banco de dados | Armazenamento de usuários, pesquisas, categorias, questionários, perguntas, lotes de senhas e respostas. |

| Segurança | Autenticação, controle de acesso, hash de senhas, validações e proteção contra ataques comuns em aplicações web. |

A equipe poderá utilizar tecnologias web compatíveis com o ambiente da disciplina, como HTML, CSS e JavaScript na interface, linguagem de programação no servidor e banco de dados relacional. O módulo de geração de senhas desenvolvido em VisualG servirá como base lógica para a implementação posterior no sistema web.

8. ANÁLISE COMPARATIVA

Para compreender o diferencial do sistema proposto, foi feita uma comparação com soluções conhecidas de formulários on-line, considerando funcionalidades ligadas à criação de questionários, análise de respostas e controle de anonimato por senha de uso único.

| Critério | Google Forms | Microsoft Forms | Sistema proposto |

| --- | --- | --- | --- |

| Criação de questionários | Possui recursos para criação de formulários e pesquisas on-line. | Permite criar formulários, pesquisas, questionários e enquetes. | Permite criar questionários institucionais vinculados a pesquisas e categorias. |

| Organização por categoria | Pode ser adaptado manualmente. | Pode ser adaptado manualmente. | Prevê categorias específicas de participantes, como alunos, docentes e funcionários. |

| Anonimato por senha única | Não é o foco principal da ferramenta. | Não é o foco principal da ferramenta. | Prevê senhas anônimas, aleatórias e de uso único como diferencial do sistema. |

| Monitoramento de participação | Permite visualizar respostas e resumos. | Permite acompanhar respostas e resultados. | Prevê dashboard com senhas geradas, senhas usadas, respostas recebidas e percentual de participação. |

| Relatórios e exportação | Permite análise e exportação de respostas. | Permite análise e exportação de resultados. | Prevê relatórios estatísticos com gráficos e exportação em PDF ou CSV. |

| Adequação ao projeto | Ferramenta genérica de formulários. | Ferramenta genérica de formulários. | Solução específica para pesquisas institucionais com controle anônimo por senha. |

A comparação indica que o sistema proposto se diferencia por tratar a geração de senhas anônimas e de uso único como requisito central, além de organizar a aplicação das pesquisas por categoria de participante.

9. CONSIDERAÇÕES FINAIS

O Sistema Web para Gestão de Pesquisas por Questionários apresenta uma proposta adequada para instituições que precisam aplicar pesquisas com maior controle, segurança e anonimato. A definição de atores, requisitos funcionais, requisitos não funcionais e requisitos de segurança oferece uma base consistente para a modelagem e desenvolvimento da solução.

O módulo de geração de senhas desenvolvido em VisualG contribui para a validação da lógica central do projeto, pois demonstra a geração de senhas por categoria, com validação de entrada, uso de vetor e sorteio de caracteres. Em etapas futuras, essa lógica poderá ser adaptada para a aplicação web.

REFERÊNCIAS

FACULDADE DE TECNOLOGIA DE LINS PROF. ANTONIO SEABRA. Projeto interdisciplinar com atividades de curricularização da extensão: desenvolvimento de algoritmo para geração de senhas aleatórias por categoria de usuário. Lins, 2026. Material da atividade.

GOOGLE. Google Forms: online form builder. Disponível em: https://workspace.google.com/products/forms/. Acesso em: 15 jun. 2026.

MICROSOFT. Microsoft Forms: surveys, polls, and quizzes. Disponível em: https://www.microsoft.com/en-us/microsoft-365/online-surveys-polls-quizzes. Acesso em: 15 jun. 2026.

NICOLÓDI, Antonio Carlos. VisualG 3.0. SourceForge, 2020. Disponível em: https://sourceforge.net/projects/visualg30/. Acesso em: 10 jun. 2026.

VISUALG WEB. Sorteios (RandI). Disponível em: https://visualg.com.br/aprender/visualg/aleatoriedade/. Acesso em: 10 jun. 2026.
