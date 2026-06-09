# CUSTOMERS AUTOUPDATE


## Customers autoupdate

```json
Endpoints    GET /api/v2/admin/customers/{member_id}/autoupdate
```

```json
GET /api/v2/admin/customers/{member_id}/autoupdate
```

### Customers autoupdate property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| member_id | 회원아이디 |
| next_grade | 다음 예상 등급 |
| total_purchase_amount | 등급 산정 기간 내 누적 사용 금액 |
| total_purchase_count | 등급 산정 기간 내 누적 사용 건수 |
| required_purchase_amount | 다음 등급까지 필요 금액 |
| required_purchase_count | 다음 등급까지 필요 건수 |

### Retrieve customer tier auto-update details   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 읽기권한 (mall.read_customer) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |

```bash
Retrieve customer tier auto-update details        Retrieve customer tier auto-update details       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
