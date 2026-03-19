# Projeto AR - Tiranossauro 🦖

Um projeto de Realidade Aumentada (RA) interativo baseado na web. Esta aplicação utiliza a câmera do dispositivo para projetar um modelo 3D animado de um Tiranossauro Rex sobre um marcador físico, permitindo interações diretas através de toques na tela.

## 🚀 Funcionalidades

* **Rastreamento de Marcador (Marker-based AR):** Utiliza o marcador padrão "Hiro" para posicionar o modelo 3D de forma precisa no ambiente físico.
* **Animações Integradas:** Reproduz automaticamente de forma contínua (loop) as animações embutidas no arquivo `.glb` do Tiranossauro.
* **Interatividade via Gestos:**
  * **Toque Simples / Clique:** Aumenta o tamanho do dinossauro (escala 1.3x). Um novo toque o retorna ao tamanho original.
  * **Duplo Toque / Duplo Clique:** Rotaciona o modelo em 360 graus no próprio eixo.

## 🛠️ Tecnologias Utilizadas

* **[A-Frame](https://aframe.io/):** Framework web para criação de experiências 3D e de realidade virtual/aumentada.
* **[AR.js](https://ar-js-org.github.io/AR.js-Docs/):** Biblioteca leve para realidade aumentada na web, responsável pelo rastreamento da câmera e identificação do marcador.
* **A-Frame Extras:** Utilizado especificamente para o componente `animation-mixer`, que habilita a reprodução de clipes de animação do modelo GLTF/GLB.
* **HTML5 / JavaScript:** Estruturação da página e lógica de interação customizada (através do componente `gesture-tap`).

## ⚙️ Como Executar o Projeto

1. Faça o clone deste repositório para a sua máquina local.
2. Como o projeto utiliza acesso à câmera, os navegadores exigem que ele seja executado em um ambiente seguro (HTTPS) ou via `localhost` para evitar bloqueios de CORS.
   * **Localmente:** Acesse o link do deploy: (https://leomatias-trex.netlify.app/)  ou utilize uma extensão como o **Live Server** no VS Code.
   * **Nuvem:** Você pode realizar o deploy da aplicação estática em serviços de computação em nuvem (como um bucket no AWS S3).
3. Acesse a página `index.html` através de um navegador em seu smartphone ou computador com webcam.
4. Conceda as permissões solicitadas para uso da câmera.
5. Aponte a câmera para um **Marcador Hiro** (você pode imprimi-lo ou simplesmente abri-lo na tela de um outro dispositivo).
6. Interaja com o modelo renderizado clicando ou tocando na tela!

## 📁 Estrutura de Arquivos

* `index.html`: Arquivo principal contendo a cena A-Frame, configuração do AR.js e os scripts de interação em JavaScript.
* `tiranosaurus.glb`: Modelo 3D do dinossauro com animações embutidas. *(Certifique-se de que este arquivo esteja no mesmo diretório que o `index.html` caso altere a estrutura)*.
