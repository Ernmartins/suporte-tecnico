ÍNDICE

Introdução

Objetivos do Sistema

Arquitetura da Solução

Desenvolvimento e Implementação

Testes Realizados

Erros Encontrados e Resolução

Conclusão

1. Introdução

O presente manual descreve o desenvolvimento do SmartHelp, um sistema de gestão de tickets criado como projeto final do curso de Técnico de Helpdesk.
O sistema permite que utilizadores registem pedidos de suporte, acompanhem o estado dos mesmos e que técnicos possam gerir e atualizar cada ticket.

A plataforma foi construída com tecnologias web modernas (HTML, CSS e JavaScript) e utiliza Firebase Firestore como base de dados, garantindo elevada fiabilidade e acesso em tempo real.

2. Objetivos do Sistema

Foram definidos os seguintes objetivos:

Criar um formulário profissional para submissão de tickets.

Implementar um painel técnico para consulta e atualização.

Permitir consulta pública do ticket através de ID.

Gerar automaticamente IDs únicos para cada registo.

Adicionar um dashboard estatístico com gráficos.

Implementar autenticação Firebase para acesso do técnico.

Criar design moderno e adaptado ao utilizador.

3. Arquitetura da Solução

A solução final adota a seguinte arquitetura:

Frontend

HTML5

CSS3 (tema dark moderno)

JavaScript ES6 (módulos)

Backend (Cloud)

Firebase Firestore (base de dados NoSQL)

Firebase Authentication (login do técnico)

Páginas do sistema

index.html — Submissão de tickets

login.html — Login do técnico

painel.html — Gestão técnica de tickets

dashboard.html — Análise visual com gráficos

consultar-ticket.html — Consulta do estado do ticket

style.css — Estilos globais

firebase.js — Configuração da ligação ao Firebase

4. Desenvolvimento e Implementação
4.1 Criação do Formulário de Tickets (index.html)

Foi construído um formulário com design moderno, campos validados e ligação direta à base de dados Firestore.
O sistema gera automaticamente um ID para cada ticket (TCK-0001, TCK-0002, etc.).

4.2 Integração com Firebase

Foi criado o ficheiro firebase.js contendo a configuração disponibilizada pelo Firebase.

4.3 Painel Técnico (painel.html)

O painel mostra:

Nome do utilizador

Categoria

Prioridade

Estado atual

Possibilidade de atualizar o estado para:

Aberto

Em tratamento

Resolvido

Fechado

4.4 Página de Consulta Pública

Através do ID do ticket, qualquer utilizador pode consultar:

Estado

Data

Detalhes da submissão

4.5 Dashboard com Gráficos

Foram criados gráficos:

Por prioridade

Por estado

Por categoria/tipo

Total de tickets

5. Testes Realizados
Testes funcionais

Submissão de ticket

Geração correta de ID

Escrita na base de dados

Login técnico com Firebase Authentication

Atualização do estado

Pesquisa por ID

Carregamento do dashboard

Testes de interface

Responsividade em mobile

Testes de visualização no GitHub Pages

Teste de temas e estilos

6. Erros Encontrados e Soluções
Erro 1 — Página em branco no GitHub Pages

Causa: Ficheiro CSS não era encontrado.
Solução: Corrigir caminhos relativos (style.css em vez de /style.css).

Erro 2 — Firebase bloqueado

Causa: Regras Firestore protegidas durante testes.
Solução: Definir temporariamente:

allow read, write: if true;


E repor segurança após testes.

Erro 3 — Script não carregava

Causa: O script era executado antes do HTML existir.
Solução: Colocar <script type="module"> no final do body.

Erro 4 — Painel não carregava

Causa: Autenticação mal configurada.
Solução: Implementar verificação onAuthStateChanged.

7. Conclusão

O sistema SmartHelp atingiu todos os objetivos propostos e demonstra uma solução robusta e moderna para suporte técnico.
Para além de cumprir os requisitos mínimos do curso, incorpora funcionalidades avançadas como:

Autenticação de técnico

Dashboard com métricas

Consulta pública do ticket

Design moderno com tema dark

O projeto constitui uma base forte para evolução futura, podendo ser expandido com funcionalidades como anexos, SLA automáticos, notificações por e-mail ou aplicação mobile.
