# Hallucination-Detector-App

A Hallucination Detection Tool powered by [uqlm](https://github.com/uqlm/uqlm), designed to identify whether outputs from Large Language Models (LLMs) are accurate or contain hallucinations.

## Features

- **Interactive Web App (Streamlit)**: User-friendly interface to analyze responses from LLMs.
- **Multiple Detection Methods**:
  - **Black-Box Scorer**: Assesses consistency of multiple model responses.
  - **White-Box Scorer**: Examines token probability confidence.
  - **LLM-as-a-Judge**: Uses other LLMs to judge the output for hallucination.
  - **Ensemble Scorer**: Combines several techniques for robust evaluation.
- **Supports Google Gemini Models**: Easily select between various Gemini LLMs.
- **Visual Confidence Scoring**: View bar charts and confidence indicators for each method.
- **Ground Truth Calibration**: Optionally provide correct answers for enhanced calibration.
- **API Key Management**: Securely input and manage your Gemini API key.

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/lasithadilshan/Hallucination-Detector-App.git
cd Hallucination-Detector-App
```

### 2. Install Requirements

It is recommended to use a Python virtual environment (Python 3.9+):

```bash
pip install -r requirements.txt
```

### 3. Set Up Environment Variables

Create a `.env` file in the project root and add your [Gemini API key](https://aistudio.google.com/app/apikey):

```
GEMINI_API_KEY=your_google_gemini_api_key_here
```

Alternatively, you can enter the key in the sidebar when running the app.

### 4. Run the App

```bash
streamlit run streamlit_app.py
```

## Usage

1. **Enter your Gemini API key** in the sidebar.
2. **Choose the LLM model** and hallucination detection method.
3. **Input a prompt** (or select from examples).
4. **Click "Generate and Score"** to analyze the LLM's response.
5. **Review the confidence scores and interpretations.**

### Example Prompts

- Factual: `What is the capital of France?`
- Fictional: `Tell me about Zorblaxians from Planet Xenu.`
- Mathematical: `What is the result of dividing 1 by 0?`

## Hallucination Detection Methods

- **Black-Box Scorer**: Generates multiple responses and checks their semantic similarity.
- **White-Box Scorer**: Analyzes model's internal confidence in its own outputs.
- **LLM-as-a-Judge**: Uses other LLMs to evaluate the output.
- **Ensemble Scorer**: Combines several scoring methods.

Higher scores (closer to 1.0) indicate higher confidence and lower likelihood of hallucination.

## Tech Stack

- [Python](https://www.python.org/)
- [Streamlit](https://streamlit.io/)
- [uqlm](https://github.com/uqlm/uqlm) (Uncertainty Quantification for Language Models)
- [LangChain](https://github.com/langchain-ai/langchain) for Gemini API integration
- [Plotly](https://plotly.com/python/) for visualizations
- [Pandas](https://pandas.pydata.org/) for data handling
- [dotenv](https://pypi.org/project/python-dotenv/) for environment variable management

## Requirements

See [requirements.txt](requirements.txt) for dependencies.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgements

- [uqlm](https://github.com/uqlm/uqlm) for providing hallucination detection tools.
- [Google Gemini](https://aistudio.google.com/app/apikey) for LLM API.
- [Streamlit](https://streamlit.io/) for the web app framework.

---
Feel free to open issues or contribute!
