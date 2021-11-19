2TDSR


Aline Triñanes Machado - RM 84449 - alinetrim@hotmail.com

Alysson Gustavo Rodrigues Maciel - RM 86484 - alymaciel8@gmail.com

Gabriel Franham - RM 80483 - gabrielfranham@gmail.com

Gabriel Garcia Pereira - RM 86288 - gabriel.garp@outlook.com

Helouíse Cristina de Almeida Itokazo - RM 85110 - helouise.almeida93@gmail.com

Jonas Muniz de Souza - RM 84575 - jonasmzsouza@gmail.com



O projeto tem como intuito auxiliar na distribuição de alimentos que sobram de escolas da rede pública de ensino, tanto municipal, quanto estadual.
Devido convivência com funcionários destas escolas, é sabido que sempre eles compram com um pouco de sobra, uma margem, e esta não é possível para alimentar um ano todo. Como uma sala não pode ter um tipo de merenda, e outra sala outro, as vezes há o desperdício de pequenas quantidades de alimentos – como frutas, verduras, até carnes próximas ao vencimento.
O app e-alimenta tem o intuito de mapear estas sobras de alimentos e bebidas nos, e distribuir às famílias que vivem em situação de risco, já previamente cadastradas pelos sistemas das unidades.
Um funcionário – seja da própria cozinha, ou setor administrativo – entra pelo app no celular da escola, ou seu próprio celular, e realiza cadastro com a data de vencimento e quantidade disponível, e assim que os pais vêm buscar os filhos, podem fazer a retirada de alimentos. 
Tudo devidamente identificado. 
Assim reduzem o desperdício e ainda auxiliam na distribuição de alimentos que podem diminuir a fome.

Funcionalidades
Cadastro de alimentos disponíveis para retirada
Listagem dos alimentos disponíveis
Retirada de alimentos disponíveis
Listagem de retiradas de alimentos


===============HOWTO================

1 - Cadastrar alimentos
2 - Editar alimentos
3 - Retirar Alimentos disponíveis



====================BANCO================

Senha:Menk@2020
login:ambers



ealimenta.database.windows.net
jdbc:sqlserver://ealimenta.database.windows.net:1433;database=ealimenta;user=ambers@ealimenta;password={your_password_here};encrypt=true;trustServerCertificate=false;hostNameInCertificate=*.database.windows.net;loginTimeout=30;


Script de criação das tabelas:

Hibernate: create table sq_tb_alimento (next_val numeric(19,0))
Hibernate: insert into sq_tb_alimento values ( 1 )
Hibernate: create table sq_tb_retirada (next_val numeric(19,0))
Hibernate: insert into sq_tb_retirada values ( 1 )
Hibernate: create table tb_alimento (id_alimento numeric(19,0) not null, data_cadastro datetime not null, data_vencimento datetime not null, nm_alimento varchar(255) not null, quantidade numeric(19,0) not null, tipo_alimento varchar(255) not null, primary key (id_alimento))
Hibernate: create table tb_retirada (id_retirada numeric(19,0) not null, data_retirada datetime not null, quantidade numeric(19,0) not null, rg_retirada varchar(255) not null, id_alimento_retirado numeric(19,0) not null, primary key (id_retirada))
Hibernate: alter table tb_retirada add constraint FKk6tnp69r4yk7242dgihce5s0i foreign key (id_alimento_retirado) references tb_alimento

=====================BANCO================

https://github.com/GarciaGP/EAlimenta

Azure app:
http://ealimenta.azurewebsites.net/

Video:
https://www.youtube.com/watch?v=UbK_Rlsz-kE


