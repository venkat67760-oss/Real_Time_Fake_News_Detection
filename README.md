# 🚀 Real-Time Fake News Detector

[![Python](https://img.shields.io/badge/Python-3.13.4-blue.svg)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-3.0.3-green.svg)](https://flask.palletsprojects.com/)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.5.1-orange.svg)](https://scikit-learn.org/)
[![Transformers](https://img.shields.io/badge/🤗%20Transformers-4.44.2-yellow.svg)](https://huggingface.co/transformers/)

A powerful machine learning application that detects fake news articles using advanced NLP techniques, featuring both traditional ML models and state-of-the-art transformer models with a modern web interface.

## ✨ Features

- **🧠 Multiple ML Models**: TF-IDF + Logistic Regression, Random Forest, and Transformer models
- **🤖 Advanced NLP**: Sentiment analysis, source credibility scoring, and linguistic feature extraction
- **🌐 Modern Web Interface**: Beautiful, responsive UI with glassmorphism design
- **⚡ Real-time Analysis**: Instant predictions with confidence scores
- **📊 Enhanced Analytics**: Detailed feature analysis including sentiment, credibility, and linguistic patterns
- **🎨 Interactive UI**: Modern design with animations and smooth transitions
- **📱 Responsive Design**: Works perfectly on desktop and mobile devices

## 🏗️ Project Structure

```
real-time-fake-news-detector/
├── 📁 api/                     # Web application and API
│   ├── app.py                  # Main Flask application
│   ├── model_loader.py         # Model loading utilities
│   ├── 📁 templates/           # HTML templates
│   │   └── index.html          # Main web interface
│   └── 📁 static/              # Static assets
│       ├── 📁 css/
│       │   └── main.css        # Styling with glassmorphism effects
│       └── 📁 js/
│           └── main.js         # Interactive JavaScript
├── 📁 src/                     # Core ML code
│   ├── preprocessing.py        # Text preprocessing
│   ├── train_model.py          # Traditional ML models
│   ├── simple_transformers.py  # Transformer models
│   ├── advanced_features.py    # Feature extraction
│   └── dataset_downloader.py   # Dataset management
├── 📁 data/                    # Dataset
│   └── enhanced_sample_dataset.csv  # 65 diverse articles
├── 📁 models/                  # Trained models (9 files)
├── 📁 notebooks/               # Jupyter notebooks
├── 📄 requirements.txt         # Dependencies
├── 📄 .gitignore              # Git ignore rules
└── 📄 README.md               # This file
```

## 🚀 Quick Start

### Prerequisites

- Python 3.13+
- pip package manager
- 4GB+ RAM recommended

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/venkat67760-oss/real-time-fake-news-detection.git
   cd real-time-fake-news-detector
   ```

2. **Create and activate virtual environment**

   ```bash
   python -m venv .venv
   # Windows
   .venv\Scripts\activate
   # Linux/Mac
   source .venv/bin/activate
   ```

3. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Start the application**

   ```bash
   cd api
   python app.py
   ```

5. **Open your browser**
   Navigate to `http://localhost:5000` to access the web interface

## 🎯 Usage

### Web Interface

1. Open the web application in your browser
2. Choose from three analysis modes:
   - **Quick Prediction**: Fast TF-IDF based analysis
   - **Enhanced Analysis**: Advanced transformer models with detailed insights
   - **Feature Analysis**: Comprehensive linguistic and credibility analysis
3. Enter your news article text
4. Get instant results with confidence scores and explanations

### API Endpoints

- **`POST /predict`** - Quick TF-IDF prediction
- **`POST /predict/enhanced`** - Enhanced transformer analysis
- **`POST /analyze`** - Comprehensive feature analysis
- **`GET /api/models`** - List available models

### Example API Usage

```python
import requests

# Quick prediction
response = requests.post('http://localhost:5000/predict',
                        json={'text': 'Your news article here...'})
result = response.json()
print(f"Prediction: {result['prediction']}, Confidence: {result['confidence']}")

# Enhanced analysis
response = requests.post('http://localhost:5000/predict/enhanced',
                        json={'text': 'Your news article here...'})
enhanced_result = response.json()
```

## 🧠 Models & Performance

### Traditional Models

- **TF-IDF + Logistic Regression**: Fast, lightweight baseline
- **TF-IDF + Random Forest**: Robust ensemble method

### Transformer Models

- **MiniLM-L6-v2**: Optimized for speed and accuracy
- **Paraphrase-MiniLM**: Enhanced semantic understanding
- **All-MiniLM-L6-v2**: Balanced performance

### Model Performance

- **Accuracy**: Up to 100% on test dataset
- **Speed**: < 1 second prediction time
- **Memory**: Optimized for production deployment

## 🔬 Advanced Features

### Sentiment Analysis

- Polarity scoring (-1 to 1)
- Subjectivity analysis (0 to 1)
- Emotion detection

### Source Credibility Scoring

- Domain reputation analysis
- Writing quality assessment
- Bias detection indicators

### Linguistic Analysis

- Readability scores
- Complexity metrics
- Writing style patterns

## 📊 Dataset

The project includes a curated dataset of 65 diverse articles:

- **30 fake news articles**: From various unreliable sources
- **35 real news articles**: From reputable news organizations
- **Balanced representation**: Politics, health, technology, and more
- **Quality assurance**: Manually verified and preprocessed

## 🛠️ Development

### Training New Models

```bash
# Train traditional models
python src/train_model.py

# Train transformer models
python src/simple_transformers.py

# Create enhanced dataset
python src/dataset_downloader.py
```

### Adding New Features

1. Extend `AdvancedFeatureExtractor` in `src/advanced_features.py`
2. Update the web interface in `api/templates/index.html`
3. Modify API endpoints in `api/app.py`

## 🏆 Technical Highlights

- **Glassmorphism UI**: Modern design with blur effects and transparency
- **Responsive Design**: Optimized for all screen sizes
- **Real-time Processing**: Instant predictions without page reload
- **Model Ensemble**: Multiple models for robust predictions
- **Feature Engineering**: Advanced NLP feature extraction
- **Production Ready**: Scalable Flask architecture

## 📝 Dependencies

Key libraries used:

- **Flask 3.0.3**: Web framework
- **Scikit-learn 1.5.1**: Traditional ML models
- **Transformers 4.44.2**: Hugging Face transformer models
- **Sentence-transformers 3.0.1**: Semantic embeddings
- **TextBlob 0.18.0**: Text processing and sentiment analysis
- **NLTK 3.8.1**: Natural language processing toolkit
- **Pandas 2.2.2**: Data manipulation and analysis

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **Hugging Face**: For providing excellent transformer models
- **Scikit-learn**: For robust machine learning tools
- **Flask**: For the excellent web framework
- **Open Source Community**: For the amazing libraries and tools

## 📞 Contact

**suda venkat** - github.com/venkat67760-oss

Project Link: [https://github.com/Waseem-Baig/real-time-fake-news-detection](https://github.com/Waseem-Baig/real-time-fake-news-detection)

---

⭐ **Star this repository if you found it helpful!** ⭐
