 Welcome to my portfolio.

On this page, I ordered the main projects I have worked on.
The text presenting my personal portfolio has the following sections:
For each project, you will find a brief description, the technologies used, a link to the repository, and, in some cases, a demo video.

## 1.Main project developed in my last working experience as a Data Engineer at Prestige Group srl:

#### Objective of the project

The company buys smartphones from six different suppliers, each of which sends their price list daily in a different format and describes the same phone in their own way. Before this project, finding out which supplier offers the best price for a given phone meant comparing thousands of rows every day by hand across six different files.

Goal of this project is to automatize this procedure: it reads all six price lists, understands when two different descriptions actually refer to the same phone(using a sentence embedding model), and produces a single clean spreadsheet where each row shows the cheapest price available, which supplier offers it, and how many units are in stock. What used to take hours of manual work now runs in minutes, giving the purchasing team a ready-to-use overview of the best deal for every smartphone on the market.

#### Tools used

- Pipeline built in Python with pandas
-  Data collection: via FTP, REST APIs, and local file parsing
-  AI matching via BAAI/bge-m3 sentence embedding model + cosine similarity
-  Blocking strategy to reduce the comparison space to be given in input to the BAAI/bge-m3 sentence embedding model
-  Color standardization: thousands of commercial color names mapped to 9 base categories
-  Regex-based extraction for key product attributes

*Note on privacy: for privacy reasons, sensitive data like API calls credentials have been removed from the notebook.*

#### Project repository:  **[Explore the complete Smartphone Price Comparison project](https://github.com/MatteoMonacis/smartphone-price-comparison)**


## 2.Main project developed during my partecipation in the Junior Enterprise  of the Bicocca University for a company  operating in the digital payment sector:

#### Objective of the project

The client, a company operating in the digital payments sector, was facing a critical problem: among thousands of daily transactions, a very small fraction — less than 3% — were fraudulent. Manually reviewing every transaction was unsustainable, and the rarity of fraud cases made it extremely difficult for any automated system to learn to distinguish them from legitimate ones. The goal of this project was to build a Machine Learning model capable of automatically flagging suspicious transactions, allowing the company to intervene promptly and reduce financial losses. To ensure reliable performance measurement despite the severe data imbalance, a balanced evaluation strategy was adopted: the test set was constructed by sampling an equal number of fraudulent and legitimate transactions, and this process was repeated across five independent splits to assess model robustness. The final solution — an optimized Decision Tree classifier achieving 95% average accuracy on the balanced test set — provided the client with an interpretable, production-ready tool to automate fraud detection.

#### Tools used

- Built in Python using pandas, NumPy, SciPy, Matplotlib, and Seaborn.
- Classification models used: Logistic Regression, Decision Tree, Random Forest, and XGBoost.
-  Class imbalance was addressed using undersampling combined with SMOTE.
-  Hyperparameters were tuned with GridSearchCV.
-  The main optimization goal was to improve recall for the fraud class.

*Note on privacy: raw data has been cleaned and preprocessed, but for privacy reasons the code of data cleaning cannot be shared and the exploratory analysis cannot display real observations, and all category names have been anonymized, the name of variables are shown in the notebook only because the dataset displayed in the notebook has been created by the author based on the raw data provided by the client.*

#### Project repository:  **[Explore the complete Fraud Detection project](https://github.com/MatteoMonacis/Fraud-detection)**

## 3.My latest university project:

#### Objective of the project

Imagine doing a workout at home and having a smart system that watches you, counts your reps, and tells you if your form is off — all without a personal trainer. That is what Virtual Coach does. The system uses two inputs: your phone and your webcam. Your phone sits in your pocket and detects what you are doing — walking, sitting, standing, or laying down — by reading its built-in motion sensors. Your webcam tracks your body in real time, drawing a skeleton over your joints to understand how you move. From that skeleton, the system figures out which exercise you are performing (out of nine supported exercises, such as squats, push-ups, pull-ups, and jumping jacks), counts every repetition automatically, and flags shallow or incorrect reps. Everything runs together on a single live dashboard: on one side you see the webcam feed with the skeleton overlay and the rep counter, on the other side you see the activity detected from your phone. No cloud, no delay — it all happens in real time on your machine. Watch the demo below to see it in action.

#### Tools used

-  Classical ML models used: Random Forest, SVM with RBF kernel, and LightGBM.
-  Deep learning architectures included InceptionTime, DeepConvLSTM, Transformer with positional encoding, and a soft-voting ensemble.
-  Models were trained for Human Activity Recognition (HAR) using scikit-learn and TensorFlow/Keras.
-  Google MediaPipe BlazePose was used for pose estimation.
-  Exercise recognition compared eight PyTorch architectures, including TwoStreamRNN, PartLSTM, CTR-GCN, and SkeleTR.
-  Performance was evaluated using grid search and 5-fold stratified cross-validation.
- Cloud environment with GPU acceleration

#### Demo video

[![Watch the demo video](https://img.youtube.com/vi/aJGU9cfcoOk/hqdefault.jpg)](https://youtu.be/aJGU9cfcoOk)

▶️ [Click here to watch the complete demo on YouTube](https://youtu.be/aJGU9cfcoOk)


## 4. Key Machine Learning Projects

### 4.1 Machine Learning Applied to Real-World Data

#### 1. Objective of the Project

We developed a data-driven platform that helps individuals and institutions understand skilled migration and identify the most attractive countries for relocation. The solution addresses the difficulty of comparing destinations across fragmented sources and multiple factors, such as employment, income, healthcare, safety, quality of life, access to services, and political freedom. To support the analysis, we created a unified dataset by integrating OECD migration flows with socioeconomic and governance indicators, then cleaning, standardizing, and normalizing the data. The resulting platform allows users to explore migration trends, compare countries, and receive personalized destination recommendations based on their priorities. The screen recording below showcases the web interface and its main functionalities from the user’s perspective

#### 2. Tools Used

-  Python for project development
-  pandas and NumPy for data processing
-  scikit-learn for K-Means, PCA, normalization, and cosine similarity
-  NetworkX and Graphviz for dominance analysis
-  Plotly and Matplotlib for data visualization
-  Streamlit for building and deploying the web application

#### Demo video

[![Watch the demo video](https://img.youtube.com/vi/5q56joTQoZE/hqdefault.jpg)](https://youtu.be/5q56joTQoZE)

▶️ [Watch the complete demo on YouTube](https://youtu.be/5q56joTQoZE)

#### Project repository:  **[Explore the complete Machine Learning Applied to Real-World Data project](https://github.com/MatteoMonacis/Machine-Learning-Applied-to-Real-World-Data)**

### 4.2 Machine Learning on Knime

#### Objective of the Project

The main goal of this project was to build a machine learning workflow able to predict whether a water sample is safe to drink. KNIME Analytics Platform was intentionally used as part of a practical learning exercise, with the aim of improving skills in visual data analysis and low-code machine learning. The project included data cleaning, feature selection, class balancing, model training, and performance comparison. Another goal was to understand whether using PCA could improve the results compared with standard feature selection. Special attention was given to false positives, because predicting unsafe water as safe could have serious consequences. Random Forest without PCA was selected as the most reliable model.

#### 2. Tools Used

-  Platform: KNIME Analytics Platform
-  Machine Learning Models: Random Forest, XGBoost, Tree Ensemble, Naive Bayes, and Logistic Regression
-  Data Processing: PCA and feature selection
-  Model Optimization: Random-search hyperparameter tuning and stratified cross-validation
-  Evaluation Metrics: ROC curves, AUC, confusion matrices, and Lift Charts

#### Project repository:  **[Explore the complete Machine Learning on KNIME project](https://github.com/MatteoMonacis/Machine-Learning-on-Knime)**

### 4.3 Machine Learning for Object detection

#### Objective of the project

This project builds a face detection system entirely from scratch, without relying on any deep learning model. Pre-trained networks like MTCNN or RetinaFace would have solved the task with minimal effort, but the explicit goal here is educational purpose for which my goal was to work at a lower level of abstraction — manually designing the feature extraction pipeline and understanding what each component contributes to the final prediction. Each image patch goes through three parallel feature extractors: Gabor filters (reduced with PCA), HOG, and LBP. Their outputs are concatenated into a single vector and fed to an SVM classifier. At inference time, a sliding window scans the image at multiple scales and Non-Maximum Suppression merges overlapping detections into clean bounding boxes, as shown below.
<img
  width="369"
  height="208"
  alt="Face detection output"
  src="https://github.com/user-attachments/assets/a86329eb-3c5f-4f1a-b22d-5df89d34aa58"
/>

#### Tools used

-  The project is developed in Python.
-  scikit-learn is used for SVM, GridSearchCV, and classification metrics.
-  scikit-image is used for feature extraction with Gabor filters, HOG, and LBP.
-  OpenCV and Pillow handle image preprocessing.
-  NumPy is used for PCA and array operations.
-  The training data combines the BioID Face Database and Kaggle’s Intel Image Classification dataset.

#### Project repository:  **[Explore the complete Machine Learning for Object Detection project](https://github.com/MatteoMonacis/Machine-Learning-for-Object-detection)**


## 5. Key Deep Learning projects

### 5.1 Galaxy Morphology Classification Using Deep Learning and Transfer Learning

#### 1. Objective of the Project

The goal of this project was to build a deep learning system able to classify galaxy images into ten different categories. I compared a custom CNN with several pretrained models to understand which approach could provide the best results. The main challenge was working with an extremely large and memory-intensive image dataset. Processing, resizing, augmenting, and training on thousands of images caused RAM limitations and very long training times, especially on local machines. For this reason, I had to reduce the dataset size, optimize the preprocessing pipeline, and move the training process to a GPU-based cloud environment. This challenge taught me how to manage large datasets, limited computational resources, and practical deep learning workflows.

#### 2. Tools Used

- Built with Python, using TensorFlow/Keras and scikit-learn.
- Custom CNN and pretrained models: ResNet50, VGG16, DenseNet201, and MobileNetV2
- ImageNet-based transfer learning
- Grad-CAM for model explainability
- Cloud environment with GPU acceleration

#### Project repository: **[Explore the complete Galaxy Morphology Classification Using Deep Learning and Transfer Learning project](https://github.com/MatteoMonacis/Galaxy-Morphology-Classification-Using-Deep-Learning-and-Transfer-Learning)**

## 6.Key Text Mining projects

### 6.1 SMS Spam Detection and Topic Modeling Using Machine Learning and Deep Learning

#### Objective of the project

This project focused on two main tasks applied to SMS messages: detecting spam and discovering recurring topics. For spam detection, three models were trained on a large dataset of about 67,000 messages and then tested on a separate, well-known benchmark to check how well they generalize to unseen data. All models shared the same text representation to make the comparison fair. For topic modeling, only non-spam messages were kept, and two methods designed for very short texts were used to uncover the main themes hidden in the data.

#### Tools used

- Classification: XGBoost, CNN–LSTM, and CNN–BiLSTM.
-  Text representation: Pre-trained 300-dimensional GloVe embeddings.

#### Project repository: **[Explore the complete SMS Spam Detection and Topic Modeling Using Machine Learning and Deep Learning project](https://github.com/MatteoMonacis/SMS-Spam-Detection-and-Topic-Modeling-Using-Machine-Learning-and-Deep-Learning)**

### 6.2 Toxic Comment Detection and Classification

#### Objective of the project

This project tackles the challenge of automatically detecting toxic content in online comments through a multilabel classification approach, simultaneously identifying six categories of toxicity — toxic, severe toxic, obscene, threat, insult, and identity hate. The core of the work lies in a systematic model escalation driven by performance analysis: Logistic Regression and Naive Bayes baselines achieved decent precision but failed on recall for minority classes, motivating the shift to deep learning. A Weighted SimpleRNN dramatically improved recall but introduced excessive false positives; replacing it with a GRU addressed the vanishing gradient problem and pushed recall further. A Bidirectional GRU showed no gains, suggesting the preprocessed sequences didn't benefit from backward context, so the focus shifted to architecture design: a CNN-GRU hybrid combined Conv1D for local n-gram pattern extraction with GRU for sequential dependencies, achieving the best precision-recall balance. The final model scaled this architecture with richer embeddings (256d), delivering the highest recall across all six categories.

#### Tools used

- Built with Python, using TensorFlow/Keras and scikit-learn.
- Deep learning models included SimpleRNN, GRU, Bidirectional GRU, and Conv1D.
- Traditional models included Logistic Regression, Multinomial Naive Bayes, Complement Naive Bayes, and One-vs-Rest classification.
- Text preprocessing used NLTK, SnowballStemmer, Keras Tokenizer, and TF-IDF.
- Class imbalance was addressed with custom weighted binary cross-entropy.
- Evaluation used Hamming Loss, multilabel confusion matrices, and per-class precision and recall.

#### Project repository: **[Explore the complete Toxic Comment Detection and Classification project](https://github.com/MatteoMonacis/Toxic-Comment-Detection-and-Classification)**

### 6.3 Text mining with big data

#### Objective of the project

The goal of this project was to automatically classify over 150,000 Wikipedia articles into 15 categories (e.g., politics, finance, science, sports). Due to the large size of the dataset (~1 GB), the entire pipeline was run on Databricks to leverage distributed computing. The workflow included data cleaning, exploratory analysis (word count statistics, word clouds), feature engineering, and model training. Two experiments were conducted — one using short article summaries and one using full article texts — to see which input leads to better classification results.

#### Tools used

- The pipeline was built using PySpark MLlib.
- RegexTokenizer, StopWordsRemover, and CountVectorizer were used for feature extraction.
- A Multinomial Naive Bayes classifier handled categorization.
- Matplotlib and WordCloud were used for visualizations.

#### Project repository: **[Explore the complete Text Mining with Big Data project](https://github.com/MatteoMonacis/Text-mining-with-big-data)**

## 7.Financial Market data analysis 

### 7.1 Enhancing Momentum Strategies with Return Skewness

#### Objective of the project

When investing in the stock market, one common approach is to buy stocks that have been going up and sell those that have been going down — a strategy known as momentum. This project asks a simple question: can we improve this approach by also looking at how "uneven" each stock's recent returns have been? For example, some stocks mostly deliver small gains with occasional large drops, while others show the opposite pattern. This unevenness is called skewness, and measuring it can help pick better stocks to buy or avoid. Using data from 600 European companies over the period 2009–2018, the project tests four different ways of measuring this unevenness and compares them against a strategy based on momentum alone. The analysis is run separately on large, medium, and small companies to see whether the results hold across different parts of the market.

#### Tools used

- The entire pipeline is built in Python.
- Pandas is used for data manipulation.
- NumPy and SciPy handle statistical calculations, including skewness and semi-deviation.
- Matplotlib is used for performance visualization.
- yfinance retrieves benchmark data.
- Portfolios are price-weighted and rebalanced monthly.
- Backtesting is performed with a custom cross-sectional engine.

#### Project repository: **[Explore the complete Enhancing Momentum Strategies with Return Skewness project](https://github.com/MatteoMonacis/Enhancing-Momentum-Strategies-with-Return-Skewness)**

## 8. Key Data Management projects

### 8.1 Evolution of tactical roles in Serie A over the last 15 years

#### Objective of the project

Football tactics in Serie A have changed dramatically over the past 15 years — defenders now join the attack, midfielders cover both ends, forwards do much more than score, and goalkeepers have become active passers. To measure this shift, we collected 15 seasons of data (2009/10–2023/24) OF serie A, from WhoScored, Transfermarkt, and Octoparse, then integrated everything into a single clean dataset through extensive merging, deduplication, name standardization, and conflict resolution across heterogeneous sources. On top of this unified foundation we built custom weighted performance scores for each role, enabling fair cross-season comparisons, and analyzed goal-scoring partnerships to track which role combinations have become most productive over time.

#### Tools used

- Player data collection: WhoScored data was gathered using Selenium WebDriver and BeautifulSoup.
- Market data: Transfermarkt data was collected through HTTP requests and BeautifulSoup.
- Team statistics: Extracted with Octoparse’s no-code scraping pipeline.
- Data analysis: MySQL Workbench was used for relational queries, season-level normalization, and role-specific scoring.
- Relationship modeling: Neo4j and Cypher queries modeled connections between players, clubs, and formations.

#### Project repository: **[Explore the complete Evolution of Tactical Roles in Serie A over the Last 15 Years project](https://github.com/MatteoMonacis/Evolution-of-tactical-roles-in-Serie-a-over-the-last-15-years)**

### 8.2 Banking system analysis

#### Objective of the project

This project involved working with a relational banking database that stores customer profiles, account details, and over 14,000 transactions spanning a three-year period. The main objective was to transform this normalized structure into a single, client-level feature table suitable for supervised machine learning. Each row captures a set of behavioral indicators per customer, including age, transaction volumes and amounts by direction, account distribution across types, and spending patterns broken down by category such as mortgage payments, Amazon purchases, hotels, flights, and supermarkets.

#### Tools used:

- Pipeline development: Built entirely in MySQL.
- Data integration: Views were used to join clients, accounts, and transactions.
- Feature engineering: Correlated subqueries and aggregation functions populated the final feature table.

#### Project repository: **[Explore the complete Banking System Analysis project](https://github.com/MatteoMonacis/Banking-system-analysis)**

## 9. Key Data Visualization project

### 9.1 GAME, SET, DATA: Unlocking tennis insights

#### Objective of the project

The aim of this project was to help tennis coaches and sports agents make better decisions using data. The team collected ATP match results, player details, and rankings from Kaggle, then merged them into a single clean dataset. The analysis explored how court surfaces, handedness, height, and ranking affect player performance, how key stats evolve across tournament rounds, and how the average age of winners has been steadily declining. All findings were combined to define a data-backed profile of the ideal player worth investing in, presented through the interactive Tableau story below.

#### Tools used

- Data preparation: Python and Pandas were used to merge and clean three source tables.
- Data visualization: Tableau Public was used to create bar charts, multi-line charts, scatter plots, and a choropleth map.

#### Interactive Tableau dashboard:

##### *Click the image to open the interactive Tableau dashboard.*
<a href="https://matteomonacis.github.io/Personal-Portfolio/">
  <img
    width="1782"
    height="1102"
    alt="GAME, SET, DATA: Unlocking Tennis Insights dashboard"
    src="https://github.com/user-attachments/assets/7ed67908-192a-44d0-8c4a-184d007368e5"
  >
</a>


#### Project repository: **[Explore the complete GAME, SET, DATA: Unlocking Tennis Insights project](https://github.com/MatteoMonacis/GAME-SET-DATA-Unlocking-tennis-insights)**
