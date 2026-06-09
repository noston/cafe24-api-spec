# ORDERS INFLOWGROUPS


## Orders inflowgroups

```json
Endpoints    GET /api/v2/admin/orders/inflowgroups
POST /api/v2/admin/orders/inflowgroups
PUT /api/v2/admin/orders/inflowgroups/{inflow_group_id}
DELETE /api/v2/admin/orders/inflowgroups/{inflow_group_id}
```

```json
GET /api/v2/admin/orders/inflowgroups
POST /api/v2/admin/orders/inflowgroups
PUT /api/v2/admin/orders/inflowgroups/{inflow_group_id}
DELETE /api/v2/admin/orders/inflowgroups/{inflow_group_id}
```

### Orders inflowgroups property list

| Attribute | Description |
| --- | --- |
| inflow_group_id | 유입경로 그룹 아이디 |
| inflow_group_name | 유입경로 그룹 이름 |

### Retrieve a list of traffic source groups   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

```bash
Retrieve a list of traffic source groups        Retrieve a list of traffic source groups Retrieve inflowgroups with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "inflowgroups": [        {            "inflow_group_id": "cafe24",            "inflow_group_name": "Cafe24"        },        {            "inflow_group_id": "gmarket",            "inflow_group_name": "Gmarket"        }    ]}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "inflowgroups": [        {            "inflow_group_id": "cafe24",            "inflow_group_name": "Cafe24"        },        {            "inflow_group_id": "gmarket",            "inflow_group_name": "Gmarket"        }    ]}
```

### Create a traffic source group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| inflow_group_idRequired최대글자수 : [40자]형식 : [a-zA-Z0-9] | 유입경로 그룹 아이디 |
| inflow_group_nameRequired최대글자수 : [100자] | 유입경로 그룹 이름 |

```bash
Create a traffic source group        Create a traffic source group Create an inflow group to a mall Try creating an inflow group by without inflow_group_id field       Request   cURL Java Python Node.js PHP Go  Copy     curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}'    Response  Copy     {    "inflowgroup": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}
```

```bash
curl -X POST \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}'
```

```json
{    "inflowgroup": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}
```

### Update a traffic source group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| inflow_group_idRequired형식 : [a-zA-Z0-9]최대글자수 : [40자] | 유입경로 그룹 아이디 |
| inflow_group_nameRequired최대글자수 : [100자] | 유입경로 그룹 이름 |

```bash
Update a traffic source group        Update a traffic source group       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups/cafe24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "inflow_group_name": "Cafe24"    }}'    Response  Copy     {    "inflowgroup": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups/cafe24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "request": {        "inflow_group_name": "Cafe24"    }}'
```

```json
{    "inflowgroup": {        "inflow_group_id": "cafe24",        "inflow_group_name": "Cafe24"    }}
```

### Delete a traffic source group   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| inflow_group_idRequired최대글자수 : [40자]형식 : [a-zA-Z0-9] | 유입경로 그룹 아이디 |

```bash
Delete a traffic source group        Delete a traffic source group       Request   cURL Java Python Node.js PHP Go  Copy     curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups/cafe24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "inflowgroup": {        "inflow_group_id": "cafe24"    }}
```

```bash
curl -X DELETE \  'https://{mallid}.cafe24api.com/api/v2/admin/orders/inflowgroups/cafe24' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "inflowgroup": {        "inflow_group_id": "cafe24"    }}
```
