# ORDERS INFLOWGROUPS INFLOWS


## Orders inflowgroups inflows

```json
Endpoints    GET /api/v2/admin/orders/inflowgroups/{group_id}/inflows
POST /api/v2/admin/orders/inflowgroups/{group_id}/inflows
PUT /api/v2/admin/orders/inflowgroups/{group_id}/inflows/{inflow_id}
DELETE /api/v2/admin/orders/inflowgroups/{group_id}/inflows/{inflow_id}
```

```json
GET /api/v2/admin/orders/inflowgroups/{group_id}/inflows
POST /api/v2/admin/orders/inflowgroups/{group_id}/inflows
PUT /api/v2/admin/orders/inflowgroups/{group_id}/inflows/{inflow_id}
DELETE /api/v2/admin/orders/inflowgroups/{group_id}/inflows/{inflow_id}
```

### Orders inflowgroups inflows property list

| Attribute | Description |
| --- | --- |
| inflow_id | 유입경로 그룹 멤버 아이디 |
| inflow_name | 유입경로 그룹 멤버 이름 |
| inflow_icon | 유입경로 아이콘 |
| group_id | 유입경로 그룹 아이디 |

### Retrieve a list of group traffic sources   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| group_idRequired최대글자수 : [40자] | 유입경로 그룹 아이디 |

```bash
Retrieve a list of group traffic sources        Retrieve a list of group traffic sources Retrieve inflows with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create a group traffic source   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| group_idRequired최대글자수 : [40자] | 유입경로 그룹 아이디 |
| inflow_idRequired최대글자수 : [40자] | 유입경로 그룹 멤버 아이디 |
| inflow_nameRequired최대글자수 : [100자] | 유입경로 그룹 멤버 이름 |
| inflow_iconRequiredURL최대글자수 : [500자] | 유입경로 아이콘 |

```bash
Create a group traffic source        Create a group traffic source Create an inflow to a certain inflow group by using only required fields Try creating an inflow to a certain inflow group by wihtout inflow_id field       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a group traffic source   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| group_idRequired최대글자수 : [40자] | 유입경로 그룹 아이디 |
| inflow_idRequired최대글자수 : [40자] | 유입경로 그룹 멤버 아이디 |
| inflow_nameRequired최대글자수 : [100자] | 유입경로 그룹 멤버 이름 |
| inflow_iconRequiredURL최대글자수 : [500자] | 유입경로 아이콘 |

```bash
Update a group traffic source        Update a group traffic source       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a group traffic source   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| group_idRequired최대글자수 : [40자] | 유입경로 그룹 아이디 |
| inflow_idRequired최대글자수 : [40자] | 유입경로 그룹 멤버 아이디 |

```bash
Delete a group traffic source        Delete a group traffic source       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
