# RESILIADATA_
Projeto Individual Módulo 3 - Sistema RESILIADATA
## Contexto 
Você foi contratado para desenvolver um banco de dados que irá armazenar dados
importantes que será utilizado pelo sistema RESILIADATA.
➔ O sistema irá auxiliar na avaliação de quais são as tecnologias que as empresas parceiras 
estão utilizando e quem são seus colaboradores; 

➔ Vamos ter o cadastro de empresas parceiras, cadastro de tecnologias com a opção de 
selecionar a área (webdev, dados, marketing, etc.), uma tabela para registrar quais 
tecnologias as empresas estão utilizando e uma tabela para cadastro de colaboradores.

O RESILIADATA é um sistema que auxilia na avaliação das tecnologias utilizadas pelas empresas parceiras, bem como no gerenciamento dos colaboradores associados a essas empresas.

## Funcionalidades
O sistema RESILIADATA possui as seguintes funcionalidades:

* Cadastro de Empresas Parceiras: Permite registrar informações sobre as empresas parceiras, incluindo nome, endereço e informações de contato.

* Cadastro de Tecnologias: Permite cadastrar as tecnologias disponíveis, incluindo nome e área de atuação.

* Registro de Tecnologias Utilizadas: Permite relacionar as tecnologias utilizadas por cada empresa parceira. Essa funcionalidade registra quais tecnologias estão sendo utilizadas por quais empresas.

* Cadastro de Colaboradores: Permite cadastrar os colaboradores associados às empresas parceiras, incluindo nome, cargo e vinculação à empresa.

## Estrutura do Banco de Dados
O sistema RESILIADATA utiliza um banco de dados para armazenar as informações. A estrutura do banco de dados é composta pelas seguintes tabelas:

1. Tabela "Empresa Parceira":
    * Campos: ID, Nome, Endereço, Contato
2. Tabela "Tecnologia":
    * Campos: ID, Nome, Área
3. Tabela "Tecnologias Utilizadas":
    * Campos: ID, ID da Empresa (chave estrangeira referenciando a tabela "Empresa Parceira"), ID da Tecnologia (chave estrangeira referenciando a tabela "Tecnologia")
4. Tabela "Colaborador":
    * Campos: ID, Nome, Cargo, ID da Empresa (chave estrangeira referenciando a tabela "Empresa Parceira")
  
## Relacionamentos

As tabelas do banco de dados estão relacionadas da seguinte maneira:

* A tabela "Tecnologias Utilizadas" estabelece uma relação de um-para-muitos com a tabela "Empresa Parceira", registrando quais tecnologias são utilizadas por cada empresa.

* A tabela "Colaborador" possui uma relação de um-para-um com a tabela "Empresa Parceira", associando cada colaborador a uma empresa específica.
--- 


Linkedin; https://www.linkedin.com/in/gustavo-daher-/

