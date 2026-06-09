# THEMES


## Themes

```json
Endpoints    GET /api/v2/admin/themes
GET /api/v2/admin/themes/count
GET /api/v2/admin/themes/{skin_no}
```

```json
GET /api/v2/admin/themes
GET /api/v2/admin/themes/count
GET /api/v2/admin/themes/{skin_no}
```

### Themes property list

| Attribute | Description |
| --- | --- |
| skin_no최소값: [1] | 디자인 번호 |
| skin_code | 디자인 코드 |
| skin_name최대글자수 : [100자] | 디자인명 |
| skin_thumbnail_url최대글자수 : [255자] | 디자인 썸네일 이미지 URL |
| usage_type | 디자인 용도 구분 S : PC 기본스킨 C : PC 복사된 스킨 I : PC 상속된 스킨 M : 모바일 기본스킨/상속된 스킨 N : 모바일 복사된 스킨 |
| editor_type | 에디터 타입 H : 스마트 디자인 (HTML) D : 에디봇 디자인 (Drag & Drop) W : 심플 디자인 (WYSIWYG) E : 스마트디자인Easy C : 콘텐츠스튜디오(Contents Studio) |
| parent_skin_no | 부모 디자인 번호 |
| seller_id | 판매자 디자인센터 아이디 |
| seller_skin_code | 판매자 디자인 코드 |
| design_purchase_no최소값: [0] | 디자인 구매 번호 |
| design_product_code | 디자인센터 상품 코드 |
| language_code최소글자수 : [5자]최대글자수 : [5자] | 언어 코드 ko_KR : 국문 en_US : 영문 zh_CN : 중문(간체) zh_TW : 중문(번체) ja_JP : 일문 pt_PT : 포르투갈어 es_ES : 스페인어 vi_VN : 베트남어 |
| published_in | 대표디자인 설정 멀티쇼핑몰 번호 |
| created_date날짜 | 생성일 |
| updated_date날짜 | 수정일 |
| preview_domain | 도메인 조회 |
| skin_lock | 디자인 잠금 T : 잠금 F : 해제 |

### Retrieve a list of themes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 읽기권한 (mall.read_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| type | 디자인 타입   pc : PC mobile : 모바일   DEFAULT pc |

```bash
Retrieve a list of themes        Retrieve a list of themes Retrieve themes with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes?type=pc' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "themes": [        {            "skin_no": 3,            "skin_code": "skin2",            "skin_name": "My Shop Default Theme",            "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",            "usage_type": "C",            "editor_type": "H",            "parent_skin_no": 1,            "seller_id": null,            "seller_skin_code": null,            "design_purchase_no": 0,            "design_product_code": null,            "language_code": "ko_KR",            "published_in": "unpublished",            "created_date": "2017-12-20T17:03:24+09:00",            "updated_date": "2017-12-20T17:03:24+09:00",            "skin_lock": "F",            "preview_domain": [                "https://myshop.cafe24.com/skin-skin2",                "https://myshop.cafe24.com/shop1/skin-skin2"            ]        },        {            "skin_no": 1,            "skin_code": "skin1",            "skin_name": "My Shop Old Theme",            "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",            "usage_type": "S",            "editor_type": "D",            "parent_skin_no": null,            "seller_id": null,            "seller_skin_code": null,            "design_purchase_no": 0,            "design_product_code": null,            "language_code": "ko_KR",            "published_in": "1",            "created_date": "2016-10-04T22:52:43+09:00",            "updated_date": null,            "skin_lock": "T",            "preview_domain": [                "https://myshop.cafe24.com/skin-skin1",                "https://myshop.cafe24.com/shop1/skin-skin1"            ]        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes?type=pc' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "themes": [        {            "skin_no": 3,            "skin_code": "skin2",            "skin_name": "My Shop Default Theme",            "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",            "usage_type": "C",            "editor_type": "H",            "parent_skin_no": 1,            "seller_id": null,            "seller_skin_code": null,            "design_purchase_no": 0,            "design_product_code": null,            "language_code": "ko_KR",            "published_in": "unpublished",            "created_date": "2017-12-20T17:03:24+09:00",            "updated_date": "2017-12-20T17:03:24+09:00",            "skin_lock": "F",            "preview_domain": [                "https://myshop.cafe24.com/skin-skin2",                "https://myshop.cafe24.com/shop1/skin-skin2"            ]        },        {            "skin_no": 1,            "skin_code": "skin1",            "skin_name": "My Shop Old Theme",            "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",            "usage_type": "S",            "editor_type": "D",            "parent_skin_no": null,            "seller_id": null,            "seller_skin_code": null,            "design_purchase_no": 0,            "design_product_code": null,            "language_code": "ko_KR",            "published_in": "1",            "created_date": "2016-10-04T22:52:43+09:00",            "updated_date": null,            "skin_lock": "T",            "preview_domain": [                "https://myshop.cafe24.com/skin-skin1",                "https://myshop.cafe24.com/shop1/skin-skin1"            ]        }    ]}
```

### Retrieve a count of themes   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 읽기권한 (mall.read_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| type | 디자인 타입   pc : PC mobile : 모바일   DEFAULT pc |

```bash
Retrieve a count of themes        Retrieve a count of themes       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 1}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 1}
```

### Retrieve a theme   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 읽기권한 (mall.read_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| skin_no최소값: [1] | 디자인 번호 |

```bash
Retrieve a theme        Retrieve a theme Retrieve a theme with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "theme": {        "skin_no": 1,        "skin_code": "skin1",        "skin_name": "My Shop Default Theme",        "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",        "usage_type": "S",        "editor_type": "D",        "parent_skin_no": null,        "seller_id": null,        "seller_skin_code": null,        "design_purchase_no": 0,        "design_product_code": null,        "language_code": "ko_KR",        "published_in": "1",        "created_date": "2016-10-04T22:52:43+09:00",        "updated_date": null,        "skin_lock": "T",        "preview_domain": [            "https://myshop.cafe24.com/skin-skin1",            "https://myshop.cafe24.com/shop1/skin-skin1"        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/themes/1' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "theme": {        "skin_no": 1,        "skin_code": "skin1",        "skin_name": "My Shop Default Theme",        "skin_thumbnail_url": "https://img.echosting.cafe24.com/smartAdmin/img/design/img_skin_default.jpg",        "usage_type": "S",        "editor_type": "D",        "parent_skin_no": null,        "seller_id": null,        "seller_skin_code": null,        "design_purchase_no": 0,        "design_product_code": null,        "language_code": "ko_KR",        "published_in": "1",        "created_date": "2016-10-04T22:52:43+09:00",        "updated_date": null,        "skin_lock": "T",        "preview_domain": [            "https://myshop.cafe24.com/skin-skin1",            "https://myshop.cafe24.com/shop1/skin-skin1"        ]    }}
```
