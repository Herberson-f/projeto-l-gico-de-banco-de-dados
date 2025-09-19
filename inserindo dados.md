# inserindo dados

```SQL

insert into servico (tipo, descrição)
 values
('Troca de Óleo', 'Substituição do óleo lubrificante e filtro de óleo'),
('Revisão Geral', 'Inspeção completa dos principais sistemas do veículo'),
('Troca de Pneus', 'Remoção e substituição de pneus desgastados'),
('Alinhamento', 'Correção da geometria da direção e suspensão'),
('Balanceamento', 'Correção do equilíbrio das rodas'),
('Troca de Bateria', 'Substituição de bateria automotiva descarregada'),
('Freios', 'Troca de pastilhas, discos ou fluído de freio'),
('Suspensão', 'Revisão e troca de amortecedores e molas'),
('Troca de Embreagem', 'Substituição do kit de embreagem completo'),
('Injeção Eletrônica', 'Limpeza e ajustes nos bicos injetores e sensores'),
('Ar Condicionado', 'Higienização e recarga do sistema de ar condicionado'),
('Troca de Correia Dentada', 'Substituição da correia e polias associadas');

desc servico;

insert into mecanico (nome, contato, especificação) values
('Carlos Andrade', '99874562', 'Suspensão'),
('João Silva', '99785431', 'Freios'),
('Pedro Souza', '99654123', 'Motor'),
('Marcos Lima', '99543287', 'Elétrica'),
('Rafael Torres', '99456321', 'Embreagem'),
('André Oliveira', '99321456', 'Troca de Óleo'),
('Diego Costa', '99213478', 'Pneus'),
('Lucas Mendes', '99187654', 'Ar Condicionado'),
('Mateus Santos', '99098765', 'Injeção Eletrônica'),
('Bruno Rocha', '98965432', 'Suspensão'),
('Thiago Nunes', '98874321', 'Transmissão'),
('Gabriel Freitas', '98765413', 'Direção'),
('Leonardo Alves', '98652147', 'Correia Dentada'),
('Felipe Martins', '98563214', 'Revisão Geral'),
('Gustavo Ramos', '98471236', 'Balanceamento');

desc mecanico;

insert into pecas (nome, quantidade) values
('Filtro de Óleo', 50),
('Filtro de Ar', 40),
('Filtro de Combustível', 35),
('Pastilha de Freio', 100),
('Disco de Freio', 60),
('Amortecedor', 45),
('Bateria 60Ah', 25),
('Bateria 70Ah', 20),
('Correia Dentada', 30),
('Correia Alternador', 25),
('Pneu Aro 15', 80),
('Pneu Aro 16', 60),
('Velas de Ignição', 120),
('Kit Embreagem', 15),
('Radiador', 10),
('Bomba de Combustível', 18),
('Rolamento de Roda', 40),
('Parafuso de Roda', 200),
('Sensor de ABS', 12),
('Retrovisor', 22);

desc pecas;

insert into mao_de_obra (valorServico, valorMao) values
(250, 120),
(800, 500),
(450, 300),
(200, 100),
(150, 80),
(350, 200),
(1200, 700),
(600, 350),
(500, 250),
(300, 180),
(220, 100),
(700, 400),
(900, 500),
(1500, 900),
(1100, 600);

desc mao_de_obra;

insert into veiculo (idServiço, modelo, placa) values
(1, 'Fiat Uno', 'ABC1234'),
(2, 'Volkswagen Golf', 'DEF5678'),
(3, 'Ford Ka', 'GHI9012'),
(4, 'Chevrolet Onix', 'JKL3456'),
(5, 'Honda Civic', 'MNO7890'),
(6, 'Toyota Corolla', 'PQR1234'),
(7, 'Hyundai HB20', 'STU5678'),
(8, 'Renault Sandero', 'VWX9012'),
(9, 'Nissan Versa', 'YZA3456'),
(10, 'Jeep Renegade', 'BCD7890');

desc veiculo;

insert into cliente (contato, endereço, idVeiculo) values
('998877665', 'Rua A, 123, Centro, Cidade X', 1),
('997766554', 'Av. B, 456, Bairro Y, Cidade X', 2),
('996655443', 'Rua C, 789, Bairro Z, Cidade Y', 3),
('995544332', 'Av. D, 101, Centro, Cidade Y', 4),
('994433221', 'Rua E, 202, Bairro W, Cidade Z', 5),
('993322110', 'Av. F, 303, Bairro V, Cidade Z', 6),
('992211009', 'Rua G, 404, Centro, Cidade X', 7),
('991100998', 'Av. H, 505, Bairro U, Cidade Y', 8),
('990099887', 'Rua I, 606, Bairro T, Cidade Z', 9),
('989988776', 'Av. J, 707, Centro, Cidade X', 10);
 
 desc cliente;
 
 insert into OS (nome, numero, data_de_emicao, prazo, valor_total, status_) values
('Troca de Óleo Uno', '000000001', '2025-09-01', '2025-09-02', 250, 'finalizado'),
('Revisão Golf', '000000002', '2025-09-03', '2025-09-05', 800, 'em andamento'),
('Troca Pneus Ka', '000000003', '2025-09-04', '2025-09-06', 450, 'em andamento'),
('Alinhamento Onix', '000000004', '2025-09-05', '2025-09-05', 200, 'finalizado'),
('Troca Bateria Civic', '000000005', '2025-09-06', '2025-09-07', 300, 'em aguardo'),
('Suspensão Corolla', '000000006', '2025-09-07', '2025-09-10', 500, 'em andamento'),
('Freios HB20', '000000007', '2025-09-08', '2025-09-09', 350, 'finalizado'),
('Injeção Sandero', '000000008', '2025-09-09', '2025-09-12', 700, 'em andamento'),
('Ar Condicionado Versa', '000000009', '2025-09-10', '2025-09-11', 220, 'finalizado'),
('Troca Correia Renegade', '000000010', '2025-09-11', '2025-09-14', 600, 'em aguardo');

desc OS;

insert into equipe (idEServico, idEMecanico, integrante, avaliação) values
(1, 6, 'Carlos Andrade', 'Excelente'),
(2, 15, 'Felipe Martins', 'Bom'),
(3, 7, 'Diego Costa', 'Excelente'),
(4, 1, 'Carlos Andrade', 'Regular'),
(5, 14, 'Gustavo Ramos', 'Bom'),
(6, 10, 'Lucas Mendes', 'Excelente'),
(7, 2, 'João Silva', 'Bom'),
(8, 9, 'Mateus Santos', 'Excelente'),
(9, 4, 'Marcos Lima', 'Regular'),
(10, 5, 'Rafael Torres', 'Excelente'),
(11, 8, 'Lucas Mendes', 'Bom'),
(12, 3, 'Pedro Souza', 'Excelente'),
(1, 6, 'Carlos Andrade', 'Bom'),
(2, 15, 'Felipe Martins', 'Excelente'),
(3, 7, 'Diego Costa', 'Bom');

desc equipe;

insert into valor (idPecas, idVorden) values
(1, 1),
(2, 1),
(3, 2),
(4, 2),
(5, 3),
(6, 4),
(7, 5),
(8, 6),
(9, 6),
(10, 7),
(11, 8),
(12, 8),
(13, 9),
(14, 3),
(15, 4),
(16, 5),
(17, 6),
(18, 7),
(19, 9),
(20, 10);

insert into valor_mao (idmao, idPorden) values
(1, 1),
(2, 2),
(3, 3),
(4, 4),
(5, 5),
(6, 6),
(7, 2),
(8, 10),
(9, 3),
(10, 5),
(11, 9),
(12, 8),
(13, 7),
(14, 6),
(15, 4);

insert into autorizacao (idACliente, cliente_autoriza) values
(1, TRUE),
(2, TRUE),
(3, TRUE),
(4, FALSE),
(5, TRUE),
(6, TRUE),
(7, FALSE),
(8, TRUE),
(9, TRUE),
(10, FALSE);
