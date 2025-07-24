# AI/ML engineer 

※ Modified in _20250724

#### Technical skills 
**Cloud**
- GCP, AWS

**Python Framework**
- Pytorch, Tensorflow, Keras, timm, onnx, ultralytics, mediapipe, opencv...
  
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

#### Task 
- Reduce manual reference time and develop an AI that enables anyone to make judgments by referencing past cases and manuals.

#### Solution
Developed a RAG system (indexing, retrieving, and generation) using the following steps:<br>

1. Chunking the PDF document.
2. Created a searchable document from the chunks by embedding.
3. Implemented the RAG system using Langchain and Chroma DB.
4. Deployed the system on Cloud Run with a Streamlit interface.
5. Integrated a feature to display specific pages of the original PDF to allow users to easily verify information sources.

#### Result
achieved approximately 80% accuracy (rated as "correct" or "helpful"). 

#### Technical Skills
Cloud Run, GCS, Streamlit, RAG, langchain, ChromaDB, 

### 2.AI for answering questions regarding loan approval authority(_November 2024 - March 2025_)

#### Situation
- There are manuals that detail the scope of approval authority for branch managers, indicating what falls under their discretion versus what requires formal deliberation. The Corporate Support Department receives and addresses inquiries on this matter.
- Branch managers and deputy loan managers(branch offices) needed to exercise extreme caution with loan approval authorities, where mistakes were unacceptable. The Corporate Support Department received approximately 80 inquiries per month, many of which were not resolved by manuals. Now, This AI is utilized within our internal chat application, enabling The Corporate Support Department's staff to respond to inquiries from branch offices. The distinctive feature is our use of a vector database built from past question-and-answer (Q&A) pairs, rather than from the original manual data. This approach was adopted for two primary reasons:
  
  1. The inquiries often originate from users who couldn't find or understand the answers even after reading the manual.
  2. We aim to generate responses that preserve the nuances and specific tone of the head office staff's previous answers.

#### Task
Develop an end-to-end AI application integrated with the internal chat system to serve as a response assistant. This involved building a vector database from approximately 5,000 past Q&A pairs (not manuals) to address complex inquiries and preserve the specific tone of HQ responses.

#### Action
Constructed a vector database using actual past Q&A cases. Implemented RAG to format answers (e.g., "answer," "conditions," "references") to maintain the nuance of HQ responses. Designed and developed the AI application for 8+ users. Implemented an evaluation process using CSV files stored in GCS, readable as temporary blobs in Streamlit.

#### Result
Achieved approximately 80% accuracy in responses. User feedback was highly positive, including "reduced search time," "helpful phrasing," "no need to search manuals from scratch," "past answers are helpful," and "highly efficient for similar cases." This not only reduced HQ staff's inquiry handling time but also supported branch staff in making quick and accurate decisions, improving overall operational quality.

#### Technical Skills
Cloud Run, GCS, Artifact Registry Streamlit, RAG, langchain, ChromaDB

### 3.AI for Suggestion Duplication and Assignment (_March 2025 - May 2025_)

#### Situation
Headquarters received requests and improvement proposals, identified by branch office staff during their daily operations, through a dedicated suggestion board system. Over the past four years, this system has accumulated approximately 4,000 unique entries. Identifying duplicate suggestions and assigning them to the correct department was time-consuming, taking up to 15 minutes per suggestion even for experienced staff, and more for new hires.

#### Task
Develop an AI solution to automate the identification of duplicate suggestions and their assignment to appropriate departments:

1. identifying whether newly submitted suggestions duplicate existing ones.
2. assigning these suggestions to the appropriate department for response.

#### Action
Developed an AI system comprising a Duplicate Detection Agent and a Department Assignment Agent. Constructed a vector database from all existing suggestion data, stored it in GCS, and loaded it as a temporary blob into Streamlit for operational use. Implemented a real-time update mechanism where users could input new suggestions via Streamlit, triggering a database update and upload to GCS, ensuring data currency.

#### Result
The similar suggestion search feature was highly praised, especially by new staff. The AI successfully reduced the time for duplicate checking from an average of 15 minutes to approximately 1 minute per suggestion, resulting in an annual saving of approximately 233 hours (14 minutes saved per suggestion × 1,000 suggestions = 14,000 minutes) for processing around 1,000 proposals annually.


#### Technical Skills
Cloud Run, GCS, Artifact Registry , Streamlit, RAG, langchain, langgraph, ChromaDB

### 4.Object Tracking Solution for Providing Signage Advertisers with Viewership Metrics and Audience Demographics (_November 2024 - Present_)

#### Situation
Anticipating a large-scale digital signage expansion in branches by 2026, the goal was to provide valuable data (viewership metrics, audience demographics) to advertisers. Privacy concerns (PII) necessitated exploring on-site data processing(local PC) or edge device solutions.

#### Task
Lead AI development in three phases: People Counting, Demographic Analysis, and Engagement Tracking, with a research-oriented approach. Focus on Phase 1 POC and feasibility of edge device migration.

#### Action
Completed initial Phase 1 (People Counting) development on GCP using Mediapipe object detection and DeepSort tracking. Migrated the cloud POC model to a local PC environment for in-house experiments with internal and 1080P USB cameras. Identified that high-definition cameras are crucial for accuracy. Identified NVIDIA Jetson Orin Nano 8GB as a key edge device for future scaling and operational use.

#### Result
The local POC validated the approach and clarified future development direction. The established roadmap includes selecting high-performance cameras, consulting legal counsel regarding PII handling in video data, and concurrently developing Phase 2 & 3 advanced models. Migration to NVIDIA Jetson Orin Nano 8GB is anticipated to support scalability and privacy protection for future large-scale deployments.

#### Technical Skills
mediapipe, pinto-model, deepsort, yolo11(ultralytics)

### 5.AI reporting for Monitoring Financial Product Sales(_Now -_)
- developing genAI System for Analyzing and Reporting on Financial Product Recommendations, Purchases, and Risk Understanding Based on Interview Transcripts
- develop on VScode ssh connection to EC2 on AWS.


### 6.AI for searching relevant information for preparing loan approval documents(Pending)
- developing same architecture for project2.



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


## Talks & Lectures
- [Introduce Data Science & Econometrics Laboratory in Hosei Univ.(Youtube)](https://www.youtube.com/watch?v=E-qVjWBCrug&t=257s)
![intro labs](/assets/img/intro_labs.png)<br>

- [AI-agent 実践集中コース Linghtning Talks hosted by Google.](https://youtu.be/d6A4VnyZTk4)
  
## Publications
1.汎化性能を考慮した食品パッケージの画像分類, 鴇田優太, (2024)<br>
[Abstract](/assets/img/20X4110-0.pdf) [Paper](/assets/img/20X4110-1.pdf) [Slide](/assets/img/20X4110-2.pdf).
