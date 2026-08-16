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

### [CriptoBitwise](https://github.com/Caetanoag/cripto-bitwise)
Uma biblioteca criptográfica autoral em JavaScript puro que integra múltiplas técnicas de segurança (obfuscação, bitwise, CBC, PRNG não-linear) para proteger mensagens. *Desenvolvida como um estudo de caso educacional e não recomendada para uso em produção.*

* **Tech Stack:** JavaScript Puro (ES6+), BigInt, Web Crypto API (`crypto.getRandomValues`).
* **Arquitetura-Chave:**
  * **PRNG Próprio (Xorshift128 Modificado):** Gerador de números pseudoaleatórios modificado e não-linear que integra soma de estados, rotação bitwise dinâmica e aritmética modular para resistir a ataques de álgebra linear.
  * **Derivação e Extensão de Chave (Key Stretching):** Utiliza um hash derivado de 128 bits (`gerarHash`) processado em 100.000 iterações de FNV-1a com `BigInt`, combinado a um Vetor de Inicialização (IV) aleatório de 48 bytes para prevenir colisões por rainbow tables.
  * **Pipeline de Criptografia:** Implementa um processo em camadas, iniciando com uma cifra de bloco em modo **Cipher Block Chaining (CBC)**, seguida por obfuscação bitwise através da **injeção dinâmica de bits de lixo**, resultando em um texto cifrado altamente não-determinístico.
  * **Autenticação (Encrypt-then-MAC):** Gera um MAC hexadecimal de 32 caracteres a partir do texto cifrado final para verificação de integridade. Inclui uma função de **comparação em tempo constante** (`constantTimeCompare`) para mitigar ataques de tempo (timing attacks) durante a descriptografia.

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
