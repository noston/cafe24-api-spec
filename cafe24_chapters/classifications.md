# CLASSIFICATIONS


## Classifications

```json
Endpoints    GET /api/v2/admin/classifications
GET /api/v2/admin/classifications/count
```

```json
GET /api/v2/admin/classifications
GET /api/v2/admin/classifications/count
```

### Classifications property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| classification_code형식 : [A-Z0-9]최소글자수 : [8자]최대글자수 : [8자] | 자체분류 코드 |
| classification_name최대글자수 : [200자] | 자체분류 명 |
| classification_description최대글자수 : [300자] | 자체분류 설명 |
| use_classification | 사용여부 |
| created_date | 생성일 |
| product_count | 상품수 |

### Retrieve a list of custom categories   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| classification_code | 자체분류 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| classification_name | 자체분류 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_classification | 사용여부 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of custom categories        Retrieve a list of custom categories Retrieve classifications with fields parameter Retrieve classifications using paging Retrieve a specific classifications with classification_code parameter Retrieve multiple classifications       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/classifications' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "classifications": [        {            "shop_no": 1,            "classification_code": "C000000A",            "classification_name": "Default Classification",            "classification_description": "Default Classification description",            "use_classification": "T",            "created_date": "2018-01-16T12:00:41+09:00",            "product_count": 2        },        {            "shop_no": 1,            "classification_code": "C000000B",            "classification_name": "Classification 1",            "classification_description": "Classification 1 description",            "use_classification": "T",            "created_date": "2018-01-16T12:00:41+09:00",            "product_count": 3        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/classifications' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "classifications": [        {            "shop_no": 1,            "classification_code": "C000000A",            "classification_name": "Default Classification",            "classification_description": "Default Classification description",            "use_classification": "T",            "created_date": "2018-01-16T12:00:41+09:00",            "product_count": 2        },        {            "shop_no": 1,            "classification_code": "C000000B",            "classification_name": "Classification 1",            "classification_description": "Classification 1 description",            "use_classification": "T",            "created_date": "2018-01-16T12:00:41+09:00",            "product_count": 3        }    ]}
```

### Retrieve a count of custom categories   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| classification_code | 자체분류 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| classification_name | 자체분류 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_classification | 사용여부 |

```bash
Retrieve a count of custom categories        Retrieve a count of custom categories       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/classifications/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 3}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/classifications/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 3}
```
