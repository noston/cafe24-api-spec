# SCRIPTTAGS


## Scripttags

```json
Endpoints    GET /api/v2/admin/scripttags
GET /api/v2/admin/scripttags/count
GET /api/v2/admin/scripttags/{script_no}
POST /api/v2/admin/scripttags
PUT /api/v2/admin/scripttags/{script_no}
DELETE /api/v2/admin/scripttags/{script_no}
```

```json
GET /api/v2/admin/scripttags
GET /api/v2/admin/scripttags/count
GET /api/v2/admin/scripttags/{script_no}
POST /api/v2/admin/scripttags
PUT /api/v2/admin/scripttags/{script_no}
DELETE /api/v2/admin/scripttags/{script_no}
```

### Scripttags property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| script_no | script의 고유번호 스크립트의 고유 번호 |
| client_id | Client ID 스크립트를 설치한 Client의 ID |
| srcURL | 원본 script 경로 설치할 스크립트의 원본 경로(절대 경로) |
| display_location | 화면 경로 스크립트를 표시할 "화면 경로". 화면 경로는 화면의 페이지 경로가 아니라 쇼핑몰의 각 페이지에 부여된 특정한 역할을 의미함. (예 : 상품분류(product_list)에 스크립트를 삽입할 경우 쇼핑몰에서 상품분류로 사용되는 모든 페이지에 스크립트가 노출됨)  화면의 역할은 해당 페이지에 사용된 모듈에 따라 자동으로 부여됨. 임의의 페이지에 상품분류 모듈을 추가하면 해당 페이지는 "상품분류" 역할로 인식된다. 쇼핑몰 관리자 화면의 [쇼핑몰 설정 > 사이트 설정 > '사이트 환경 설정 > 쇼핑몰 환경 설정 > 화면경로 > 화면경로 설정']에서 각 페이지에 부여된 화면 역할을 조회하고 설정할 수 있음.  "all" 일 경우 전체 페이지에 스크립트가 적용됨.  display_location_code |
| exclude_path | 제외 경로 |
| skin_no | 스킨 번호 스크립트를 적용할 스킨 번호 |
| integrity | 하위 리소스 무결성 스크립트 위변조를 방지하기위한 무결성 검증용 해시. (sha384, sha512 해시 알고리즘 지원)  Integrity 해시 생성방법 참고 |
| created_date | 생성일 스크립트 설치 날짜 |
| updated_date | 수정일 스크립트 수정 날짜 |

### Retrieve a list of script tags   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| script_no | script의 고유번호   스크립트의 고유 번호 검색 |
| srcURL | 원본 script 경로   원본 스크립트 경로 검색 |
| display_location | 화면 경로   스크립트를 표시할 "화면 경로". 화면 경로는 화면의 페이지 경로가 아니라 쇼핑몰의 각 페이지에 부여된 특정한 역할을 의미함. (예 : 상품분류(product_list)에 스크립트를 삽입할 경우 쇼핑몰에서 상품분류로 사용되는 모든 페이지에 스크립트가 노출됨)  화면의 역할은 해당 페이지에 사용된 모듈에 따라 자동으로 부여됨. 임의의 페이지에 상품분류 모듈을 추가하면 해당 페이지는 "상품분류" 역할로 인식된다. 쇼핑몰 관리자 화면의 [쇼핑몰 설정 > 사이트 설정 > '사이트 환경 설정 > 쇼핑몰 환경 설정 > 화면경로 > 화면경로 설정']에서 각 페이지에 부여된 화면 역할을 조회하고 설정할 수 있음.  "all" 일 경우 전체 페이지에 스크립트가 적용됨.  display_location_code    ,(콤마)로 여러 건을 검색할 수 있다. |
| exclude_path | 제외 경로   ,(콤마)로 여러 건을 검색할 수 있다. |
| skin_no | 스킨 번호   스크립트를 적용할 스킨 번호   ,(콤마)로 여러 건을 검색할 수 있다. |
| integrity | 하위 리소스 무결성 |
| created_start_date날짜 | 스크립트 설치일 검색 시작일   스크립트 설치 날짜가 해당 날짜 이후인 스크립트 검색 검색 종료일과 같이 사용해야함. |
| created_end_date날짜 | 스크립트 설치일 검색 종료일   스크립트 설치 날짜가 해당 날짜 이전인 스크립트 검색 검색 시작일과 같이 사용해야함. |
| updated_start_date날짜 | 스크립트 수정일 검색 시작일   스크립트 수정 날짜가 해당 날짜 이후인 스크립트 검색 검색 종료일과 같이 사용해야함. |
| updated_end_date날짜 | 스크립트 수정일 검색 종료일   스크립트 수정 날짜가 해당 날짜 이전인 스크립트 검색 검색 시작일과 같이 사용해야함. |

```bash
Retrieve a list of script tags        Retrieve a list of script tags Retrieve scripttags with fields parameter Retrieve a specific scripttags with script_no parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "scripttags": [        {            "shop_no": 1,            "script_no": "1509432821494844",            "client_id": "AMj8UZhBC9zsyTlFGI6PzC",            "src": "https://yourdomain-sample.com/sample-script.js",            "display_location": [                "BOARD_FREE_LIST"            ],            "skin_no": [                1,                2            ],            "exclude_path": [                "/board/free/list.html"            ],            "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",            "created_date": "2017-10-31T15:53:41+09:00",            "updated_date": "2017-11-03T18:05:32+09:00"        },        {            "shop_no": 1,            "script_no": "1509699932016345",            "client_id": "AMj8UZhBC9zsyTlFGI6PzC",            "src": "https://yourdomain-sample.com/sample-script.js",            "display_location": [                "PRODUCT_LIST",                "PRODUCT_DETAIL"            ],            "skin_no": null,            "exclude_path": null,            "integrity": "sha512-liS6Zvj8DUdCw4DyxdGvS3Bo1REcsEQBia6/MKKl2xgVGlUspT5MlCmFfdbtM32rwqwEgIUzJrgUYZFUsKcEeg==",            "created_date": "2017-11-03T18:05:32+09:00",            "updated_date": "2017-11-03T18:05:32+09:00"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "scripttags": [        {            "shop_no": 1,            "script_no": "1509432821494844",            "client_id": "AMj8UZhBC9zsyTlFGI6PzC",            "src": "https://yourdomain-sample.com/sample-script.js",            "display_location": [                "BOARD_FREE_LIST"            ],            "skin_no": [                1,                2            ],            "exclude_path": [                "/board/free/list.html"            ],            "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",            "created_date": "2017-10-31T15:53:41+09:00",            "updated_date": "2017-11-03T18:05:32+09:00"        },        {            "shop_no": 1,            "script_no": "1509699932016345",            "client_id": "AMj8UZhBC9zsyTlFGI6PzC",            "src": "https://yourdomain-sample.com/sample-script.js",            "display_location": [                "PRODUCT_LIST",                "PRODUCT_DETAIL"            ],            "skin_no": null,            "exclude_path": null,            "integrity": "sha512-liS6Zvj8DUdCw4DyxdGvS3Bo1REcsEQBia6/MKKl2xgVGlUspT5MlCmFfdbtM32rwqwEgIUzJrgUYZFUsKcEeg==",            "created_date": "2017-11-03T18:05:32+09:00",            "updated_date": "2017-11-03T18:05:32+09:00"        }    ]}
```

### Retrieve a count of script tags   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| script_no | script의 고유번호   스크립트의 고유 번호 검색 |
| srcURL | 원본 script 경로   원본 스크립트 경로 검색 |
| display_location | 화면 경로   스크립트를 표시할 "화면 경로". 화면 경로는 화면의 페이지 경로가 아니라 쇼핑몰의 각 페이지에 부여된 특정한 역할을 의미함. (예 : 상품분류(product_list)에 스크립트를 삽입할 경우 쇼핑몰에서 상품분류로 사용되는 모든 페이지에 스크립트가 노출됨)  화면의 역할은 해당 페이지에 사용된 모듈에 따라 자동으로 부여됨. 임의의 페이지에 상품분류 모듈을 추가하면 해당 페이지는 "상품분류" 역할로 인식된다. 쇼핑몰 관리자 화면의 [쇼핑몰 설정 > 사이트 설정 > '사이트 환경 설정 > 쇼핑몰 환경 설정 > 화면경로 > 화면경로 설정']에서 각 페이지에 부여된 화면 역할을 조회하고 설정할 수 있음.  "all" 일 경우 전체 페이지에 스크립트가 적용됨.  display_location_code |
| skin_no | 스킨 번호   스크립트를 적용할 스킨 번호.   ,(콤마)로 여러 건을 검색할 수 있다. |
| created_start_date날짜 | 스크립트 설치일 검색 시작일   스크립트 설치 날짜가 해당 날짜 이후인 스크립트 검색 검색 종료일과 같이 사용해야함. |
| created_end_date날짜 | 스크립트 설치일 검색 종료일   스크립트 설치 날짜가 해당 날짜 이전인 스크립트 검색 검색 종료일과 같이 사용해야함. |
| updated_start_date날짜 | 스크립트 수정일 검색 시작일   스크립트 수정 날짜가 해당 날짜 이후인 스크립트 검색 검색 종료일과 같이 사용해야함. |
| updated_end_date날짜 | 스크립트 수정일 검색 종료일   스크립트 수정 날짜가 해당 날짜 이전인 스크립트 검색 검색 시작일과 같이 사용해야함. |

```bash
Retrieve a count of script tags        Retrieve a count of script tags       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```

### Retrieve a script tag   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 읽기권한 (mall.read_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| script_no | script의 고유번호   스크립트의 고유 번호 검색 |

```bash
Retrieve a script tag        Retrieve a script tag       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "scripttag": {        "shop_no": 1,        "script_no": "1509699932016345",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-11-03T18:05:32+09:00",        "updated_date": "2017-11-03T18:05:32+09:00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "scripttag": {        "shop_no": 1,        "script_no": "1509699932016345",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-11-03T18:05:32+09:00",        "updated_date": "2017-11-03T18:05:32+09:00"    }}
```

### Create a script tag   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 10 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| srcURL | 원본 script 경로   설치할 스크립트의 원본 경로(절대 경로) |
| display_locationRequired | 화면 경로   스크립트를 표시할 "화면 경로". 화면 경로는 화면의 페이지 경로가 아니라 쇼핑몰의 각 페이지에 부여된 특정한 역할을 의미함. (예 : 상품분류(product_list)에 스크립트를 삽입할 경우 쇼핑몰에서 상품분류로 사용되는 모든 페이지에 스크립트가 노출됨)  화면의 역할은 해당 페이지에 사용된 모듈에 따라 자동으로 부여됨. 임의의 페이지에 상품분류 모듈을 추가하면 해당 페이지는 "상품분류" 역할로 인식된다. 쇼핑몰 관리자 화면의 [쇼핑몰 설정 > 사이트 설정 > '사이트 환경 설정 > 쇼핑몰 환경 설정 > 화면경로 > 화면경로 설정']에서 각 페이지에 부여된 화면 역할을 조회하고 설정할 수 있음.  "all" 일 경우 전체 페이지에 스크립트가 적용됨.  display_location_code |
| exclude_path | 제외 경로 |
| skin_no | 스킨 번호   스크립트를 적용할 스킨 번호. |
| integrity | 하위 리소스 무결성   스크립트 위변조를 방지하기위한 무결성 검증용 해시. (sha384, sha512 해시 알고리즘 지원)  Integrity 해시 생성방법 참고 |

```bash
Create a script tag        Create a script tag Insert scripttag to specific location Try to insert scripttag without location Insert scripttag to specific skin Insert scripttag to all location but specific path       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo"    }}'    Response  Copy     {    "scripttag": {        "shop_no": 1,        "script_no": "1527128695613925",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-03-15T13:27:53+09:00",        "updated_date": "2017-03-15T13:27:53+09:00"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo"    }}'
```

```json
{    "scripttag": {        "shop_no": 1,        "script_no": "1527128695613925",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-03-15T13:27:53+09:00",        "updated_date": "2017-03-15T13:27:53+09:00"    }}
```

### Update a script tag   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 10 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| script_noRequired | script의 고유번호   스크립트의 고유 번호 |
| srcURL | 원본 script 경로   설치할 스크립트의 원본 경로(절대 경로) |
| display_location | 화면 경로   스크립트를 표시할 "화면 경로". 화면 경로는 화면의 페이지 경로가 아니라 쇼핑몰의 각 페이지에 부여된 특정한 역할을 의미함. (예 : 상품분류(product_list)에 스크립트를 삽입할 경우 쇼핑몰에서 상품분류로 사용되는 모든 페이지에 스크립트가 노출됨)  화면의 역할은 해당 페이지에 사용된 모듈에 따라 자동으로 부여됨. 임의의 페이지에 상품분류 모듈을 추가하면 해당 페이지는 "상품분류" 역할로 인식된다. 쇼핑몰 관리자 화면의 [쇼핑몰 설정 > 사이트 설정 > '사이트 환경 설정 > 쇼핑몰 환경 설정 > 화면경로 > 화면경로 설정']에서 각 페이지에 부여된 화면 역할을 조회하고 설정할 수 있음.  "all" 일 경우 전체 페이지에 스크립트가 적용됨.  display_location_code |
| exclude_path | 제외 경로 |
| skin_no | 스킨 번호   스크립트를 적용할 스킨 번호. |
| integrity | 하위 리소스 무결성   스크립트 위변조를 방지하기위한 무결성 검증용 해시. (sha384, sha512 해시 알고리즘 지원)  Integrity 해시 생성방법 참고 |

```bash
Update a script tag        Update a script tag Update path of the script Update skin_no in which the script is displayed       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo"    }}'    Response  Copy     {    "scripttag": {        "shop_no": 1,        "script_no": "1509432821494844",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-10-31T15:53:41+09:00",        "updated_date": "2017-11-06T10:33:57+09:00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo"    }}'
```

```json
{    "scripttag": {        "shop_no": 1,        "script_no": "1509432821494844",        "client_id": "AMj8UZhBC9zsyTlFGI6PzC",        "src": "https://yourdomain-sample.com/sample-script.js",        "display_location": [            "PRODUCT_LIST",            "PRODUCT_DETAIL"        ],        "exclude_path": [            "/product/list.html",            "/product/detail.html"        ],        "skin_no": [            3,            4        ],        "integrity": "sha384-UttGu98Tj02YSyWJ5yU0dHmx4wisywedBShWqEz+TL3vFOCXdeMWmo6jMVR8IdFo",        "created_date": "2017-10-31T15:53:41+09:00",        "updated_date": "2017-11-06T10:33:57+09:00"    }}
```

### Delete a script tag   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 앱 쓰기권한 (mall.write_application) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| script_noRequired | script의 고유번호   스크립트의 고유 번호 |

```bash
Delete a script tag        Delete a script tag       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "scripttag": {        "script_no": "1509699932016345"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/scripttags/1509699932016345' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "scripttag": {        "script_no": "1509699932016345"    }}
```
