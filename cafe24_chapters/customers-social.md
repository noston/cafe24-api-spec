# CUSTOMERS SOCIAL


## Customers social

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/social
```

```json
GET /api/v2/admin/customers/{member_id}/social
```

### Customers social property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id | 회원아이디 |
| social_name | 연동 된 SNS명 |
| social_member_code | 연동 된 SNS 제공코드 |
| linked_date | 연동 날짜 |

### Retrieve a customer's social account   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired | 회원아이디 |

```bash
Retrieve a customer's social account        Retrieve a customer's social account       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
