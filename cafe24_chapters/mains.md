# MAINS


## Mains

```json
Endpoints    GET /api/v2/admin/mains
POST /api/v2/admin/mains
PUT /api/v2/admin/mains/{display_group}
DELETE /api/v2/admin/mains/{display_group}
```

```json
GET /api/v2/admin/mains
POST /api/v2/admin/mains
PUT /api/v2/admin/mains/{display_group}
DELETE /api/v2/admin/mains/{display_group}
```

### Mains property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| module_code | 모듈 코드 각 메인분류에 지정된 모듈 코드 |
| display_group | 메인분류 번호 |
| group_name | 메인분류 명 메인분류 생성 당시 지정한 분류명 |
| soldout_sort_type | 품절상품진열 품절상품을 진열할 위치 |
| use_autodisplay | 자동진열 T : 사용함 F : 사용안함 |

### Retrieve a list of main categories   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 읽기권한 (mall.read_category) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a list of main categories        Retrieve a list of main categories Retrieve mains with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mains' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "mains": [        {            "shop_no": 1,            "module_code": "product_listmain_1",            "display_group": 2,            "group_name": "Main Recommendations",            "soldout_sort_type": "B",            "use_autodisplay": "T"        },        {            "shop_no": 1,            "module_code": "product_listmain_2",            "display_group": 3,            "group_name": "New Arrival",            "soldout_sort_type": "N",            "use_autodisplay": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mains' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "mains": [        {            "shop_no": 1,            "module_code": "product_listmain_1",            "display_group": 2,            "group_name": "Main Recommendations",            "soldout_sort_type": "B",            "use_autodisplay": "T"        },        {            "shop_no": 1,            "module_code": "product_listmain_2",            "display_group": 3,            "group_name": "New Arrival",            "soldout_sort_type": "N",            "use_autodisplay": "F"        }    ]}
```

### Add main category   cafe24

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
| group_nameRequired최대글자수 : [50자] | 메인분류 명 |
| soldout_sort_type | 품절상품진열   B : 품절상품 맨 뒤로  N : 품절상품 상관없음   DEFAULT N |

```bash
Add main category        Add main category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/mains' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}'    Response  Copy     {    "mains": {        "shop_no": 1,        "module_code": "product_listmain_1",        "display_group": 2,        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/mains' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}'
```

```json
{    "mains": {        "shop_no": 1,        "module_code": "product_listmain_1",        "display_group": 2,        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}
```

### Update main category   cafe24

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
| display_groupRequired | 메인분류 번호 |
| group_name최대글자수 : [50자] | 메인분류 명 |
| soldout_sort_type | 품절상품진열   B : 품절상품 맨 뒤로  N : 품절상품 상관없음 |

```bash
Update main category        Update main category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}'    Response  Copy     {    "mains": {        "shop_no": 1,        "module_code": "product_listmain_1",        "display_group": 2,        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}'
```

```json
{    "mains": {        "shop_no": 1,        "module_code": "product_listmain_1",        "display_group": 2,        "group_name": "Main Recommendations",        "soldout_sort_type": "B"    }}
```

### Delete main category   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 쓰기권한 (mall.write_category) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| display_groupRequired | 메인분류 번호 |

```bash
Delete main category        Delete main category       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/6' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "mains": {        "display_group": 6    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/6' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "mains": {        "display_group": 6    }}
```
