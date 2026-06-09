# CARTS


## Carts

```json
Endpoints    GET /api/v2/admin/carts
```

```json
GET /api/v2/admin/carts
```

### Carts property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| basket_product_no | 장바구니 상품번호 |
| member_id | 회원아이디 |
| created_date | 담은일자 |
| product_no | 상품번호 |
| additional_option_values | 추가입력 옵션 |
| variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 상품 품목 코드 |
| quantity | 수량 |
| product_price | 상품 판매가 |
| option_price | 옵션 추가 가격 |
| product_bundle | 세트상품 여부 T : 세트상품 F : 세트상품 아님 |
| shipping_type | 배송 유형 A : 국내 B : 해외 |
| category_no | 분류 번호 |

### Retrieve a shopping cart   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 개인화정보 읽기권한 (mall.read_personal) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디   ,(콤마)로 여러 건을 검색할 수 있다. |
| offset최대값: [10000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   DEFAULT 10 |

```bash
Retrieve a shopping cart        Retrieve a shopping cart Retrieve carts with fields parameter Retrieve carts using paging       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/carts?member_id=sampleid,sampleid2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "carts": [        {            "shop_no": 1,            "basket_product_no": 5,            "member_id": "sampleid",            "created_date": "2019-08-09T10:49:11+09:00",            "product_no": 9,            "additional_option_values": [                {                    "key": "item_option_add",                    "type": "text",                    "value": "Custom Option",                    "name": "Custom Option Value"                },                {                    "key": "file_option",                    "type": "url",                    "value": "http://sample.com/api/product/fileupload/?cmd=download&path=b%2Fe%2Fbee9c3eb338e6161886c8e6fefedbd4a5c170bac0dfc4&filename=35_shop1_123081.gif",                    "name": "Attached File"                }            ],            "variant_code": "P000000R000C",            "quantity": 2,            "product_price": "5000.00",            "option_price": "5000.00",            "product_bundle": "F",            "shipping_type": "A",            "category_no": 1        },        {            "shop_no": 1,            "basket_product_no": 6,            "member_id": "sampleid2",            "created_date": "2019-08-08T10:26:05+09:00",            "product_no": 10,            "additional_option_values": [],            "variant_code": "P000000J000A",            "quantity": 1,            "product_price": "10000.00",            "option_price": "0.00",            "product_bundle": "F",            "shipping_type": "A",            "category_no": 1        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/carts?member_id=sampleid,sampleid2' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "carts": [        {            "shop_no": 1,            "basket_product_no": 5,            "member_id": "sampleid",            "created_date": "2019-08-09T10:49:11+09:00",            "product_no": 9,            "additional_option_values": [                {                    "key": "item_option_add",                    "type": "text",                    "value": "Custom Option",                    "name": "Custom Option Value"                },                {                    "key": "file_option",                    "type": "url",                    "value": "http://sample.com/api/product/fileupload/?cmd=download&path=b%2Fe%2Fbee9c3eb338e6161886c8e6fefedbd4a5c170bac0dfc4&filename=35_shop1_123081.gif",                    "name": "Attached File"                }            ],            "variant_code": "P000000R000C",            "quantity": 2,            "product_price": "5000.00",            "option_price": "5000.00",            "product_bundle": "F",            "shipping_type": "A",            "category_no": 1        },        {            "shop_no": 1,            "basket_product_no": 6,            "member_id": "sampleid2",            "created_date": "2019-08-08T10:26:05+09:00",            "product_no": 10,            "additional_option_values": [],            "variant_code": "P000000J000A",            "quantity": 1,            "product_price": "10000.00",            "option_price": "0.00",            "product_bundle": "F",            "shipping_type": "A",            "category_no": 1        }    ]}
```
