## 💡 Prototype
Designed by [Adobe XD](https://www.adobe.com/kr/products/xd.html)

### 1. HY-WEP의 자기소개서 작성 기능에 연결
HY-WEP에서 자기소개서를 작성할 때 **냥소서** 서비스 화면 추가
![prototype(1)](https://user-images.githubusercontent.com/101695597/209562577-36508379-954d-4393-9621-a0908786bce1.png)

### 2. 자기소개서 문항을 입력하면 유형 분류
자기소개서 질문을 입력하면 자기소개/지원동기, 성격/강약점, 역량/관련 활동, 각오/뽑아야 하는 이유 등 4가지로 분류하여, 이에 따라 다른 커리어 데이터를 추천함
![prototype(2)](https://user-images.githubusercontent.com/101695597/209562957-1b58e7af-9f5b-4a15-8d53-8468c1c5a0d0.PNG)

### 3. 추천된 토픽(커리어 데이터)를 활용
자기소개서를 작성할 때 커리어 데이터가 위젯의 형태로 추천되며, 이를 드래그&드랍하면 해당 토픽으로 예시 문장이 작성됨  
![prototype(3)](https://user-images.githubusercontent.com/101695597/209563138-accd6604-3ced-408e-9303-d52a27aa987a.jpg)

## 🚂 Pipeline
### 1. RFC/PoC Composing
아이디어 개요, 목표 등 작성
실현가능성, 필요 성능 등 확인

### 2. Data Crawling & Preprocessing
잡코리아에서 7284건의 자기소개서 문항을 크롤링 후 중복 질문 제거  
지인 10명의 CDP 데이터(적성검사, 학점, 자격증, 수상 경력 등) 조사해 그룹화

### 3. Text Analyzing
초기 목표 : 정답지를 200개 매긴 후 KoBERT 파인 튜닝을 통해 분류 모델 구축  
수정 방안 : 각 유형에 많이 포함되는 단어 20개씩 세팅하여 연관성을 계산하여 임계값 3.5를 넘는 라벨을 모두 뽑도록 설정
