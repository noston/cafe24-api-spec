# SUPPLIERS USERS


## Suppliers users

```json
Endpoints    GET /api/v2/admin/suppliers/users
GET /api/v2/admin/suppliers/users/count
GET /api/v2/admin/suppliers/users/{user_id}
POST /api/v2/admin/suppliers/users
PUT /api/v2/admin/suppliers/users/{user_id}
DELETE /api/v2/admin/suppliers/users/{user_id}
```

```json
GET /api/v2/admin/suppliers/users
GET /api/v2/admin/suppliers/users/count
GET /api/v2/admin/suppliers/users/{user_id}
POST /api/v2/admin/suppliers/users
PUT /api/v2/admin/suppliers/users/{user_id}
DELETE /api/v2/admin/suppliers/users/{user_id}
```

### Suppliers users property list

| Attribute | Description |
| --- | --- |
| user_id형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디 공급사 운영자가 로그인할 경우 사용하는 로그인 아이디. 부운영자와 마찬가지로 쇼핑몰 관리자 화면에 로그인하면 공급사 관리자 화면에 접근할 수 있다. |
| supplier_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 공급사 코드 시스템에서 부여한 공급사의 코드. 해당 쇼핑몰 내에서 공급사 코드는 중복되지 않는다. |
| supplier_name최대글자수 : [100자] | 공급사명 공급사의 이름. 공급사명은 쇼핑몰 관리자 화면에서 공급사를 구분할 수 있는 기본적인 정보이다. |
| permission_category_select | 상품 등록 시 분류선택 권한 공급사 운영자가 상품 등록시 상품 분류를 선택하여 등록할 수 있는지에 대한 권한 설정 |
| permission_product_modify | 상품 수정 권한 공급사 운영자가 상품을 등록한 후 상품 정보를 수정할 수 있는 권한 설정 |
| permission_product_display | 상품 진열 권한 공급사 운영자가 상품을 등록한 후 쇼핑몰 화면에 진열할 수 있는 권한 설정 |
| permission_product_selling | 상품 판매 권한 공급사 운영자가 상품을 등록한 후 해당 상품의 판매여부를 설정할 수 있는 권한 설정 |
| permission_product_delete | 등록 상품 삭제 권한 공급사 운영자가 자신이 등록한 상품을 삭제할 수 있는 권한 설정 |
| permission_amount_inquiry | 주문 금액 조회 권한 |
| permission_board_manage | 게시판 권한 설정 공급사 운영자가 쇼핑몰의 게시판에 접근할 수 있는 권한 설정 T : 허용함 F : 허용안함 |
| permission_order_menu | 주문 메뉴 접근 권한 |
| permission_order_cs | 취소/교환/반품/환불 처리 권한 |
| permission_order_refund | 환불 완료 처리 |
| user_name | 공급사운영자명 공급사 운영자의 이름. 공급사 운영자 명은 공급사 운영자가 쇼핑몰 관리자 화면에서 어떤 작업을 할 경우 "작업을 실행한 사람(처리자)" 부분에 표시되는 이름을 의미한다. 공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| nick_name | 별명 공급사 운영자의 별명. 공급사 운영자 별명은 공급사 운영자가 게시판에 게시글 작성할 경우 "게시자" 부분에 표시되는 별명을 의미한다.(단, 해당 게시판이 작성자명 대신 '별명'을 노출하도록 설정되어있을 경우에 한 함) 공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| nick_name_icon_type | 별명 아이콘 타입 공급사 운영자의 별명 옆에 표시되는 아이콘을 설정할 수 있다.  직접 아이콘 등록 : 별명 아이콘을 직접 업로드하여 설정할 수 있다. 샘플 아이콘 등록 : 미리 제공되는 아이콘을 선택하여 설정할 수 있다. 공급사 운영자 상세 조회 API에서만 확인 가능하다. D : 직접 S : 샘플 |
| nick_name_icon_url최대글자수 : [255자] | 별명 아이콘 URL 공급사 운영자의 별명 아이콘의 이미지 경로.  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| use_nick_name_icon | 게시판 닉네임 아이콘 노출 설정 공급사 운영자가 게시판에 게시글 작성시 별명 아이콘을 노출할 것인지 여부 표시  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| use_writer_name_icon | 게시판 작성자 노출 설정 공급사 운영자가 게시판에 게시글 작성시 작성자 명을 노출할 것인지 여부 표시  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| email이메일 | 이메일 공급사 운영자의 이메일 주소. 공급사 운영자의 연락처 저장 목적으로 사용함.  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| phone | 전화번호 공급사 운영자의 전화번호. 공급사 운영자의 연락처 저장 목적으로 사용함.  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| permission_shop_no | 접근가능 쇼핑몰 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| permitted_category_list | 상품 등록시 허용 상품분류 공급사 운영자가 상품 등록시 선택 가능한 상품 분류. 공급사 운영자는 상품 등록시 해당 상품 분류에만 상품을 올릴 수 있다.  공급사 운영자 상세 조회 API에서만 확인 가능하다. |
| permission_delivery_fee_inquiry | 배송비 조회 권한 |

### Retrieve a list of supplier users   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| user_id형식 : [a-zA-Z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디   공급사 운영자가 로그인할 경우 사용하는 로그인 아이디. 부운영자와 마찬가지로 쇼핑몰 관리자 화면에 로그인하면 공급사 관리자 화면에 접근할 수 있다. |
| supplier_code최대글자수 : [8자] | 공급사 코드   시스템에서 부여한 공급사의 코드. 해당 쇼핑몰 내에서 공급사 코드는 중복되지 않는다. |
| supplier_name최대글자수 : [100자] | 공급사명   공급사의 이름. 공급사명은 쇼핑몰 관리자 화면에서 공급사를 구분할 수 있는 기본적인 정보이다. |
| offset최대값: [8000] | 조회결과 시작위치   DEFAULT 0 |
| limit최소: [1]~최대: [100] | 조회결과 최대건수   조회하고자 하는 최대 건수를 지정할 수 있음. 예) 10 입력시 10건만 표시함.   DEFAULT 10 |

```bash
Retrieve a list of supplier users        Retrieve a list of supplier users Retrieve users with fields parameter Retrieve a specific users with supplier_code parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "users": [        {            "user_id": "S0000000",            "supplier_code": "S0000000",            "supplier_name": "Default Supplier",            "permission_category_select": "",            "permission_product_modify": "T",            "permission_product_display": "",            "permission_product_selling": "T",            "permission_product_delete": "",            "permission_board_manage": "F",            "permission_amount_inquiry": "F",            "permission_order_menu": "F",            "permission_order_cs": "F",            "permission_order_refund": "F"        },        {            "user_id": "applesupply",            "supplier_code": "S000000A",            "supplier_name": "Apple",            "permission_category_select": "T",            "permission_product_modify": "T",            "permission_product_display": "T",            "permission_product_selling": "T",            "permission_product_delete": "T",            "permission_board_manage": "T",            "permission_amount_inquiry": "T",            "permission_order_menu": "F",            "permission_order_cs": "F",            "permission_order_refund": "F"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "users": [        {            "user_id": "S0000000",            "supplier_code": "S0000000",            "supplier_name": "Default Supplier",            "permission_category_select": "",            "permission_product_modify": "T",            "permission_product_display": "",            "permission_product_selling": "T",            "permission_product_delete": "",            "permission_board_manage": "F",            "permission_amount_inquiry": "F",            "permission_order_menu": "F",            "permission_order_cs": "F",            "permission_order_refund": "F"        },        {            "user_id": "applesupply",            "supplier_code": "S000000A",            "supplier_name": "Apple",            "permission_category_select": "T",            "permission_product_modify": "T",            "permission_product_display": "T",            "permission_product_selling": "T",            "permission_product_delete": "T",            "permission_board_manage": "T",            "permission_amount_inquiry": "T",            "permission_order_menu": "F",            "permission_order_cs": "F",            "permission_order_refund": "F"        }    ]}
```

### Retrieve a count of supplier users   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| user_id형식 : [a-zA-Z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디   공급사 운영자가 로그인할 경우 사용하는 로그인 아이디. 부운영자와 마찬가지로 쇼핑몰 관리자 화면에 로그인하면 공급사 관리자 화면에 접근할 수 있다. |
| supplier_code최대글자수 : [8자] | 공급사 코드   시스템에서 부여한 공급사의 코드. 해당 쇼핑몰 내에서 공급사 코드는 중복되지 않는다. |
| supplier_name최대글자수 : [100자] | 공급사명   공급사의 이름. 공급사명은 쇼핑몰 관리자 화면에서 공급사를 구분할 수 있는 기본적인 정보이다. |

```bash
Retrieve a count of supplier users        Retrieve a count of supplier users       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "count": 2}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/count' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "count": 2}
```

### Retrieve supplier user details   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 읽기권한 (mall.read_supply) |
| 호출건수 제한 | 10 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| user_id형식 : [a-zA-Z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디   공급사 운영자가 로그인할 경우 사용하는 로그인 아이디. 부운영자와 마찬가지로 쇼핑몰 관리자 화면에 로그인하면 공급사 관리자 화면에 접근할 수 있다. |

```bash
Retrieve supplier user details        Retrieve supplier user details Retrieve a supplier user with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/supplyone' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "user": {        "user_id": "supplyone",        "supplier_code": "S000000A",        "supplier_name": "Apple",        "user_name": "Apple Product Supplier",        "nick_name": "Guysinapple",        "nick_name_icon_type": "D",        "nick_name_icon_url": "https://{domain}/web/upload/admin1.gif",        "use_nick_name_icon": "T",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "010-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            29,            27,            28,            33        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "F",        "permission_board_manage": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "F",        "permission_order_cs": "F",        "permission_order_refund": "F"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/supplyone' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "user": {        "user_id": "supplyone",        "supplier_code": "S000000A",        "supplier_name": "Apple",        "user_name": "Apple Product Supplier",        "nick_name": "Guysinapple",        "nick_name_icon_type": "D",        "nick_name_icon_url": "https://{domain}/web/upload/admin1.gif",        "use_nick_name_icon": "T",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "010-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            29,            27,            28,            33        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "F",        "permission_board_manage": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "F",        "permission_order_cs": "F",        "permission_order_refund": "F"    }}
```

### Create a supplier user   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| user_idRequired형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디 |
| supplier_codeRequired형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 공급사 코드 |
| user_name | 공급사운영자명   필수 입력 필요 |
| user_name 하위 요소 보기     shop_noRequired멀티쇼핑몰 번호 user_nameRequired공급사운영자명 |
| nick_name | 별명 |
| nick_name 하위 요소 보기     shop_no멀티쇼핑몰 번호 nick_name별명 |
| passwordRequired | 접속 비밀번호 |
| use_nick_name_icon | 게시판 닉네임 아이콘 노출 설정   T : 사용함 F : 사용안함   DEFAULT F |
| use_writer_name_icon | 게시판 작성자 노출 설정   T : 사용함 F : 사용안함   DEFAULT F |
| email이메일 | 이메일 |
| phone | 전화번호 |
| permission_shop_noRequired | 접근가능 쇼핑몰 |
| permission_category_select | 상품 등록 시 분류선택 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permitted_category_list | 상품 등록시 허용 상품분류 |
| permission_product_modify | 상품 수정 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permission_product_display | 상품 진열 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permission_product_selling | 상품 판매 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permission_product_delete | 등록 상품 삭제 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permission_order_menu | 주문 메뉴 접근 권한   T : 사용함 F : 사용안함   DEFAULT T |
| permission_amount_inquiry | 주문 금액 조회 권한   T : 사용함 F : 사용안함   DEFAULT F |
| permission_order_cs | 취소/교환/반품/환불 처리 권한   T : 사용함 F : 사용안함   DEFAULT F |
| permission_order_refund | 환불 완료 처리   T : 사용함 F : 사용안함   DEFAULT F |
| permission_delivery_fee_inquiry | 배송비 조회 권한   T : 사용함 F : 사용안함   DEFAULT F |

```bash
Create a supplier user        Create a supplier user Create a supplier user by using only required fields Try creating a supplier user wihtout using user_id field Try creating a supplier user wihtout using supplier_code field Try creating a supplier user wihtout using user_name field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "password": "abc1237890",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_order_menu": "T",        "permission_amount_inquiry": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}'    Response  Copy     {    "user": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_order_menu": "T",        "permission_amount_inquiry": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "password": "abc1237890",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_order_menu": "T",        "permission_amount_inquiry": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}'
```

```json
{    "user": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_order_menu": "T",        "permission_amount_inquiry": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}
```

### Update a supplier user   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| user_idRequired형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디 |
| user_name | 공급사운영자명   필수 입력 필요 |
| user_name 하위 요소 보기     shop_no멀티쇼핑몰 번호 user_name공급사운영자명 |
| nick_name | 별명 |
| nick_name 하위 요소 보기     shop_no멀티쇼핑몰 번호 nick_name별명 |
| password | 접속 비밀번호 |
| use_nick_name_icon | 게시판 닉네임 아이콘 노출 설정   T : 사용함 F : 사용안함 |
| use_writer_name_icon | 게시판 작성자 노출 설정   T : 사용함 F : 사용안함 |
| email이메일 | 이메일 |
| phone | 전화번호 |
| permission_shop_no | 접근가능 쇼핑몰 |
| permission_category_select | 상품 등록 시 분류선택 권한   T : 사용함 F : 사용안함 |
| permitted_category_list | 상품 등록시 허용 상품분류 |
| permission_product_modify | 상품 수정 권한   T : 사용함 F : 사용안함 |
| permission_product_display | 상품 진열 권한   T : 사용함 F : 사용안함 |
| permission_product_selling | 상품 판매 권한   T : 사용함 F : 사용안함 |
| permission_product_delete | 등록 상품 삭제 권한   T : 사용함 F : 사용안함 |
| permission_order_menu | 주문 메뉴 접근 권한   T : 사용함 F : 사용안함 |
| permission_amount_inquiry | 주문 금액 조회 권한   T : 사용함 F : 사용안함 |
| permission_order_cs | 취소/교환/반품/환불 처리 권한   T : 사용함 F : 사용안함 |
| permission_order_refund | 환불 완료 처리   T : 사용함 F : 사용안함 |
| permission_delivery_fee_inquiry | 배송비 조회 권한   T : 사용함 F : 사용안함   DEFAULT F |

```bash
Update a supplier user        Update a supplier user Update supplier's name, email, phone number Update supplier's permission       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "password": "abc1237890",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2,            3        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}'    Response  Copy     {    "user": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2,            3        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "password": "abc1237890",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2,            3        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}'
```

```json
{    "user": {        "user_id": "sampleid",        "supplier_code": "S000000J",        "user_name": [            {                "shop_no": 1,                "user_name": "John Doe"            },            {                "shop_no": 2,                "user_name": "John Doe"            }        ],        "nick_name": [            {                "shop_no": 1,                "nick_name": "nickname1"            },            {                "shop_no": 2,                "nick_name": "nickname2"            }        ],        "use_nick_name_icon": "F",        "use_writer_name_icon": "F",        "email": "sample@sample.com",        "phone": "02-0000-0000",        "permission_shop_no": [            1,            2        ],        "permission_category_select": "T",        "permitted_category_list": [            1,            2,            3        ],        "permission_product_modify": "T",        "permission_product_display": "T",        "permission_product_selling": "T",        "permission_product_delete": "T",        "permission_amount_inquiry": "T",        "permission_order_menu": "T",        "permission_order_cs": "F",        "permission_order_refund": "F",        "permission_delivery_fee_inquiry": "F"    }}
```

### Delete a supplier user   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 공급사 정보 쓰기권한 (mall.write_supply) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| user_idRequired형식 : [a-z0-9]글자수 최소: [4자]~최대: [16자] | 공급사 운영자 아이디 |

```bash
Delete a supplier user        Delete a supplier user       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "user": {        "user_id": "sampleid"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/suppliers/users/sampleid' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "user": {        "user_id": "sampleid"    }}
```
