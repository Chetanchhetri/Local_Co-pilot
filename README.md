# Local Copilot 🚀
A lightning-fast, 100% offline, privacy-first AI coding assistant built directly into VS Code. Powered by local LLMs via Ollama, this extension provides real-time ghost text, a multi-modal chat agent, and a unique "Talking Teacher" to explain complex code.

✨ Features
Real-Time Ghost Text: Lightning-fast, line-by-line code autocomplete powered by Qwen 2.5 Coder.

Agent Chat Sidebar: Ask questions, generate code, and inject solutions directly into your editor with 1-click "Apply" buttons.

Pro Mode Toggle: Instantly switch between fast, lightweight models and heavy reasoning models depending on the complexity of your task.

The Talking Teacher: Highlight code and get a conversational, spoken-word tutoring session explaining the logic behind the code.

Multi-Modal Support: Attach images or PDF documents directly into the chat for context.

Right-Click Context Menus: Highlight any code, right-click, and instantly select Explain Code, Fix Bugs, or Generate Tests.

🛠️ Step 1: System Requirements & Setup
Because this extension runs entirely on your local machine, you need to install the AI engine and the specific models the extension uses.

1. Install Ollama
Ollama is the engine that runs the AI models locally.

Download and install it from: https://ollama.com/

Once installed, ensure the Ollama app is running in your system tray/background.

2. Download the Required Models
Open your terminal (PowerShell, Command Prompt, or Mac Terminal) and run the following commands to download the models required by Local Copilot:

The Autocomplete & Standard Chat Model (Super Fast):

Bash
ollama pull qwen2.5-coder:1.5b


The Teacher Model (Conversational):

Bash
ollama pull phi3:latest


The Pro Mode Model (Heavy Reasoning):

Bash
ollama pull qwen3.5:9b


(Note: Ensure your Ollama server is running on 127.0.0.1:11434 before using the extension.)

📦 Step 2: Packaging & Installation
To install this extension permanently into VS Code, you must package it into a .vsix file.

1. Install the VS Code Packager
Open your terminal and install the official packager globally:

Bash
npm install -g @vscode/vsce
2. Package the Extension


Navigate to your extension's project folder in your terminal and run:

Bash
vsce package


Note: If prompted about a missing repository field, type y to continue. This command will generate a file named local-copilot-0.3.0.vsix in your folder.

3. Install in VS Code
Open VS Code.

Go to the Extensions view (Ctrl+Shift+X or Cmd+Shift+X).

Click the "..." (Views and More Actions) menu at the top right of the Extensions panel.

Select "Install from VSIX..."

Locate and select the local-copilot-0.3.0.vsix file you just generated.

🚀 Step 3: How to Use
👻 Ghost Text Autocomplete
Simply start typing in any code file. If you pause for 500ms, the AI will predict the next chunk of code.

Press Tab to accept the suggestion.

You can toggle this feature on/off using the robot icon $(hubot) in your bottom right Status Bar.

💬 Agent Chat
Click the robot icon in the left Activity Bar to open the Local Copilot sidebar.

Ask questions, or click the ➕ icon to attach PDFs and Images.

Hover over any generated code blocks to reveal the "Apply" and "Copy" buttons.

🧑‍🏫 The Talking Teacher
Switch to the TEACHER tab in the sidebar.

Highlight a confusing block of code in your editor and click "Explain My Code".

The AI will act as a tutor, explaining the concepts conceptually. You can ask follow-up doubts using the input box at the bottom.

🖱️ Right-Click Actions
Highlight any code in your editor, right-click, and select from the menu:

Copilot: Explain Code

Copilot: Fix Bugs

Copilot: Generate Tests
