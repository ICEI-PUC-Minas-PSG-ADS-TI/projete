# Especificações do Projeto

<span style="color:red">Pré-requisitos: <a href="01-Documentação de Contexto.md"> Documentação de Contexto</a></span>

Definição do problema e ideia de solução a partir da perspectiva do usuário. É composta pela definição do  diagrama de personas, histórias de usuários, requisitos funcionais e não funcionais além das restrições do projeto.

Apresente uma visão geral do que será abordado nesta parte do documento, enumerando as técnicas e/ou ferramentas utilizadas para realizar a especificações do projeto

## Personas
1.Carlos Gestor

Carlos, um gestor sênior em uma empresa de engenharia, trabalha longas horas e supervisiona vários projetos de construção. Com foco na segurança, ele se preocupa especialmente com a prevenção de incêndios nos canteiros de obra, onde há materiais inflamáveis e maquinários pesados. No entanto, sua agenda lotada não lhe permite lidar pessoalmente com a inspeção e manutenção dos sistemas de segurança. Ele precisa de uma empresa confiável que cuide das inspeções regulares e da manutenção dos equipamentos de prevenção de incêndio, garantindo que tudo esteja dentro das normas. Isso lhe proporcionaria tranquilidade tanto no trabalho quanto em casa, sabendo que está seguro.

<div align = "center">
<img <img width="350" alt="empresario" src="https://github.com/user-attachments/assets/ecdee88f-d09e-4fb0-8a20-1dfc0d489eac">
</div>

2.Mariana Arquiteta

Mariana, uma arquiteta talentosa, vive uma rotina agitada entre projetos e reuniões. Embora ame seu trabalho, ela raramente tem tempo para cuidar dos detalhes de sua casa. Preocupada com a segurança de sua residência, especialmente com o risco de incêndio, Mariana quer garantir que sua casa esteja protegida. Ela precisa de um serviço especializado em prevenção de incêndios que possa realizar inspeções regulares e garantir que os alarmes, extintores e outros equipamentos de segurança estejam funcionando corretamente. Assim, Mariana pode focar no trabalho, sabendo que sua casa está segura.

<div align = "center">
<img <img width="350" alt="advogada" src="https://github.com/user-attachments/assets/1bd95fc0-6bf8-4672-a4fa-2ef59999e528">
</div>

3.Rafael Chef de Restaurante

Rafael, um chef renomado, comanda um restaurante movimentado e sabe que o risco de incêndio na cozinha é alto. Com a agenda cheia, ele precisa de um serviço confiável de prevenção de incêndios para garantir que os extintores, sprinklers e alarmes estejam em perfeito estado. Assim, Rafael pode focar na culinária, sabendo que o restaurante está seguro.

<div align = "center">
<img <img width="350" alt="cozinha" src="https://github.com/user-attachments/assets/c7fc2ed6-1da4-44f9-b9c7-03821dac6514">
</div>

4.Luciana Dona de Casa

Luciana é dona de casa e cuida sozinha de seu lar e de seus dois filhos pequenos. Com tantos afazeres, ela se preocupa com a segurança da família, especialmente com o risco de incêndios, já que utiliza diversos eletrodomésticos diariamente. Ela precisa de um serviço especializado que possa instalar e manter alarmes de incêndio, extintores e sensores de fumaça em perfeito estado. Isso garantiria a proteção de sua casa e a tranquilidade de saber que sua família está segura, permitindo que ela se concentre nas demais tarefas do dia a dia.

<div align = "center">
<img <img width="350"  alt="donadecsa" src="https://github.com/user-attachments/assets/b45e9dc0-1715-4687-bcee-fa7a09932678">
</div>

## Histórias de Usuários

Com base na análise das personas forma identificadas as seguintes histórias de usuários:

|EU COMO... `PERSONA`| QUERO/PRECISO ... `FUNCIONALIDADE` |PARA ... `MOTIVO/VALOR`                 |
|--------------------|------------------------------------|----------------------------------------|
|Usuário do sistema  | Registrar minhas tarefas           | Não esquecer de fazê-las               |
|Administrador       | Alterar permissões                 | Permitir que possam administrar contas |

Apresente aqui as histórias de usuário que são relevantes para o projeto de sua solução. As Histórias de Usuário consistem em uma ferramenta poderosa para a compreensão e elicitação dos requisitos funcionais e não funcionais da sua aplicação. Se possível, agrupe as histórias de usuário por contexto, para facilitar consultas recorrentes à essa parte do documento.

> **Links Úteis**:
> - [Histórias de usuários com exemplos e template](https://www.atlassian.com/br/agile/project-management/user-stories)
> - [Como escrever boas histórias de usuário (User Stories)](https://medium.com/vertice/como-escrever-boas-users-stories-hist%C3%B3rias-de-usu%C3%A1rios-b29c75043fac)
> - [User Stories: requisitos que humanos entendem](https://www.luiztools.com.br/post/user-stories-descricao-de-requisitos-que-humanos-entendem/)
> - [Histórias de Usuários: mais exemplos](https://www.reqview.com/doc/user-stories-example.html)
> - [9 Common User Story Mistakes](https://airfocus.com/blog/user-story-mistakes/)



## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto. Para determinar a prioridade de requisitos, aplicar uma técnica de priorização de requisitos e detalhar como a técnica foi aplicada.

### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-----------------------------------------|----|
|RF-001| Permitir que o usuário cadastre tarefas | ALTA | 
|RF-002| Emitir um relatório de tarefas no mês   | MÉDIA |

### Requisitos não Funcionais

|ID     | Descrição do Requisito  |Prioridade |
|-------|-------------------------|----|
|RNF-001| O sistema deve ser responsivo para rodar em um dispositivos móvel | MÉDIA | 
|RNF-002| Deve processar requisições do usuário em no máximo 3s |  BAIXA | 

Com base nas Histórias de Usuário, enumere os requisitos da sua solução. Classifique esses requisitos em dois grupos:

- [Requisitos Funcionais
 (RF)](https://pt.wikipedia.org/wiki/Requisito_funcional):
 correspondem a uma funcionalidade que deve estar presente na
  plataforma (ex: cadastro de usuário).
- [Requisitos Não Funcionais
  (RNF)](https://pt.wikipedia.org/wiki/Requisito_n%C3%A3o_funcional):
  correspondem a uma característica técnica, seja de usabilidade,
  desempenho, confiabilidade, segurança ou outro (ex: suporte a
  dispositivos iOS e Android).
Lembre-se que cada requisito deve corresponder à uma e somente uma
característica alvo da sua solução. Além disso, certifique-se de que
todos os aspectos capturados nas Histórias de Usuário foram cobertos.

## Restrições

O projeto está restrito pelos itens apresentados na tabela a seguir.

|ID| Restrição                                             |
|--|-------------------------------------------------------|
|01| O projeto deverá ser entregue até o final do semestre |
|02| Não pode ser desenvolvido um módulo de backend        |

Enumere as restrições à sua solução. Lembre-se de que as restrições geralmente limitam a solução candidata.

> **Links Úteis**:
> - [O que são Requisitos Funcionais e Requisitos Não Funcionais?](https://codificar.com.br/requisitos-funcionais-nao-funcionais/)
> - [O que são requisitos funcionais e requisitos não funcionais?](https://analisederequisitos.com.br/requisitos-funcionais-e-requisitos-nao-funcionais-o-que-sao/)
