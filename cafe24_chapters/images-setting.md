# IMAGES SETTING


## Images setting

```json
Endpoints    GET /api/v2/admin/images/setting
PUT /api/v2/admin/images/setting
```

```json
GET /api/v2/admin/images/setting
PUT /api/v2/admin/images/setting
```

### Images setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| product_image_size | 상품 이미지 사이즈 설정값 |

### Retrieve product image size settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve product image size settings        Retrieve product image size settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/images/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "image": {        "shop_no": 1,        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/images/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "image": {        "shop_no": 1,        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}
```

### Update product image size settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 쓰기권한 (mall.write_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_image_sizeRequired | 상품 이미지 사이즈 설정값 |
| product_image_size 하위 요소 보기     detail_image_width상세 이미지 가로 detail_image_height상세이미지 세로 list_image_width목록 이미지 가로 list_image_height목록 이미지 세로 tiny_image_width작은 목록 이미지 가로 tiny_image_height작은 목록 이미지 세로 zoom_image_width확대 이미지 가로 zoom_image_height확대 이미지 세로 small_image_width축소 이미지 가로 small_image_height축소 이미지 세로 |

```bash
Update product image size settings        Update product image size settings Try to change image setting without using required field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/images/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}'    Response  Copy     {    "image": {        "shop_no": 1,        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/images/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}'
```

```json
{    "image": {        "shop_no": 1,        "product_image_size": {            "detail_image_width": 500,            "detail_image_height": 500,            "list_image_width": 300,            "list_image_height": 300,            "tiny_image_width": 220,            "tiny_image_height": 220,            "zoom_image_width": 500,            "zoom_image_height": 500,            "small_image_width": 100,            "small_image_height": 100        }    }}
```
