# OPEN AI CLI TOOL (CLAI)

A lightweight, zero-dependency Bash script to query OpenAI's GPT models directly from your terminal. It uses `curl` for API requests and `jq` for robust JSON parsing and output formatting.

## Prerequisites

Ensure you have the following installed:
* **curl**
* **jq** (Command-line JSON processor)

## ⚙️ Configuration

You need an OpenAI API Key to use this tool. You can configure it in two ways:

### Option 1: Environment Variable (Recommended)
Add your key to your shell profile (`~/.bashrc` or `~/.zshrc`):

```bash
export OPENAI_API_KEY="your-api-key-here"
```
**Please remember to change ```.bashrc``` permissions so only you can access your API Key**
```bash
chmod 600 ~/.bashrc
```

### Option 2: Secret File
Alternatively, create a hidden file in your home directory containing only the key:
```bash
echo "your-api-key-here" > ~/.openai_key
chmod 600 ~/.openai_key
```
## 📦 Installation

To use the script globally (e.g., by typing clai), choose one of the methods below.

### Method A: With Admin Privileges (sudo)
Recommended for system-wide availability.

1. Rename and move the script to /usr/local/bin:
   ```bash
   sudo mv clai /usr/local/bin/clai
   ```
2. Make it executable:
   ```bash
   sudo chmod +x /usr/local/bin/clai
   ```
### Method B: Without Admin Privileges
Recommended for shared servers (e.g., university labs) or personal preference.

1. Create a local bin directory:
   ```bash
   mkdir -p ~/bin
   ```
2. Move the script there:
   ```bash
   mv clai ~/bin/clai
   chmod +x ~/bin/clai
   ```
3. Add the directory to your PATH in ~/.bashrc:
   ```bash
   echo 'export PATH="$HOME/bin:$PATH"' >> ~/.bashrc
   source ~/.bashrc
   ```
## 🚀 Usage

Run the script followed by your prompt in quotes:
```bash
clai "Write a bash function to list all empty files in a directory"
```
