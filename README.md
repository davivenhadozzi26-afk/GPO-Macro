# GPO-Macro
Computer Vision Automation

![Python](https://img.shields.io/badge/python-3.10+-blue.svg)
![Status](https://img.shields.io/badge/status-stable-green.svg)
![UI](https://img.shields.io/badge/UI-Tkinter-black.svg)

**GPO Macro** é uma ferramenta de automação de alta performance desenvolvida em Python, focada na otimização de ciclos no modo Battle Royale do Grand Piece Online (Roblox). O projeto utiliza visão computacional para tomada de decisão em tempo real e emulação de hardware para interação com o ambiente 3D.

## 🚀 Diferenciais Técnicos

* **Sentinel Vision:** Diferente de macros baseados em tempo, o Sentinel utiliza reconhecimento de imagem (OpenCV/PyAutoGUI) para identificar o fim de partidas e estados do servidor (Match Found).
* **Hardware Emulation:** Utiliza a biblioteca `pydirectinput` para enviar comandos de entrada de baixo nível (Scancodes), ignorando bloqueios comuns de APIs de entrada de software.
* **Safe Loading Logic:** Implementa buffers de segurança de 105s e loops de espera dinâmicos para suportar variações de latência de rede e carregamento de assets.
* **Visual Debug GUI:** Interface intuitiva desenvolvida em Tkinter com feedback em tempo real de coordenadas mapeadas e contador de ciclos concluídos.

## 🛠️ Tecnologias Utilizadas

* **Python 3.10+**
* **PyAutoGUI / OpenCV:** Reconhecimento de padrões e visão computacional.
* **PyDirectInput:** Emulação de inputs de hardware para jogos.
* **Pynput:** Gerenciamento de eventos de mouse para calibração.
* **Keyboard:** Hooks globais para Hotkeys (F1/F2).
* **Tkinter:** Interface gráfica customizada.

## 📋 Como Usar

1.  **Instalação:**
    ```bash
    pip install -r requirements.txt
    ```
2.  **Calibração:**
    - Execute o script e utilize os botões `MAP` para registrar as coordenadas de interface no seu monitor.
    - O sistema salvará automaticamente em um arquivo `config.json`.
3.  **Inputs Visuais:**
    - Certifique-se de que as imagens de referência (`btn_open.png`, `btn_continue.png`, `match_found.png`) estão na pasta raiz e correspondem à sua resolução de tela.
4.  **Execução:**
    - **F1:** Inicia o ciclo de automação (Start).
    - **F2:** Interrupção de emergência (Kill-switch).

## 🧠 Visão de Engenharia

Este projeto foi desenvolvido com foco em **estabilidade e escalabilidade**. A arquitetura separa a lógica de interface (Main Thread) da lógica de execução (Worker Thread), garantindo que a GUI permaneça responsiva mesmo durante processos intensivos de busca visual.

---
*Aviso: Este software é um estudo técnico de automação e visão computacional. O uso em ambientes online deve respeitar os termos de serviço das plataformas.*
