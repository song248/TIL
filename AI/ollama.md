# Ollama
https://ollama.com/  
  
로컬 환경에서 대규모 언어 모델(LLM)을 쉽게 실행하고 관리할 수 있도록 도와주는 오픈소스 도구  

## Ollama의 주요 특징
1. 로컬 실행
    - 클라우드 없이 로컬에서 LLM을 실행할 수 있어 개인정보 보호와 보안성이 뛰어남
    - 인터넷 연결 없이도 사용할 수 있어 개발 및 연구에 유용함
2. 간편한 설치와 실행
    - ollama run <모델명> 명령어 한 줄로 모델 실행 가능
    - 별도의 복잡한 설정 없이도 사용할 수 있음
3. 경량화된 모델 지원
    - 최신 경량화 모델을 활용하여 비교적 적은 리소스로 LLM을 실행할 수 있음
    - Mistral, Llama, Gemma 등의 다양한 오픈소스 LLM 지원
4. 커스텀 모델 구축 가능
    - 기존 모델을 수정하거나, 새로운 모델을 추가할 수 있음
    - Modelfile을 사용해 모델을 튜닝 가능
5. FastAPI와의 통합 가능
    - REST API 형태로 LLM을 제공할 수 있어 웹 애플리케이션과 쉽게 연동 가능
  
  
<br></br>


## Ollama와 Open-WebUI 이용한 local AI챗봇 세팅
1. Ollama 세팅
```
curl -fsSL https://ollama.com/install.sh | sh
ollam --version
```
ollama version is 0.5.7  
  

```
ollama run llama3.2:3b
ollama list
```

2. Open WebUI
- Docker 이용
```
sudo apt update && sudo apt install -y docker.io
docker --version
```
Docker version 27.5.0, build a187fa5    
    
```
sudo apt install -y docker-compose
docker-compose --version
```

```
docker run -d \
  --name open-webui \
  -p 3000:3000 \
  -v open-webui-data:/app/backend/data \
  --network host \
  ghcr.io/open-webui/open-webui:main
```
- 접속정보  
http://localhost:3000 or http://localhost:8080
