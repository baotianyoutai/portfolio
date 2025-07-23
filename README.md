# AI/ML engineer 

※ Modified in _20250510

#### Technical skills 
**Cloud**
- GCP, AWS, Azure(used for Intelligence doccument for pdf processing)

**Python Framework**
- Pytorch, Tensorflow, Keras, timm, onnx, ultralytics, mediapipe
  
**Python skills**
- ML(lightgbm, catboost, xgboost, tabnet), CV(kf, skf, group-kf), ensemble/voting
- NLP(BERT, DEBERTA, ROBERTa,), DL(CNN, RNN, GLU, transformer)
- ImageClassification(timm,TTA, TTAch), ObjectDetection(Yolo series, Mediapipe ObjectDetector(effiecientdet), PINTO-model-zoo), Object Tracking(Centroid, DeepSort)
- GenAI(VertexAI, genai, langchain/langsmith), AI-agent(google-adk, langgraph)

## Education (birth : 2001)
B.S., Statistics | Hosei Univ.(_May 2024_)

## Work Experience
**AI/ML engineer @ Chibabank.Ltd (_May 2024 - Present_)**
- experienced [The ASL ML Immersive Education in Google]((https://cloud.google.com/customers/chiba-bank?hl=ja)), learned how to build end-to-end ML solutions using **tensorflow**  for 3 weeks, developed 1 prototype(japanese sign language AI using DNN, CNN, Transformer) for 1 weeks.(_October 2024_)<br>
- developing 5 **ai-agent** applications in **Streamlit** on **Cloud Run**, keep developing 1 **edge computing** application.

## Projects

### 1.AI for searching International Balance of Payments Item Numbers(_November 2024 - March 2025_)

#### Situation
- The Market Operations Department handles foreign remittances, a process that requires the use of international balance of payments item numbers. Foreign remittance operations required employees to consult an 80-page manual published by Bank of Japan, consuming significant time. 
- Centralized operations(caused by concentration of decision-making and information at the head office) increased workload, and knowledge sharing for new hires was a challenge.

- [AI Process]
We developed a RAG system (indexing, retrieving, and generation) using the following steps:<br>
1.began by chunking the PDF document.<br>
2.created a searchable document from the chunks.<br>
3.implemented the RAG system using Langchain and Chroma DB.<br>
4.deployed the system on Cloud Run with a Streamlit interface.<br>
5.To enhance usability, especially for users, we integrated the following feature:<br>
The Streamlit interface displays the specific sections of the original PDF document from which retrieved information originates, using metadata from the document chunks. This helps users easily verify the source of the information.
- [Technical Skills] Cloud Run, GCS, Streamlit, RAG, langchain, ChromaDB, 

### 2.AI for answering questions regarding loan approval authority(_November 2024 - March 2025_)
- responsible for the end-to-end development of an AI application designed for eight users. 
- [Background]
This system is utilized within our internal chat application, enabling head office staff to respond to inquiries from branch offices. The distinctive feature is our use of a vector database built from past question-and-answer (Q&A) pairs, rather than from the original manual data. This approach was adopted for two primary reasons:<br>
1.The inquiries often originate from users who couldn't find or understand the answers even after reading the manual.<br>
2.We aim to generate responses that preserve the nuances and specific tone of the head office staff's previous answers.<br>
- [Evaluation process]
The application's workflow involves storing designated evaluation CSV files in Google Cloud Storage (GCS). These files are then read as blobs into temporary files within the Streamlit interface, and the actual writing of this data is triggered by a button press.
- [Technical Skills]
Cloud Run, GCS, Artifact Registry Streamlit, RAG, langchain, ChromaDB

### 3.AI for Suggestion Triage and Assignment(_March 2025 - May 2025_)
- [Background]
Head office personnel currently receive requests and improvement proposals, identified by branch office staff during their daily operations, through a dedicated suggestion board system. Over the past four years, this system has accumulated approximately 4,000 entries. The responsible personnel requested an AI solution to automate two key tasks:<br>
1.identifying whether newly submitted suggestions duplicate existing ones.<br>
2.assigning these suggestions to the appropriate department for response.<br>
- [AI process]
An AI system was developed, comprising two primary agents:<br>
1.A Duplicate Detection Agent to identify recurring suggestions.<br>
2.A Department Assignment Agent to allocate suggestions to the relevant department.<br>
- [Evaluation Process]
The application's workflow involves storing designated evaluation CSV files in Google Cloud Storage (GCS). These files are then read as blobs into temporary files within the Streamlit interface, and the actual writing of this data is triggered by a button press.
- [Operational Process]
Initially, a vector database is created using all suggestion data accumulated to date. This database is stored in GCS and loaded into Streamlit as a temporary blob for operational use. To add new suggestions, users input the required information for each respective field into text areas on the Streamlit interface. Upon clicking a button, the new suggestion is processed (added via an add_document function) and the updated data is uploaded to a designated GCS bucket, ensuring the vector database remains current.
- [Technical Skills]
Cloud Run, GCS, Artifact Registry , Streamlit, RAG, langchain, langgraph, ChromaDB

### 4.AI for searching relevant information for preparing loan approval documents(_Now -_)
- developing same architecture for above.
  
### 5.AI reporting for Monitoring Financial Product Sales(_Now -_)
- developing genAI System for Analyzing and Reporting on Financial Product Recommendations, Purchases, and Risk Understanding Based on Interview Transcripts

### 6.Object Tracking solution for providing Signage Advertisers with Viewership Metrics and Audience Demographics(_November 2024 - Now_)
- [Background]
We're exploring ways to provide valuable information to advertisers in anticipation of expanding large-scale digital signage at our branches in 2026. I am solely responsible for the AI development, taking a research-oriented approach.<br>
The AI project is divided into 3 phases:<br>
1.  People Counting: Counting the number of people.<br>
2.  Demographic Analysis: Gathering information about the characteristics of the people (e.g., age, gender).<br>
3.  Engagement Tracking: Determining whether people are looking at the digital signage or not.<br>
The initial development of 1st phases was completed on Google Cloud Platform (GCP), using the Mediapipe object detection model and the DeepSort tracking algorithm. However, we are now exploring edge devices due to privacy concerns (PII).

- [AI Process]
Currently, we are planning to use Mediapipe combined with DeepSort. We are also evaluating PINTO-model alongside DeepSort as a potential alternative.<br>
We are in the process of selecting an edge device now. The leading contenders are:<br>
1.Google Coral<br>
2.NVIDIA Jetson Orin Nano 8GB

- [Technical Skills]
Edge computing, mediapipe, pinto-model, deepsort

## Certification([Credly](https://www.credly.com/users/yuta-tokita))
**AWS**<br>
- AWS Certified Cloud Practitioner(_June 2024_)<br>
- AWS Certified Solutions Architect – Associate(_July 2024_)<br>
- AWS Certified AI Practitioner(_February 2025_)<br>

**Google Cloud**<br>
- Associate Cloud Engineer(_July 2024_)<br>
- Advanced Solutions Lab ML Immersive Education(_October 2024_)<br>
- Professional Machine Learning Engineer(_November 2024_)<br>
- Professional Cloud Architect(_May 2025_)<br>


## Competitions Awards
**SIGNATE(Master 85th in 200,000th(🥇1🥈1🥉4)**
[My profile in Signate](https://signate.jp/users/84569)
- 7th in 325th(Solo🥇)<br>
[テクノプロ・デザイン社 食品パッケージ画像解析チャレンジ （一般部門・学生部門）食品パッケージを食料・飲料に分類しよう!](https://signate.jp/competitions/1106)
![comp1](/assets/img/tokita_compe.png)
- 14th in 140th(Solo🥈)<br>
[テクノプロ・デザイン社 日本舞踊の画像・動画解析チャレンジ（学生部門・社会人部門）画像から踊り手が扇子を持っているか否かを当てよう!](https://signate.jp/competitions/1506)


**Kaggle(🥈1)**
[My profile in Kaggle](https://www.kaggle.com/tok1t4)
- 219th in 3757th(Forecasting Competition end in _July 2025_)
[Jane Street Real-Time Market Data Forecasting](https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting)<br>
![comp1](/assets/img/header.png)<br>
Predict financial market responders using real-world data.<br>

## Talks & Lectures
- [Introduce Data Science & Econometrics Laboratory in Hosei Univ.(Youtube)](https://www.youtube.com/watch?v=E-qVjWBCrug&t=257s)
![intro labs](/assets/img/intro_labs.png)<br>

- [AI-agent 実践集中コース LTs hosted by Google.](https://youtu.be/d6A4VnyZTk4)
  
## Publications
1.汎化性能を考慮した食品パッケージの画像分類, 鴇田優太, (2024)<br>
[Abstract](/assets/img/20X4110-0.pdf) [Paper](/assets/img/20X4110-1.pdf) [Slide](/assets/img/20X4110-2.pdf).
