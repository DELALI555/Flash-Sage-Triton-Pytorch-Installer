# Flash-Sage-Triton-Pytorch-Installer 🚀

<p align="center">
  <img src="https://raw.githubusercontent.com/Bliip-Studio/Flash-Sage-Triton-Pytorch-Installer/main/EasyInstall.png" alt="Win-AI-Toolkit Banner"/>
</p>

---

[![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=for-the-badge&logo=windows)](https://www.microsoft.com/windows)
[![Version](https://img.shields.io/badge/Version-12.8-blue.svg?style=for-the-badge)](https://github.com/YOUR_USERNAME/YOUR_REPO/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

The ultimate installer and environment manager for AI art on Windows. This toolkit provides a robust, step-by-step command-line wizard to help you flawlessly install and configure a complete Python environment with PyTorch, CUDA, and all the necessary dependencies for running applications like ComfyUI, Fooocus, and more.

## The Problem

Installing the correct versions of PyTorch, CUDA, Triton, and various attention libraries on Windows is a major challenge. Users often face cryptic errors, version mismatches, and frustrating dependency conflicts. This toolkit was built to solve that problem.

## ✨ Features

*   **Wizard-like Experience**: A simple, guided, step-by-step process that tells you exactly what to do at each stage.
*   **Resumable Installation**: If any step fails or requires a restart, you can simply run the script again and it will pick up exactly where you left off.
*   **Automated Prerequisite Checking**: Automatically checks for your NVIDIA GPU, CUDA Toolkit, and Visual Studio Build Tools.
*   **Intelligent Environment Detection**: Detects your exact Python, CUDA, and PyTorch versions to provide a personalized "cheat sheet" for downloading the correct, complex wheel files.
*   **Idempotent & Skippable Steps**: The script is smart. If it detects that a package (like PyTorch or FlashAttention) is already installed, it will skip that step automatically.
*   **Built for Reliability**: Engineered with a robust `GOTO`-based structure to avoid common Windows batch scripting bugs, ensuring it works even in paths with spaces.

## ⚙️ Prerequisites

Before you begin, ensure you have the following:

1.  **An NVIDIA GPU**: This toolkit is specifically designed for CUDA acceleration.
2.  **Windows 10 or 11**: The script is built for modern Windows environments.
3.  **Python 3.10 - 3.12**: You must have Python installed, and it must be added to your system's PATH during its installation. You can download it from the [official Python website](https://www.python.org/downloads/).
4.  **An Internet Connection**: Required for downloading packages.
5.  **Pre-Existing Venv**: If You have an existing venv where you would like to install and check, pleease change the name of the venv in the bat file.

## 🚀 How to Use

1.  **Download the Script**: Go to the [Releases page](https://github.com/YOUR_USERNAME/YOUR_REPO/releases) on this repository and download the latest `Win-AI-Toolkit.bat` file.
2.  **Create a Folder**: Create a new, empty folder with a simple path to serve as the home for your AI environment (e.g., `D:\AI-Toolkit`). **Place the `.bat` file inside this folder.**
3.  **Run the Script**: Double-click the `Win-AI-Toolkit.bat` file to start the process.
4.  **Follow the Instructions**: The script will guide you through every step. Read the on-screen prompts carefully.

## The Installation Process

The toolkit will walk you through the following resumable steps:

*   **Step 0: GPU Driver Check**: Verifies that `nvidia-smi` is working.
*   **Step 1: Create Virtual Environment**: Creates an isolated Python environment in a `.venv` folder.
*   **Step 2: Check Python Version**: Confirms your Python version.
*   **Step 3: Check for Visual Studio Build Tools**: Checks if the required C++ compiler tools are present.
*   **Step 4: Check for NVIDIA CUDA Toolkit**: Verifies that `nvcc` is installed and in your PATH.
*   **Step 5: Upgrade Pip**: Ensures you have the latest Python packaging tools.
*   **Step 6: Install PyTorch**: Guides you to get the correct installation command from the official PyTorch website.
*   **Step 7: Install Triton**: Installs the Windows-compatible version of Triton.
*   **Step 8: Install Attention Libraries**: Intelligently detects your environment to help you download the exact `sageattention` and `flash-attn` wheel files you need.
*   **Step 9: Final Verification**: Runs a final, robust check to ensure all key packages are installed and that PyTorch can communicate with your GPU.

## 🔧 Troubleshooting

*   **Script crashes with a `. was unexpected` error**: Ensure the script is located in a folder with a simple path (e.g., `D:\AI-Toolkit`). While the script is robust, extremely complex paths can sometimes cause issues.
*   **`'nvcc' is not recognized`**: This means the NVIDIA CUDA Toolkit is not in your system's PATH. This can happen if you forgot to restart after installing it. Close the script window, open a new one, and run the script again. If the problem persists, you may need to add it to your Windows Environment Variables manually.
*   **PyTorch Fails to Install**: Double-check the command you copied from the PyTorch website. Ensure it was copied completely and without any extra characters.

## 🛣️ Future Plans (Roadmap)

This toolkit provides the essential foundation. Future versions aim to build upon it with:

*   **Git Installation Check**: Verify that `git` is installed.
*   **A Central Launcher**: A simple `launch.bat` to easily start any of your installed applications.
*   Many other usefull Packages required to run Diffusion frontends.

## ❤️ Acknowledgements

This toolkit was developed through a rigorous process of testing, debugging, and feedback. A huge thank you to the open-source community and all the users whose real-world issues helped forge this script into the reliable tool it is today.

## License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
