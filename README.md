# Python Calculator - FastAPI 기반 웹 계산기

## 프로젝트 개요
이 프로젝트는 **FastAPI를 활용한 웹 기반 계산기**입니다.
사용자는 웹 인터페이스를 통해 입력값을 제공하고, 서버에서 연산을 수행한 후 결과를 반환합니다.

## 주요 기능
- **FastAPI 기반 RESTful API 제공** (`POST /compute`)
- **HTML, CSS, JavaScript 기반 웹 인터페이스 제공**
- **덧셈, 뺄셈, 곱셈, 나눗셈, 거듭제곱, 나머지 연산 지원**
- **정적 파일 서빙 (HTML, CSS, JS 포함)**

## 프로젝트 구조
```
python-calculator/
│── main.py  # FastAPI 서버 실행 파일
│── operation.py  # 연산 기능 구현 (덧셈, 뺄셈, 곱셈, 나눗셈 등)
│── util.py  # 문자열을 숫자로 변환하는 유틸리티 함수
│── requirements.txt  # 필요 라이브러리 목록
│── static/
│   ├── index.html  # 웹 계산기 UI
│   ├── css/styles.css  # 스타일링 파일
│   ├── js/main.js  # 클라이언트 로직
│── README.md  # 프로젝트 설명 파일
```

## 설치 및 실행 방법
### 1. 필수 라이브러리 설치
```bash
pip install -r requirements.txt
```

### 2. FastAPI 애플리케이션 실행
```bash
uvicorn main:app --reload
```

### 3. 웹 UI 접속
웹 브라우저에서 다음 주소로 접속:
```
http://127.0.0.1:8000/
```

## API 사용 방법
### 1. 수식 계산 요청 (`POST /compute`)
- **요청 예시**:
    ```json
    {
        "operands": ["10", "2"],
        "operators": ["+"]
    }
    ```
- **응답 예시**:
    ```json
    {
        "message": "success",
        "answer": 12
    }
    ```

## 필요 라이브러리
- `fastapi`
- `uvicorn`

## 기여 방법
1. 본 레포지토리를 포크합니다.
2. 새로운 브랜치를 생성합니다.
3. 변경 사항을 커밋하고 푸시합니다.
4. Pull Request를 생성하여 기여합니다.

## 라이선스
이 프로젝트는 MIT 라이선스를 따릅니다.

