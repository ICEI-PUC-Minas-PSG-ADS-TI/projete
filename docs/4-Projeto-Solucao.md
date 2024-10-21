## 4. Projeto da Solução

<span style="color:red">Pré-requisitos: <a href="03-Modelagem do Processo de Negocio.md"> Modelagem do Processo de Negocio</a></span>

### 4.1. Arquitetura da solução

![Fluxograma Pedido Azul Cinza](https://github.com/user-attachments/assets/f47bad5c-bfc2-4cd3-a827-a82c623e4300)

### 4.2. Protótipos de telas

<img src="https://github.com/user-attachments/assets/924ece57-2c74-4b3e-9423-73d9abcc76dc">
<img src="https://github.com/user-attachments/assets/86d64b1b-90a2-4530-8e2f-76e20132ced5">
<img src="https://github.com/user-attachments/assets/828c4268-d025-450f-a0fe-6865bc814a33">
<img src="https://github.com/user-attachments/assets/ca4e42b8-80c4-4f8f-810b-74f418602889">
<img src="https://github.com/user-attachments/assets/ce3cd2fe-7c29-4008-b0ea-1b496c42fb7e">
<img src="https://github.com/user-attachments/assets/4cc3ce18-948b-445c-8cc0-ae907392cef4">
<img src="https://github.com/user-attachments/assets/0c2d1926-3d70-4b49-bba8-1aa9d1215644">
<img src="https://github.com/user-attachments/assets/e6e1c708-dff5-40f4-8f9a-0caae5e89b3a">

### 4.3. Modelo DER

O Modelo ER representa através de um diagrama como as entidades (coisas, objetos) se relacionam entre si na aplicação interativa.]

As referências abaixo irão auxiliá-lo na geração do artefato “Modelo ER”.

> - [Como fazer um diagrama entidade relacionamento | Lucidchart](https://www.lucidchart.com/pages/pt/como-fazer-um-diagrama-entidade-relacionamento)

### 4.3.1. Modelo Físico

Insira aqui o script de criação das tabelas do banco de dados.

Veja um exemplo:

<code>

 -- Criação da tabela Médico
CREATE TABLE Medico (
    MedCodigo INTEGER PRIMARY KEY,
    MedNome VARCHAR(100)
);


-- Criação da tabela Paciente
CREATE TABLE Paciente (
    PacCodigo INTEGER PRIMARY KEY,
    PacNome VARCHAR(100)
);

-- Criação da tabela Consulta
CREATE TABLE Consulta (
    ConCodigo INTEGER PRIMARY KEY,
    MedCodigo INTEGER,
    PacCodigo INTEGER,
    Data DATE,
    FOREIGN KEY (MedCodigo) REFERENCES Medico(MedCodigo),
    FOREIGN KEY (PacCodigo) REFERENCES Paciente(PacCodigo)
);

-- Criação da tabela Medicamento
CREATE TABLE Medicamento (
    MdcCodigo INTEGER PRIMARY KEY,
    MdcNome VARCHAR(100)
);

-- Criação da tabela Prescricao
CREATE TABLE Prescricao (
    ConCodigo INTEGER,
    MdcCodigo INTEGER,
    Posologia VARCHAR(200),
    PRIMARY KEY (ConCodigo, MdcCodigo),
    FOREIGN KEY (ConCodigo) REFERENCES Consulta(ConCodigo),
    FOREIGN KEY (MdcCodigo) REFERENCES Medicamento(MdcCodigo)
);

</code>

Este script deverá ser incluído em um arquivo .sql na pasta src\bd.

### 4.4. Tecnologias

Para a implementação da solução, será utilizada uma combinação de tecnologias para garantir que o sistema funcione de maneira eficiente, tanto no front-end quanto no back-end. As principais tecnologias e ferramentas a serem utilizadas são:

1. Visual Studio Code: IDE de desenvolvimento, que permite a edição de código e integração com várias ferramentas.
2. HTML: Para estruturar o conteúdo das páginas web.
3. CSS: Para estilizar e personalizar a interface do usuário.
4. JavaScript: Linguagem de programação usada para tornar a página interativa no lado do cliente e controlar o comportamento dinâmico da aplicação.
5. Bootstrap: Framework CSS que facilita a criação de layouts responsivos e estilos modernos com componentes prontos.
6. Node.js: Ambiente de execução JavaScript no lado do servidor, que será usado em conjunto com Express.js para gerenciar o back-end e processar requisições do usuário.
7. Express.js: Framework para Node.js que permite criar rotas, middleware e lidar com requisições HTTP de maneira eficiente.
8. MySQL: Sistema de gerenciamento de banco de dados relacional, que armazenará as informações da aplicação, como dados de clientes, produtos, etc.

| **Dimensão**   | **Tecnologia**  |
| ---            | ---             |
| SGBD           | MySQL           |
| Front end      | HTML+CSS+JS     |
| Back end       | Node.js+Express.js |
| Deploy         | Netlify    |

