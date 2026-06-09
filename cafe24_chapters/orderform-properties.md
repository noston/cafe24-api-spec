# ORDERFORM PROPERTIES


## Orderform properties

```json
Endpoints    GET /api/v2/admin/orderform/properties
POST /api/v2/admin/orderform/properties
PUT /api/v2/admin/orderform/properties/{orderform_property_id}
DELETE /api/v2/admin/orderform/properties/{orderform_property_id}
```

```json
GET /api/v2/admin/orderform/properties
POST /api/v2/admin/orderform/properties
PUT /api/v2/admin/orderform/properties/{orderform_property_id}
DELETE /api/v2/admin/orderform/properties/{orderform_property_id}
```

### Orderform properties property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| additional_items | 주문서 추가항목 |
| input_type | 주문서 추가항목 입력 형식 T : 텍스트박스(한줄) M : 텍스트박스(여러줄) R : 라디오버튼 C : 체크박스 S : 셀렉트박스 D : 캘린더 I : 시간 |
| is_required | 주문서 추가항목 필수 여부 T : 필수 F : 선택 |
| subject | 주문서 추가항목명 |
| available_product_type | 적용 대상 상품 설정 A : 전체상품 C : 상품분류별 P : 개별상품 |
| input_scope | 입력값 적용 범위 (공통 또는 상품별) A : 공통으로 한번만 입력 받기 P : 상품별로 입력 받기 |
| description | 주문서 추가항목 설명 |
| field_length | 주문서 추가항목 필드 길이 (텍스트박스) |
| max_input_length | 주문서 추가항목 입력 가능한 최대 글자 수 |
| textarea_rows | 주문서 추가항목 행 수 (여러 줄 입력 시) |
| width_percentage | 주문서 추가항목 가로길이 (%) |
| option_values | 주문서 추가항목 입력값 |
| display_lines_desktop | 한 줄에 표시할 옵션 개수 (PC) |
| display_lines_mobile | 한 줄에 표시할 옵션 개수 (모바일) |
| category_no | 주문서 추가항목 지정 상품분류 번호 |
| product_no | 주문서 추가항목 지정 상품 번호 |
| orderform_property_id | 주문서 추가항목 고유번호 |

### Retrieve an additional checkout field   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve an additional checkout field        Retrieve an additional checkout field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "properties": {        "shop_no": 1,        "additional_items": [            {                "orderform_property_id": 1,                "input_type": "T",                "is_required": "T",                "subject": "text additional item name",                "description": "text additional item description",                "field_length": 10,                "max_input_length": 10,                "textarea_rows": 0,                "width_percentage": 0,                "option_values": "",                "display_lines_desktop": 0,                "display_lines_mobile": 0,                "available_product_type": "C",                "input_scope": "A",                "category_no": 24,                "product_no": null            },            {                "orderform_property_id": 6,                "input_type": "I",                "is_required": "F",                "subject": "time additional item name",                "description": "time additional item description",                "field_length": 0,                "max_input_length": 0,                "textarea_rows": 0,                "width_percentage": 0,                "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",                "display_lines_desktop": 0,                "display_lines_mobile": 0,                "available_product_type": "P",                "input_scope": "A",                "category_no": null,                "product_no": "22,23"            }        ]    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "properties": {        "shop_no": 1,        "additional_items": [            {                "orderform_property_id": 1,                "input_type": "T",                "is_required": "T",                "subject": "text additional item name",                "description": "text additional item description",                "field_length": 10,                "max_input_length": 10,                "textarea_rows": 0,                "width_percentage": 0,                "option_values": "",                "display_lines_desktop": 0,                "display_lines_mobile": 0,                "available_product_type": "C",                "input_scope": "A",                "category_no": 24,                "product_no": null            },            {                "orderform_property_id": 6,                "input_type": "I",                "is_required": "F",                "subject": "time additional item name",                "description": "time additional item description",                "field_length": 0,                "max_input_length": 0,                "textarea_rows": 0,                "width_percentage": 0,                "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",                "display_lines_desktop": 0,                "display_lines_mobile": 0,                "available_product_type": "P",                "input_scope": "A",                "category_no": null,                "product_no": "22,23"            }        ]    }}
```

### Create an additional checkout field   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| input_typeRequired | 주문서 추가항목 입력 형식   T : 텍스트박스(한줄) M : 텍스트박스(여러줄) R : 라디오버튼 C : 체크박스 S : 셀렉트박스 D : 캘린더 I : 시간 |
| is_requiredRequired | 주문서 추가항목 필수 여부   T : 필수 F : 선택 |
| subjectRequired | 주문서 추가항목명 |
| available_product_typeRequired | 적용 대상 상품 설정   A : 전체상품 C : 상품분류별 P : 개별상품 |
| input_scopeRequired | 입력값 적용 범위 (공통 또는 상품별)   A : 공통으로 한번만 입력 받기 P : 상품별로 입력 받기 |
| description최대글자수 : [500자] | 주문서 추가항목 설명 |
| field_length최소: [1]~최대: [250] | 주문서 추가항목 필드 길이 (텍스트박스)   input_type를 "T"로 선택 하였을때만 입력 가능 |
| max_input_length최소: [1]~최대: [250] | 주문서 추가항목 입력 가능한 최대 글자 수   input_type를 "T"로 선택 하였을때만 입력 가능 |
| textarea_rows최소: [1]~최대: [70] | 주문서 추가항목 행 수 (여러 줄 입력 시)   input_type를 "M"로 선택 하였을때만 입력 가능 |
| width_percentage최소: [1]~최대: [100] | 주문서 추가항목 가로길이 (%)   input_type를 "M"로 선택 하였을때만 입력 가능 |
| option_values | 주문서 추가항목 입력값   input_type를 "R", "C", "S", "I"로 선택 하였을때만 입력 가능input_type를 "R", "C", "S" 로 입력한 경우 구분자 "/" 로 입력(빨강/노랑/파랑)input_type를 "I" 로 입력한 경우 아래와 같이 시간정보를 입력예) "{"time_start":"00:00","time_end":"01:00","time_interval":"60"}   예) 빨강/노랑/파랑 |
| display_lines_desktop최소: [1]~최대: [999] | 한 줄에 표시할 옵션 개수 (PC)   input_type를 "R", "C"로 선택 하였을때만 입력 가능 |
| display_lines_mobile최소: [1]~최대: [999] | 한 줄에 표시할 옵션 개수 (모바일)   input_type를 "R", "C"로 선택 하였을때만 입력 가능 |
| category_no | 주문서 추가항목 지정 상품분류 번호   available_product_type를 "P"로 선택 하였을때만 입력 가능(C도 마찬가지) |
| product_no | 주문서 추가항목 지정 상품 번호   available_product_type를 "P"로 선택 하였을때만 입력 가능(C도 마찬가지) |

```bash
Create an additional checkout field        Create an additional checkout field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "input_type": "T",            "is_required": "T",            "subject": "text additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "text additional item description",            "field_length": 10,            "max_input_length": 10,            "textarea_rows": null,            "width_percentage": null,            "option_values": null,            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        },        {            "input_type": "I",            "is_required": "F",            "subject": "time additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "time additional item description",            "field_length": null,            "max_input_length": null,            "textarea_rows": null,            "width_percentage": null,            "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        }    ]}'    Response  Copy     {    "properties": [        {            "shop_no": 1,            "input_type": "T",            "is_required": "T",            "subject": "text additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "text additional item description",            "field_length": 10,            "max_input_length": 10,            "textarea_rows": null,            "width_percentage": null,            "option_values": null,            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        },        {            "shop_no": 1,            "input_type": "I",            "is_required": "F",            "subject": "time additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "time additional item description",            "field_length": null,            "max_input_length": null,            "textarea_rows": null,            "width_percentage": null,            "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        }    ]}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "requests": [        {            "input_type": "T",            "is_required": "T",            "subject": "text additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "text additional item description",            "field_length": 10,            "max_input_length": 10,            "textarea_rows": null,            "width_percentage": null,            "option_values": null,            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        },        {            "input_type": "I",            "is_required": "F",            "subject": "time additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "time additional item description",            "field_length": null,            "max_input_length": null,            "textarea_rows": null,            "width_percentage": null,            "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        }    ]}'
```

```json
{    "properties": [        {            "shop_no": 1,            "input_type": "T",            "is_required": "T",            "subject": "text additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "text additional item description",            "field_length": 10,            "max_input_length": 10,            "textarea_rows": null,            "width_percentage": null,            "option_values": null,            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        },        {            "shop_no": 1,            "input_type": "I",            "is_required": "F",            "subject": "time additional item name",            "available_product_type": "A",            "input_scope": "A",            "description": "time additional item description",            "field_length": null,            "max_input_length": null,            "textarea_rows": null,            "width_percentage": null,            "option_values": "{\"time_start\":\"00:00\",\"time_end\":\"01:00\",\"time_interval\":\"60\"}",            "display_lines_desktop": null,            "display_lines_mobile": null,            "category_no": null,            "product_no": null        }    ]}
```

### Update an additional checkout field   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| orderform_property_idRequired | 주문서 추가항목 고유번호 |
| input_type | 주문서 추가항목 입력 형식   T : 텍스트박스(한줄) M : 텍스트박스(여러줄) R : 라디오버튼 C : 체크박스 S : 셀렉트박스 D : 캘린더 I : 시간 |
| is_required | 주문서 추가항목 필수 여부   T : 필수 F : 선택 |
| subject | 주문서 추가항목명 |
| description최대글자수 : [500자] | 주문서 추가항목 설명 |
| field_length최소: [1]~최대: [250] | 주문서 추가항목 필드 길이 (텍스트박스)   input_type를 "T"로 선택 하였을때만 입력 가능 |
| max_input_length최소: [1]~최대: [250] | 주문서 추가항목 입력 가능한 최대 글자 수   input_type를 "T"로 선택 하였을때만 입력 가능 |
| textarea_rows최소: [1]~최대: [70] | 주문서 추가항목 행 수 (여러 줄 입력 시)   input_type를 "M"로 선택 하였을때만 입력 가능 |
| width_percentage최소: [1]~최대: [100] | 주문서 추가항목 가로길이 (%)   input_type를 "M"로 선택 하였을때만 입력 가능 |
| option_values | 주문서 추가항목 입력값   input_type를 "R", "C", "S", "I"로 선택 하였을때만 입력 가능input_type를 "R", "C", "S" 로 입력한 경우 구분자 "/" 로 입력(빨강/노랑/파랑)input_type를 "I" 로 입력한 경우 아래와 같이 시간정보를 입력예) "{"time_start":"00:00","time_end":"01:00","time_interval":"60"}   예) 빨강/노랑/파랑 |
| display_lines_desktop최소: [1]~최대: [999] | 한 줄에 표시할 옵션 개수 (PC)   input_type를 "R", "C"로 선택 하였을때만 입력 가능 |
| display_lines_mobile최소: [1]~최대: [999] | 한 줄에 표시할 옵션 개수 (모바일)   input_type를 "R", "C"로 선택 하였을때만 입력 가능 |
| available_product_type | 적용 대상 상품 설정   A : 전체상품 C : 상품분류별 P : 개별상품 |
| input_scope | 입력값 적용 범위 (공통 또는 상품별)   A : 공통으로 한번만 입력 받기 P : 상품별로 입력 받기 |
| category_no | 주문서 추가항목 지정 상품분류 번호   available_product_type를 "P"로 선택 하였을때만 입력 가능(C도 마찬가지) |
| product_no | 주문서 추가항목 지정 상품 번호   available_product_type를 "P"로 선택 하였을때만 입력 가능(C도 마찬가지) |

```bash
Update an additional checkout field        Update an additional checkout field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "input_type": "T",        "is_required": "T",        "subject": "text additional item name",        "description": "text additional item description",        "field_length": 10,        "max_input_length": 10,        "available_product_type": "A",        "input_scope": "A"    }}'    Response  Copy     {    "properties": {        "shop_no": 1,        "input_type": "T",        "is_required": "T",        "subject": "text additional item name",        "description": "text additional item description",        "field_length": 10,        "max_input_length": 10,        "available_product_type": "A",        "input_scope": "A"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "input_type": "T",        "is_required": "T",        "subject": "text additional item name",        "description": "text additional item description",        "field_length": 10,        "max_input_length": 10,        "available_product_type": "A",        "input_scope": "A"    }}'
```

```json
{    "properties": {        "shop_no": 1,        "input_type": "T",        "is_required": "T",        "subject": "text additional item name",        "description": "text additional item description",        "field_length": 10,        "max_input_length": 10,        "available_product_type": "A",        "input_scope": "A"    }}
```

### Delete an additional checkout field   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| orderform_property_idRequired | 주문서 추가항목 고유번호 |

```bash
Delete an additional checkout field        Delete an additional checkout field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "properties": {        "shop_no": 1,        "orderform_property_id": 10    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orderform/properties/10' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "properties": {        "shop_no": 1,        "orderform_property_id": 10    }}
```
