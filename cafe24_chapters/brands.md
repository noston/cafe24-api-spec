# BRANDS


## Brands

```json
Endpoints    GET /api/v2/admin/brands
GET /api/v2/admin/brands/count
POST /api/v2/admin/brands
PUT /api/v2/admin/brands/{brand_code}
DELETE /api/v2/admin/brands/{brand_code}
```

```json
GET /api/v2/admin/brands
GET /api/v2/admin/brands/count
POST /api/v2/admin/brands
PUT /api/v2/admin/brands/{brand_code}
DELETE /api/v2/admin/brands/{brand_code}
```

### Brands property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. DEFAULT 1 |
| brand_code | 브랜드 코드 |
| brand_name최대글자수 : [50자] | 브랜드 명 |
| use_brand | 브랜드 사용여부 T : 사용함 F : 사용안함 |
| search_keyword최대글자수 : [200자] | 검색어 설정 |
| product_count | 상품수 |
| created_date | 생성일 |

### Retrieve a list of brands   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| brand_code | 브랜드 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| brand_name | 브랜드 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_brand | 브랜드 사용여부   T : 사용함 F : 사용안함 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of brands        Retrieve a list of brands Retrieve brands with fields parameter Retrieve brands using paging Retrieve a specific brands with brand_code parameter Retrieve multiple brands       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/brands' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "brands": [        {            "shop_no": 1,            "brand_code": "B0000000",            "brand_name": "Default Brand",            "use_brand": "T",            "search_keyword": "keyword",            "product_count": 2,            "created_date": "2017-12-19T14:39:22+09:00"        },        {            "shop_no": 1,            "brand_code": "B000000A",            "brand_name": "Default Brand",            "use_brand": "F",            "search_keyword": "keyword",            "product_count": 3,            "created_date": "2017-12-19T14:39:22+09:00"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/brands' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "brands": [        {            "shop_no": 1,            "brand_code": "B0000000",            "brand_name": "Default Brand",            "use_brand": "T",            "search_keyword": "keyword",            "product_count": 2,            "created_date": "2017-12-19T14:39:22+09:00"        },        {            "shop_no": 1,            "brand_code": "B000000A",            "brand_name": "Default Brand",            "use_brand": "F",            "search_keyword": "keyword",            "product_count": 3,            "created_date": "2017-12-19T14:39:22+09:00"        }    ]}
```

### Retrieve a count of brands   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| brand_code | 브랜드 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| brand_name | 브랜드 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_brand | 브랜드 사용여부   T : 사용함 F : 사용안함 |

```bash
Retrieve a count of brands        Retrieve a count of brands       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```

### Create a brand   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 쓰기권한 (mall.write_collection) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| brand_nameRequired | 브랜드 명 |
| use_brand | 브랜드 사용여부   T : 사용함 F : 사용안함   DEFAULT T |
| search_keyword최대글자수 : [200자] | 검색어 설정 |

```bash
Create a brand        Create a brand Create a brand using only brand_name field Try creating a brand without brand_name field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/brands' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword"    }}'    Response  Copy     {    "brand": {        "shop_no": 1,        "brand_code": "B000000A",        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword",        "created_date": "2017-12-19T14:39:22+09:00"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/brands' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword"    }}'
```

```json
{    "brand": {        "shop_no": 1,        "brand_code": "B000000A",        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword",        "created_date": "2017-12-19T14:39:22+09:00"    }}
```

### Update a brand   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 쓰기권한 (mall.write_collection) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| brand_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 브랜드 코드 |
| brand_name | 브랜드 명 |
| use_brand | 브랜드 사용여부   T : 사용함 F : 사용안함   DEFAULT T |
| search_keyword최대글자수 : [200자] | 검색어 설정 |

```bash
Update a brand        Update a brand Update the brand name Disable the brand       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/B000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword"    }}'    Response  Copy     {    "brand": {        "shop_no": 1,        "brand_code": "B000000A",        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword",        "created_date": "2017-12-19T14:39:22+09:00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/B000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword"    }}'
```

```json
{    "brand": {        "shop_no": 1,        "brand_code": "B000000A",        "brand_name": "Sample Brand",        "use_brand": "T",        "search_keyword": "keyword",        "created_date": "2017-12-19T14:39:22+09:00"    }}
```

### Delete a brand   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 쓰기권한 (mall.write_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| brand_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 브랜드 코드 |

```bash
Delete a brand        Delete a brand       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/B000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "brand": {        "brand_code": "B000000A"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/brands/B000000A' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "brand": {        "brand_code": "B000000A"    }}
```
