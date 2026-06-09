# COMMONEVENTS


## Commonevents

```json
Endpoints    GET /api/v2/admin/commonevents
POST /api/v2/admin/commonevents
PUT /api/v2/admin/commonevents/{event_no}
DELETE /api/v2/admin/commonevents/{event_no}
```

```json
GET /api/v2/admin/commonevents
POST /api/v2/admin/commonevents
PUT /api/v2/admin/commonevents/{event_no}
DELETE /api/v2/admin/commonevents/{event_no}
```

### Commonevents property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| event_no | 이벤트 번호 |
| name | 이벤트 이름 |
| status | 이벤트 상태 |
| category_no | 카테고리 번호 |
| register_date | 등록일 |
| display_position | 표시 위치 |
| content | 내용 |

### Retrieve a list of storewide promotions   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 읽기권한 (mall.read_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| limit최대값: [100] | 조회결과 최대건수   DEFAULT 20 |
| offset최대값: [8000] | 조회결과 시작위치 |

```bash
Retrieve a list of storewide promotions        Retrieve a list of storewide promotions       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "commonevents": [        {            "shop_no": 1,            "event_no": 3,            "name": "Outwear Common Event",            "status": "T",            "category_no": 24,            "register_date": "2025-08-18 11:05:01"        },        {            "shop_no": 1,            "event_no": 2,            "name": "All Common Event",            "status": "T",            "category_no": 0,            "register_date": "2025-08-18 11:01:54"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/commonevents?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/commonevents?limit=10&offset=20"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "commonevents": [        {            "shop_no": 1,            "event_no": 3,            "name": "Outwear Common Event",            "status": "T",            "category_no": 24,            "register_date": "2025-08-18 11:05:01"        },        {            "shop_no": 1,            "event_no": 2,            "name": "All Common Event",            "status": "T",            "category_no": 0,            "register_date": "2025-08-18 11:01:54"        }    ],    "links": [        {            "rel": "prev",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/commonevents?limit=10&offset=0"        },        {            "rel": "next",            "href": "https://{mallid}.cafe24api.com/api/v2/admin/commonevents?limit=10&offset=20"        }    ]}
```

### Create a storewide promotion   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| nameRequired최대글자수 : [255자] | 이벤트 이름 |
| status | 이벤트 상태   T: 진행 F: 진행안함   DEFAULT T |
| category_no최소값: [0] | 카테고리 번호   0: 전체   DEFAULT 0 |
| display_position | 표시 위치   top_detail: 상품상세정보 위 side_image: 상품이미지 옆   DEFAULT top_detail |
| content | 내용 |

```bash
Create a storewide promotion        Create a storewide promotion       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "Common Event",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "Common Event Content"    }}'    Response  Copy     {    "commonevent": {        "shop_no": 1,        "event_no": 4,        "name": "Common Event",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "Common Event Content",        "register_date": "2025-08-21 11:05:01"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "Common Event",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "Common Event Content"    }}'
```

```json
{    "commonevent": {        "shop_no": 1,        "event_no": 4,        "name": "Common Event",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "Common Event Content",        "register_date": "2025-08-21 11:05:01"    }}
```

### Update a storewide promotion   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| event_noRequired최소값: [1] | 이벤트 번호 |
| name최대글자수 : [255자] | 이벤트 이름 |
| status | 이벤트 상태   T: 진행 F: 진행안함 |
| category_no최소값: [0] | 카테고리 번호   0: 전체 |
| display_position | 표시 위치   top_detail: 상품상세정보 위 side_image: 상품이미지 옆 |
| content | 내용 |

```bash
Update a storewide promotion        Update a storewide promotion       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents/{#id}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "Updated Event Name",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "This is updated event content."    }}'    Response  Copy     {    "commonevent": {        "shop_no": 1,        "event_no": 123,        "name": "Updated Event Name",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "This is updated event content.",        "register_date": "2025-08-21 11:20:30"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents/{#id}' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "name": "Updated Event Name",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "This is updated event content."    }}'
```

```json
{    "commonevent": {        "shop_no": 1,        "event_no": 123,        "name": "Updated Event Name",        "status": "T",        "category_no": 24,        "display_position": "top_detail",        "content": "This is updated event content.",        "register_date": "2025-08-21 11:20:30"    }}
```

### Delete a storewide promotion   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 프로모션 쓰기권한 (mall.write_promotion) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| event_noRequired최소값: [1] | 이벤트 번호 |

```bash
Delete a storewide promotion        Delete a storewide promotion       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents/4' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "commonevent": {        "event_no": 4    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/commonevents/4' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "commonevent": {        "event_no": 4    }}
```
