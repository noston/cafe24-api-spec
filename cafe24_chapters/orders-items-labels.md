# ORDERS ITEMS LABELS


## Orders items labels

```json
Endpoints    GET /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
POST /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
PUT /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
DELETE /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels/{name}
```

```json
GET /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
POST /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
PUT /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels
DELETE /api/v2/admin/orders/{order_id}/items/{order_item_code}/labels/{name}
```

### Orders items labels property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 DEFAULT 1 |
| names | 주문 라벨명 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| name | 주문 라벨명 |

### Retrieve an order label   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 읽기권한 (mall.read_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| order_item_codeRequired | 품주코드 |

```bash
Retrieve an order label        Retrieve an order label       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create an order label   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| order_item_codeRequired | 품주코드 |
| namesRequired | 주문 라벨명 |

```bash
Create an order label        Create an order label       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update an order label   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| order_item_codeRequired | 품주코드 |
| namesRequired | 주문 라벨명 |

```bash
Update an order label        Update an order label       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete an order label   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 주문 쓰기권한 (mall.write_order) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| order_idRequired주문번호 | 주문번호 |
| order_item_codeRequired | 품주코드 |
| nameRequired | 주문 라벨명 |

```bash
Delete an order label        Delete an order label       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
