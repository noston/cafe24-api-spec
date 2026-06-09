# ACTIVITYLOGS


## Activitylogs

```json
Endpoints    GET /api/v2/admin/activitylogs
GET /api/v2/admin/activitylogs/{process_no}
```

```json
GET /api/v2/admin/activitylogs
GET /api/v2/admin/activitylogs/{process_no}
```

### Activitylogs property list

| Attribute | Description |
| --- | --- |
| process_no | 업무처리 넘버 |
| mode | 모드 P : PC 어드민 M : 모바일 어드민 S : (구)스마트모드 |
| type | 구분 |
| content | 업무내용 |
| process_date | 처리일시 |
| manager_id형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 처리자 |
| manager_type | 처리자 타입 |

### Retrieve a list of action logs   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| manager_type | 처리자 타입   P : 대표운영자 A : 부운영자 S : 공급사 |
| manager_id형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 처리자 |
| mode | 모드   P : PC 어드민 M : 모바일 어드민 S : (구)스마트모드 |
| type | 구분 |
| content최대글자수 : [500자] | 업무내용 |
| start_dateRequired날짜 | 검색 시작일 |
| end_dateRequired날짜 | 검색 종료일 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a list of action logs        Retrieve a list of action logs Retrieve activitylogs with fields parameter Retrieve a specific activitylogs with mode parameter Retrieve activitylogs using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/activitylogs?start_date=2020-01-01T00:00:00+09:00&end_date=2020-03-01T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "activitylogs": [        {            "process_no": 130,            "mode": "P",            "type": "product management > product management > product list",            "content": "Edit product name",            "process_date": "2020-02-01T00:00:00+09:00",            "manager_id": "sampleid",            "manager_type": "representative operator"        },        {            "process_no": 131,            "mode": "P",            "type": "product management > product management > product list",            "content": "Edit product name",            "process_date": "2020-02-02T00:00:00+09:00",            "manager_id": "sampleid",            "manager_type": "representative operator"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/activitylogs?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/activitylogs?start_date=2020-01-01T00:00:00+09:00&end_date=2020-03-01T23:59:59+09:00' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "activitylogs": [        {            "process_no": 130,            "mode": "P",            "type": "product management > product management > product list",            "content": "Edit product name",            "process_date": "2020-02-01T00:00:00+09:00",            "manager_id": "sampleid",            "manager_type": "representative operator"        },        {            "process_no": 131,            "mode": "P",            "type": "product management > product management > product list",            "content": "Edit product name",            "process_date": "2020-02-02T00:00:00+09:00",            "manager_id": "sampleid",            "manager_type": "representative operator"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/activitylogs?limit=10&offset=10"        }    ]}
```

### Retrieve an action log   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| process_noRequired | 업무처리 넘버 |

```bash
Retrieve an action log        Retrieve an action log Retrieve an activitylog with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/activitylogs/130' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "activitylog": {        "process_no": 130,        "type": "product management > product management > product list",        "manager_id": "sampleid",        "manager_type": "representative operator",        "process_date": "2020-02-01T00:00:00+09:00",        "content": "Edit product name"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/activitylogs/130' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "activitylog": {        "process_no": 130,        "type": "product management > product management > product list",        "manager_id": "sampleid",        "manager_type": "representative operator",        "process_date": "2020-02-01T00:00:00+09:00",        "content": "Edit product name"    }}
```
