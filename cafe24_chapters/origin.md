# ORIGIN


## Origin

```json
Endpoints    GET /api/v2/admin/origin
```

```json
GET /api/v2/admin/origin
```

### Origin property list

| Attribute | Description |
| --- | --- |
| origin_place_no | 원산지 번호 |
| origin_place_name | 원산지 이름 |
| foreign | 해외 여부 |
| made_in_code | 원산지 국가코드 |

### Retrieve a list of origins   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 판매분류 읽기권한 (mall.read_collection) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| origin_place_no | 원산지 번호 |
| origin_place_name최대글자수 : [50자] | 원산지 이름 |
| foreign | 해외 여부 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of origins        Retrieve a list of origins Retrieve origin with fields parameter Retrieve origin using paging Retrieve a specific origin with origin_place_no parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/origin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "origin": [        {            "origin_place_no": "1",            "origin_place_name": [                "Gangwon",                "Gangneung-si"            ],            "foreign": "F",            "made_in_code": "KR"        },        {            "origin_place_no": "2",            "origin_place_name": [                "Gangwon",                "Goseong-gun"            ],            "foreign": "F",            "made_in_code": "KR"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/origin' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "origin": [        {            "origin_place_no": "1",            "origin_place_name": [                "Gangwon",                "Gangneung-si"            ],            "foreign": "F",            "made_in_code": "KR"        },        {            "origin_place_no": "2",            "origin_place_name": [                "Gangwon",                "Goseong-gun"            ],            "foreign": "F",            "made_in_code": "KR"        }    ]}
```
