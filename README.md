# Alura Album - Copa do Mundo Tech

Este projeto é um **Álbum de Figurinhas Virtual Interativo** que homenageia grandes personalidades da tecnologia, tanto internacionais quanto nacionais, divididos em categorias como Inteligência Artificial, Python, Banco de Dados, Sistemas Operacionais e Celebridades Tech do Brasil. O projeto foi desenvolvido como parte da Imersão da Alura.

---

## 🎯 Objetivo do Projeto

O objetivo principal é criar uma experiência rica, imersiva e visualmente impressionante para colecionar figurinhas virtuais de gigantes da tecnologia. O álbum simula a sensação física de folhear um livro através de animações fluidas de dobra de páginas, efeitos sonoros gerados dinamicamente e carregamento dinâmico de figurinhas via integração com uma API backend.

---

## 🚀 Principais Funcionalidades

- **Efeito Page-Flip Realista**: Navegação interativa simulando o folhear de páginas reais (usando a biblioteca `page-flip`), com suporte a arraste com o mouse/dedo e teclas direcionais do teclado.
- **Efeitos de Som Dinâmicos**: Geração de som de papel virando em tempo real utilizando a *Web Audio API* (sem necessidade de arquivos de áudio pesados).
- **Carregamento Dinâmico de Figurinhas**: Integração assíncrona com uma API backend para buscar as URLs das imagens e preencher os slots correspondentes no álbum de forma automática.
- **Visual Premium e Moderno**: Interface futurista com tema escuro (*dark mode*), efeitos de iluminação néon, animações de micro-interações e efeitos de *glitch* na capa.

---

## 📂 Estrutura de Arquivos e Suas Funcionalidades

O projeto é composto por três arquivos principais na pasta raiz:

### 1. 📄 [index.html](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/index.html)
Define toda a estrutura semântica da aplicação. 
* Contém a estrutura do livro (`.flip-book`) e a divisão de cada uma das páginas (da Capa à Contracapa).
* Organiza os slots numerados (`#01` a `#30`) com os nomes e descrições dos respectivos pioneiros da tecnologia.
* Inclui botões para navegação manual e controle de som (mudo/ativado).
* Importa a biblioteca de efeitos `page-flip` via CDN, além de vincular a folha de estilos e o script principal.

### 2. ⚡ [app.js](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/app.js)
Controla a lógica, a interatividade e a integração de dados da aplicação.
* **Integração com a API**: A função [`preencherFigurinhas()`](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/app.js#L12) faz um `fetch` para o servidor backend local (`http://localhost:8000/figurinhas`) para obter os dados das figurinhas e colá-las nos slots corretos.
* **Inicialização e Controle do Livro**: Configura a biblioteca `St.PageFlip` com parâmetros de redimensionamento e transições personalizadas.
* **Simulador de Som**: A função [`playPaperTurnSound()`](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/app.js#L215) gera dinamicamente ruído branco filtrado por envelopes de volume e frequência para simular o atrito de folhas de papel sendo viradas.
* **Navegação**: Escuta eventos de botões, toques em tela e teclas direcionais (`ArrowLeft` e `ArrowRight`) para navegar pelas páginas do álbum.

### 3. 🎨 [style.css](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/style.css)
Responsável por toda a estilização e identidade visual da aplicação.
* Define variáveis globais CSS (`:root`) para uma paleta de cores consistente de azul espacial e tons escuros.
* Cria o layout tridimensional do álbum e o comportamento de transição suave das páginas.
* Estiliza os slots das figurinhas, incluindo o visual brilhante especial dos slots raros (*special slots*).
* Adiciona efeitos modernos, como o efeito *glitch* na tipografia do título da capa, efeitos de brilho em neon (*glow*) e micro-animações nas interações com botões.

---

## 🛠️ Como Executar o Projeto

1. Certifique-se de que a API backend está em execução no endereço `http://localhost:8000`.
   *(Geralmente inicializada via FastAPI: `uvicorn main:app --reload` dentro da pasta do backend)*.
2. Abra o arquivo [index.html](file:///d:/dowload%20crome/i-arq-ia-alura-album-main/i-arq-ia-alura-album-main/index.html) diretamente em seu navegador web (ou utilizando extensões como o Live Server no VS Code).
3. Use os botões laterais ou as setas do teclado para folhear o álbum e colecione todas as figurinhas!

---
## lingugens utilizadas
python
javascript
html
css
e bibliotecas python :fastApi e Uvicorn
