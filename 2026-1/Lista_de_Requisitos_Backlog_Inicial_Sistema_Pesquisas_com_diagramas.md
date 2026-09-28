CENTRO ESTADUAL DE EDUCAÇÃO TECNOLÓGICA PAULA SOUZA

FACULDADE DE TECNOLOGIA DE LINS PROF. ANTONIO SEABRA

CURSO SUPERIOR DE TECNOLOGIA EM ANÁLISE E DESENVOLVIMENTO DE SISTEMAS

RICHARD DE OLIVEIRA BARRA JUNIOR

GUSTAVO WILLIAN GODOY DA SILVA

MATHEUS SOARES GOMES

MARCELO CARDOSO VENDRAME

SISTEMA WEB PARA GESTÃO DE PESQUISAS POR QUESTIONÁRIOS

Lista de Requisitos - Backlog Inicial

LINS/SP

1º SEMESTRE/2026

SUMÁRIO

1. INTRODUÇÃO .......................................................................................... 4

2. ÉPICO 1 - GESTÃO DE ACESSO E PERFIS ............................................. 4

3. ÉPICO 2 - GESTÃO DE PESQUISAS E CATEGORIAS .............................. 6

4. ÉPICO 3 - QUESTIONÁRIOS E PERGUNTAS ........................................... 8

5. ÉPICO 4 - GERAÇÃO E DISTRIBUIÇÃO DE SENHAS ............................. 11

6. ÉPICO 5 - COLETA DE RESPOSTAS ..................................................... 15

7. ÉPICO 6 - MONITORAMENTO E RELATÓRIOS ...................................... 19

8. BACKLOG RESUMIDO PRIORIZADO ..................................................... 20

REFERÊNCIAS ........................................................................................... 20

1. INTRODUÇÃO

O backlog inicial é uma lista organizada e priorizada das funcionalidades necessárias para o desenvolvimento do Sistema Web para Gestão de Pesquisas por Questionários. Ele serve como base para orientar o planejamento da equipe, relacionando épicos, histórias de usuário, prioridades e critérios de aceitação.

Este documento foi elaborado a partir dos requisitos funcionais, requisitos de segurança e do módulo de geração de senhas em VisualG desenvolvido no projeto interdisciplinar. O foco do sistema é permitir a criação de pesquisas, a aplicação de questionários anônimos por senha única e a geração de relatórios para análise dos resultados.

Cada item do backlog segue a estrutura:

- ID;

- História do usuário;

- Prioridade;

- Requisitos relacionados;

- Critérios de aceitação.

2. ÉPICO 1 - GESTÃO DE ACESSO E PERFIS

Não há diagrama de caso de uso disponível no material enviado para este épico.

US01 – Autenticar usuários administrativos

Como Administrador, Coordenador/Pesquisador ou Responsável pela Distribuição das Senhas,

quero realizar login no sistema,

para acessar apenas as funcionalidades permitidas ao meu perfil.

Prioridade: Alta.

Requisito(s) relacionado(s): RS01, RS03, RS08, RS15.

Critérios de aceitação:

- Deve exigir e-mail ou usuário e senha para acesso administrativo.

- Deve bloquear o acesso a páginas administrativas sem autenticação.

- Deve armazenar senhas administrativas com hash seguro.

- Deve encerrar a sessão após período de inatividade.

US02 – Controlar permissões por perfil

Como Administrador,

quero gerenciar permissões dos usuários,

para garantir que cada perfil acesse somente as funcionalidades autorizadas.

Prioridade: Alta.

Requisito(s) relacionado(s): RS02, RS09, RS13.

Critérios de aceitação:

- Deve diferenciar os perfis Administrador, Coordenador/Pesquisador e Responsável pela Distribuição das Senhas.

- Deve impedir alterações de dados por usuários sem permissão.

- Deve registrar ações administrativas importantes.

- Deve permitir ao Administrador manter o controle geral da plataforma.

3. ÉPICO 2 - GESTÃO DE PESQUISAS E CATEGORIAS

Diagramas de caso de uso disponíveis para este épico:

Diagrama RF01 - Cadastrar pesquisa

Diagrama RF02 - Gerenciar categorias de participantes

US03 – Cadastrar pesquisa

Como Administrador ou Coordenador/Pesquisador,

quero cadastrar uma nova pesquisa,

para iniciar um processo de coleta de dados institucional.

Prioridade: Alta.

Requisito(s) relacionado(s): RF01, RS12.

Critérios de aceitação:

- Deve permitir informar título e descrição da pesquisa.

- Deve permitir definir data de início e data de encerramento.

- Deve validar campos obrigatórios antes de salvar.

- Deve impedir período de validade inválido.

- Deve salvar a pesquisa no banco de dados.

US04 – Gerenciar categorias de participantes

Como Administrador ou Coordenador/Pesquisador,

quero cadastrar e manter categorias de participantes,

para organizar questionários e senhas por grupos, como alunos, docentes e funcionários.

Prioridade: Alta.

Requisito(s) relacionado(s): RF02, RS12.

Critérios de aceitação:

- Deve permitir cadastrar categoria de participante.

- Deve permitir listar categorias cadastradas.

- Deve permitir editar categorias existentes.

- Deve permitir excluir categorias não vinculadas a pesquisas ou questionários.

- Deve impedir duplicidade de categorias com o mesmo nome.

4. ÉPICO 3 - QUESTIONÁRIOS E PERGUNTAS

Diagramas de caso de uso disponíveis para este épico:

Diagrama RF03 - Criar questionário

Diagrama RF04 - Cadastrar perguntas

Diagrama RF05 - Definir tipo de questão

US05 – Criar questionário

Como Administrador ou Coordenador/Pesquisador,

quero criar questionários vinculados a uma pesquisa e categoria,

para coletar informações específicas de cada grupo de participantes.

Prioridade: Alta.

Requisito(s) relacionado(s): RF03, RS12.

Critérios de aceitação:

- Deve permitir selecionar a pesquisa relacionada.

- Deve permitir selecionar a categoria de participante.

- Deve validar se pesquisa e categoria foram informadas.

- Deve salvar o questionário no banco de dados.

- Deve permitir posterior inclusão de perguntas.

US06 – Cadastrar perguntas

Como Administrador ou Coordenador/Pesquisador,

quero adicionar perguntas aos questionários,

para definir quais informações serão coletadas dos respondentes.

Prioridade: Alta.

Requisito(s) relacionado(s): RF04, RS09, RS12.

Critérios de aceitação:

- Deve permitir informar o enunciado da pergunta.

- Deve permitir definir se a pergunta é obrigatória ou opcional.

- Deve validar perguntas sem enunciado.

- Deve salvar as perguntas no questionário correspondente.

- Deve permitir edição posterior, conforme permissões do usuário.

US07 – Definir tipo de questão

Como Administrador ou Coordenador/Pesquisador,

quero definir o tipo de cada pergunta,

para configurar a forma correta de resposta no questionário.

Prioridade: Alta.

Requisito(s) relacionado(s): RF05, RS12.

Critérios de aceitação:

- Deve oferecer tipos como múltipla escolha, escala de avaliação e resposta aberta.

- Deve exigir alternativas quando o tipo for múltipla escolha.

- Deve validar se o tipo de questão foi selecionado.

- Deve salvar o tipo da questão junto à pergunta.

- Deve impedir respostas incompatíveis com o tipo configurado.

5. ÉPICO 4 - GERAÇÃO E DISTRIBUIÇÃO DE SENHAS

Diagramas de caso de uso disponíveis para este épico:

Diagrama RF06 - Gerar senhas anônimas

Diagrama RF07 - Exportar senhas

US08 – Gerar senhas anônimas

Como Administrador ou Coordenador/Pesquisador,

quero gerar lotes de senhas anônimas para uma pesquisa,

para permitir que os respondentes acessem o questionário sem identificação direta.

Prioridade: Alta.

Requisito(s) relacionado(s): RF06, RS04, RS05, RS06, RS12.

Critérios de aceitação:

- Deve permitir selecionar pesquisa e categoria de participante.

- Deve permitir informar a quantidade de senhas a serem geradas.

- Deve validar quantidade maior que zero.

- Deve gerar senhas aleatórias, únicas e difíceis de adivinhar.

- Deve registrar o lote de senhas no banco de dados.

- Cada senha deve permitir apenas uma resposta.

Algoritmo desenvolvido na disciplina de Algoritmos

O módulo em VisualG utilizado como base gera dez senhas, valida a categoria P, A ou F, utiliza vetor para armazenamento e sorteia sete caracteres após o primeiro caractere obrigatório da categoria. No sistema web, essa lógica será adaptada para gerar lotes de senhas por pesquisa e categoria.

algoritmo "gerador_de_senhas_por_categoria"
var
 senhas: vetor[1..10] de caractere
 caracteresPermitidos, categoria, senhaAtual: caractere
 i, j, posicao: inteiro
inicio
 caracteresPermitidos <- "ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789@!#"
 para i de 1 ate 10 faca
 repita
 escreval("")
 escreval("Geracao da senha ", i, " de 10")
 escreval("Informe a categoria do usuario:")
 escreva("P - Professor, A - Aluno ou F - Funcionario: ")
 leia(categoria)
 categoria <- maiusc(categoria)
 se (categoria <> "P") e (categoria <> "A") e (categoria <> "F") entao
 escreval("Categoria invalida. Digite somente P, A ou F.")
 fimse
 ate (categoria = "P") ou (categoria = "A") ou (categoria = "F")
 senhaAtual <- categoria
 para j de 1 ate 7 faca
 posicao <- randi(39) + 1
 senhaAtual <- senhaAtual + copia(caracteresPermitidos, posicao, 1)
 fimpara
 senhas[i] <- senhaAtual
 escreval("Senha gerada: ", senhas[i])
 fimpara
 escreval("")
 escreval("LISTA FINAL DAS 10 SENHAS GERADAS")
 para i de 1 ate 10 faca
 escreval(i, " - ", senhas[i])
 fimpara
fimalgoritmo

Figura 5.1 - Fluxograma do módulo de geração de senhas

Fonte: Elaborado com base no projeto interdisciplinar de geração de senhas, 2026.

US09 – Exportar senhas

Como Administrador, Coordenador/Pesquisador ou Responsável pela Distribuição das Senhas,

quero exportar lotes de senhas,

para distribuir as senhas aos participantes da pesquisa.

Prioridade: Alta.

Requisito(s) relacionado(s): RF07, RS02, RS14.

Critérios de aceitação:

- Deve permitir selecionar uma pesquisa ou lote de senhas.

- Deve permitir exportar em PDF ou CSV.

- Deve impedir exportação quando não houver senhas geradas.

- Deve disponibilizar o arquivo para download.

- Deve permitir acesso apenas a usuários autorizados.

6. ÉPICO 5 - COLETA DE RESPOSTAS

Diagramas de caso de uso disponíveis para este épico:

Diagrama RF08 - Acessar pesquisa com senha

Diagrama RF09 - Validar senha de acesso

US10 – Acessar pesquisa com senha

Como Respondente,

quero acessar a pesquisa por meio de uma senha anônima,

para responder ao questionário sem revelar minha identidade.

Prioridade: Alta.

Requisito(s) relacionado(s): RF08, RF09, RS06, RS07.

Critérios de aceitação:

- Deve exibir campo para informar a senha.

- Deve impedir acesso sem senha informada.

- Deve encaminhar a senha para validação.

- Deve liberar o questionário somente quando a senha for válida.

- Deve exibir mensagem em caso de senha rejeitada.

US11 – Validar senha de acesso

Como Respondente,

quero ter minha senha validada pelo sistema,

para acessar somente pesquisas disponíveis e evitar respostas duplicadas.

Prioridade: Alta.

Requisito(s) relacionado(s): RF09, RS05, RS07.

Critérios de aceitação:

- Deve verificar se a senha existe.

- Deve verificar se pertence à pesquisa correta.

- Deve verificar se a pesquisa está dentro do período de validade.

- Deve verificar se a senha ainda não foi utilizada.

- Deve bloquear acesso com senha inválida, vencida ou já usada.

US12 – Responder questionário

Como Respondente,

quero visualizar e responder às perguntas da pesquisa,

para participar da coleta de dados de forma simples e anônima.

Prioridade: Alta.

Requisito(s) relacionado(s): RF10, RS12.

Critérios de aceitação:

- Deve exibir as perguntas do questionário.

- Deve permitir preencher respostas conforme o tipo de questão.

- Deve validar perguntas obrigatórias.

- Deve informar respostas pendentes antes do envio.

- Deve permitir envio após validação.

US13 – Registrar respostas

Como Respondente,

quero ter minhas respostas registradas pelo sistema,

para concluir minha participação na pesquisa.

Prioridade: Alta.

Requisito(s) relacionado(s): RF11, RS06, RS12.

Critérios de aceitação:

- Deve armazenar as respostas no banco de dados.

- Deve associar as respostas à pesquisa correta.

- Não deve associar respostas diretamente à identidade do respondente.

- Deve exibir confirmação após registro.

- Deve tratar falhas de salvamento.

US14 – Impedir reutilização de senha

Como Respondente,

quero ter minha senha marcada como utilizada após o envio,

para garantir que cada senha permita apenas uma resposta.

Prioridade: Alta.

Requisito(s) relacionado(s): RF12, RS05.

Critérios de aceitação:

- Deve marcar a senha como utilizada após o registro das respostas.

- Deve impedir novo acesso com senha já utilizada.

- Não deve marcar a senha como utilizada se as respostas não forem registradas.

- Deve exibir mensagem quando a senha já tiver sido usada.

- Deve proteger a integridade do processo de coleta.

7. ÉPICO 6 - MONITORAMENTO E RELATÓRIOS

Não há diagrama de caso de uso disponível no material enviado para este épico.

US15 – Monitorar participação

Como Administrador ou Coordenador/Pesquisador,

quero acompanhar a participação nas pesquisas,

para verificar o andamento da coleta de dados.

Prioridade: Média.

Requisito(s) relacionado(s): RF13.

Critérios de aceitação:

- Deve exibir total de senhas geradas.

- Deve exibir total de senhas utilizadas.

- Deve exibir total de respostas recebidas.

- Deve calcular percentual de participação.

- Deve permitir acompanhamento por pesquisa e categoria.

US16 – Gerar relatórios estatísticos

Como Administrador ou Coordenador/Pesquisador,

quero visualizar relatórios com gráficos e indicadores,

para analisar os resultados das pesquisas.

Prioridade: Média.

Requisito(s) relacionado(s): RF14, RS14.

Critérios de aceitação:

- Deve permitir selecionar a pesquisa desejada.

- Deve buscar as respostas registradas.

- Deve processar os dados coletados.

- Deve gerar gráficos e indicadores estatísticos.

- Deve informar quando não houver dados suficientes.

US17 – Exportar resultados

Como Administrador ou Coordenador/Pesquisador,

quero exportar os resultados da pesquisa,

para documentar os dados coletados e permitir análises externas.

Prioridade: Média.

Requisito(s) relacionado(s): RF15, RS13, RS14.

Critérios de aceitação:

- Deve permitir exportar resultados em PDF ou CSV.

- Deve impedir exportação de relatórios sem dados.

- Deve disponibilizar o arquivo para download.

- Deve permitir acesso apenas a usuários autorizados.

- Deve registrar a ação de exportação.

8. BACKLOG RESUMIDO PRIORIZADO

| ID | História de usuário | Prioridade |

| --- | --- | --- |

| US01 | Autenticar usuários administrativos | Alta |

| US02 | Controlar permissões por perfil | Alta |

| US03 | Cadastrar pesquisa | Alta |

| US04 | Gerenciar categorias de participantes | Alta |

| US05 | Criar questionário | Alta |

| US06 | Cadastrar perguntas | Alta |

| US07 | Definir tipo de questão | Alta |

| US08 | Gerar senhas anônimas | Alta |

| US09 | Exportar senhas | Alta |

| US10 | Acessar pesquisa com senha | Alta |

| US11 | Validar senha de acesso | Alta |

| US12 | Responder questionário | Alta |

| US13 | Registrar respostas | Alta |

| US14 | Impedir reutilização de senha | Alta |

| US15 | Monitorar participação | Média |

| US16 | Gerar relatórios estatísticos | Média |

| US17 | Exportar resultados | Média |

REFERÊNCIAS

FACULDADE DE TECNOLOGIA DE LINS PROF. ANTONIO SEABRA. Projeto interdisciplinar com atividades de curricularização da extensão: desenvolvimento de algoritmo para geração de senhas aleatórias por categoria de usuário. Lins, 2026. Material da atividade.

NICOLÓDI, Antonio Carlos. VisualG 3.0. SourceForge, 2020. Disponível em: https://sourceforge.net/projects/visualg30/. Acesso em: 10 jun. 2026.

VISUALG WEB. Sorteios (RandI). Disponível em: https://visualg.com.br/aprender/visualg/aleatoriedade/. Acesso em: 10 jun. 2026.
