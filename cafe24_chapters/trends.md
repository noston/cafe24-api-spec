# TRENDS


## Trends

```json
Endpoints    GET /api/v2/admin/trends
GET /api/v2/admin/trends/count
```

```json
GET /api/v2/admin/trends
GET /api/v2/admin/trends/count
```

### Trends property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| trend_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 트렌드 코드 |
| trend_name최대글자수 : [50자] | 트렌드 명 |
| use_trend | 트렌드 사용여부 T : 사용함 F : 사용안함 |
| created_date | 생성일 |
| product_count | 상품수 |

### Retrieve a list of trends   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| trend_code | 트렌드 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| trend_name | 트렌드 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_trend | 트렌드 사용여부   T : 사용함 F : 사용안함 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of trends        Retrieve a list of trends Retrieve trends with fields parameter Retrieve trends using paging Retrieve a specific trends with trend_code parameter Retrieve multiple trends       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/trends' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "trends": [        {            "shop_no": 1,            "trend_code": "T0000000",            "trend_name": "Default Trend",            "use_trend": "T",            "created_date": "2019-10-21T15:25:35+09:00",            "product_count": 2        },        {            "shop_no": 1,            "trend_code": "T000000A",            "trend_name": "Default Trend",            "use_trend": "F",            "created_date": "2019-10-21T15:25:35+09:00",            "product_count": 3        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/trends' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "trends": [        {            "shop_no": 1,            "trend_code": "T0000000",            "trend_name": "Default Trend",            "use_trend": "T",            "created_date": "2019-10-21T15:25:35+09:00",            "product_count": 2        },        {            "shop_no": 1,            "trend_code": "T000000A",            "trend_name": "Default Trend",            "use_trend": "F",            "created_date": "2019-10-21T15:25:35+09:00",            "product_count": 3        }    ]}
```

### Retrieve a count of trends   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| trend_code | 트렌드 코드   ,(콤마)로 여러 건을 검색할 수 있다. |
| trend_name | 트렌드 명   ,(콤마)로 여러 건을 검색할 수 있다. |
| use_trend | 트렌드 사용여부   T : 사용함 F : 사용안함 |

```bash
Retrieve a count of trends        Retrieve a count of trends       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/trends/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/trends/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```
