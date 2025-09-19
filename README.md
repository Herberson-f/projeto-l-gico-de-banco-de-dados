# projeto lógico de banco de dados

## Sistema de Controle de Ordem de Serviço de Oficina

O projeto consiste na criação de um sistema de banco de dados relacional para gerenciar as operações de uma oficina mecânica, desenvolvido como parte do curso da DIO. O sistema permite o controle completo de clientes, veículos, serviços, peças, mão de obra, equipe e ordens de serviço (OS), garantindo que todas as informações estejam integradas e organizadas.

### O banco de dados contempla tabelas que representam os principais elementos de uma oficina:

* Cliente e Veículo: cadastro de clientes e seus veículos, possibilitando relacionamentos diretos com os serviços realizados.

* Serviço e Mão de Obra: registros detalhados de serviços oferecidos, incluindo o custo da mão de obra e a descrição do serviço.

* Peças e Valores: controle de peças utilizadas nas ordens de serviço, vinculado aos respectivos valores e estoque.

* Equipe e Mecânicos: gerenciamento dos profissionais responsáveis pelos serviços, incluindo avaliações de desempenho.

* Ordens de Serviço (OS) e Autorizações: acompanhamento das OS abertas, seu status e a autorização do cliente para execução do serviço.

### Além disso, o projeto inclui inserts populados com dados fictícios, permitindo simular cenários reais de funcionamento da oficina. Com isso, o sistema possibilita consultas complexas para análise de dados, como: 
peças usadas por OS, valores totais de serviços, mecânicos mais atuantes, status de ordens e clientes que não autorizaram serviços.

O desenvolvimento desse projeto proporcionou prática avançada em modelagem de dados, criação de relacionamentos com chaves estrangeiras, consultas SQL complexas e integração de múltiplas tabelas, preparando o estudante para cenários reais de gestão de bancos de dados relacionais.
