# Caetano Gonçalves
Software and Web Development Student | Systems, IoT & Deep Learning

[![Português](https://img.shields.io/badge/Language-Português-333333?style=flat-square)](./README.pt.md)

## About Me
I am studying Web Development at IFRS. While my formal coursework focuses on full-stack web applications, I am a self-learner driven by low-level systems, hardware, and AI.

* **Cybersecurity & Infrastructure:** Focused on networking, cryptography, and DevOps. Developed a custom cryptographic algorithm and actively manage a home server using Docker and Tailscale for secure remote access.
* **IoT & Embedded Systems:** Worked for two years at the FabLab-affiliated laboratory on campus, gaining hands-on experience with microcontrollers using ESP-IDF and Arduino frameworks.
* **Deep Learning:** Certified by the NVIDIA Deep Learning Institute (DLI). Built neural networks from scratch, trained models, and tuned hyperparameters, backed by a solid understanding of the underlying mathematics.

---

## Skills

| Category | Technologies |
| :--- | :--- |
| **Languages** | JavaScript, TypeScript, Go, C, C++, OdinLang |
| **Web Development** | React, ExpressJS, HTML5, CSS3, WebAssembly (Wasm), Web Workers |
| **DevOps & Infra** | Docker, Tailscale, Linux (Home Server) |
| **Embedded & IoT** | ESP-IDF, Arduino Framework, Emscripten, Microcontrollers |

---

## Featured Projects

### [Vectra](https://github.com/Caetanoag/Vectra)
A lightweight 2D rendering and linear algebra engine for the browser, built on top of the HTML Canvas API using TypeScript.

* **Tech Stack:** TypeScript, HTML5 Canvas.
* **Key Architecture:**
  * **Custom Math Engine:** Built-in immutable 2D vectors (`Vector2`) and 3x3 transformation matrices (`Matrix3`) for handling affine transformations.
  * **Hierarchical Scene Graph:** A `Transform` system supporting parent-child object hierarchies, computing world matrices down the chain.
  * **Polled Input Management:** A frame-based `InputManager` that abstracts mouse, touch, and keyboard interactions for real-time applications.
  * **High-Level Renderer:** Encapsulates the native canvas context, offering a strongly-typed API for geometry, text, and state management.

---

### [CriptoBitwise](https://github.com/Caetanoag/cripto-bitwise)
A custom pure JavaScript cryptographic library that integrates multiple security techniques (obfuscation, bitwise, CBC, non-linear PRNG) to protect messages. *Designed as an educational case study and not for production use.*

* **Tech Stack:** Pure JavaScript (ES6+), BigInt, Web Crypto API (`crypto.getRandomValues`).
* **Key Architecture:**
  * **Custom PRNG (Xorshift128 Modified):** Developed a modified, non-linear Xorshift128 pseudo-random number generator that integrates state addition, dynamic bitwise rotation, and modular arithmetic to resist linear algebra attacks.
  * **Key Derivation & Stretching:** Employs a derived 128-bit hash (`gerarHash`) using 100,000 iterations of FNV-1a with `BigInt`, combined with a randomly generated 48-byte Initialization Vector (IV) to prevent rainbow table collisions.
  * **Encryption Pipeline:** Implements a multi-layered process, starting with a block cipher in **Cipher Block Chaining (CBC)** mode, followed by bitwise obfuscation through dynamic **garbage bit injection**, resulting in a highly non-deterministic ciphertext.
  * **Authentication (Encrypt-then-MAC):** Generates a 32-character hexadecimal MAC from the final ciphertext for message authentication. Critically, it includes a **constant-time comparison** function (`constantTimeCompare`) to mitigate timing attacks during decryption.

---

### [3D Rendering Engine](https://github.com/Caetanoag/3D-Rendering-Engine) (Research / WIP)
A lightweight 3D software wireframe renderer built from first principles using vanilla JavaScript and the Canvas 2D API.

* **Tech Stack:** Vanilla JavaScript (ES6+), HTML5 Canvas.
* **Core Architecture:**
  * **Custom Linear Algebra Library:** Implements raw `Matrix` storage and transformation algorithms (`MatrixMath`) from scratch, handling standard matrix multiplication, transposition, and Hadamard products.
  * **Graphics Pipeline Mathematics:** Manually processes 3D vertex transformations using X and Y axis rotation matrices alongside 3D coordinate translations.
  * **Perspective Projection:** Simulates depth and Field of View (FoV) through analytical division mechanics (`fov / (fov + z)`), projecting 3D environments onto a 2D screen viewport.
  * **Centroid-Based Scaling:** Dynamically computes geometric centroids for arbitrary polyhedral meshes to isolate uniform scaling relative to the object's center of mass.

---

## Contact
* Email: caetanogoncalves@proton.me
