# AUTODISPLAY


## Autodisplay

```json
Endpoints    GET /api/v2/admin/autodisplay
POST /api/v2/admin/autodisplay
PUT /api/v2/admin/autodisplay/{display_no}
DELETE /api/v2/admin/autodisplay/{display_no}
```

```json
GET /api/v2/admin/autodisplay
POST /api/v2/admin/autodisplay
PUT /api/v2/admin/autodisplay/{display_no}
DELETE /api/v2/admin/autodisplay/{display_no}
```

### Autodisplay property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| display_no | 자동진열 번호 |
| use_main | 메인분류 여부 T: 메인분류 F: 상품분류 |
| category_no | 분류 번호 |
| display_group | 상세 상품분류 |
| display_count최소: [1]~최대: [200] | 자동진열 최대 상품 수 |
| use_reservation | 예약진열 사용여부 T: 사용함 F: 사용안함 |
| start_date | 예약 시작일 |
| use_hashtag | 해시태그 사용여부 T: 사용함 F: 사용안함 |
| hash_tags | 해시태그 |
| display_sort | 정렬순서 AOD: 주문 수 높은 순서대로 AOA: 주문 수 낮은 순서대로 AVD: 조회 수 높은 순서대로 AVA: 조회 수 낮은 순서대로 ARD: 주문율 높은 순서대로 ARA: 주문율 낮은 순서대로 ACD: 클릭 가치 높은 순서대로 AND: 신규 등록된 순서대로 APD: 판매가 높은 순서대로 APA: 판매가 낮은 순서대로 RD : 최근 등록상품이 위로  RA : 최근 등록상품이 아래로  UD : 최근 수정상품이 위로 UA : 최근 수정상품이 아래로 NA : 상품명 가나다순 ND : 상품명 가나다역순 PD : 판매가 높은 상품이 위로 PA : 판매가 높은 상품이 아래로 SD : 판매량 높은 상품이 위로 SA : 판매량 높은 상품이 아래로 CD : 조회수가 높은 상품이 위로 CA : 조회수가 높은 상품이 아래로 LD : 좋아요수가 높은 상품이 위로 LA : 좋아요수가 높은 상품이 아래로 |
| timetable배열 최대사이즈: [24] | 업데이트 시간 |
| period | 데이터 집계 기간 1: 1일 3: 3일 7: 1주(7일) 30: 30일 |
| except_categories_scope | 제외 분류 설정 A: 모든 분류에 적용 C : 이 분류만 적용 |
| except_categories | 제외 분류 |

### Retrieve a list of auto layouts   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 읽기권한 (mall.read_category) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_no | 자동진열 번호 |

```bash
Retrieve a list of auto layouts        Retrieve a list of auto layouts Retrieve autodisplay with fields parameter Retrieve a specific autodisplay with display_no parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "autodisplay": [        {            "shop_no": 1,            "display_no": 1,            "use_main": "T",            "category_no": 1,            "display_group": 2,            "display_count": 12,            "use_reservation": "T",            "start_date": "2020-01-01T10:00:00+09:00",            "use_hashtag": "F",            "hash_tags": null,            "display_sort": "ACD",            "timetable": [                12,                20            ],            "period": 1,            "except_categories_scope": "C",            "except_categories": [                30,                41            ]        },        {            "shop_no": 1,            "display_no": 2,            "use_main": "F",            "category_no": 24,            "display_group": 2,            "display_count": 48,            "use_reservation": "F",            "start_date": null,            "use_hashtag": "T",            "hash_tags": [                "new",                "winter"            ],            "display_sort": "RD",            "timetable": [                12,                20            ],            "period": 7,            "except_categories_scope": "A",            "except_categories": [                30,                41            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "autodisplay": [        {            "shop_no": 1,            "display_no": 1,            "use_main": "T",            "category_no": 1,            "display_group": 2,            "display_count": 12,            "use_reservation": "T",            "start_date": "2020-01-01T10:00:00+09:00",            "use_hashtag": "F",            "hash_tags": null,            "display_sort": "ACD",            "timetable": [                12,                20            ],            "period": 1,            "except_categories_scope": "C",            "except_categories": [                30,                41            ]        },        {            "shop_no": 1,            "display_no": 2,            "use_main": "F",            "category_no": 24,            "display_group": 2,            "display_count": 48,            "use_reservation": "F",            "start_date": null,            "use_hashtag": "T",            "hash_tags": [                "new",                "winter"            ],            "display_sort": "RD",            "timetable": [                12,                20            ],            "period": 7,            "except_categories_scope": "A",            "except_categories": [                30,                41            ]        }    ]}
```

### Create auto layout for selected product category   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 쓰기권한 (mall.write_category) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| use_mainRequired | 메인분류 여부   T: 메인분류 F: 상품분류 |
| category_noRequired | 분류 번호 |
| display_groupRequired | 상세 상품분류 |
| display_countRequired최소: [1]~최대: [200] | 자동진열 최대 상품 수 |
| use_reservationRequired | 예약진열 사용여부   T: 사용함 F: 사용안함 |
| start_date | 예약 시작일 |
| use_hashtagRequired | 해시태그 사용여부   T: 사용함 F: 사용안함 |
| hash_tags | 해시태그 |
| display_sort | 정렬순서   정렬 조건(RD, RA, UD, UA, NA, ND, PD, PA, SD, SA, AD, AA, LD, LA)은 use_hashtag가 "T"일 경우에만 사용 가능   AOD: 주문 수 높은 순서대로 AOA: 주문 수 낮은 순서대로 AVD: 조회 수 높은 순서대로 AVA: 조회 수 낮은 순서대로 ARD: 주문율 높은 순서대로 ARA: 주문율 낮은 순서대로 ACD: 클릭 가치 높은 순서대로 AND: 신규 등록된 순서대로 APD: 판매가 높은 순서대로 APA: 판매가 낮은 순서대로 RD : 최근 등록상품이 위로  RA : 최근 등록상품이 아래로  UD : 최근 수정상품이 위로 UA : 최근 수정상품이 아래로 NA : 상품명 가나다순 ND : 상품명 가나다역순 PD : 판매가 높은 상품이 위로 PA : 판매가 높은 상품이 아래로 SD : 판매량 높은 상품이 위로 SA : 판매량 높은 상품이 아래로 CD : 조회수가 높은 상품이 위로 CA : 조회수가 높은 상품이 아래로 LD : 좋아요수가 높은 상품이 위로 LA : 좋아요수가 높은 상품이 아래로 |
| timetable배열 최대사이즈: [24] | 업데이트 시간 |
| period | 데이터 집계 기간   1: 1일 3: 3일 7: 1주(7일) 30: 30일 |
| except_categories_scope | 제외 분류 설정   A: 모든 분류에 적용 C : 이 분류만 적용   DEFAULT A |
| except_categories | 제외 분류 |

```bash
Create auto layout for selected product category        Create auto layout for selected product category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "display_sort": "ACD",        "timetable": [            12,            20        ],        "period": 1,        "except_categories_scope": "A",        "except_categories": [            30,            41        ]    }}'    Response  Copy     {    "autodisplay": {        "shop_no": 1,        "display_no": 1,        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "hash_tags": null,        "display_sort": "ACD",        "timetable": [            12,            20        ],        "period": 1,        "except_categories_scope": "A",        "except_categories": [            30,            41        ]    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "display_sort": "ACD",        "timetable": [            12,            20        ],        "period": 1,        "except_categories_scope": "A",        "except_categories": [            30,            41        ]    }}'
```

```json
{    "autodisplay": {        "shop_no": 1,        "display_no": 1,        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "hash_tags": null,        "display_sort": "ACD",        "timetable": [            12,            20        ],        "period": 1,        "except_categories_scope": "A",        "except_categories": [            30,            41        ]    }}
```

### Update auto layout for selected product category   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 쓰기권한 (mall.write_category) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_noRequired | 자동진열 번호 |
| display_count최소: [1]~최대: [200] | 자동진열 최대 상품 수 |
| use_reservation | 예약진열 사용여부   T: 사용함 F: 사용안함 |
| start_date | 예약 시작일 |
| use_hashtag | 해시태그 사용여부   T: 사용함 F: 사용안함 |
| hash_tags | 해시태그 |
| display_sort | 정렬순서   정렬 조건(RD, RA, UD, UA, NA, ND, PD, PA, SD, SA, AD, AA, LD, LA)은 use_hashtag가 "T"일 경우에만 사용 가능   AOD: 주문 수 높은 순서대로 AOA: 주문 수 낮은 순서대로 AVD: 조회 수 높은 순서대로 AVA: 조회 수 낮은 순서대로 ARD: 주문율 높은 순서대로 ARA: 주문율 낮은 순서대로 ACD: 클릭 가치 높은 순서대로 AND: 신규 등록된 순서대로 APD: 판매가 높은 순서대로 APA: 판매가 낮은 순서대로 RD : 최근 등록상품이 위로  RA : 최근 등록상품이 아래로  UD : 최근 수정상품이 위로 UA : 최근 수정상품이 아래로 NA : 상품명 가나다순 ND : 상품명 가나다역순 PD : 판매가 높은 상품이 위로 PA : 판매가 높은 상품이 아래로 SD : 판매량 높은 상품이 위로 SA : 판매량 높은 상품이 아래로 CD : 조회수가 높은 상품이 위로 CA : 조회수가 높은 상품이 아래로 LD : 좋아요수가 높은 상품이 위로 LA : 좋아요수가 높은 상품이 아래로 |
| timetable배열 최대사이즈: [24] | 업데이트 시간 |
| period | 데이터 집계 기간   1: 1일 3: 3일 7: 1주(7일) 30: 30일 |
| except_categories_scope | 제외 분류 설정   A: 모든 분류에 적용 C : 이 분류만 적용 |
| except_categories | 제외 분류 |

```bash
Update auto layout for selected product category        Update auto layout for selected product category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "display_sort": "ACD",        "timetable": [            0,            12        ],        "period": 1,        "except_categories_scope": "C",        "except_categories": [            30,            41        ]    }}'    Response  Copy     {    "autodisplay": {        "shop_no": 1,        "display_no": 1,        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "hash_tags": null,        "display_sort": "ACD",        "timetable": [            0,            12        ],        "period": 1,        "except_categories_scope": "C",        "except_categories": [            30,            41        ]    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "display_sort": "ACD",        "timetable": [            0,            12        ],        "period": 1,        "except_categories_scope": "C",        "except_categories": [            30,            41        ]    }}'
```

```json
{    "autodisplay": {        "shop_no": 1,        "display_no": 1,        "use_main": "T",        "category_no": 1,        "display_group": 2,        "display_count": 12,        "use_reservation": "T",        "start_date": "2020-01-01T10:00:00+09:00",        "use_hashtag": "F",        "hash_tags": null,        "display_sort": "ACD",        "timetable": [            0,            12        ],        "period": 1,        "except_categories_scope": "C",        "except_categories": [            30,            41        ]    }}
```

### Delete auto layout for selected product category   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 쓰기권한 (mall.write_category) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_noRequired | 자동진열 번호 |

```bash
Delete auto layout for selected product category        Delete auto layout for selected product category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "autodisplay": {        "display_no": 1    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/autodisplay/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "autodisplay": {        "display_no": 1    }}
```
