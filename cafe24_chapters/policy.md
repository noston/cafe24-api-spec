# POLICY


## Policy

```json
Endpoints    GET /api/v2/admin/policy
PUT /api/v2/admin/policy
```

```json
GET /api/v2/admin/policy
PUT /api/v2/admin/policy
```

### Policy property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| privacy_all | 개인정보처리방침 전체내용 |
| terms_using_mall | 쇼핑몰 이용약관 |
| use_privacy_join | 회원가입 개인정보처리방침 사용 여부 T: 사용함 F: 사용안함 |
| privacy_join | 회원가입 개인정보처리방침 내용 |
| use_withdrawal | 청약철회방침 사용여부 T: 사용함 F: 사용안함 |
| required_withdrawal | 청약철회방침 사용자 동의 필수 여부 T : 필수 F : 선택 |
| withdrawal | 청약철회방침 내용 |

### Retrieve a store profile   cafe24

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
Retrieve a store profile        Retrieve a store profile       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/policy' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "policy": {        "shop_no": 1,        "privacy_all": "<p>** This form is intended to assist in the operation...",        "terms_using_mall": "<p>**This form is provided by the Fair Trade Commission...",        "use_privacy_join": "T",        "privacy_join": "<p>1. Purposes of Collection and Use of Personal Information...",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": "<p>Withdrawal Policy Agreement...</p>"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/policy' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "policy": {        "shop_no": 1,        "privacy_all": "<p>** This form is intended to assist in the operation...",        "terms_using_mall": "<p>**This form is provided by the Fair Trade Commission...",        "use_privacy_join": "T",        "privacy_join": "<p>1. Purposes of Collection and Use of Personal Information...",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": "<p>Withdrawal Policy Agreement...</p>"    }}
```

### Update a store profile   cafe24

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
| save_type | 저장 방식   S: 표준 약관 적용 C: 사용자 정의 약관 적용   DEFAULT S |
| privacy_all | 개인정보처리방침 전체내용 |
| terms_using_mall | 쇼핑몰 이용약관 |
| use_privacy_join | 회원가입 개인정보처리방침 사용 여부   T: 사용함 F: 사용안함 |
| privacy_join | 회원가입 개인정보처리방침 내용 |
| use_withdrawal | 청약철회방침 사용여부   T: 사용함 F: 사용안함 |
| required_withdrawal | 청약철회방침 사용자 동의 필수 여부   T : 필수 F : 선택 |
| withdrawal | 청약철회방침 내용 |

```bash
Update a store profile        Update a store profile       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/policy' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "privacy_all": "",        "terms_using_mall": "",        "use_privacy_join": "T",        "privacy_join": "",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": ""    }}'    Response  Copy     {    "policy": {        "shop_no": 1,        "privacy_all": "<p>** This form is intended to assist in the operation...",        "terms_using_mall": "<p>**This form is provided by the Fair Trade Commission...",        "use_privacy_join": "T",        "privacy_join": "<p>1. Purposes of Collection and Use of Personal Information...",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": "<p>Withdrawal Policy Agreement...</p>"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/policy' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "privacy_all": "",        "terms_using_mall": "",        "use_privacy_join": "T",        "privacy_join": "",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": ""    }}'
```

```json
{    "policy": {        "shop_no": 1,        "privacy_all": "<p>** This form is intended to assist in the operation...",        "terms_using_mall": "<p>**This form is provided by the Fair Trade Commission...",        "use_privacy_join": "T",        "privacy_join": "<p>1. Purposes of Collection and Use of Personal Information...",        "use_withdrawal": "T",        "required_withdrawal": "T",        "withdrawal": "<p>Withdrawal Policy Agreement...</p>"    }}
```
