# Pexels Image Analyzer with Google Charts

Resource - Pexels [free to use hd images source]
Tool - Google Charts

A Python project that fetches images from Pexels based on user input, calculates visual metrics, ranks the images, and visualizes the results using **Google Charts**. The project also displays image thumbnails and allows downloading the top-ranked image.  

---

## Features

- Fetch top `N` images from Pexels based on a keyword.  
- Compute **colorfulness** and **resolution** metrics.  
- Rank images by a combined score.  
- Visualize the image ranking using **Google Charts** (bar chart).  
- Display thumbnails of fetched images.  
- Provide a download link for the top-ranked image.  

---

## Requirements

- Python 3.8+
- Packages:
  - `requests`
  - `Pillow`
  - `numpy`
  - `python-dotenv`
  - `IPython`

---

## Setup Instructions

1. **Clone or download the repository**  
   ```bash
   git clone <your-repo-url>
   cd <project-folder>
