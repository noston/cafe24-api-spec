# SOCIAL


## Social

```json
Endpoints    GET /api/v2/admin/social
```

```json
GET /api/v2/admin/social
```

### Social property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id | 회원아이디 |
| social_name | 연동 된 SNS명 |
| social_member_code | 연동 된 SNS 제공코드 |
| linked_date | 연동 날짜 |

### List all social   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| social_name | 연동 된 SNS명 |
| linked_start_date날짜 | 연동 날짜 검색 시작일 |
| linked_end_date날짜 | 연동 날짜 검색 종료일 |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
List all social        List all social       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/social' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "social": [        {            "shop_no": 1,            "member_id": "sampleid",            "social_name": "line",            "social_member_code": "U1e0014229a08c2f95e12ee29904da597",            "linked_date": "2024-02-18T13:03:11+09:00"        },        {            "shop_no": 1,            "member_id": "sampleid2",            "social_name": "kakao",            "social_member_code": "U2f1125330b19d3g06f23ff30015eb608",            "linked_date": "2026-05-10T09:00:00+09:00"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/social?limit=10&offset=10"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/social' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "social": [        {            "shop_no": 1,            "member_id": "sampleid",            "social_name": "line",            "social_member_code": "U1e0014229a08c2f95e12ee29904da597",            "linked_date": "2024-02-18T13:03:11+09:00"        },        {            "shop_no": 1,            "member_id": "sampleid2",            "social_name": "kakao",            "social_member_code": "U2f1125330b19d3g06f23ff30015eb608",            "linked_date": "2026-05-10T09:00:00+09:00"        }    ],    "links": [        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/social?limit=10&offset=10"        }    ]}
```
