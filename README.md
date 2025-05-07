# AI/ML engineer (GenAI enginner)

#### Technical skills 
**Cloud**
- GCP(Main), AWS, Azure(used for Intelligence doccument for pdf processing)
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
- experienced [The ASL ML Immersive Education in Google]((https://cloud.google.com/customers/chiba-bank?hl=ja)), **learned how to build end-to-end ML solutions using tensorflow**  for 3 weeks, **developed 1 prototype(japanese sign language AI using DNN, CNN, Transformer)** for 1 weeks.(_October 2024_)<br>
- developing 5 **ai-agent applications in streamlit on Cloud Run**, keep developing 1 **edge computing** application.

## Projects

## Write down 6 AI applications in detail till _June 2025_

### 1.AI for searching International Balance of Payments Item Numbers(_November 2024 - March 2025_)
- 
  For improving UX(for anyone who has no expertise), checking the PDF pages that RAG retrieving in streamlit app.
- [Technical Skills] Cloud Run, GCS, Streamlit, RAG, langchain, ChromaDB, 

### 2.AI for answering questions regarding loan approval authority(_November 2024 - March 2025_)
- I was **responsible for the end-to-end development of an AI application** designed for eight users. 
- [Background]
This system is utilized within our internal chat application, enabling head office staff to respond to inquiries from branch offices. The distinctive feature is our use of a vector database built from past question-and-answer (Q&A) pairs, rather than from the original manual data. This approach was adopted for two primary reasons:
1.The inquiries often originate from users who couldn't find or understand the answers even after consulting the manual.
2.We aim to generate responses that preserve the nuances and specific tone of the head office staff's previous answers.
- [Evaluation process]
The application's workflow involves storing designated evaluation CSV files in Google Cloud Storage (GCS). These files are then read as blobs into temporary files within the Streamlit interface, and the actual writing of this data is triggered by a button press.
- [Technical Skills]
Cloud Run, GCS, Streamlit, RAG, langchain, ChromaDB

### 3.AI System for Suggestion Triage and Assignment(_March 2025 - May 2025_)
- [Background]
Head office personnel currently receive requests and improvement proposals, identified by branch office staff during their daily operations, through a dedicated suggestion board system. Over the past four years, this system has accumulated approximately 4,000 entries. The responsible personnel requested an AI solution to automate two key tasks: 1) identifying whether newly submitted suggestions duplicate existing ones, and 2) assigning these suggestions to the appropriate department for response.
- [AI process]
An AI system was developed, comprising two primary agents:
1.A Duplicate Detection Agent to identify recurring suggestions.
2.A Department Assignment Agent to allocate suggestions to the relevant department.
- [Evaluation Process]
For evaluation purposes, a designated CSV file containing evaluation data is stored in Google Cloud Storage (GCS). This file is loaded into Streamlit as a temporary blob. Evaluation results are then written to a designated location when a button is pressed within the Streamlit interface, confirming the assessment.
- [Operational Process]
Initially, a vector database is created using all suggestion data accumulated to date. This database is stored in GCS and loaded into Streamlit as a temporary blob for operational use. To add new suggestions, users input the required information for each respective field into text areas on the Streamlit interface. Upon clicking a button, the new suggestion is processed (presumably added via an add_document function or similar mechanism) and the updated data is uploaded to a designated GCS bucket, ensuring the vector database remains current.
- [Technical Skills]
Cloud Run, GCS, Streamlit, RAG, langchain, langgraph, ChromaDB

### 4.

### 5.
### 6.

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


**Kaggle(🥉1)**
[My profile in Kaggle](https://www.kaggle.com/tok1t4)
- 219th in 3757th(Forecasting Competition end in _July 2025_)
[Jane Street Real-Time Market Data Forecasting](https://www.kaggle.com/competitions/jane-street-real-time-market-data-forecasting)<br>
![comp1](/assets/img/header.png)<br>
Predict financial market responders using real-world data.<br>

## Talks & Lectures
- [Introduce Data Science & Econometrics Laboratory in Hosei Univ.(Youtube)](https://www.youtube.com/watch?v=E-qVjWBCrug&t=257s)
![intro labs](/assets/img/intro_labs.png)<br>
  
## Publications
1.汎化性能を考慮した食品パッケージの画像分類, 鴇田優太, (2024)<br>
[Abstract](/assets/img/20X4110-0.pdf) [Paper](/assets/img/20X4110-1.pdf) [Slide](/assets/img/20X4110-2.pdf).
