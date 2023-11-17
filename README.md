# MultiLingual Sentiment Analyzer

[![License](https://img.shields.io/github/license/Bella1i/MLSA)](https://github.com/Bella1i/MLSA/blob/master/LICENSE)
![Python](https://img.shields.io/badge/python-3.8+-blue.svg)

Multitask Sentiment Analysis Powered by GPT-3.5

![Sentiment Analysis](https://github.com/Bella1i/MLSA/assets/87021559/56e39a24-199c-4299-bf09-547ac8368892)
![Analysis Results](https://github.com/Bella1i/MLSA/assets/87021559/e8ece483-5534-4267-afe2-3bc197bd613e)

## Overview
The MultiLingual Sentiment Analyzer is a comprehensive system designed to analyze user feedback on products and services. Leveraging the power of GPT-3.5, this tool extracts sentiment orientation, intensity, intentions, keywords, and other crucial insights from user comments. It supports multiple languages, making it versatile for global applications. This project is ideal for analyzing various types of user feedback, such as suggestions, complaints, and bug reports, helping businesses better understand their customers and improve their offerings.

## Features
- **Sentiment Analysis**: Detects the sentiment orientation (positive, neutral, negative) and intensity of user comments.
- **Intention Recognition**: Identifies the purpose behind user comments (e.g., advertisement issues, refund requests).
- **Keyword Extraction**: Extracts significant phrases and words from user feedback.
- **Multi-language Support**: Capable of analyzing comments in various languages.

## API Endpoint
Make a POST request to analyze a review:
```
http://xxx:8800/service/review_analysis
```

## Input Data Example
Here's an example of the JSON input for the analysis:
```json
{
   "commentId": 1,
   "content": "Ads won't load, the game is always lagging; I'm planning to uninstall it, please issue a refund."
}
```

## Output Data Example
The system provides the following JSON output:
```json
{
    "commentId": 1,
    "result": {
        "sentiment": "negative",
        "intensity": "-0.8",
        "intention": [1, 4],
        "keywords": {
            "1": ["game lagging", "Ads won't load"],
            "4": ["issue a refund"]
        }
    },
    "status": 1
}
```

## Getting Started
Follow these instructions to set up and run the MultiLingual Sentiment Analyzer on your local machine.

### Prerequisites
- Python 3.8 or higher

### Installation

1. **Clone the repository**:
    ```bash
    git clone https://github.com/Bella1i/MLSA.git
    ```

2. **Navigate to the project directory**:
    ```bash
    cd MLSA
    ```

3. **Install the required dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Application

1. **Start the system**:
    ```bash
    python main.py pro
    ```

### Usage

Once the system is running, you can send POST requests to the specified endpoint to analyze user comments. Ensure your input data is formatted as shown in the example.

## Contributing

Contributions are welcome! Please read the [contributing guidelines](CONTRIBUTING.md) for more information.

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
For any inquiries or issues, please reach out to [Bella1i](https://github.com/Bella1i).

---

Enhance your product feedback analysis with the MultiLingual Sentiment Analyzer and gain invaluable insights to drive improvements and customer satisfaction.
