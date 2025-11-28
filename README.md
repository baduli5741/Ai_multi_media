# AI 애니메이션 큐레이터

이 프로젝트는 사용자의 애니메이션 취향을 분석하여 맞춤형 애니메이션 3개를 추천해주는 AI 기반 큐레이터 애플리케이션입니다.

## 🚀 프로젝트 실행 방법 (로컬)

### 1. 의존성 설치

프로젝트 디렉터리로 이동하여 필요한 Node.js 패키지를 설치합니다:

```bash
cd C:\Users\kw\ai-anime-curator
npm install
```

### 2. Gemini API 키 설정

이 애플리케이션은 Google Gemini API를 사용합니다. `GEMINI_API_KEY` 환경 변수에 자신의 Gemini API 키를 설정해야 합니다.

**Windows (PowerShell) 예시:**

```powershell
$env:GEMINI_API_KEY="[YOUR_GEMINI_API_KEY]"; npm start
```

**CMD (명령 프롬프트) 예시:**

```cmd
set GEMINI_API_KEY=[YOUR_GEMINI_API_KEY] && npm start
```

`[YOUR_GEMINI_API_KEY]` 부분에 발급받은 실제 Gemini API 키를 입력하세요.

### 3. 백엔드 서버 시작

API 키 설정 후 다음 명령어로 백엔드 서버를 시작합니다:

```bash
npm start
```

서버가 성공적으로 시작되면 `Backend 서버가 http://localhost:3000 에서 실행 중입니다.` 메시지를 볼 수 있습니다.

### 4. 프론트엔드 접속

백엔드 서버가 실행 중인 상태에서 `index.html` 파일을 웹 브라우저로 열면 애플리케이션을 사용할 수 있습니다.

## 🌐 배포

현재 이 프로젝트는 프론트엔드(`index.html`)와 백엔드(`server.js`)로 구성되어 있습니다.

*   **프론트엔드:** GitHub Pages는 정적 파일만 호스팅하므로, `index.html` 파일은 GitHub Pages에 배포 가능합니다.
*   **백엔드:** `server.js`는 동적 Node.js 서버이므로 GitHub Pages에서 직접 실행할 수 없습니다. 따라서 **Vercel, Netlify, Render**와 같은 Node.js 서버 호스팅을 지원하는 서비스에 별도로 배포해야 합니다.

프론트엔드가 백엔드 API에 접근하려면, `index.html`에서 호출하는 API 엔드포인트(`http://localhost:3000/recommend`)를 배포된 백엔드 서버의 URL로 변경해야 합니다.