# **MCP Series**

Welcome to the **MCP Playlist** repository!  

This playlist is designed to help you understand the **Model Context Protocol (MCP)** from the ground up — starting with what MCP is and how its JSON-RPC messages work, all the way to building your own servers, clients, and letting an LLM call your MCP tools.  
Each video walks you through real, practical examples so you can connect AI applications to tools and data in one consistent way.

---

## 🐍 **Install Python Using Miniconda / Miniforge**

To keep your AI projects clean and organized, it is recommended to use **conda environments**. Follow the steps below to install Miniforge and set up your environment.

---

### 🔗 **Download Miniforge for macOS (ARM64)**

Download from the official repository:  
https://github.com/conda-forge/miniforge/releases/latest/download/Miniforge3-MacOSX-arm64.sh

---

### 💻 **Install Miniforge**

Run the following commands:

```bash
chmod +x ~/Downloads/Miniforge3-MacOSX-arm64.sh
sh ~/Downloads/Miniforge3-MacOSX-arm64.sh
source ~/miniforge3/bin/activate
```

---

### 🧱 **Create a project-specific conda environment**

```bash
conda create --prefix ./env python=3.13
conda activate ./env
```

---

### 📦 **Install packages from requirements.txt**

```bash
pip install -r requirements.txt
```

---

### 🔑 **Set up your OpenAI API key**

Episode 4 uses an OpenAI model. Create a `.env` file in the project root:

```bash
OPENAI_API_KEY=your-api-key-here
```

---

### 🔍 **(Optional) MCP Inspector**

A visual debugger for MCP servers (requires Node.js):

```bash
npx @modelcontextprotocol/inspector python server_basic.py
```

Your MCP environment is ready to build powerful AI apps 🚀

---

# **📺 Playlist Breakdown**

### **0. What is MCP?** — `00_what_is_mcp.ipynb`

- Understanding the **Host → Client → Server** architecture and the three primitives: **tools, resources, prompts**.
- Looking under the hood at the plain **JSON-RPC messages** MCP uses.

### **1. Build Your First MCP Server** — `01_first_mcp_server.ipynb`

- Creating a server with `MCPServer` and turning Python functions into tools with `@mcp.tool()`.
- How **type hints** become the input schema and **docstrings** become the tool description, tested with a tiny stdio client.

### **2. Resources and Prompts** — `02_resources_and_prompts.ipynb`

- Exposing data with **resources** and reusable templates with **prompts**.
- Knowing **when to use a tool, a resource, or a prompt**.

### **3. Build a Reusable MCP Client** — `03_mcp_client.ipynb`

- Wrapping connection code into a small **helper client**: connect → initialize → list → call.
- Exploring **any MCP server** in one line.

### **4. Let an OpenAI Model Use Your MCP Tools** — `04_llm_with_mcp.ipynb`

- Passing your server's **tool list to an LLM** and letting it decide which tools to call.
- Building the **tool-calling loop** that apps like ChatGPT, Claude Desktop and Cursor use.

---

# **📄 requirements.txt**

```
mcp>=2
openai
python-dotenv
notebook
```

---

# **🤝 Contributing**

Got suggestions or improvements?  
Feel free to open an issue or submit a pull request.

---

# **📬 Stay Connected**

- [YouTube Channel](https://www.youtube.com/@yashjainio)
- [LinkedIn](https://www.linkedin.com/in/yashjainio)

---

Thank you for checking out the **MCP Playlist**!  
Happy building with AI 🚀
