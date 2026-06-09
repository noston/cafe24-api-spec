# ICONS


## Icons

```json
Endpoints    GET /api/v2/admin/icons
PUT /api/v2/admin/icons
```

```json
GET /api/v2/admin/icons
PUT /api/v2/admin/icons
```

### Icons property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| id | 아이콘 아이디 |
| type | 디자인 타입 pc : PC mobile : 모바일 |
| group_code | 그룹 코드 A : 상품 아이콘 B : 게시판 아이콘 C : 카드 아이콘 E : 이벤트 아이콘 |
| path | 아이콘 URL |
| display | 아이콘 노출여부 T : 노출함 F : 노출안함 |
| description | 아이콘 설명 |

### Retrieve a list of desgin icons   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 읽기권한 (mall.read_design) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| type | 디자인 타입   pc : PC mobile : 모바일   DEFAULT pc |

```bash
Retrieve a list of desgin icons        Retrieve a list of desgin icons       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "icons": [        {            "shop_no": 1,            "id": 2,            "type": "pc",            "group_code": "A",            "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/ico_product_point.gif",            "display": "T",            "description": "Points for purchase"        },        {            "shop_no": 1,            "id": 8,            "type": "pc",            "group_code": "A",            "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/btn_prd_zoom.gif",            "display": "T",            "description": "Zoom-in"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "icons": [        {            "shop_no": 1,            "id": 2,            "type": "pc",            "group_code": "A",            "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/ico_product_point.gif",            "display": "T",            "description": "Points for purchase"        },        {            "shop_no": 1,            "id": 8,            "type": "pc",            "group_code": "A",            "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/btn_prd_zoom.gif",            "display": "T",            "description": "Zoom-in"        }    ]}
```

### Update store icon settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 디자인 쓰기권한 (mall.write_design) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| idRequired최소값: [1] | 아이콘 아이디 |
| group_codeRequired | 그룹 코드   A : 상품 아이콘 B : 게시판 아이콘 C : 카드 아이콘 E : 이벤트 아이콘 |
| type | 디자인 타입   pc : PC mobile : 모바일   DEFAULT pc |
| pathURL | 아이콘 URL |
| display | 아이콘 노출여부   T : 노출함 F : 노출안함 |

```bash
Update store icon settings        Update store icon settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "id": 3,        "group_code": "A",        "type": "pc",        "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/ico_soldout.gif",        "display": "T"    }}'    Response  Copy     {    "icons": {        "shop_no": 1,        "id": 3,        "type": "pc",        "group_code": "A",        "path": "/web/upload/icon_202511241132420800.gif",        "display": "T",        "description": "Out of stock"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/icons' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "id": 3,        "group_code": "A",        "type": "pc",        "path": "https://img.echosting.cafe24.com/design/skin/admin/ko_KR/ico_soldout.gif",        "display": "T"    }}'
```

```json
{    "icons": {        "shop_no": 1,        "id": 3,        "type": "pc",        "group_code": "A",        "path": "/web/upload/icon_202511241132420800.gif",        "display": "T",        "description": "Out of stock"    }}
```
