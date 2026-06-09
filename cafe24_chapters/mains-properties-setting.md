# MAINS PROPERTIES SETTING


## Mains properties setting

```json
Endpoints    GET /api/v2/admin/mains/properties/setting
PUT /api/v2/admin/mains/properties/setting
```

```json
GET /api/v2/admin/mains/properties/setting
PUT /api/v2/admin/mains/properties/setting
```

### Mains properties setting property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| strikethrough_retail_price | 소비자가 취소선 표시 |
| strikethrough_price | 판매가 취소선 표시 |
| product_tax_type_text | 판매가 부가세 표시문구 |
| product_discount_price_text | 할인판매가 할인금액 표시문구 |
| optimum_discount_price_text | 최적할인가 할인금액 표시문구 |

### Retrieve additional settings for products on the main screen   cafe24

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
Retrieve additional settings for products on the main screen        Retrieve additional settings for products on the main screen       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/properties/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "main": {        "shop_no": 1,        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "T",            "color": "#999999",            "font_size": 12,            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": 14,            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": 14,            "font_type": "N"        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/properties/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "main": {        "shop_no": 1,        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "T",            "color": "#999999",            "font_size": 12,            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": 14,            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": 14,            "font_type": "N"        }    }}
```

### Update additional settings for products on the main screen   cafe24

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
| strikethrough_retail_price | 소비자가 취소선 표시   T : 사용함 F : 사용안함 |
| strikethrough_price | 판매가 취소선 표시   T : 사용함 F : 사용안함 |
| product_tax_type_text | 판매가 부가세 표시문구 |
| product_tax_type_text 하위 요소 보기     use사용 여부T : 사용함 F : 사용안함 color글자 색상 font_size글자 크기 font_type글자 타입N : 보통(Normal) B : 굵게(Bold) I : 기울임(Italic) D : 굵게 기울임(Bold Italic) |
| product_discount_price_text | 할인판매가 할인금액 표시문구 |
| product_discount_price_text 하위 요소 보기     use사용 여부T : 사용함 F : 사용안함 color글자 색상 font_size글자 크기 font_type글자 타입N : 보통(Normal) B : 굵게(Bold) I : 기울임(Italic) D : 굵게 기울임(Bold Italic) |
| optimum_discount_price_text | 최적할인가 할인금액 표시문구 |
| optimum_discount_price_text 하위 요소 보기     use사용 여부T : 사용함 F : 사용안함 color글자 색상 font_size글자 크기 font_type글자 타입N : 보통(Normal) B : 굵게(Bold) I : 기울임(Italic) D : 굵게 기울임(Bold Italic) |

```bash
Update additional settings for products on the main screen        Update additional settings for products on the main screen       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/properties/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "F",            "color": "#999999",            "font_size": "12",            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": "14",            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": "14",            "font_type": "N"        }    }}'    Response  Copy     {    "main": {        "shop_no": 1,        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "F",            "color": "#999999",            "font_size": "12",            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": "14",            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": "14",            "font_type": "N"        }    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/mains/properties/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "F",            "color": "#999999",            "font_size": "12",            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": "14",            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": "14",            "font_type": "N"        }    }}'
```

```json
{    "main": {        "shop_no": 1,        "strikethrough_retail_price": "F",        "strikethrough_price": "T",        "product_tax_type_text": {            "use": "F",            "color": "#999999",            "font_size": "12",            "font_type": "N"        },        "product_discount_price_text": {            "use": "T",            "color": "#FF5B59",            "font_size": "14",            "font_type": "N"        },        "optimum_discount_price_text": {            "use": "T",            "color": "#0066FF",            "font_size": "14",            "font_type": "N"        }    }}
```
