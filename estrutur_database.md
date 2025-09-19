# estrutura database ordem de serviço

```SQL 
create database OS_oficina;
use os_oficina;

create table OS(
	IDos int primary key auto_increment, 
	nome varchar(30),
    numero char(9),
    data_de_emicao date,
    prazo date,
    valor_total int,
    status_ enum ('em aguardo', 'em andamento', 'finalizado')
);

create table autorizacao(
	id_autoriza int auto_increment primary key,
    idACliente int,
    cliente_autoriza boolean,
    constraint autoriza_cliente foreign key (idACliente) references cliente(idCliente)
);

create table cliente(
	idCliente int auto_increment primary key,
    contato char (9),
    endereço varchar(250),
    idVeiculo int, 
    constraint cliente_cveiculo foreign key (idVeiculo) references veiculo(idServiço) 
);

create table veiculo(
	idVeiculo int auto_increment primary key,
	idServiço int,
    modelo varchar (25),
    placa char (8),
    constraint cliente_veiculo foreign key (idServiço) references servico(idServiço)
);

create table servico(
	idServiço int auto_increment primary key,
    tipo varchar(40),
    descrição varchar(200)
);

create table equipe(
	idEquipe int auto_increment primary key,
    idEServico int,
    idEMecanico int,
    integrante varchar(45),
    avaliação varchar (45),
    constraint equipe_servico foreign key (idEServico) references servico(idServiço),
    constraint equipe_mecanico foreign key (idEMecanico) references mecanico(idMecanico)
);

create table mecanico(
	idMecanico int auto_increment primary key,
    nome varchar(50),
    contato char(8),
    especificação varchar (20)
);

create table valor(
	idvalor int auto_increment primary key,
    idPecas int,
    idVorden int,
    constraint valor_pecas foreign key (idPecas) references pecas(idPecas_valor),
	constraint valor_vOS foreign key (idVorden) references OS(IDos)
);

create table pecas(
	idPecas_valor int auto_increment primary key,
    nome varchar(30),
    quantidade int
);

create table valor_mao(
	idValor_pecas int auto_increment primary key,
    idmao int,
    idPorden int,
    constraint valor_mao foreign key (idmao) references mao_de_obra(idMao),
    constraint valor_pOS foreign key (idPorden) references OS(IDos)
);

create table mao_de_obra(
	idMao int auto_increment primary key,
    valorServico int,
    valorMao int
);
