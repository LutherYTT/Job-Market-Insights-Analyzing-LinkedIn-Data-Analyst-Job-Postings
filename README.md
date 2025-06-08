# Job Market Insights: Analyzing LinkedIn Data Analyst Job Postings

---

## Project Description

In today's competitive job market, understanding employer expectations is vital for job seekers aiming to align their skills with industry demands. This project analyzes job postings from LinkedIn to extract actionable insights into required skills, job description trends, and corporate recruitment strategies. Leveraging data analysis and natural language processing (NLP) techniques, it identifies in-demand skills, uncovers hidden requirements within job descriptions, and decodes company hiring patterns. These findings empower job seekers to tailor their applications and skill development effectively, while demonstrating proficiency in data science methodologies applicable across various domains.

---

## Objectives

- **Identify In-Demand Skills**: Determine the most frequently required skills across LinkedIn job postings.
- **Analyze Job Descriptions**: Extract hidden requirements and thematic trends from job descriptions.
- **Cluster Corporate Strategies**: Group companies by skill requirements to reveal recruitment patterns.
- **Visualize Insights**: Provide interactive visualizations and dashboards for data exploration.

## Data Source and Preprocessing

The dataset comprises job postings sourced from LinkedIn, including fields such as job titles, descriptions, and skills. Due to privacy and LinkedIn's terms of service, the raw data is not included in this repository. Instead, a sample dataset with a comparable structure is provided (`sample_linkedin_data.csv`) for demonstration. Preprocessing steps, implemented in `01_Data-Preprocess.ipynb`, include:

- **Data Cleaning**: Removing rows with missing or empty skill entries.
- **Skill Normalization**: Standardizing skill formats by replacing "和" with "、" and combining skill columns into a unified list.

---

## Methodology

The analysis is structured across multiple Jupyter notebooks, each addressing a distinct analytical component:

1. **`02_WordCloud.ipynb`**  
   - **Technique**: Generates word clouds and frequency charts using the `WordCloud` library.
   - **Purpose**: Visualizes the most common skills and keywords in job postings.

2. **`03_Core-Skills-Requirements-Analysis.ipynb`**  
   - **Techniques**: 
     - Frequency analysis to identify prevalent skills.
     - Association rule mining with `mlxtend` to detect skill co-occurrences.
     - K-means clustering (`scikit-learn`) on TF-IDF vectors to group companies by skill preferences.
   - **Purpose**: Uncovers skill combinations and company-specific skill trends.

3. **`04_Job-Content-Deep-Dive.ipynb`**  
   - **Techniques**: 
     - Named Entity Recognition (NER) with `spaCy` to extract technical entities (e.g., tools, languages).
     - Topic modeling via Latent Dirichlet Allocation (LDA) using `Gensim` to identify description themes.
   - **Purpose**: Analyzes job description content for hidden requirements and thematic patterns.

4. **`05_Corporate-Recruitment-Strategy-Decoding.ipynb`**  
   - **Techniques**: 
     - TF-IDF transformation (`scikit-learn`) for skill vectorization.
     - Cosine similarity to measure company skill profile similarity.
     - LDA topic modeling for company skill topics.
     - Interactive dashboard creation with `Plotly`.
   - **Purpose**: Clusters companies by skill requirements and visualizes recruitment strategies.

---

## Results

Key findings include:

- **Top Skills**: Python, SQL, and Analytical Skills emerged as the most frequently demanded competencies.
- **Skill Combinations**: Strong associations were found, e.g., "Troubleshooting" frequently co-occurs with "Networking" (confidence: 1.0).
- **Job Description Themes**: Topics such as "Data Analysis" and "Technical Support" dominate postings.
- **Company Clusters**: Five distinct clusters identified, reflecting varied recruitment focuses (e.g., technical vs. analytical roles).

Visualizations enhance interpretability:
- Word clouds and bar charts (`02_WordCloud.ipynb`).
- Association rule networks and cluster plots (`03_Core-Skills-Requirements-Analysis.ipynb`).
- LDA topic visualizations (`04_Job-Content-Deep-Dive.ipynb`).
- An interactive dashboard (`tech_stack_dashboard.html` from `05_Corporate-Recruitment-Strategy-Decoding.ipynb`).

---

## Visualization
### 02_WordCloud.ipynb
![Skill Keyword Wordcloud](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/02_skill_keyword_wordcloud.png)
![Skill Keyword Bar Chart](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/02_skill_keyword_bar_chart.png)
![Job Description Wordcloud](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/02_job_desc_keyword_wordcloud.png)
![Job Description Bar Chart](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/02_job_desc_keyword_bar_chart.png)

### 03_Core-Skills-Requirements-Analysis.ipynb
![Skill Association Rule](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skill_association_rule.png)
![Frequent Skill Combinations](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_frequent_skill_combinations.png)
![Company Cluster By Skill Preferences](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_company_cluster_by_skill_preferences.png)
![Skills in Cluster 0](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skills_in_cluster0.png)
![Skills in Cluster 1](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skills_in_cluster1.png)
![Skills in Cluster 2](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skills_in_cluster2.png)
![Skills in Cluster 3](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skills_in_cluster3.png)
![Skills in Cluster 4](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/03_skills_in_cluster4.png)

### 04_Job-Content-Deep-Dive.ipynb
![Dashboard](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/04_dashboard.png)

### 05_Corporate-Recruitment-Strategy-Decoding.ipynb
![Dashboard Part 1](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/05_dashboard1.png)
![Dashboard Part 2](https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings/blob/main/asstes/05_dashboard2.png)

---

## Usage

To replicate the analysis using Google Colab:

1. **Access the Repository**:
   - Download the Jupyter notebooks (`00_pip-install-libary` to `05_Corporate-Recruitment-Strategy-Decoding.ipynb`), and `preprocessed_linkedin_data`.
   OR
   - Download the Repository (`git clone https://github.com/LutherYTT/Job-Market-Insights-Analyzing-LinkedIn-Data-Analyst-Job-Postings.git`)

3. **Upload to Google Colab**:
   - Open [Google Colab](https://colab.research.google.com/).
   - Upload the downloaded notebooks and `preprocessed_linkedin_data.csv` to your Colab environment.

4. **Run Notebooks**:
   - Open each notebook in Colab and execute them sequentially from `01_Data-Preprocess.ipynb` to `05_Corporate-Recruitment-Strategy-Decoding.ipynb`.
   - Use the provided `preprocessed_linkedin_data.csv` or replace it with your own dataset in the same format.

5. **View Dashboard**:
   - After running `04_Job-Content-Deep-Dive`, download `lda_visualization.html`.
   - After running `05_Corporate-Recruitment-Strategy-Decoding.ipynb`, download `tech_stack_dashboard.html`.
   - Open it in a web browser to explore the interactive dashboard.

---

## Technologies Used

- **Programming Language**: Python 3.x
- **Data Manipulation**: Pandas, NumPy
- **Visualization**: Matplotlib, WordCloud, Plotly
- **NLP**: spaCy, NLTK, Gensim
- **Machine Learning**: Scikit-learn, mlxtend
- **Development Tools**: Jupyter Notebooks, Git

---

## Skills Demonstrated

This project highlights proficiency in:

- **Data Preprocessing**: Cleaning and structuring unstructured data with Pandas (`01_Data-Preprocess.ipynb`).
- **Natural Language Processing**: Entity extraction and topic modeling (`04_Job-Content-Deep-Dive.ipynb`).
- **Data Visualization**: Creating insightful plots and dashboards (`02_WordCloud.ipynb`, `05_Corporate-Recruitment-Strategy-Decoding.ipynb`).
- **Machine Learning**: Clustering and association rule mining (`03_Core-Skills-Requirements-Analysis.ipynb`).

---

## Future Work

Potential enhancements include:
- **Temporal Analysis**: Tracking skill trends over time with historical data.
- **Multi-Platform Integration**: Expanding to include data from Indeed or Glassdoor.
- **Recommendation System**: Matching job seekers to postings based on skills.
- **Automation**: Streamlining data collection and analysis pipelines.

---

### Conclusion

This project offers a data-driven lens into the job market, providing actionable insights for job seekers while showcasing advanced data science techniques. The methodologies and skills demonstrated are broadly applicable, making it a strong portfolio piece for roles in data analysis, NLP, and machine learning.
