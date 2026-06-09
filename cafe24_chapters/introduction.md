# INTRODUCTION


## Introduction

### Cafe24 API

### API Diagram

### Request/Response Format

```bash
요청 예제 (조회)   cURL Java Python Node.js PHP Go      curl -X GET \  'https://{mallid}.cafe24api.com/{endpoint_url}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    요청 예제 (등록/수정)   cURL Java Python Node.js PHP Go      curl -X POST \  'https://{mallid}.cafe24api.com/{endpoint_url}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{ .... }'    정상 응답 예제    {
  "resource": {
      "key": "value",
      "key": "value"
   }
}    에러 응답 예제    {
  "error": {
      "code": "error code",
      "message": "error message",
      "more_info": {
      }
  }
}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/{endpoint_url}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/{endpoint_url}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{ .... }'
```

```json
{
  "resource": {
      "key": "value",
      "key": "value"
   }
}
```

```json
{
  "error": {
      "code": "error code",
      "message": "error message",
      "more_info": {
      }
  }
}
```

### Method

### Admin API Intro

```json
사용 예시    https://{mallid}.cafe24api.com/api/v2/admin/sampleapi
```

```json
https://{mallid}.cafe24api.com/api/v2/admin/sampleapi
```

### API Status Code

| Code | 발생하는 사례 | 오류 해결 방법 |
| --- | --- | --- |
| 200 | GET 성공, PUT 성공, DELETE 성공시 |  |
| 201 | POST 성공시 |  |
| 202 | 비동기 처리 요청이 접수되었으나 아직 처리가 완료되지 않은 경우 |  |
| 204 | DELETE 성공시 응답 본문이 없는 경우 |  |
| 207 | 다중 요청 등록시 상태가 객체별로 다른 경우 | 오류 상태를 객체별로 확인하여 해당 상태에 따라 대응합니다. |
| 400 | 서버에서 요청을 이해할 수 없음1) Content-Type이 잘못 지정되어있음2) application/type이 json이 아님 | 요청시 "Content-Type"이 application/json으로 되어있는지 확인합니다. |
| 400 | 요청 API URL에 한글 또는 특수문자를 인코딩하지 않고 그대로 사용한 경우 | 요청 API URL에 한글 또는 특수문자를 URL 인코딩하였는지 확인합니다. |
| 401 | 1) Access Token 없이 호출한 경우2) Access Token이 유효하지 않은 경우3) Access Token이 만료된 경우4) 알 수 없는 클라이언트일 경우 | 유효한 발급 절차에 따라 발급받은 Access Token을 사용하였는지 확인합니다. |
| 401 | Front API 사용시 client_id를 미입력한 경우 | 유효한 클라이언트 ID를 사용하였는지 확인합니다. |
| 403 | 1) Access Token은 있으나 해당 Scope에 권한이 없음2) Front API에서 볼 수 있는 권한이 없을 경우 | API를 호출할 수 있는 권한이 있는지 API의 Scope 또는 쇼핑몰의 설정을 확인합니다. |
| 403 | https 프로토콜이 아닌 경우 | API 요청시 https 로 요청하였는지 확인합니다. |
| 403 | 뉴상품 쇼핑몰이 아닌 경우 | 쇼핑몰이 (뉴)상품관리로 업그레이드 되어야 사용 가능합니다. |
| 403 | (Admin API 호출시) 쇼핑몰에서 해당 앱이 삭제된 경우 | 쇼핑몰에 앱이 설치되었는지 확인 후 앱을 다시 설치합니다. |
| 403 | (Front API 호출시) 쇼핑몰에서 해당 앱이 삭제된 경우 | 쇼핑몰에 앱이 설치되었는지 확인 후 앱을 다시 설치합니다. |
| 403 | (Customer API 호출시) 쇼핑몰에서 해당 앱이 삭제된 경우 | 쇼핑몰에 앱이 설치되었는지 확인 후 앱을 다시 설치합니다. |
| 404 | 1) API URL을 잘못 호출한 경우2) 리소스를 찾을 수 없을 경우3) {#id}가 없는 경우 | 엔드포인트 URL의 오류가 있는지 API 문서를 참고하여 확인합니다. |
| 409 | 동일 리소스에 동일 내용을 업데이트할 경우 | 수정할 데이터를 요청해주세요. |
| 422 | 조회/처리 요청시 값이 정해진 스펙과 다를 경우1) 필수 파라메터 누락함2) 정해진 스펙과 다를 경우 | API 문서를 참고하여 필수 파라메터가 입력되지 않았거나 유효하지 않은 값을 입력하였는지 확인합니다. |
| 429 | 클라이언트의 API 요청이 Bucket을 초과한 경우 | API 최대 허용 요청 건수를 초과하지 않도록 잠시 후 다시 요청합니다. |
| 500 | 내부 서버 에러, 알 수 없는 에러 | 일시적으로 에러가 발생하였습니다. 잠시 후에 다시 시도합니다. |
| 503 | 현재 서버가 다운된 경우 | 개발자센터로 문의해주세요. |
| 503 | 서버가 다운된 경우. API를 사용할 수 없음. | 개발자센터로 문의해주세요. |
| 504 | 요청 시간이 초과된 경우(Timeout) | 일시적으로 에러가 발생하여 응답이 지연되고 있습니다. 잠시 후에 다시 시도해주세요. |

### How to use GET API

#### 1. 검색조건 추가

```json
검색조건 추가  예) 특정 브랜드 내에서 상품 판매가가 1000원 이상인 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?brand_code=B000000A&price_min=1000    예) 상품 등록일 범위를 지정하여 상품 조회 GET https://{mallid}.cafe24api.com/api/v2/admin/products?created_start_date=2018-01-03&created_end_date=2018-02-03 예) 상품 수정일 범위를 지정하여 상품 조회 GET https://{mallid}.cafe24api.com/api/v2/admin/products?updated_start_date=2018-01-03T14:01:26+09:00&updated_end_date=2018-02-03T14:01:26+09:00 ```
```

```json
예) 특정 브랜드 내에서 상품 판매가가 1000원 이상인 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?brand_code=B000000A&price_min=1000
```

#### 2. 콤마로 여러 건을 검색

```json
콤마로 여러 건을 검색    예) 특정 상품번호를 지정하여 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=11,12,13

예) 특정 상품번호와 상품코드를 지정하여 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=11,12,13&product_code=P000000X,P000000W
```

```json
예) 특정 상품번호를 지정하여 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=11,12,13

예) 특정 상품번호와 상품코드를 지정하여 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=11,12,13&product_code=P000000X,P000000W
```

#### 3. 멀티쇼핑몰 정보 조회

```json
멀티쇼핑몰 정보 조회    예) 특정 멀티쇼핑몰의 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?shop_no=2
```

```json
예) 특정 멀티쇼핑몰의 상품 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?shop_no=2
```

#### 4. 상세 조회와 단건 조회

```json
상세 조회와 단건 조회    예) 특정 상품번호를 지정하여 상품 상세 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products/128

예) 특정 상품번호를 지정하여 상품 단건 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=128
```

```json
예) 특정 상품번호를 지정하여 상품 상세 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products/128

예) 특정 상품번호를 지정하여 상품 단건 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?product_no=128
```

#### 5. Pagination

```json
Pagination    예 ) 상품 100개 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?limit=100

예) 201번째 상품부터 300번째 상품까지 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?limit=100&offset=200
```

```json
예 ) 상품 100개 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?limit=100

예) 201번째 상품부터 300번째 상품까지 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?limit=100&offset=200
```

#### 6. 특정 항목 조회

```json
특정 항목 조회    예) 상품명과 상품번호 항목만 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?fields=product_name,product_no
```

```json
예) 상품명과 상품번호 항목만 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products?fields=product_name,product_no
```

#### 7. 하위 리소스 조회

```json
하위 리소스 조회    예) 상품 조회시 품목과 재고 데이터를 함께 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products/570?embed=variants,inventories
```

```json
예) 상품 조회시 품목과 재고 데이터를 함께 조회
GET https://{mallid}.cafe24api.com/api/v2/admin/products/570?embed=variants,inventories
```

### API Limit

#### 요청 수 제한

```json
X-Api-Call-Limit : 1/40
```

```json
X-Api-Call-Limit : 1/40
```

#### 사용량 제한

```json
X-Cafe24-Call-Usage : 120.04
X-Cafe24-Call-Remain : 32
X-Cafe24-Time-Usage : 100.5
X-Cafe24-Time-Remain : 7
```

```json
X-Cafe24-Call-Usage : 120.04
X-Cafe24-Call-Remain : 32
X-Cafe24-Time-Usage : 100.5
X-Cafe24-Time-Remain : 7
```

### Versioning

```bash
예시 코드 (요청)   cURL Java Python Node.js PHP Go      curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/categories' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: 2026-03-01'
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/categories' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: 2026-03-01'
```
