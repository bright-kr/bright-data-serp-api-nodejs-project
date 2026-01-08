# Bright Data SERP API Nodejs project
Bright Data SERP API Nodejs 보일러플레이트 코드

[![Bright Data Promo](https://github.com/bright-kr/LinkedIn-Scraper/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/)


[StackBlitz editor에서 편집 ⚡️](https://stackblitz.com/~/github.com/bright-kr/bright-data-serp-api-nodejs-project?file=index.js)

## Bright Data SERP API example

이 프로젝트는 [Bright Data's SERP API](https://brightdata.co.kr/products/serp-api)를 사용하여 [Bright Data SERP API](https://brightdata.co.kr/products/serp-api)를 통해 차단되지 않고 검색 엔진 쿼리 결과에 접근하는 방법을 보여줍니다.


### StackBlitz에서 환경 변수 사용하기

1. `.env` 파일을 선택합니다
2. 다음 변수를 추가합니다:
   - `BRIGHT_DATA_API_TOKEN`: Bright Data [API Token](https://docs.brightdata.com/general/account/api-token)
   - `BRIGHT_DATA_ZONE`: Bright Data SERP API [Zone](https://brightdata.co.kr/cp/zones) 이름(예: `serp_api1`)

### 직접 구성

또는 스크립트에서 CONFIG 객체를 직접 편집합니다:

```javascript
const CONFIG = {
  apiToken: process.env.BRIGHT_DATA_API_TOKEN || 'YOUR_API_TOKEN', // Replace with your actual token
  zone: process.env.BRIGHT_DATA_ZONE || 'serp_api1',           // Replace with your SERP APIzone
  searchEngineQueryUrl: 'https://geo.brdtest.com/welcome.txt'                 // Replace with your search engine query URL
};
```

## 예제 실행하기

1. `API token`과 `zone`이 구성되었는지 확인합니다
2. 터미널에서 `node index.js`를 실행합니다
3. 결과는 콘솔 출력에서 확인합니다

## 작동 방식은 무엇인가요?

1. 스크립트가 Bright Data의 SERP API API エンドポイント로 POST リクエスト를 보냅니다
2. 認証 토큰과 검색 엔진 쿼리 URL을 포함합니다
3. Bright Data의 SERP API가 검색 엔진 쿼리 URL에 접근합니다
4. レスポンス가 스크립트로 반환되며 콘솔에 표시됩니다

## 문제 해결

오류가 발생하는 경우:

- API token이 올바른지 확인합니다
- zone 이름이 유효한지 확인합니다
- 검색 엔진 쿼리 URL 형식이 올바른지 확인합니다

## 예제 수정하기

다른 URL을 요청하려면:
1. CONFIG 객체에서 `searchEngineQueryUrl`을 업데이트합니다
2. 스크립트를 다시 실행합니다

## 추가 리소스

- [Bright Data SERP API API](https://docs.brightdata.com/scraping-automation/serp-api/introduction)
- [API Token 받기](https://docs.brightdata.com/general/account/api-token)
- [Zones 관리](https://brightdata.co.kr/cp/zones)

**Note:** 이는 교육 목적의 예시 구현입니다. 프로덕션에서 사용하려면 추가적인 오류 처리, 로깅 및 보안 조치 추가를 고려하시기 바랍니다.