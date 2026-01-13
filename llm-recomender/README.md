# 🍽️ Restaurant Recommender with AI

A complete restaurant recommendation system using AI and machine learning. CLI-based with full Russian interface.

## 🚀 Quick Start

```bash
# Clone and setup
conda env create -f env.yml
conda activate llm-recommender

# Run the app
python3 app.py
```

## 📁 Project Structure
```
app.py              # Main CLI application
analyzer.py         # AI analysis with DeepSeek API
recommender.py      # Hybrid ML recommender
geolocator.py       # Yandex Maps geolocation
scraper.py          # Mock data generator
database.py         # Data persistence
config.py           # Configuration
.env               # API keys (optional)
```

## 🎯 Features

### ✅ Core Features
- **AI Review Analysis**: DeepSeek API for sentiment & keyword extraction
- **Smart Recommendations**: Hybrid ML algorithm (content + location)
- **Russian Cities**: Moscow, SPB, Novosibirsk, Kazan, etc.
- **No API Required**: Full mock mode for testing
- **Russian Interface**: Complete localization

### 🔧 Setup
1. Install: `conda env create -f env.yml`
2. Activate: `conda activate llm-recommender`
3. Optional: Add API keys to `.env`
4. Run: `python3 app.py`

### 📊 How It Works
```
User Input → Location + Preferences
         ↓
Find Nearby Restaurants
         ↓
AI Analysis (Reviews → Sentiment/Keywords)
         ↓
ML Scoring (Location + Content + Ratings)
         ↓
Personalized Recommendations
```

### 🎨 Sample Output
```
#1 Teremok #5
📍 Moscow | 🚗 1.2км | 🍽 Russian | ⭐ 4.7/5
💰 Цена: ₽₽ | 😊 Отзывы: Позитивные
📝 Customers love traditional cuisine
🔢 Совпадение: [████████░░] 85%
```

### ⚙️ Configuration
```bash
# .env file (optional)
DEEPSEEK_API_KEY=your_key
YANDEX_API_KEY=your_key
MOCK_MODE=True
DATA_FILE=restaurants.pkl
```

### 📈 Tech Stack
- **AI**: DeepSeek LLM API
- **ML**: Scikit-learn (cosine similarity)
- **Geo**: Yandex Maps API / Geopy
- **Data**: Pandas, NumPy
- **Storage**: Pickle

### 🛠️ Commands
```bash
# Main app
python3 app.py

# Test components
python3 scraper.py      # Generate mock data
python3 analyzer.py     # Test AI analysis
python3 recommender.py  # Test recommendation engine
```

### 🔍 Algorithm
- **Location**: 35% (distance-based)
- **Content**: 25% (cuisine similarity)
- **Rating**: 20% (normalized score)
- **Preferences**: 20% (user choices)

### 📦 Dependencies
```yaml
# From env.yml
python=3.9, pandas, numpy, scikit-learn, geopy
requests, beautifulsoup4, python-dotenv
```

### 🎮 Usage Example
```
1. Enter location: "Москва" or coordinates
2. Set preferences: Cuisine (Russian), Max price (3), Radius (10km)
3. Get AI-powered recommendations
4. Optionally save to CSV
```

### 💡 Key Points
- Works offline in mock mode
- Russian-first design
- Realistic mock data generation
- Export results to CSV
- Fast and lightweight

### 🐛 Troubleshooting
- No restaurants? → Increase search radius
- Data issues? → Delete `restaurants.pkl`
- API errors? → Enable `MOCK_MODE=True`

---

**Ready in 3 steps:** Install → Configure → Run  
**Perfect for:** Russian market, AI/ML projects, restaurant discovery