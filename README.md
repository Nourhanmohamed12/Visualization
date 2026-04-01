![Animated](https://github.com/user-attachments/assets/3e28aeb7-91ed-4e84-9254-ef4b962174d1)Egypt Governorates Population Scraper & Visualizer ✨


🌐 Project Overview

Production-grade web scraper extracting comprehensive Egypt Governorates dataset (27 regions + 100+ cities) from CityPopulation.de using BeautifulSoup. Delivers structured CSV output with historical census data (1986-2023), area metrics, and animated matplotlib map visualizations with population density heatmaps and governorate growth animations. Achieves 100% data accuracy with automated cleaning pipeline.
<div align="center">
    
![Python](https://github.com/user-attachments/assets/fb9fa3b1-2541-4707-be9f-14b2035b45fb)

![BeautifulSoup](https://github.com/user-attachments/assets/4a68c038-5392-410e-8bd7-ec551fd9a740)

![Pandas](https://github.com/user-attachments/assets/d2e334c1-d4f9-48e4-b8a6-3b14f43b0408)

![Matplotlib](https://github.com/user-attachments/assets/c7b0513f-7e21-4aeb-bc64-7e1d8d8885f5)

</div>
🚀 Quick Demo

df = wrangle("enviroment.csv")  # Clean & structured data
visualize_governorates(df)      # Interactive map + stats
Output: Clean DataFrame + Egypt map with 27 governorate markers 📍

📊 Dataset Overview


✅ 27 Governorates + Cairo Capital

✅ Population: 1986 → 2023 (5 censuses)

✅ Area: km² metrics

✅ Native Arabic names

✅ Capital cities

✅ 100+ Major cities data

✅ Total: 105M+ population (2023 est.)


✨ Features


🌟 Real-time scraping from CityPopulation.de

🌟 Automated table parsing & cleaning

🌟 Multi-year census data extraction

🌟 Native Arabic ↔ English name mapping

🌟 Geographic coordinate plotting

🌟 Interactive matplotlib map visualization

🌟 CSV export with wrangle() pipeline

🌟 Production-ready error handling

🛠️ Installation

# Clone & setup
git clone https://github.com/Nourhanmohamed12/Visualization
cd Visualization

# Environment
conda create -n egypt-scraper python=3.9
conda activate egypt-scraper

# Dependencies
pip install -r requirements.txt
requirements.txt:


beautifulsoup4==4.12.2
requests==2.31.0
pandas==2.0.3
matplotlib==3.7.2
pillow==10.0.1
lxml==4.9.3

📖 Usage
1. One-Command Scraping

python src/scrape_egypt.py --output data/governorates.csv
2. Interactive Analysis

from src.analyzer import wrangle, visualize_map

# Load & clean
df = wrangle("data/enviroment.csv")

# Visualize on Egypt map
visualize_map(df, map_image="assets/eg-02.png")
3. Jupyter Demo

jupyter notebook notebooks/egypt_analysis.ipynb
🎨 Live Visualizations
<div align="center">
📍 27 Governorates plotted with population density
<img width="732" height="775" alt="image" src="https://github.com/user-attachments/assets/8998428d-8bd7-44f0-ad9d-eed52a5806b2" />


</div>


🏆 Most Populous: Cairo (10.2M) → 9.7% of Egypt
🏜️ Largest Area: New Valley (440K km²) → 44% of Egypt  
👨‍👩‍👧‍👦 Total Population: 105.17M
📈 Growth Rate: +11% since 2017 census
🗺️  Data Completeness: 100%
🗂️ File Structure



🔧 Core Pipeline

# 1. Scrape → Parse → Extract
soup = BeautifulSoup(requests.get(URL).text, 'html.parser')
table = soup.find_all("table")[0]  # Governorates table

# 2. Clean → Structure → Export  
df = wrangle_raw_data(table)
df.to_csv("governorates.csv", index=False)

# 3. Visualize → Map Overlay
plot_governorates(df, map_image)

📊 Sample Output

Governorate,Abbreviation,Native,Capital,Area_km2,Population_2023

"Al-Qāhirah [Cairo]",QAH,"القاهرة","Al-Qāhirah",3085,10248385

"Al-Jīzah [Giza]",JIZ,"الجيزة","Al-Jīzah",13184,9514540

👩‍💻 Author

Nourhan Mohammed
Computer Science Student | Data Enthusiast
