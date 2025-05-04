# Chainlit Demo Project

A demo project showcasing the integration of Chainlit with OpenAI's GPT-4 Vision API for image analysis and chat functionality.

## Features

- Interactive chat interface using Chainlit
- Image analysis capabilities using OpenAI's GPT-4 Vision API
- Support for both text and image-based conversations
- Message history tracking for context-aware responses
- Streaming responses for real-time interaction

## Prerequisites

- Python 3.8 or higher (for local development)
- OpenAI API key
- Virtual environment (recommended for local development)
- Docker and Docker Compose (for containerized deployment)

## Setup

### Local Development

1. Clone the repository:
```bash
git clone <repository-url>
cd chainlit_demo
```

2. Create and activate a virtual environment:
```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows, use: .venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Set up environment variables:
Create a `.env` file in the project root and add your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

### Docker Deployment

1. Clone the repository:
```bash
git clone <repository-url>
cd chainlit_demo
```

2. Set up environment variables:
Create a `.env` file in the project root and add your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

3. Build and start the container:
```bash
docker compose up --build
```

To run in detached mode (in the background):
```bash
docker compose up -d
```

To stop the container:
```bash
docker compose down
```

## Running the Application

### Local Development
1. Start the Chainlit application:
```bash
chainlit run app.py
```

2. Open your web browser and navigate to the URL shown in the terminal (typically http://localhost:8000)

### Docker Deployment
The application will be automatically available at http://localhost:8000 after starting the container.

## Usage

- **Text Chat**: Simply type your message in the chat interface and press enter
- **Image Analysis**: Upload an image and ask questions about it
- The application maintains conversation history for context-aware responses
- Responses are streamed in real-time for a better user experience

## Configuration

The application uses the following default settings:
- Model: GPT-4 Vision
- Temperature: 0.4
- Max Tokens: 500

These settings can be modified in the `app.py` file under the `model_kwargs` dictionary.

## Dependencies

The project uses the following main dependencies:
- Chainlit: For the chat interface
- OpenAI: For GPT-4 Vision API integration
- Python-dotenv: For environment variable management

See `requirements.txt` for the complete list of dependencies.

## Docker Configuration

The project includes Docker configuration for containerized deployment:
- `Dockerfile`: Defines the container image using Python 3.11
- `docker-compose.yml`: Configures the service, ports, and environment variables
- `.dockerignore`: Specifies files to exclude from the Docker build

## License

[Add your license information here]
