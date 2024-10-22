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

![WhatsApp Image 2024-10-21 at 22 50 10](https://github.com/user-attachments/assets/1e609d69-27d5-4efc-8c5f-1851ed9e8e12)


### 4.3.1. Modelo Físico

CREATE TABLE produtos (
    produto_id BIGINT PRIMARY KEY IDENTITY(1,1),
   nome_produto NVARCHAR(255) NOT NULL,
    preco_produto DECIMAL(10, 2) NOT NULL,
    tipo_produto NVARCHAR(255) NOT NULL,
    qtde_estoque INT DEFAULT 0
);

CREATE TABLE usuarios (
    usuario_id BIGINT PRIMARY KEY IDENTITY(1,1),  
    nome NVARCHAR(255) NOT NULL,
    email NVARCHAR(255) NOT NULL,
    telefone NVARCHAR(50),                        
    endereco NVARCHAR(255)                        
);

CREATE TABLE feedbacks (
    feedback_id BIGINT PRIMARY KEY IDENTITY(1,1),
    usuario_id BIGINT NOT NULL,                       
    nome_feedback NVARCHAR(255) NOT NULL,         
    texto NVARCHAR(MAX),                          
    avaliacao INT NOT NULL,                       
    FOREIGN KEY (usuario_id) REFERENCES usuarios(usuario_id)  
);

CREATE TABLE servicos (
    servico_id BIGINT PRIMARY KEY IDENTITY(1,1),   
    nome_servico NVARCHAR(255) NOT NULL,           
    preco_servico DECIMAL(10, 2) NOT NULL,         
    descricao_servico NVARCHAR(MAX)                
);

CREATE TABLE orcamentos (
    orcamento_id BIGINT PRIMARY KEY IDENTITY(1,1),  
    usuario_id BIGINT NOT NULL,                     
    preco_total DECIMAL(10, 2) NOT NULL,            
    status NVARCHAR(50) NOT NULL,                   
    FOREIGN KEY (usuario_id) REFERENCES usuarios(usuario_id)  
);

CREATE TABLE orcamentos_servicos (
    orcamento_servico_id BIGINT PRIMARY KEY IDENTITY(1,1),  
    orcamento_id BIGINT NOT NULL,                          
    servico_id BIGINT NOT NULL,                            
    FOREIGN KEY (orcamento_id) REFERENCES orcamentos(orcamento_id),  
    FOREIGN KEY (servico_id) REFERENCES servicos(servico_id)         
);

CREATE TABLE orcamentos_produtos (
    orcamento_produto_id BIGINT PRIMARY KEY IDENTITY(1,1),  
    orcamento_id BIGINT NOT NULL,                          
    produto_id BIGINT NOT NULL,                            
    qtde_estoque INT NOT NULL,                             
    FOREIGN KEY (orcamento_id) REFERENCES orcamentos(orcamento_id),  
    FOREIGN KEY (produto_id) REFERENCES produtos(produto_id)         
);

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

