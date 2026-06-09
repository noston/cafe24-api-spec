# STORE ACCOUNTS


## Store accounts

```json
Endpoints    GET /api/v2/admin/store/accounts
```

```json
GET /api/v2/admin/store/accounts
```

### Store accounts property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| bank_account_id | 무통장 입금 은행 ID |
| bank_name | 은행명 |
| bank_code최대글자수 : [50자] | 은행코드 bank_code |
| bank_account_no | 계좌번호 |
| bank_account_holder | 예금주 |
| use_account | 사용여부 T : 사용함 F : 사용안함 |

### Retrieve a list of store bank accounts   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve a list of store bank accounts        Retrieve a list of store bank accounts       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/accounts' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "accounts": [        {            "shop_no": 1,            "bank_account_id": 1,            "bank_name": "Hana Bank",            "bank_code": "bank_81",            "bank_account_no": "123123123",            "bank_account_holder": "Depositor Name",            "use_account": "T"        },        {            "shop_no": 1,            "bank_account_id": 2,            "bank_name": "KB Bank",            "bank_code": "bank_04",            "bank_account_no": "123456789",            "bank_account_holder": "Depositor Name",            "use_account": "T"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/store/accounts' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "accounts": [        {            "shop_no": 1,            "bank_account_id": 1,            "bank_name": "Hana Bank",            "bank_code": "bank_81",            "bank_account_no": "123123123",            "bank_account_holder": "Depositor Name",            "use_account": "T"        },        {            "shop_no": 1,            "bank_account_id": 2,            "bank_name": "KB Bank",            "bank_code": "bank_04",            "bank_account_no": "123456789",            "bank_account_holder": "Depositor Name",            "use_account": "T"        }    ]}
```
