# 📚 감성 대화 챗봇 프로젝트

 이 프로젝트는 BERT&GPT 파인튜닝을 활용한 감성 대화 챗봇을 구현하는 것을 목표로 한다.
 
 챗봇은 사용자의 입력 문장의 감정을 분석하고 해당 감정을 적절하게 응답 문장에 반영하여, 사용자와 자연스러운 대화를 수행할 수 있다.

<br>

## 🏗️ 프로젝트 구조

* `fine-tuned-bert`
  - BERT 모델을 fine-tuning 하고 테스트하는 코드가 포함되어 있다. 실제 모델은 Hugging Face에 저장되어 있으며, 이 프로젝트를 실행하는 데 있어서 해당 repo는 clone할 필요가 없다. 모델은 backend 쪽 코드에서 자동으로 불러온다.

* `nlp-model-server`
  - 백엔드 코드가 포함되어 있다. Flask를 사용하여 구현되었으며, BERT 모델을 불러와 사용자의 입력을 처리하고 응답을 생성하는 서버 역할을 한다.

* `.github`
  - 프로젝트 설명 및 사용법이 포함되어 있다.

* `emotion-helper-web`
  - 프론트엔드 코드가 포함되어 있다. React로 개발되었으며, 사용자와의 인터페이스를 담당하고 백엔드와 통신하여 사용자와의 대화를 제어한다.

* `documents-archive`
  - 프로젝트와 관련된 문서 및 자료가 저장되어 있다.

<br>

## 🏃 설치 및 실행

### 1. nlp-model-server
1. repo clone
```shell
git clone https://github.com/khucd-pringles/nlp-model-server.git
```
2. 필수 패키지 설치
```shell
cd nlp-model-server
pip install -r requirements.txt
```
3. 서버 실행
```shell
python app.py
```

### 2. emotion-helper-web
1. repo clone
```shell
git clone https://github.com/khucd-pringles/emotion-helper-web.git
```
2. 필수 패키지 설치
```shell
cd emotion-helper-web
npm install
```
3. 애플리케이션 실행
```shell
npm start
```
