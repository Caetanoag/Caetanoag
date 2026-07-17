# Caetano Gonçalves
Estudante de Desenvolvimento de Software e Web | Sistemas, IoT e Deep Learning

## Sobre Mim
Estou estudando Desenvolvimento Web no IFRS. Embora meu curso formal seja focado em aplicações web full-stack, sou um estudante autodidata movido por sistemas de baixo nível, hardware e IA. 

* **Cibersegurança e Infraestrutura:** Focado em redes, criptografia e DevOps. Desenvolvi um algoritmo criptográfico próprio e gerencio ativamente um servidor caseiro utilizando Docker e Tailscale para acesso remoto seguro.
* **IoT e Sistemas Embarcados:** Trabalhei por dois anos no laboratório afiliado ao FabLab no campus, ganhando experiência prática com microcontroladores utilizando os frameworks ESP-IDF e Arduino.
* **Deep Learning:** Certificado pelo NVIDIA Deep Learning Institute (DLI). Construí redes neurais do zero, treinei modelos e ajustei hiperparâmetros, com uma base sólida na matemática por trás dos sistemas.

---

## Habilidades

| Categoria | Tecnologias |
| :--- | :--- |
| **Linguagens** | JavaScript, TypeScript, Go, C, C++, OdinLang |
| **Desenvolvimento Web** | React, ExpressJS, HTML5, CSS3, WebAssembly (Wasm), Web Workers |
| **DevOps e Infra** | Docker, Tailscale, Linux (Servidor Caseiro) |
| **Embarcados e IoT** | ESP-IDF, Arduino Framework, Emscripten, Microcontroladores |

---

## Projetos em Destaque

### [Vectra](https://github.com/Caetanoag/Vectra)
Uma engine leve de renderização 2D e álgebra linear para o navegador, construída sobre a API HTML Canvas utilizando TypeScript.

* **Tech Stack:** TypeScript, HTML5 Canvas.
* **Arquitetura-Chave:**
  * **Motor Matemático Próprio:** Primitivas vetoriais 2D imutáveis (`Vector2`) e matrizes de transformação 3x3 (`Matrix3`) para manipulação de transformações afins.
  * **Grafo de Cena Hierárquico:** Sistema de `Transform` com suporte a hierarquia de objetos (pai/filho), computando matrizes globais de forma encadeada.
  * **Gerenciamento de Input por Varredura:** Um `InputManager` baseado em frames que abstrai interações de mouse, toque e teclado para aplicações em tempo real.
  * **Renderizador de Alto Nível:** Encapsula o contexto nativo do canvas, oferecendo uma API fortemente tipada para geometria, texto e gerenciamento de estado.

---

### [Strong Password Validator](https://github.com/Caetanoag/Strong-password-validator) (WIP / Pesquisa)
Um estimador de complexidade de senhas multithread e simulador de brute-force que conecta C++ ao navegador para avaliar a força de criptografias.

* **Tech Stack:** C++, WebAssembly (Wasm), Emscripten, Web Workers, JavaScript (BigInt).
* **Arquitetura-Chave:**
  * **Matemática Combinatória e BigInt:** Mapeia strings para sua ordem lexicográfica exata em um sistema de numeração bijetivo de base 71 usando `BigInt`, prevendo o espaço de permutação total antes da execução.
  * **Benchmark Dinâmico:** Executa um benchmark em tempo de execução no hardware assim que inicializado para calcular as operações por milissegundo da CPU local, alimentando um modelo preditivo de tempo de quebra.
  * **Loops Assíncronos em Lotes:** Executa computações Wasm em lotes de 1.000.000 de passos por frame dentro de um Web Worker. Utiliza um padrão de recursão assíncrona (`setTimeout`) para manter a execução não-bloqueante e permitir sinais de interrupção de thread.

---

### [3D Rendering Engine](https://github.com/Caetanoag/3D-Rendering-Engine) (Pesquisa / WIP)
Um renderizador software wireframe 3D leve construído do zero (first principles) usando JavaScript puro e a API Canvas 2D.

* **Tech Stack:** Vanilla JavaScript (ES6+), HTML5 Canvas.
* **Arquitetura-Chave:**
  * **Biblioteca Própria de Álgebra Linear:** Implementa armazenamento bruto de `Matrix` e algoritmos de transformação (`MatrixMath`) do zero, lidando com multiplicação padrão de matrizes, transposição e produtos Hadamard.
  * **Matemática de Pipeline Gráfico:** Processa manualmente transformações de vértices 3D usando matrizes de rotação dos eixos X e Y, juntamente com translações de coordenadas 3D.
  * **Projeção de Perspectiva:** Simula profundidade e Campo de Visão (FoV) através de mecânicas de divisão analítica (`fov / (fov + z)`), projetando ambientes 3D em um viewport de tela 2D.
  * **Escalonamento Baseado em Centroide:** Computa dinamicamente centroides geométricos para malhas poliédricas arbitrárias para isolar o escalonamento uniforme em relação ao centro de massa do objeto.

---

## Contato
* Email: caetanogoncalves@proton.me
