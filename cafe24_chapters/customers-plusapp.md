# CUSTOMERS PLUSAPP


## Customers plusapp

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/plusapp
```

```json
GET /api/v2/admin/customers/{member_id}/plusapp
```

### Customers plusapp property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| os_type | OS 타입 |
| install_date | 설치일 |
| auto_login_flag | 자동로그인 설정 여부 |
| use_push_flag | 알림 수신 여부 |

### Retrieve app installation information   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |

```bash
Retrieve app installation information        Retrieve app installation information       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
