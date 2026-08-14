# 🚀 Alura Album - Copa do Mundo Tech

Um tributo interativo em forma de álbum de figurinhas digital que celebra as mentes mais brilhantes e pioneiras do mundo da tecnologia. Desenvolvido durante a **Imersão Alura (Julho de 2026)**.

O projeto combina uma experiência visual premium de simulação de livro físico com integração dinâmica a um servidor de backend.

---

## 🎯 Objetivo do Projeto

O objetivo do **Alura Album** é criar um álbum de figurinhas interativo e imersivo, homenageando figuras históricas e contemporâneas divididas em cinco categorias essenciais da tecnologia:
1. **Inteligência Artificial (IA)** (Pioneiros como Alan Turing, Geoffrey Hinton e Sam Altman)
2. **Python** (Arquitetos da simplicidade como Guido van Rossum e criadores de grandes bibliotecas como Pandas e NumPy)
3. **Banco de Dados** (De Edgar F. Codd aos criadores de MongoDB, Redis e MySQL)
4. **Sistemas Operacionais** (Desenvolvedores fundamentais como Linus Torvalds, Dennis Ritchie e Steve Jobs)
5. **Devs do Brasil** (Profissionais de destaque e educadores da tecnologia brasileira, como Paulo e Guilherme Silveira, Gustavo Guanabara, Rafaela Ballerini e outros)

---

## 🛠️ Tecnologias Utilizadas

* **HTML5**: Estrutura semântica das páginas do álbum.
* **CSS3**: Estilização premium baseada em variáveis personalizadas, gradientes ricos, efeitos de vidro fosco (*glassmorphism*), animações de *glitch* e responsividade.
* **JavaScript (Vanilla)**: Lógica de controle do álbum, gestos de arraste, som dinâmico e integração com API.
* **St.PageFlip API**: Biblioteca externa para simulação e renderização realista do folheamento físico tridimensional das páginas.
* **Web Audio API**: Para geração e síntese de áudio procedural e efeitos realistas de atrito de papel.

---

## 📂 Estrutura de Arquivos e Suas Funcionalidades

### 1. `index.html`
Define a marcação estrutural do site. É o esqueleto onde as páginas do álbum são estruturadas de `#0` (Capa) até `#7` (Contracapa). Ele abriga todos os slots (`sticker-slot`) onde as imagens das figurinhas e suas respectivas informações de id, nome e descrição são renderizadas, além de carregar os scripts necessários e os botões de navegação da interface.

### 2. `style.css`
A folha de estilos contendo o sistema de design visual do projeto:
* **Paleta de Cores**: Configurada por meio de variáveis customizadas no `:root` com tons futuristas de azul escuro, neon e preto.
* **Layouts**: Uso intenso de CSS Grid e Flexbox para organizar a grade das páginas e a grade interna das figurinhas.
* **Efeitos Especiais**: Animações de brilho de néon, efeito de texto *glitch* na capa, colagem de miniaturas flutuantes e estilização das bordas do livro.

### 3. `app.js`
A lógica e o comportamento interativo do frontend. Suas funções incluem:
* **Integração com Backend**: Faz requisições HTTP (`fetch`) para a API na porta `8000` (`http://localhost:8000/figurinhas`) buscando a lista de figurinhas ativas para preencher dinamicamente os slots correspondentes com imagens.
* **Configuração e Gestão do PageFlip**: Instancia e inicializa o componente `St.PageFlip`, configurando tamanhos mínimos/máximos, sombras e velocidade de transição.
* **Detecção de Gestos**: Implementa uma detecção de arraste nativa para cliques e gestos de toque (*touch events*) a fim de simular o folheamento do livro de forma realista.
* **Síntese de Som (Web Audio API)**: Cria efeitos sonoros em tempo real de papel roçando por meio de ruído branco modulado e filtros passa-banda, ativados no momento em que as páginas mudam de estado.
* **Controles do Usuário**: Gerencia ações de habilitar/desabilitar som, botões de anterior/próximo e atalhos de teclado (setas direcionais).

---

## 🚀 Como Executar o Projeto

1. Abra a pasta do projeto em um servidor local (como a extensão Live Server do VS Code ou seu próprio servidor web local).
2. Para carregar as fotos das figurinhas dinamicamente nos slots em vez de ver apenas os contornos cinzas, certifique-se de que a API do backend correspondente esteja rodando na porta `8000`.
   * Comando de exemplo para inicializar a API:
     ```bash
     cd backend/dia-3
     uvicorn main:app --reload
     ```
3. Abra `index.html` em seu navegador de preferência e interaja folheando as páginas!
