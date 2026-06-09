# BOARDS SETTING


## Boards setting

```json
Endpoints    GET /api/v2/admin/boards/setting
PUT /api/v2/admin/boards/setting
```

```json
GET /api/v2/admin/boards/setting
PUT /api/v2/admin/boards/setting
```

### Boards setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| admin_name | 게시판 관리자명 |
| password_rules | 게시판 비밀번호 작성 규칙 설정 여부 |
| linked_board | 게시판 연동 |
| review_button_mode | 구매 후기 작성 버튼 노출 시점 |
| spam_auto_prevention | 스팸 자동 생성 방지 설정 |

### Retrieve board settings   cafe24

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
Retrieve board settings        Retrieve board settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/boards/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "board": {        "shop_no": 1,        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/boards/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "board": {        "shop_no": 1,        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}
```

### Update board settings   cafe24

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
| admin_name | 게시판 관리자명   운영자명 : name 운영자 닉네임 : nickname 쇼핑몰명 : shopname 상호명 : storename |
| password_rules | 게시판 비밀번호 작성 규칙 설정 여부   T : 사용함 F : 사용안함 |
| linked_board | 게시판 연동   사용안함 : F 게시판 번호 : 1 |
| review_button_mode | 구매 후기 작성 버튼 노출 시점   주문상태와 상관없음 : all 배송중 상태 : shipbegin_date 배송완료 후 : shipend_date |
| spam_auto_prevention | 스팸 자동 생성 방지 설정 |
| spam_auto_prevention 하위 요소 보기     type스팸 자동 생성 방지 설정 방식S : 보안문자 입력 방식 R : 구글 리캡챠 방식 site_keyRequired구글 리캡챠 사이트 키 secret_keyRequired구글 리캡챠 비밀 키 |

```bash
Update board settings        Update board settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/boards/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}'    Response  Copy     {    "board": {        "shop_no": 1,        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/boards/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}'
```

```json
{    "board": {        "shop_no": 1,        "admin_name": "name",        "password_rules": "T",        "linked_board": "F",        "review_button_mode": "all",        "spam_auto_prevention": {            "type": "R",            "site_key": "SAMPLE_RECAPTCHA_SITE_KEY",            "secret_key": "SAMPLE_RECAPTCHA_SECRET_KEY"        }    }}
```
