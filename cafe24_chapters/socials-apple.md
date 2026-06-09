# SOCIALS APPLE


## Socials apple

```json
Endpoints    GET /api/v2/admin/socials/apple
PUT /api/v2/admin/socials/apple
```

```json
GET /api/v2/admin/socials/apple
PUT /api/v2/admin/socials/apple
```

### Socials apple property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| use_apple_login | 애플 로그인 사용 T : 사용함 F : 사용안함 |
| client_id | client id |
| team_id | Team ID |
| key_id | Key ID |
| auth_key_file_name | Auth Key 파일명 |
| use_certification | 애플 로그인 본인인증 T : 사용함 F : 사용안함 |

### Apple login sync details   cafe24

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
Apple login sync details        Apple login sync details       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/apple' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "apple": {        "shop_no": 1,        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "use_certification": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/apple' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "apple": {        "shop_no": 1,        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "use_certification": "T"    }}
```

### Apple login sync settings   cafe24

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
| use_apple_login | 애플 로그인 사용   T : 사용함 F : 사용안함 |
| client_id최대글자수 : [300자] | Client ID   애플 개발자 센터의 Service ID 생성 시 설정한 Identifier |
| team_id최대글자수 : [300자] | Team ID   애플 개발자 센터의 App ID Prefix |
| key_id최대글자수 : [300자] | Key ID   애플 개발자 센터의 Key ID |
| auth_key_file_name최대글자수 : [30자] | Auth Key 파일명   App ID의 Key파일로 .p8파일만 가능 |
| auth_key_file_contents최대글자수 : [300자] | Auth Key 파일 내용   .p8파일을 텍스트 파일로 열어 줄바꿈 없이 값을 작성 |
| use_certification | 애플 로그인 본인인증   T : 사용함 F : 사용안함 |

```bash
Apple login sync settings        Apple login sync settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/apple' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "auth_key_file_contents": "M1ZWc1NGWkVTVlVaT1VXRGIKoZIzj0DAQehRkhoU01VNUJzUWxvd1ZraFJNRTU0kVWpGT1RrNLQ3oUViRUprTUZaSlVXdG9jbVjE10sJMWgCgYF5VWpOVFZVcENWVlpHwYiW5cCJ1VoT01GTnJWblJhVkVwVlVrRZSbTnZORkZWYkd0UFNHUmFWR9Ua1VpGZVFZaS1NH",        "use_certification": "T"    }}'    Response  Copy     {    "apple": {        "shop_no": 1,        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "use_certification": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/socials/apple' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "auth_key_file_contents": "M1ZWc1NGWkVTVlVaT1VXRGIKoZIzj0DAQehRkhoU01VNUJzUWxvd1ZraFJNRTU0kVWpGT1RrNLQ3oUViRUprTUZaSlVXdG9jbVjE10sJMWgCgYF5VWpOVFZVcENWVlpHwYiW5cCJ1VoT01GTnJWblJhVkVwVlVrRZSbTnZORkZWYkd0UFNHUmFWR9Ua1VpGZVFZaS1NH",        "use_certification": "T"    }}'
```

```json
{    "apple": {        "shop_no": 1,        "use_apple_login": "T",        "client_id": "wpv6z7snuJiDYfSsN9ea",        "team_id": "T3VC5A6A2E",        "key_id": "N2Q4JKNZSM",        "auth_key_file_name": "AuthKey_N2Q4JKNZSM.p8",        "use_certification": "T"    }}
```
