# PAYMENT SETTING


## Payment setting

```json
Endpoints    GET /api/v2/admin/payment/setting
PUT /api/v2/admin/payment/setting
```

```json
GET /api/v2/admin/payment/setting
PUT /api/v2/admin/payment/setting
```

### Payment setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_escrow | 에스크로 사용여부 |
| use_escrow_account_transfer | 에스크로(계좌이체) 사용여부 |
| use_escrow_virtual_account | 에스크로(가상계좌) 사용여부 |
| pg_shipping_registration | PG사 배송등록 |
| purchase_protection_amount | 매매보호 적용 결제금액 설정 |
| use_direct_pay | 빠른 결제 수단 사용여부 |
| payment_display_type | 결제수단 표기 방식 T : 텍스트 L : 로고 아이콘 |

### Retrieve payment settings   cafe24 youtube

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
Retrieve payment settings        Retrieve payment settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "setting": {        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "F",        "pg_shipping_registration": "A",        "purchase_protection_amount": 0,        "use_direct_pay": "T",        "payment_display_type": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "setting": {        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "F",        "pg_shipping_registration": "A",        "purchase_protection_amount": 0,        "use_direct_pay": "T",        "payment_display_type": "T"    }}
```

### Update payment settings   cafe24 youtube

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
| use_escrow | 에스크로 사용여부   T : 사용함 F : 사용안함 |
| use_escrow_account_transfer | 에스크로(계좌이체) 사용여부   T : 사용함 F : 사용안함 |
| use_escrow_virtual_account | 에스크로(가상계좌) 사용여부   T : 사용함 F : 사용안함 |
| pg_shipping_registration | PG사 배송등록   A : 자동 등록(매일 오후 8시 수집) M : 수동 등록 |
| use_direct_pay | 빠른 결제 수단 사용여부   T : 사용함 F : 사용안함 |
| payment_display_type | 결제수단 표기 방식   T : 텍스트 L : 로고 아이콘 |

```bash
Update payment settings        Update payment settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "T",        "pg_shipping_registration": "A",        "use_direct_pay": "T",        "payment_display_type": "T"    }}'    Response  Copy     {    "setting": {        "shop_no": 1,        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "T",        "pg_shipping_registration": "A",        "use_direct_pay": "T",        "payment_display_type": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/payment/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "T",        "pg_shipping_registration": "A",        "use_direct_pay": "T",        "payment_display_type": "T"    }}'
```

```json
{    "setting": {        "shop_no": 1,        "use_escrow": "T",        "use_escrow_account_transfer": "T",        "use_escrow_virtual_account": "T",        "pg_shipping_registration": "A",        "use_direct_pay": "T",        "payment_display_type": "T"    }}
```
