# TuringBots vs Human Developers: An Analysis Using GitHub Data

## Overview
This project investigates the capabilities of AI tools like GitHub CoPilot and ChatGPT in software development, focusing on their potential to replace or complement human developers. Using GitHub Archive data (~1.36 TiB) stored on Google Cloud, the analysis covers programming language trends, repository growth, commit patterns, and technological breakthroughs. Insights are supported by comprehensive data preprocessing, exploratory data analysis (EDA), and visualizations.

---

## Objectives
1. **AI Impact**:
   - Assess whether AI tools improve developer productivity and can replace human creativity and problem-solving.
2. **Programming Language Trends**:
   - Analyze language adoption trends and licensing correlations.
3. **Repository Growth**:
   - Examine factors driving repository growth, including Big Tech contributions and open-source frameworks.
4. **Commit Patterns**:
   - Identify reasons for commits and analyze the influence of prolific contributors.
5. **Text Similarity**:
   - Evaluate duplication in commit messages across programming languages.

---

## Data Overview
- **Source**: GitHub Archive (Google Cloud Storage).
- **Datasets**:
  1. **commits_sampled**: Cleaned and sampled commit data.
  2. **contents_cleaned**: Metadata on file contents.
  3. **files_filtered**: Metadata on file paths and modes.
  4. **languages_filtered**: Programming language usage.
  5. **licenses_filtered**: Repository licenses.
- **Total Data Size**: ~1.36 TiB.
- **Tools Used**: PySpark, Matplotlib, Pandas.

---

## Methodology

### 1. Data Cleaning and Sampling
- Filtered rows to remove null values and duplicates.
- Selected relevant fields for analysis.
- Sampled 20% of the `commits` dataset for efficient processing.
- Filtered other datasets (`files`, `languages`, and `licenses`) to align with sampled repositories.

### 2. Exploratory Data Analysis (EDA)
- Conducted analysis to identify trends, correlations, and patterns across the datasets.
- Applied cosine similarity to evaluate text duplication in commit messages.

---

## Visualizations

### 1. **Timeline Analysis**
**Objective**: Identify peaks, valleys, and data gaps in commit activity from 2008–2022.  
**Insights**:
- Peaks aligned with major open-source events (e.g., TensorFlow and React releases).
- Declines in activity post-2016 reflect project stabilization.


---

### 2. **Programming Language Trends**
**Objective**: Analyze the most popular languages by bytes and commits, and their trends over time.  
**Insights**:
- Python and JavaScript exhibit consistent growth, driven by data science and web development.
- C remains influential, but its usage is declining compared to modern languages.

---

### 3. **License Distribution**
**Objective**: Examine the distribution of licenses and their correlations with programming languages.  
**Insights**:
- The MIT license dominates, particularly for Python and JavaScript.
- GPL licenses are commonly associated with older languages like C and C++.


---

### 4. **Repository Growth**
**Objective**: Identify popular and rapidly growing repositories.  
**Insights**:
- Big Tech projects (e.g., TensorFlow, Chromium) dominate, showcasing open-source leadership.
- Explosive growth in repositories often correlates with modern frameworks.

---

### 5. **Commit Reasons**
**Objective**: Classify commit reasons (e.g., bug fixes, new features) and analyze their distribution.  
**Insights**:
- New technology development (48.8%) and bug fixes (33.1%) dominate commit activities.
- Documentation updates, refactoring, and testing account for smaller but significant shares.


---

### 6. **Text Similarity Analysis**
**Objective**: Evaluate duplication in `subject` and `message` fields across programming languages.  
**Insights**:
- ~85% of commit messages are unique, highlighting diverse developer practices.
- Higher similarity rates are observed in templated workflows for languages like HTML and CSS.


---

## Key Insights
1. **AI in Development**:
   - AI tools improve efficiency for routine tasks but cannot replace human creativity.
   - Open-source contributions by Big Tech drive the adoption of tools like CoPilot.
   
2. **Language and Licensing Trends**:
   - Python and JavaScript dominate GitHub activity.
   - Permissive licenses (e.g., MIT) enable open collaboration and innovation.

3. **Repository Growth**:
   - Popular projects (e.g., TensorFlow, Chromium) reflect Big Tech’s influence.
   - Significant growth driven by modern frameworks and distributed systems.

4. **Commit Patterns**:
   - New technology development and bug fixes account for 82% of commits.
   - Commit messages show a balance between innovation and maintenance.

---

## Actionable Recommendations

### For Developers:
- Leverage AI tools for routine tasks like debugging and documentation.
- Enhance skills in AI frameworks to stay competitive in the software landscape.

### For Organizations:
- Adopt AI-augmented development processes to boost team productivity.
- Balance human ingenuity with AI tools for software design and architecture.
- Collaborate with open-source communities to drive innovation.

