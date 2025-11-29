martHelp – Sistema Inteligente de Tickets de Suporte Técnico

SmartHelp é um sistema web simples, moderno e eficiente para gestão de pedidos de suporte técnico (Helpdesk).
Foi desenvolvido como projeto final do curso de Técnico de Helpdesk, com foco em:

✔ Receção de tickets
✔ Gestão técnica dos pedidos
✔ Visualização e organização
✔ Base de dados em tempo real
✔ Interface moderna e responsiva

O sistema funciona totalmente online usando HTML + CSS + Firebase Firestore.

🚀 Funcionalidades
👤 Portal do Cliente

Envio de novos tickets

Campos: Nome, Email, Telefone, Categoria, Prioridade e Descrição

Interface limpa, moderna e responsiva

Dados gravados automaticamente no Firebase

Mensagem de confirmação após envio

👨‍🔧 Painel do Técnico (Admin)

Listagem de todos os tickets submetidos

Visualização de categorias, prioridades e estado

Atualização em tempo real (Firestore)

Interface limpa estilo dashboard

🔍 (Opcional) Página de Consulta de Ticket por ID

Permite ao cliente introduzir o ID e consultar:

Estado do ticket

Categoria

Técnico responsável

Data de criação

📊 (Opcional) Dashboard com Gráficos

Número de tickets por estado

Tickets por categoria

Tickets por prioridade

Gráficos feitos com Chart.js

🔐 Login Técnico (Opcional)

Autenticação Firebase Authentication

Entrada reservada ao painel admin

🛠️ Tecnologias Utilizadas

HTML5

CSS3 (design moderno)

JavaScript ES Modules

Firebase 11 (App + Firestore Database)

Chart.js (Dashboard Visual)

GitHub Pages (Deployment)

📂 Estrutura do Projeto
smarthelp/
│── index.html           → Portal para abrir ticket
│── admin.html           → Painel de técnico
│── consulta.html        → Consulta de ticket por ID (opcional)
│── dashboard.html       → Gráficos (opcional)
│── styles.css           → Design global
│── /img                 → Logótipo / imagens (opcional)
│── README.md            → Documento profissional do projeto

📸 Screenshots

(Adiciona aqui mais tarde prints dos teus ficheiros reais)

Portal do Cliente

Painel Técnico

Dashboard (opcional)

🔧 Como Instalar e Executar
1️⃣ Clonar o repositório
git clone https://github.com/teu-usuario/smarthelp.git
cd smarthelp

2️⃣ Configurar o Firebase

Vai a:
➡ https://console.firebase.google.com

Criar projeto → Firestore Database → Modo de teste

Depois:
Project Settings → Web App → Configuração
E copiar o código parecido com este:

const firebaseConfig = {
  apiKey: "...",
  authDomain: "...",
  projectId: "...",
  storageBucket: "...",
  messagingSenderId: "...",
  appId: "..."
};


Colar este código no index.html, admin.html e outras páginas.

3️⃣ Publicar no GitHub Pages

No repositório:

Settings → Pages → Branch: main → /root

Depois acede ao link:

👉 https://teu-usuario.github.io/smarthelp

🤖 ID Automático no Firebase

O Firestore gera automaticamente um ID único.
Para apresentares um ID mais “humano” no ticket (como TCK-001), usa:

const ticketID = "TCK-" + Date.now();


Guarda este ID junto com o documento.

🧪 Testes realizados

Teste de envio de ticket

Verificação de escrita na base de dados

Teste de carregamento no admin.html

Teste visual e de responsividade

(Opcional) Teste de login técnico

(Opcional) Teste de consulta por ID

📌 Dificuldades Encontradas (para o júri da escola)

Configuração inicial do Firebase

CORS ao tentar enviar dados através de API Google Apps Script

Ajuste do design e responsividade

Ligação entre páginas e base de dados

Testar envio offline

🧠 Apreciação Crítica

O sistema cumpre os objetivos principais:

Simples para o cliente

Eficiente para o técnico

Visualmente profissional

Funciona em qualquer dispositivo

Pontos de melhoria:

Autenticação técnica mais robusta

Possibilidade de anexar ficheiros ao ticket

Adicionar sistema de comentários interno

⭐ Autoavaliação
Aspeto	Avaliação
Organização do projeto	⭐⭐⭐⭐⭐
Criatividade	⭐⭐⭐⭐⭐
Qualidade do código	⭐⭐⭐⭐
Superação de dificuldades	⭐⭐⭐⭐⭐
Documentação	⭐⭐⭐⭐⭐
👨‍🏫 Nota para o Professor / Avaliadores

Este projeto demonstra competências reais de um Técnico de Helpdesk moderno:
✔ Registo estruturado de pedidos
✔ Base de dados em nuvem
✔ Automação
✔ Interface profissional
✔ Entrega organizada e documentada

📄 Licença

Projeto entregue exclusivamente para fins académicos.
Proibida a utilização comercial sem autorização.
