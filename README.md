readme
agrotrack_robot v2
criador: davi carbone

projeto de automação desenvolvido usando Power Automate de forma independente com foco em automação de processos repetitivos.
fluxo do robô:

-> inserção de número de container que deseja ser rastreado a partir de um excel previamente preenchido (seria tipo: quero que você preencha tudo sobre este container em específico);
-> rastreamento no site para saber onde se encontra o container;
-> instalação do arquivo json gerado a partir do front-end (javascript)
-> ler arquivo json
-> inserção dos dados obtidos pelo site numa tabela excel, contendo todas as informações.

--> loop se repete ENQUANTO TIVER container para preencher (é ilimitado e automático).

o que é obtido: dados brutos prontos para futuras análises utilizando PowerBI ou outras ferramentas.

ganhos: o TEMPO que é gasto trabalhando num processo repetitivo como este pode ser dirigido a alguma outra tarefa mais complexa ou que tenha mais prioridade.

resumo do impacto para inserção de dados sobre 50 containeres:
👤 Humano:   ~3 horas
🤖 Robô:     ~7 minutos
⚡ Ganho:     96% de redução no tempo

e o robô ainda:

não erra digitação
não se cansa
roda de madrugada se precisar
já entrega os dados prontos para o Power BI


regras do projeto:

1. o front-end web foi criado através de um prompt com o Claude, porém a foi totalmente ideia minha.
2. é um MVP (minimum viable product), o que significa que não conta com sistemas de segurança robustos nem dados sobre containeres reais. é um projeto teste.
3. o site não possui comunicação com back-end algum (o que seria, no caso, o banco de dados onde os status dos contêineres estão guardados.
exemplo: conteinerA está em X cidade, X país e está se dirigindo a Y localidade através do navio Z. esses são dados incluídos já no front-end o que, na vida real, nunca aconteceria. os dados estariam protegidos no database, permitindo acesso somente através da chave da API.

numa situação real, esses dados seriam obtidos através de uma requisição para a API para obter os dados no banco de dados da empresa (um GET). porém, a informação retornaria da mesma forma que é retornada neste projeto, e o robô funcionaria da mesma forma.

a. logo, todos os status são fictícios e servem para mostrar a funcionalidade do robô.
porém, mesmo se tratando de dados fictícios, a eficácia dele é demonstrada através do que ele faz a partir dos dados e como agiliza um trabalho manual e extremamente repetitivo.

Stack: HTML/CSS/JS · Power Automate Desktop · Excel · (futuro: API REST + banco de dados real)
