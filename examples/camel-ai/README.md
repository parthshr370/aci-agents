# CAMEL AI with ACI Integration Examples

This repository contains two different approaches to integrate ACI.dev with CAMEL AI agents:

1. **Direct ACI Toolkit Integration** (`aci_toolkit_camel.py`)
2. **MCP Server Integration** (`aci_mcp_camel.py`)

## 🚀 Features

- **Two Integration Approaches**: Choose between direct ACI toolkit usage or MCP server integration
- **Multiple AI Tools**: Access to BRAVE_SEARCH, GITHUB, and ARXIV through ACI
- **Gemini Model Integration**: Uses Google's Gemini 2.5 Pro model for AI responses
- **Error Handling**: Comprehensive error handling with detailed traceback information

## 📁 Project Structure

```
.
├── aci_toolkit_camel.py    # Direct ACI Toolkit integration
├── camel_mcp_aci.py        # MCP server integration approach
├── create_config.py        # MCP configuration generator
├── README.md               # This file
└── env.example            # Environment variables template
```

## 🛠️ Setup

### Prerequisites

- Python 3.10+
- ACI API access
- Google Gemini API access

### Installation

1. **Clone the repository**:

   ```bash
   git clone https://github.com/aipotheosis-labs/aci-agents
   cd agents/examples/camel-ai/
   ```

2. **Install dependencies**:

   ```bash
   uv pip install camel-ai python-dotenv rich aci-mcp
   ```

3. **Set up environment variables**:
   ```bash
   cp env.example .env
   # Edit .env with your API keys and configuration
   ```

## 🔧 Configuration

### Environment Variables

Create a `.env` file with the following variables:

- `ACI_API_KEY`: Your ACI API key
- `GOOGLE_API_KEY`: Your Google Gemini API key
- `LINKED_ACCOUNT_OWNER_ID`: Your linked account owner ID (e.g., GitHub username)

You can get these from:

- **ACI API Key**: Configure your apps and get your key at [ACI Platform](https://platform.aci.dev/apps)
- **Google API Key**: Get your Gemini API key from [Google AI Studio](https://aistudio.google.com/)

## 🎯 Usage

### Approach 1: Direct ACI Toolkit Integration

This approach uses the ACI toolkit directly within the CAMEL AI framework:

```bash
python aci_toolkit_camel.py
```

**Features**:

- Direct integration with ACI toolkit
- Simpler setup and configuration
- Immediate access to ACI tools
- Rich console output with progress indicators

### Approach 2: MCP Server Integration

This approach uses MCP (Model Context Protocol) servers to provide ACI functionality:

```bash
python camel_mcp_aci.py
```

**Features**:

- Uses MCP protocol for tool integration
- More modular and extensible architecture
- Interactive user input for queries
- Automatic configuration generation
- Support for multiple MCP servers

## 🔧 Troubleshooting

### Common Issues

1. **Missing API Keys**: Ensure all required environment variables are set in your `.env` file
2. **ACI MCP Installation**: Make sure `aci-mcp` is properly installed for MCP approach
3. **Network Issues**: Check internet connectivity for API calls
4. **Permission Issues**: Ensure proper permissions for file creation (config.json)

### Debug Mode

Both scripts include comprehensive error handling with traceback information for debugging.

## Links

- [CAMEL AI](https://github.com/camel-ai/camel) - Multi-agent framework
- [ACI](https://github.com/aci-labs) - AI Compute Infrastructure
