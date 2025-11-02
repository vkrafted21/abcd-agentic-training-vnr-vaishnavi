# 📸 Pexels Image Analyzer with Google Charts

A Python-based project that fetches images from **Pexels** based on user input, analyzes them for visual quality (colorfulness & resolution), ranks them using a composite score, and visualizes the results through **Google Charts**.  
It also displays image thumbnails and allows downloading the top-ranked image.

---

## 🌐 Overview

- **Resource:** [Pexels API](https://www.pexels.com/api/) — Free, high-quality image source  
- **Visualization Tool:** [Google Charts](https://developers.google.com/chart)  
- **Goal:** Move beyond simple popularity-based sorting (likes/downloads) by ranking images on **visual metrics** like colorfulness and resolution.

---

## ✨ Features

- Fetch top `N` images from Pexels based on keyword input  
- Compute:
  - 🎨 **Colorfulness** — measures vibrancy and color diversity  
  - 📏 **Resolution** — evaluates pixel clarity (width × height)  
- Generate a **composite ranking score** combining both metrics  
- Visualize rankings using **Google Charts** (Bar Chart)  
- Display image thumbnails inline  
- Provide a **download link for the top-ranked image**

---

## ⚙️ Tech Stack

- **Language:** Python 3.8+
- **Libraries:**
  - `requests` — API requests  
  - `Pillow` — image processing  
  - `numpy` — numeric computations  
  - `python-dotenv` — environment variable management  
  - `IPython.display` — display visuals in Jupyter  
- **Visualization:** Google Charts (HTML + JavaScript)

---

## 🧩 Setup Instructions

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/vkrafted21/abcd-agentic-training-vnr-vaishnavi.git
cd abcd-agentic-training-vnr-vaishnavi/testResource
2️⃣ Create and Activate a Python Virtual Environment
💻 macOS / Linux
bash
Copy code
python3 -m venv .venv
source .venv/bin/activate
🪟 Windows
bash
Copy code
python -m venv .venv
.venv\Scripts\activate
✅ You’ll know your environment is active when your terminal prompt starts with (.venv).

3️⃣ Install Dependencies
bash
Copy code
pip install requests Pillow numpy python-dotenv IPython
To verify:

bash
Copy code
pip list
4️⃣ Set Up Your .env File
Create a new file named .env in your project folder and add your Pexels API key:

env
Copy code
PEXELS_API_KEY=your_pexels_api_key_here
Get your free API key at https://www.pexels.com/api

5️⃣ Run the Project
Open the main.ipynb notebook in VS Code or Jupyter Notebook.
Run all cells — it will:

Ask for a search keyword (e.g., "mountain", "city", "forest")

Fetch top N images from Pexels

Calculate colorfulness & resolution metrics

Rank images using a combined score

Display a Google Charts bar graph

Show thumbnails and a download link for the top image

📊 How Image Analysis Works
🧮 Colorfulness Metric
Measures visual richness by analyzing RGB channel variation.

Formula:

cpp
Copy code
Colorfulness = sqrt(σ_RG² + σ_YB²) + 0.3 × sqrt(μ_RG² + μ_YB²)
Where:

RG = R - G

YB = 0.5 × (R + G) - B

📏 Resolution Metric
Calculates total pixel count:

arduino
Copy code
Resolution = width × height
⚖️ Combined Score
Ranks images by weighted metrics:

ini
Copy code
Score = 0.6 × Colorfulness + 0.4 × Normalized Resolution
🔍 Comparison: Existing vs Proposed System
Approach	Description
Existing Platforms	Most stock sites (e.g., Pexels, Unsplash) rank by downloads or likes.
Proposed Agentic System	Uses objective visual quality metrics like color richness and pixel clarity for ranking.

📈 Example Run
Input:

javascript
Copy code
Keyword: "ocean"
Number of Photos: 10
Output:

Fetches 10 ocean images

Computes colorfulness & resolution

Displays bar chart using Google Charts

Shows thumbnails

Provides download link for top-ranked image

🚀 Future Enhancements
Integrate Gemini / LangChain for automated image captioning

Add metrics like brightness, contrast, and sharpness

Generate comparative keyword insights

👩‍💻 Author
Vaishnavi Koppakula
🎓 Student Developer | 🌐 GitHub: vkrafted21
