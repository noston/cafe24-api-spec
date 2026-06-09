# CUSTOMERGROUPS CUSTOMERS


## Customergroups customers

```json
Endpoints    POST /api/v2/admin/customergroups/{group_no}/customers
```

```json
POST /api/v2/admin/customergroups/{group_no}/customers
```

### Customergroups customers property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| group_no | 회원등급번호 |
| member_id | 회원아이디 |
| fixed_group | 회원등급 고정 여부 특정 회원이 회원자동등급변경에 적용되지 않기 위한 등급 고정 여부. 회원자동등급변경 기능을 사용하는 몰에서만 사용 가능하다. T : 고정함 F : 고정안함 |

### Update a customer's customer tier   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 회원 쓰기권한 (mall.write_customer) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 200 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| group_noRequired | 회원등급번호 |
| member_idRequired최대글자수 : [20자] | 회원아이디 |
| fixed_group | 회원등급 고정 여부   특정 회원이 회원자동등급변경에 적용되지 않기 위한 등급 고정 여부 회원자동등급변경 기능을 사용하는 몰에서만 사용 가능하다.   T : 고정함 F : 고정안함   DEFAULT F |

```bash
Update a customer's customer tier        Update a customer's customer tier Add a customer to a certain customer group Try adding a customer to a certain customer group without using member_id       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
