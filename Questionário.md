# Pereguntas 
1. Quais são as entidades necessárias?;
2. Quais são os principais campos e seus respectivos tipos?;
3. Como essas entidades estão relacionadas?;
4. Simule 2 registros para cada entidade.

# Respostas 
## 1. Quais são as entidades necessárias?;

* Empresa Parceira: Representa as empresas parceiras que serão cadastradas no sistema.

* Tecnologia: Representa as tecnologias disponíveis que podem ser utilizadas pelas empresas parceiras.

* Tecnologias Utilizadas: É uma tabela de junção que registra as tecnologias utilizadas por cada empresa parceira. Ela relaciona as entidades Empresa Parceira e Tecnologia.

* Colaborador: Representa os colaboradores associados às empresas parceiras. Cada colaborador está vinculado a uma empresa parceira.

## 2. Quais são os principais campos e seus respectivos tipos?;
* Empresa Parceira:

  PK ID: (Identificador único da empresa)

  Nome: Texto (Nome da empresa)

  Endereço: Texto (Endereço da empresa)

  Contato: Texto (Informações de contato da empresa)


* Tecnologia:

  PK ID: (Identificador único da tecnologia)
  
  Nome: Texto (Nome da tecnologia)
  
  Área: Texto (Área de atuação da tecnologia)


* Tecnologias Utilizadas:

  ID: Inteiro (Identificador único da relação entre uma tecnologia utilizada e uma empresa)
  
  ID da Empresa: Inteiro (Chave estrangeira referenciando o ID da Empresa Parceira)
  
  ID da Tecnologia: Inteiro (Chave estrangeira referenciando o ID da Tecnologia)


* Colaborador:

  ID: Inteiro (Identificador único do colaborador)
  
  Nome: Texto (Nome do colaborador)
  
  Cargo: Texto (Cargo do colaborador)
  
  ID da Empresa: Inteiro (Chave estrangeira referenciando o ID da Empresa Parceira)
  

## 3. Como essas entidades estão relacionadas?;

Relação entre Empresa Parceira e Tecnologias Utilizadas:

A entidade Empresa Parceira tem uma relação de um para muitos com a entidade Tecnologias Utilizadas, ou seja, uma empresa pode utilizar várias tecnologias e cada tecnologia utilizada está associada a uma única empresa parceira.
Essa relação é estabelecida através do campo "ID da Empresa" na tabela Tecnologias Utilizadas, que é uma chave estrangeira referenciando o ID da Empresa Parceira.

Relação entre Tecnologia e Tecnologias Utilizadas:

A entidade Tecnologia tem uma relação de um para muitos com a entidade Tecnologias Utilizadas, ou seja, uma tecnologia pode ser utilizada por várias empresas e cada uso específico da tecnologia está registrado na tabela Tecnologias Utilizadas.
Essa relação é estabelecida através do campo "ID da Tecnologia" na tabela Tecnologias Utilizadas, que é uma chave estrangeira referenciando o ID da Tecnologia.

Relação entre Empresa Parceira e Colaborador:

A entidade Empresa Parceira tem uma relação de um para muitos com a entidade Colaborador, ou seja, uma empresa pode ter vários colaboradores e cada colaborador está associado a uma única empresa parceira.
Essa relação é estabelecida através do campo "ID da Empresa" na tabela Colaborador, que é uma chave estrangeira referenciando o ID da Empresa Parceira.

## 4. Simule 2 registros para cada entidade.

Empresa Parceira 

| ID | Nome       | Endereço          | Contato                |
|----|------------|-------------------|------------------------|
| 1  | Empresa A  | Rua A, Cidade A   | empresaA@example.com   |
| 2  | Empresa B  | Rua B, Cidade B   | empresaB@example.com   |

Tecnologia

| ID | Nome   | Área             |
|----|--------|------------------|
| 1  | Python | Desenvolvimento   |
| 2  | SQL    | Banco de Dados    |

Tecnologias Utilizadas 

| ID | ID da Empresa | ID da Tecnologia |
|----|---------------|-----------------|
| 1  | 1             | 1               |
| 2  | 1             | 2               |
| 3  | 2             | 1               |
| 4  | 2             | 2               |

Colaborador

| ID | Nome          | Cargo              | ID da Empresa |
|----|---------------|--------------------|---------------|
| 1  | João Silva    | Desenvolvedor      | 1             |
| 2  | Maria Santos  | Analista de Dados  | 2             |

