**Knowledge Graph Builder for DataCatalog**

A powerful tool for automatically building Knowledge Graphs from Data Catalog metadata using Google's Gemini AI and LangChain. This project transforms textual schema descriptions into structured knowledge graphs that can be visualized or stored in Neo4j databases.

**Features**

    Automated KG Generation: Convert data catalog metadata to knowledge graphs using LLM
    Dual Storage Options: Visualize graphs as HTML files or store in Neo4j database
    Schema-Aware Processing: Define custom node types and relationships for consistent extraction
    Interactive Visualization: Generate beautiful, interactive HTML visualizations using pyvis
    Flexible Input: Handle various metadata formats and structures

**Prerequisites**

    Google Colab account (or local Python environment)
    Google AI Studio API key for Gemini models
    Neo4j database (optional, for persistent storage)

**Installation**

The notebook automatically installs required packages:

pip install --quiet langchain-community langchain-experimental langchain_google_genai json-repair
pip install --quiet neo4j  # Optional: for Neo4j integration
pip install --quiet pyvis  # Optional: for graph visualization

⚙️ Configuration
1. Google AI Setup

Store your Google AI API key in Google Colab's secret manager as pkst_apikey:

    os.environ["GOOGLE_API_KEY"] = userdata.get('pkst_apikey')
    llm = ChatGoogleGenerativeAI(model="gemini-2.5-flash-lite", temperature=0)

2. Neo4j Setup (Optional)

For database storage, configure Neo4j credentials :

    neo4jurl: Your Neo4j database URL
    neo4jusername: Database username
    neo4jpassword: Database password


📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

**Acknowledgments**

    LangChain: For the excellent graph transformation capabilities
    Google AI: For providing the Gemini models
    Neo4j: For graph database functionality
    Pyvis: For beautiful graph visualizations
