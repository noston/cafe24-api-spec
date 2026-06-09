# PRODUCTS DECORATIONIMAGES


## Products decorationimages

```json
Endpoints    GET /api/v2/admin/products/{product_no}/decorationimages
POST /api/v2/admin/products/{product_no}/decorationimages
PUT /api/v2/admin/products/{product_no}/decorationimages
DELETE /api/v2/admin/products/{product_no}/decorationimages/{code}
```

```json
GET /api/v2/admin/products/{product_no}/decorationimages
POST /api/v2/admin/products/{product_no}/decorationimages
PUT /api/v2/admin/products/{product_no}/decorationimages
DELETE /api/v2/admin/products/{product_no}/decorationimages/{code}
```

### Products decorationimages property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_show_date | 표시기간 사용 여부 T : 사용함 F : 사용안함 |
| show_start_date | 표시기간 시작 일자 |
| show_end_date | 표시기간 종료 일자 |
| image_list | 꾸미기 이미지 리스트 수평위치(image_horizontal_position) L : 왼쪽 C : 가운데 R : 오른쪽  수직위치(image_vertical_position) T : 상단 C : 중단 B : 하단 |
| code | 꾸미기 이미지 코드 |

### Retrieve a list of product decoration images   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |

```bash
Retrieve a list of product decoration images        Retrieve a list of product decoration images Retrieve decorationimages with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Set decoration images for a product   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호 |
| use_show_date | 표시기간 사용 여부   T : 사용함 F : 사용안함 |
| show_start_date날짜 | 표시기간 시작 일자 |
| show_end_date날짜 | 표시기간 종료 일자 |
| image_listRequired | 꾸미기 이미지 리스트   수평위치(image_horizontal_position) L : 왼쪽 C : 가운데 R : 오른쪽  수직위치(image_vertical_position) T : 상단 C : 중단 B : 하단 |
| image_list 하위 요소 보기     code꾸미기 이미지 코드 path꾸미기 이미지 경로 image_horizontal_position꾸미기 이미지 수평값 image_vertical_position꾸미기 이미지 수직값 |

```bash
Set decoration images for a product        Set decoration images for a product Set a decoration images to a product by using only required fields Try setting a decoration images to a product with wrong position       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update product decoration images   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| use_show_date | 표시기간 사용 여부   T : 사용함 F : 사용안함 |
| show_start_date날짜 | 표시기간 시작 일자 |
| show_end_date날짜 | 표시기간 종료 일자 |
| image_listRequired | 꾸미기 이미지 리스트   수평위치(image_horizontal_position) L : 왼쪽 C : 가운데 R : 오른쪽  수직위치(image_vertical_position) T : 상단 C : 중단 B : 하단 |
| image_list 하위 요소 보기     code꾸미기 이미지 코드 path꾸미기 이미지 경로 image_horizontal_position꾸미기 이미지 수평값 image_vertical_position꾸미기 이미지 수직값 |

```bash
Update product decoration images        Update product decoration images Update vertical position and horizontal position of decoration images Update display periods of decoration images       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Remove a product decoration image   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| codeRequired | 꾸미기 이미지 코드 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |

```bash
Remove a product decoration image        Remove a product decoration image       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

## Products decorationimages

```json
Endpoints    GET /api/v2/admin/products/decorationimages
```

```json
GET /api/v2/admin/products/decorationimages
```

### Products decorationimages property list

| Attribute | Description |
| --- | --- |
| code | 꾸미기 이미지 코드 |
| path | 꾸미기 이미지 URL |

### Retrieve a list of decoration images   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

```bash
Retrieve a list of decoration images        Retrieve a list of decoration images Retrieve decorationimages with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/decorationimages' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "decorationimages": [        {            "code": "imageicon_28_02",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_recommend2.png"        },        {            "code": "imageicon_27_01",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_plan1.png"        },        {            "code": "imageicon_26_02",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_own2.png"        },        {            "code": "image_custom_3",            "path": "https://{domain}/web/upload/image_custom_615421761805558.gif"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/decorationimages' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "decorationimages": [        {            "code": "imageicon_28_02",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_recommend2.png"        },        {            "code": "imageicon_27_01",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_plan1.png"        },        {            "code": "imageicon_26_02",            "path": "https://img.echosting.cafe24.com/skin/admin_ko_KR/product/ico_thumb_own2.png"        },        {            "code": "image_custom_3",            "path": "https://{domain}/web/upload/image_custom_615421761805558.gif"        }    ]}
```
