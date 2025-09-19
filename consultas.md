# fazendo consultas

````SQL

-- Listar todos os clientes com seus respectivos veículos.

select idCliente as dono, modelo as carro, placa
from cliente c join veiculo v on c.idVeiculo = v.idVeiculo;

-- Listar todos os serviços disponíveis na oficina.
select modelo as carro, placa
from veiculo;

-- Listar todos os mecânicos e suas especializações.alter
select nome as mecânico, especificação
from mecanico;

-- Listar todas as peças cadastradas e suas quantidades.
select nome as 'peças', quantidade 
from pecas;

-- Listar todas as ordens de serviço com status atual. 
select nome as 'nome da ordem', status_ as 'status'
from OS;

-- Listar as peças utilizadas em cada ordem de serviço.
select*
from OS o join valor v on o.IDos = v.idVorden
join pecas p on v.idPecas = p.idPecas_valor; 

-- Listar a equipe responsável por cada serviço.
select *
from mecanico m join servico s on m.idMecanico = s.idServiço;
