# 업무 말투 변환기 (Business Tone Converter)

AI 기반 비즈니스 커뮤니케이션 지원 서비스입니다. 일상적인 말투로 입력한 메시지를 선택한 수신 대상(상사, 동료, 고객 등)에 적합한 업무 언어로 변환해 줍니다.

## 기술 스택
- **Frontend**: HTML5, CSS3, JavaScript (Vanilla JS)
- **Backend**: Python 3.11+, FastAPI
- **AI Engine**: Upstage Solar-Pro2 (via LangChain)

## 시작하기

### 백엔드 실행
```bash
cd backend
python -m venv .venv
# 활성화 (Windows)
.venv\Scripts\activate
# 의존성 설치
pip install -r requirements.txt
# 서버 실행
uvicorn main:app --reload --port 8000
```

### 프론트엔드 확인
`frontend/index.html` 파일을 브라우저에서 직접 엽니다.
