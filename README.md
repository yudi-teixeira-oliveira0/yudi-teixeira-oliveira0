- 👋 Hi, I’m @yudi-teixeira-oliveira0
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
-yudi-teixeira-oliveira0/yudi-teixeira-oliveira0 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
-You can click the Preview link to take a look at your changes.
--->
-drop table if exists Produto;
-drop table if exists Produto_precos;
-drop table if exists Usuario_Role;
-drop table if exists Role;
-drop table if exists Usuario;
-create table Produto (id integer not null auto_increment, dataLancamento datetime, descricao varchar(255), paginas integer not null, sumarioPath varchar(255), titulo varchar(255), primary key (id));
-create table Produto_precos (Produto_id integer not null, tipo integer, valor decimal(19,2));
-create table Role (nome varchar(255) not null, primary key (nome));
-create table Usuario (email varchar(255) not null, nome varchar(255), senha varchar(255), primary key (email));
-create table Usuario_Role (email varchar(255) not null, role_nome varchar(255) not null);
-alter table Produto_precos add constraint FK_hl4xdmygc7v2x607r4rbs6x3a foreign key (Produto_id) references Produto (id);
-alter table Usuario_Role add constraint FK_5nbp4m2sk65w2mq9rfn680cx2 foreign key (role_nome) references Role (nome);
-alter table Usuario_Role add constraint FK_4w45e3buitnd4f3ok8jdlrqkh foreign key (email) references Usuario (email);
