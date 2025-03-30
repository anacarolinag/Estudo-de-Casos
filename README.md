# Estudo-de-Casos
#Trabalho Banco de dados



/* brModelo - Lógico Ana Carolina: */

CREATE TABLE Cliente (
    Nome VARCHAR(255),
    Telefone NUMERIC,
    id_Cliente INTEGER PRIMARY KEY,
    Email VARCHAR(100)
);

CREATE TABLE Venda (
    id_Venda INTEGER PRIMARY KEY,
    Data_ Hora DATE,
    fk_id_Cliente INTEGER,
    fk_id_Colaborador INTEGER,
    fk_id_Produto INTEGER
);

CREATE TABLE Colaborador (
    Nome VARCHAR(255),
    Cargo VARCHAR(100),
    id_Colaborador INTEGER PRIMARY KEY
);

CREATE TABLE Estoque (
    Quantidade INTEGER,
    id_Estoque INTEGER PRIMARY KEY,
    Nome VARCHAR(255),
    Categoria VARCHAR(100),
    Preço DECIMAL(10, 2),
);

CREATE TABLE Produto (
    id_Estoque INTEGER,
    id_Produto INTEGER PRIMARY KEY,
    Nome VARCHAR(255),
    Preço DECIMAL(10, 2),
);
