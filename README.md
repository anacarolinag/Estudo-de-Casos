# Estudo-de-Casos
#Trabalho Banco de dados



/* brModelo - Lógico Ana Carolina: */

CREATE TABLE Cliente (
  Nome VARCHAR(255),
  Telefone NUMERIC,
  id_Cliente INT PRIMARY KEY,
  Email VARCHAR(100)
);

CREATE TABLE Colaborador (
  Nome VARCHAR(255),
  Cargo VARCHAR(100),
  id_Colaborador INT PRIMARY KEY
);

CREATE TABLE Produto (
  id_Produto INT PRIMARY KEY,
  Nome VARCHAR(255),
  Preco DECIMAL(10, 2)
);

CREATE TABLE Estoque (
  Quantidade INT,
  id_Estoque INT PRIMARY KEY,
  id_Produto INT,
  FOREIGN KEY (id_Produto) REFERENCES Produto(id_Produto)
);

CREATE TABLE Venda (
  id_Venda INT PRIMARY KEY,
  Data_Hora DATETIME,
  fk_id_Cliente INT,
  fk_id_Colaborador INT,
  FOREIGN KEY (fk_id_Cliente) REFERENCES Cliente(id_Cliente),
  FOREIGN KEY (fk_id_Colaborador) REFERENCES Colaborador(id_Colaborador)
);
