# Hanomi MAS

Hanomi MAS (Multi-Agent System) is an advanced multi-agent platform for analyzing mechanical parts images and generating actionable insights. The system leverages state-of-the-art frameworks such as **CrewAI**, **LangChain**, and **LangGraph**, alongside a dedicated image processing agent, to provide comprehensive analysis and diagnostics for mechanical components.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Architecture](#architecture)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

In modern industrial and manufacturing settings, accurate and timely analysis of mechanical parts is crucial. Hanomi MAS addresses this need by combining:

- **CrewAI** for orchestrating multi-agent interactions.
- **LangChain** to build natural language reasoning pipelines.
- **LangGraph** for creating and visualizing knowledge graphs.
- An **Image Agent** that processes and extracts critical features from mechanical parts images.

Together, these components enable automated diagnostics, predictive maintenance insights, and enhanced decision-making for personal and enterprise-level applications.

## Features

- **Multi-Agent Coordination:**  
  Integrates multiple specialized agents to perform different tasks, ensuring a modular and scalable approach.

- **Image Analysis:**  
  Utilizes an image agent to process and analyze images of mechanical parts, extracting key features for further evaluation.

- **Natural Language Insights:**  
  Leverages LangChain to generate human-readable insights and recommendations based on the analyzed data.

- **Knowledge Graph Construction:**  
  Employs LangGraph to represent relationships and dependencies between various mechanical components and issues.

- **Extensible & Customizable:**  
  Designed for easy integration with additional data sources, custom agents, and further enhancements as needed.

## Architecture

Hanomi MAS is built on a layered architecture where each component specializes in a distinct task:

1. **Data Ingestion:**  
   - Retrieves images and metadata from user uploads or external APIs.
2. **Image Agent:**  
   - Processes images to detect and extract features of mechanical parts.
3. **Language Processing Pipeline:**  
   - Uses LangChain to interpret image data, generating contextual insights.
4. **Knowledge Graph Module:**  
   - Constructs and updates a dynamic knowledge graph via LangGraph, mapping interdependencies.
5. **Agent Orchestration:**  
   - CrewAI manages agent communication and workflow coordination, ensuring a seamless end-to-end process.

## Installation

### Prerequisites

- Python 3.8 or higher
- [pip](https://pip.pypa.io/)
- Redis (if using asynchronous task queues with Celery)
- Git

### Clone the Repository

```bash
git clone https://github.com/AGAMPANDEYY/Hanomi_MAS.git
cd Hanomi_MAS
```

# Hanomi Multi-Agent System

## Install Dependencies
Ensure you have a virtual environment activated, then install the required packages:

```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
pip install -r requirements.txt
```

## Usage

### Running the Application
Depending on your configuration, you can start the multi-agent system by running the main entry point:

```bash
python main.py
```

### Scheduling & Automation
If your project uses Celery for task management, start the Celery worker with:

```bash
celery -A hanomi_mas worker --loglevel=info
```

### Workflow Integration with n8n
To automate content generation and data processing, integrate the system with n8n workflows by setting up appropriate API endpoints and triggers as documented in the n8n docs.

## Project Structure
Below is an overview of the main directories and files:

```bash
Hanomi_MAS/
├── agents/              # Contains various agent implementations (e.g., image agent, language agents)
├── core/                # Core logic for orchestrating the multi-agent system
├── integrations/        # Modules for CrewAI, LangChain, LangGraph, and external APIs
├── data/                # Sample data, images, and test datasets
├── tests/               # Unit and integration tests for the system
├── requirements.txt     # Python dependencies
├── main.py              # Main entry point for the application
└── README.md            # Project documentation
```

## Contributing
Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/YourFeature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to your branch: `git push origin feature/YourFeature`
5. Open a Pull Request detailing your changes and improvements

For major changes, please open an issue first to discuss what you would like to change.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.


