# CUSTOMERS INVITATION


## Customers invitation

```json
Endpoints    POST /api/v2/admin/customers/{member_id}/invitation
```

```json
POST /api/v2/admin/customers/{member_id}/invitation
```

### Customers invitation property list

| Attribute | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호 |
| member_id최대글자수 : [16자] | 회원아이디 |

### Send an invitation to activate account   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 알림 쓰기권한 (mall.write_notification) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [16자] | 회원아이디 |
| invitation_typeRequired | 계정 활성화 초대 수단 |

```bash
Send an invitation to activate account        Send an invitation to activate account       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
