# CORD-19 Data Analysis and Streamlit App

This project is part of the **Frameworks Assignment**. It explores the **CORD-19 research dataset** (`metadata.csv`) and provides a simple interactive **Streamlit application** for data exploration.

---

## 📌 Project Overview
By completing this project, I practiced:
- Loading and exploring a real-world dataset
- Performing basic data cleaning and preparation
- Creating meaningful visualizations
- Building an interactive web application using **Streamlit**
- Documenting findings and workflow

---

## 🛠️ Tools and Requirements
- Python 3.7+
- [pandas](https://pandas.pydata.org/) – data manipulation
- [matplotlib](https://matplotlib.org/) / [seaborn](https://seaborn.pydata.org/) – data visualization
- [streamlit](https://streamlit.io/) – web application framework
- [wordcloud](https://github.com/amueller/word_cloud) – generate word clouds (optional)
- Jupyter Notebook – for initial exploration (optional)

Install dependencies:
```bash
pip install pandas matplotlib seaborn streamlit wordcloud
📂 Project Structure
nginx
Copy code
WEEK 8/
│
├── analysis.ipynb    # Jupyter notebook with exploration & cleaning
├── app.py            # Streamlit application
├── README.md         # Project documentation (this file)
└── .vscode/          # VS Code tasks/launch config (optional)
📊 Dataset Information
The project uses the CORD-19 metadata file which contains details of COVID-19 research papers (titles, abstracts, authors, publication dates, journals, etc.).

Since the dataset is large, it is not included in this repository.
You can download it from Kaggle:

🔗 CORD-19 Research Dataset (metadata.csv)

After downloading, place metadata.csv in the project root folder (same level as app.py).

🚀 Running the Project
1. Run the Jupyter Notebook (optional)
For exploration and testing:

bash
Copy code
jupyter notebook analysis.ipynb
2. Run the Streamlit App
Launch the web app:

bash
Copy code
streamlit run app.py
This will open the app in your browser at:

arduino
Copy code
http://localhost:8501
📊 Features in the Streamlit App
Filter papers by year range

Display sample data from the dataset

Show number of publications per year

Visualize top publishing journals

Generate a word cloud of paper titles (optional)

📝 Example Visualizations
Publications by Year (bar chart)

Top Journals (bar chart)

Word Cloud of Titles

Distribution of papers by source

💡 Notes
Ensure metadata.csv is placed in the project root before running.

If the dataset is too large, you may work with a smaller sample of rows (e.g., df.sample(5000)).

Always run the app with:

bash
Copy code
streamlit run app.py
