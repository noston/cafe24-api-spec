# KAKAOPAY SETTING


## Kakaopay setting

```json
Endpoints    GET /api/v2/admin/kakaopay/setting
PUT /api/v2/admin/kakaopay/setting
```

```json
GET /api/v2/admin/kakaopay/setting
PUT /api/v2/admin/kakaopay/setting
```

### Kakaopay setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| shop_key | 입점시 부여 받는 판매점의 고유 식별자 |
| pixel_code | 연동사(ECP/독립몰)에서 이미 사용중인 카카오 광고 픽셀 ID |
| use_kakaopay | 카카오페이 구매 사용여부 T : 사용함 F : 사용안함 |
| product_detail_button_size | 쇼핑몰 상세상품 페이지 버튼 사이즈 |
| basket_button_size | 쇼핑몰 장바구니 페이지 버튼 사이즈 |
| use_dark_mode | 쇼핑몰 다크모드 적용여부 T : 활성화 F : 비활성화 |
| button_authorization_key | 입점시 부여 받는 판매점의 버튼 인증 |
| thirdparty_agree | 제3자 제공 동의 여부 T : 동의함 F : 동의안함 |
| thirdparty_agree_date | 제3자 제공 동의 날짜 |

### Retrieve settings for KakaoPay orders   cafe24

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
Retrieve settings for KakaoPay orders        Retrieve settings for KakaoPay orders       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaopay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "kakaopay": {        "shop_no": 1,        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaopay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "kakaopay": {        "shop_no": 1,        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}
```

### Update settings for KakaoPay orders   cafe24

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
| shop_key | 입점시 부여 받는 판매점의 고유 식별자 |
| pixel_code | 연동사(ECP/독립몰)에서 이미 사용중인 카카오 광고 픽셀 ID |
| use_kakaopay | 카카오페이 구매 사용여부   T : 사용함 F : 사용안함 |
| product_detail_button_size | 쇼핑몰 상세상품 페이지 버튼 사이즈 |
| product_detail_button_size 하위 요소 보기     pcpc mobilemobile |
| basket_button_size | 쇼핑몰 장바구니 페이지 버튼 사이즈 |
| basket_button_size 하위 요소 보기     pcpc mobilemobile |
| use_dark_mode | 쇼핑몰 다크모드 적용여부   T : 활성화 F : 비활성화 |
| button_authorization_key | 입점시 부여 받는 판매점의 버튼 인증 |
| thirdparty_agree | 제3자 제공 동의 여부   T : 동의함 F : 동의안함 |
| thirdparty_agree_date날짜 | 제3자 제공 동의 날짜 |

```bash
Update settings for KakaoPay orders        Update settings for KakaoPay orders       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaopay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}'    Response  Copy     {    "kakaopay": {        "shop_no": 1,        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/kakaopay/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}'
```

```json
{    "kakaopay": {        "shop_no": 1,        "shop_key": "S12345",        "pixel_code": "653867785974233605",        "use_kakaopay": "T",        "product_detail_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "basket_button_size": {            "pc": "210x83",            "mobile": "290x95"        },        "use_dark_mode": "T",        "button_authorization_key": "dummy_12345",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2021-07-15T17:59:00+09:00"    }}
```
