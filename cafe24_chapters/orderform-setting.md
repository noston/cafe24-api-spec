# ORDERFORM SETTING


## Orderform setting

```json
Endpoints    GET /api/v2/admin/orderform/setting
PUT /api/v2/admin/orderform/setting
```

```json
GET /api/v2/admin/orderform/setting
PUT /api/v2/admin/orderform/setting
```

### Orderform setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| buy_limit_type | 구매 제한 M:회원만 구매 A:모두 구매 가능 |
| guest_purchase_button_display | 비회원 구매버튼 노출 buy_limit_type를 M(회원만 구매)으로 선택 하였을때만 설정 가능 T : 사용함 F : 사용안함 |
| junior_purchase_block | 14세 미만 구매 차단 buy_limit_type를 A(모두 구매 가능)으로 선택하였을때만 설정 가능 T : 사용함 F : 사용안함 |
| reservation_order | 예약주문 T : 사용함 F : 사용안함 |
| discount_amount_display | 주문상품 할인금액 표시 T : 사용함 F : 사용안함 |
| order_item_delete | 주문서 내 상품삭제 T : 사용함 F : 사용안함 |
| quick_signup | 주문서 간단회원가입 T : 사용함 F : 사용안함 |
| check_order_info | 주문서 입력정보 확인 T : 사용함 F : 사용안함 |
| order_form_input_type | 주문서 입력정보 구성 A : 배송정보만 입력 S : 주문/배송정보 개별입력 |
| shipping_info | 주문서 입력정보 상세설정 > 배송 정보 |
| order_info | 주문서 입력정보 상세설정 > 주문 정보 order_form_input_type이 A일때 order_info 입력 불가 |
| china_taiwan_id_input | 중국/대만 신분증 ID 입력 T : 사용함 F : 사용안함 |
| print_type | 인쇄버튼 타입 |
| orderform_additional_enabled | 주문서 추가항목 사용여부 T : 사용 F : 사용안함 |

### Retrieve the order/order form settings   cafe24

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
Retrieve the order/order form settings        Retrieve the order/order form settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "orderform": {        "shop_no": 1,        "buy_limit_type": "M",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "F",        "discount_amount_display": "T",        "order_item_delete": "F",        "quick_signup": "F",        "check_order_info": "F",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "F",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "orderform": {        "shop_no": 1,        "buy_limit_type": "M",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "F",        "discount_amount_display": "T",        "order_item_delete": "F",        "quick_signup": "F",        "check_order_info": "F",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "F",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}
```

### Update the order/order form settings   cafe24

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
| buy_limit_type | 구매 제한   M:회원만 구매 A:모두 구매 가능 |
| guest_purchase_button_display | 비회원 구매버튼 노출   buy_limit_type를 M(회원만 구매)으로 선택 하였을때만 설정 가능   T : 사용함 F : 사용안함 |
| junior_purchase_block | 14세 미만 구매 차단   buy_limit_type를 A(모두 구매 가능)으로 선택하였을때만 설정 가능   T : 사용함 F : 사용안함 |
| reservation_order | 예약주문   T : 사용함 F : 사용안함 |
| discount_amount_display | 주문상품 할인금액 표시   T : 사용함 F : 사용안함 |
| order_item_delete | 주문서 내 상품삭제   T : 사용함 F : 사용안함 |
| quick_signup | 주문서 간단회원가입   T : 사용함 F : 사용안함 |
| check_order_info | 주문서 입력정보 확인   T : 사용함 F : 사용안함 |
| order_form_input_type | 주문서 입력정보 구성   A : 배송정보만 입력 S : 주문/배송정보 개별입력 |
| shipping_info | 주문서 입력정보 상세설정 > 배송 정보 |
| shipping_info 하위 요소 보기     key배송정보 설정항목키name(이름) address(주소) detail_address(상세주소) phone(전화번호) cellphone(휴대폰번호) shipping_message(배송메시지) email(이메일) : order_form_input_type이 S일때 입력 불가 use배송정보 설정항목 사용여부 required배송정보 설정항목 필수여부 |
| order_info | 주문서 입력정보 상세설정 > 주문 정보   order_form_input_type이 A일때 order_info 입력 불가 |
| order_info 하위 요소 보기     key주문정보 설정항목키name(이름) address(주소) detail_address(상세주소) phone(전화번호) cellphone(휴대폰번호) email(이메일) use주문정보 설정항목 사용여부 required주문정보 설정항목 필수여부 |
| china_taiwan_id_input | 중국/대만 신분증 ID 입력   T : 사용함 F : 사용안함 |
| print_type | 인쇄버튼 타입 |
| print_type 하위 요소 보기     invoice_print거래명세서 인쇄버튼T : 표시함 F : 표시안함 receipt_print매출전표 인쇄버튼T : 표시함 F : 표시안함 address_print수령지정보 인쇄버튼T : 표시함 F : 표시안함 |
| orderform_additional_enabled | 주문서 추가항목 사용여부   T:사용 F:사용안함 |

```bash
Update the order/order form settings        Update the order/order form settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "buy_limit_type": "A",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "T",        "discount_amount_display": "T",        "order_item_delete": "T",        "quick_signup": "T",        "check_order_info": "T",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "T",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}'    Response  Copy     {    "orderform": {        "shop_no": 1,        "buy_limit_type": "A",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "T",        "discount_amount_display": "T",        "order_item_delete": "T",        "quick_signup": "T",        "check_order_info": "T",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "T",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "buy_limit_type": "A",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "T",        "discount_amount_display": "T",        "order_item_delete": "T",        "quick_signup": "T",        "check_order_info": "T",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "T",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}'
```

```json
{    "orderform": {        "shop_no": 1,        "buy_limit_type": "A",        "guest_purchase_button_display": "T",        "junior_purchase_block": "F",        "reservation_order": "T",        "discount_amount_display": "T",        "order_item_delete": "T",        "quick_signup": "T",        "check_order_info": "T",        "order_form_input_type": "S",        "shipping_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "order_info": [            {                "key": "phone",                "use": "T",                "required": "F"            },            {                "key": "cellphone",                "use": "T",                "required": "F"            }        ],        "china_taiwan_id_input": "T",        "print_type": {            "invoice_print": "T",            "receipt_print": "F",            "address_print": "F"        },        "orderform_additional_enabled": "T"    }}
```
