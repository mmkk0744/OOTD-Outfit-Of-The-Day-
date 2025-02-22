# 2023 미디어 뉴테크 경진대회 [유스리그] - <br> 사용자를 위한 의류 추천시스템 서비스 구축

<br>

> # <b> 1. 아이디어 배경 </b>
<br>
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/a65cab86-3594-48a1-be48-d655c4b40476" />

- 국내 인공지능 시장은 2023년 기준 향후 5년간 연평균 성장률 14.9%를 기록하며 2027년까지 4조억원 규모에 이를 전망
- 4차 산업혁명 기술 특허출원이 10년간 연평균 14.7%씩 성장한 가운데, AI 기술이 특허 출원량(27.2%)로 1위를 차지

<br>

<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/70a80137-8b54-44db-ad03-af2201d8eab0" />

- 생성형 AI란, 텍스트나 이미지, 음성 등을 생성하는 데 특화된 인공지능을 의미함
- 서비스 목적에 따라 생성형 AI 모델을 개발하는데, Chat GPT와 같은 챗봇 서비스에 가장 널리 쓰이고 있음


<br>

 > # <b> 2. 데이터 수집 및 전처리 </b>
<img width="1000" alt="Image" src="https://github.com/user-attachments/assets/2f46ab22-f79d-4726-bc69-31a92c2bf2c6" />

 ### 1. Hugging Face 모델 로드 및 설정
 #### youngmki/musinsaigo-2.0 및 stabilityai/stable-diffusion-xl-base-1.0 모델을 Hugging Face에서 다운로드하고, Lora 가중치를 적용하여 Stable Diffusion 파이프라인을 구축합니다.
 
 ### 2. STABLE DIFFUSION을 위한 데이터 전처리
 #### 수집된 이미지 데이터를 Stable Diffusion 모델 학습 및 활용에 적합하도록 리사이징, 필터링, 보정 등의 전처리를 수행합니다.
 
 ### 3. STABLE DIFFUSION 모델링 진행
 #### 최적의 결과를 도출하기 위해 Stable Diffusion 모델을 학습시키고, 필요한 파라미터를 조정하여 이미지 생성의 품질을 개선합니다.
 
 ### 4. STABLE DIFFUSION을 활용한 이미지 생성
 #### 학습된 Stable Diffusion 모델을 활용하여 새로운 패션 스타일과 트렌드를 반영한 이미지를 생성합니다.
 
 ### 5. 생성된 이미지 검토 및 후처리
 #### 생성된 이미지의 품질을 평가하고, 필요에 따라 보정 및 후처리를 수행하여 최종적으로 활용 가능한 결과물을 완성합니다.

 <br>
 
 > # <b> 3. 챗봇 운영 프로세스 </b>
 <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/f72ef9ac-0a79-4aca-872f-5404a6b43b7e" />

 
