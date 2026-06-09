# SOCIALS KAKAOSYNC


## Socials kakaosync

```json
Endpoints    GET /api/v2/admin/socials/kakaosync
PUT /api/v2/admin/socials/kakaosync
```

```json
GET /api/v2/admin/socials/kakaosync
PUT /api/v2/admin/socials/kakaosync
```

### Socials kakaosync property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_kakaosync | 카카오싱크 사용여부 T : 사용함 F : 사용안함 |
| rest_api_key | REST API 키 |
| javascript_key | JavaScript 키 |
| auto_login | 자동 로그인 사용 카카오 웹브라우저로 쇼핑몰 이용시 카카오 아이디로 로그인 기능 사용 여부 T : 사용함 F : 사용안함 |
| thirdparty_agree | 제3자 제공 동의 여부 T : 동의함 F : 동의안함 |
| thirdparty_agree_date | 제3자 제공 동의 날짜 |
| use_signup_result_page | 쇼핑몰 가입 후 이동 페이지 T : 가입 완료 페이지로 이동 F : 가입 완료 페이지 없이 즉시 가입 |

### Kakao Sync details   cafe24

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
Kakao Sync details        Kakao Sync details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/kakaosync' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "kakaosync": {        "shop_no": 1,        "use_kakaosync": "T",        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2020-11-05T17:59:00+09:00",        "use_signup_result_page": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/kakaosync' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "kakaosync": {        "shop_no": 1,        "use_kakaosync": "T",        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "thirdparty_agree": "T",        "thirdparty_agree_date": "2020-11-05T17:59:00+09:00",        "use_signup_result_page": "T"    }}
```

### Kakao Sync updates   cafe24

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
| rest_api_keyRequired형식 : [a-zA-Z0-9]최대글자수 : [255자] | REST API 키 |
| javascript_keyRequired형식 : [a-zA-Z0-9]최대글자수 : [255자] | JavaScript 키 |
| auto_login | 자동 로그인 사용   카카오 웹브라우저로 쇼핑몰 이용시 카카오 아이디로 로그인 기능 사용 여부   T : 사용함 F : 사용안함   DEFAULT F |
| use_signup_result_page | 쇼핑몰 가입 후 이동 페이지   T : 가입 완료 페이지로 이동 F : 가입 완료 페이지 없이 즉시 가입   DEFAULT F |

```bash
Kakao Sync updates        Kakao Sync updates       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/kakaosync' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "use_signup_result_page": "T"    }}'    Response  Copy     {    "kakaosync": {        "shop_no": 1,        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "use_signup_result_page": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/kakaosync' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "use_signup_result_page": "T"    }}'
```

```json
{    "kakaosync": {        "shop_no": 1,        "rest_api_key": "4acf565d122354e36b942c5a51dc129e",        "javascript_key": "a201bef3340f797aac6b83de0b5c27a1",        "auto_login": "T",        "use_signup_result_page": "T"    }}
```
