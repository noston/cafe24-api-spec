# NAVERPAY SETTING


## Naverpay setting

```json
Endpoints    GET /api/v2/admin/naverpay/setting
POST /api/v2/admin/naverpay/setting
PUT /api/v2/admin/naverpay/setting
```

```json
GET /api/v2/admin/naverpay/setting
POST /api/v2/admin/naverpay/setting
PUT /api/v2/admin/naverpay/setting
```

### Naverpay setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| authentication_key | 네이버 공통 인증키 |
| naverpay_version | 네이버페이 연동버전 |
| shop_id | 페이센터 ID |
| is_button_show | 네이버페이 구매 버튼 노출 |
| is_used_order | 네이버 주문연동 |
| is_used_review | 네이버 구매평연동 |
| is_show_review | 네이버 구매평노출 |
| is_order_page | 네이버페이 구매 버튼 클릭 시 페이지 이동 |
| certi_key | 네이버 가맹점 인증키 |
| image_key | 네이버 버튼 인증키 |
| naver_button_pc_product | 네이버 버튼 디자인 : PC 상품상세페이지 |
| naver_button_pc_basket | 네이버 버튼 디자인 : PC 장바구니페이지 |
| naver_button_mobile_product | 네이버 버튼 디자인 : Mobile 상품상세페이지 |
| naver_button_mobile_basket | 네이버 버튼 디자인 : Mobile 장바구니페이지 |

### Retrieve Naver Pay settings   cafe24

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
Retrieve Naver Pay settings        Retrieve Naver Pay settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "naverpay": {        "shop_no": "1",        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "naverpay": {        "shop_no": "1",        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}
```

### Create Naver Pay settings   cafe24

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
| authentication_key형식 : [a-zA-Z0-9_-]최대글자수 : [50자] | 네이버 공통 인증키 |
| naverpay_version | 네이버페이 연동버전   DEFAULT 2.1 |
| shop_idRequired | 페이센터 ID |
| is_button_show | 네이버페이 구매 버튼 노출   DEFAULT T |
| is_used_order | 네이버 주문연동   DEFAULT T |
| is_used_review | 네이버 구매평연동   DEFAULT T |
| is_show_review | 네이버 구매평노출   DEFAULT T |
| is_order_page | 네이버페이 구매 버튼 클릭 시 페이지 이동   DEFAULT N |
| certi_keyRequired | 네이버 가맹점 인증키 |
| image_keyRequired | 네이버 버튼 인증키 |
| naver_button_pc_product | 네이버 버튼 디자인 : PC 상품상세페이지   DEFAULT A|1|2 |
| naver_button_pc_basket | 네이버 버튼 디자인 : PC 장바구니페이지   DEFAULT A|1|1 |
| naver_button_mobile_product | 네이버 버튼 디자인 : Mobile 상품상세페이지   DEFAULT MA|1|2 |
| naver_button_mobile_basket | 네이버 버튼 디자인 : Mobile 장바구니페이지   DEFAULT MA|1|1 |

```bash
Create Naver Pay settings        Create Naver Pay settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}'    Response  Copy     {    "naverpay": {        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}'
```

```json
{    "naverpay": {        "authentication_key": "s_abcdefg",        "naverpay_version": "2.1",        "shop_id": "c_abcdefg",        "is_button_show": "T",        "is_used_order": "T",        "is_used_review": "T",        "is_show_review": "T",        "s_order_page": "N",        "certi_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "image_key": "ABC1234A-1A1A-1A23-1234-A12345A1A12A",        "naver_button_pc_product": "A|1|2",        "naver_button_pc_basket": "A|1|1",        "naver_button_mobile_product": "MA|1|2",        "naver_button_mobile_basket": "MA|1|1"    }}
```

### Update Naver Pay settings   cafe24

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
| authentication_key형식 : [a-zA-Z0-9_-]최대글자수 : [50자] | 네이버 공통 인증키 |

```bash
Update Naver Pay settings        Update Naver Pay settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "authentication_key": "s_abcdefg"    }}'    Response  Copy     {    "naverpay": {        "shop_no": 1,        "authentication_key": "s_abcdefg"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/naverpay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "authentication_key": "s_abcdefg"    }}'
```

```json
{    "naverpay": {        "shop_no": 1,        "authentication_key": "s_abcdefg"    }}
```
