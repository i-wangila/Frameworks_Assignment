# Copilot Instructions for CORD-19 Data Explorer

## Project Overview
- This is a Streamlit-based data exploration app for the CORD-19 COVID-19 research dataset.
- Main file: `app.py` (all logic and UI in a single script).
- Data source: `metadata.csv` (CSV file with research paper metadata).

## Key Components & Data Flow
- Data is loaded and cached using `@st.cache_data` for performance.
- The `publish_time` column is parsed to datetime, and a `year` column is derived for filtering.
- The app provides:
  - Year range filtering via a Streamlit slider
  - Data sample display with `st.dataframe`
  - Publications by year (matplotlib bar chart)
  - Top journals (seaborn barplot)

## Developer Workflows
- **Run the app:**
  ```powershell
  streamlit run app.py
  ```
- **Dependencies:**
  - Required: `streamlit`, `pandas`, `matplotlib`, `seaborn`
  - Install with:
    ```powershell
    pip install streamlit pandas matplotlib seaborn
    ```
- **Data updates:**
  - Place updated `metadata.csv` in the project root.
  - The app will reload data on restart or cache clear.

## Project Conventions
- All code is in `app.py` (no modules or package structure).
- Use Streamlit widgets for all user interaction.
- Use matplotlib/seaborn for plotting; always display plots with `st.pyplot(fig)`.
- Data filtering is performed in-memory after loading the full CSV.
- No explicit test or build scripts; manual testing via app UI.

## Integration Points
- Expects `metadata.csv` with at least `publish_time` and `journal` columns.
- No external APIs or services are called.

## Examples
- Filtering by year:
  ```python
  year_range = st.slider("Select year range", int(df['year'].min()), int(df['year'].max()), (2020, 2021))
  filtered = df[(df['year'] >= year_range[0]) & (df['year'] <= year_range[1])]
  ```
- Plotting with matplotlib:
  ```python
  fig, ax = plt.subplots()
  ax.bar(year_counts.index, year_counts.values)
  st.pyplot(fig)
  ```

---

For questions or unclear conventions, review `app.py` or ask for clarification.
