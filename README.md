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

패션 추천 챗봇은 사용자의 질문과 답변을 분석하여 개인 맞춤형 패션 이미지를 생성하고 트렌드를 추천하는 시스템 

<br> 

이 과정은 크게 세 가지 단계로 구성된다: 

 - 1. 텍스트(PROMPT) 분석 
 - 2. Stable Diffusion 모델을 활용한 이미지 생성 
 - 3. 최종 패션 추천.

<br>

### 1. 텍스트(PROMPT) 분석
#### 사용자가 패션 관련 질문을 입력하면 챗봇은 이를 해석하고 적절한 답변을 제공한다. 이 과정에서 챗봇은 사용자의 패션 선호도를 파악하며, 정보가 부족한 경우 추가 질문을 통해 보다 상세한 정보를 수집한다.

- 사용자 질문 입력

사용자가 챗봇에게 패션 관련 질문을 한다.
예를 들어, "올봄 트렌드 컬러는 무엇인가요?" 또는 "데이트룩 추천해 주세요." 같은 질문이 포함될 수 있다.
챗봇의 답변 및 추가 질문

챗봇은 기존 데이터베이스에 저장된 정보를 바탕으로 답변을 제공한다.
그러나 사용자의 패션 선호도가 명확하지 않을 경우, 추가 질문을 통해 세부 정보를 수집한다.
예를 들어, "평소 선호하는 스타일이 무엇인가요? 클래식, 스트릿, 미니멀 중에서 선택해 주세요."와 같은 질문을 던질 수 있다.
패션 선호도 파악 및 데이터 축적

사용자의 답변을 바탕으로 패션 취향을 분석한다.
이를 데이터베이스에 저장하여 향후 보다 정교한 맞춤형 추천이 가능하도록 한다.

### 2. Stable Diffusion을 활용한 패션 이미지 생성
#### 사용자의 선호도가 파악되면, 이를 기반으로 Stable Diffusion 모델을 활용해 패션 이미지를 생성한다.

- Stable Diffusion 모델 활용

Musinsaigo Stable Diffusion 모델을 사용하여 사용자의 취향에 맞는 패션 이미지를 생성한다.
예를 들어, "스트릿 스타일의 봄 패션"을 원한다면 해당 콘셉트에 맞는 패션 이미지를 만들어낸다.
사용자 기호에 따른 이미지 조정

생성된 이미지가 사용자의 스타일과 정확히 일치하지 않을 경우, 피드백을 반영하여 추가적으로 조정할 수 있다.
이를 통해 사용자가 더욱 만족할 수 있는 맞춤형 패션 이미지를 제공한다.

### 3. 맞춤형 패션 추천
#### Musinsaigo 모델을 통해 생성된 이미지를 기반으로, 최종적으로 사용자에게 적합한 패션 스타일과 트렌드를 추천한다.

 - 개인 맞춤형 패션 이미지 제공

사용자의 취향과 최신 트렌드를 반영한 스타일을 제안한다.
예를 들어, "2024년 봄 트렌드에 맞는 미니멀 룩" 등의 추천이 가능하다.

- 트렌드 분석 및 제안

최신 패션 트렌드를 분석하여 사용자에게 유용한 정보를 제공한다.
예를 들어, 현재 인기 있는 컬러, 패턴, 스타일을 반영하여 스타일링 팁을 함께 제공할 수 있다.

<br>

 > # <b> 4. 챗봇 예시
 <img width="1000" alt="Image" src="https://github.com/user-attachments/assets/03bed83c-e435-47b4-b808-662f3c08b222" />

<br>

 > # <b> 5. 결론 </b>
이러한 과정을 통해 패션 추천 챗봇은 단순한 텍스트 기반의 추천을 넘어, AI 기반의 이미지 생성과 맞춤형 트렌드 분석을 결합하여 보다 직관적이고 효과적인 패션 추천 서비스를 제공한다. 이를 통해 사용자는 자신의 취향에 맞는 스타일을 쉽고 빠르게 찾을 수 있으며, 최신 트렌드까지 반영된 맞춤형 패션 제안을 받을 수 있다.
 
