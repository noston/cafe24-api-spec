# ORDERS ITEMS OPTIONS


## Orders items options

```json
Endpoints    POST /api/v2/admin/orders/{order_id}/items/{order_item_code}/options
PUT /api/v2/admin/orders/{order_id}/items/{order_item_code}/options
```

```json
POST /api/v2/admin/orders/{order_id}/items/{order_item_code}/options
PUT /api/v2/admin/orders/{order_id}/items/{order_item_code}/options
```

### Orders items options property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| order_id | 주문번호 |
| order_item_code | 품주코드 |
| product_bundle | 세트상품 여부 |
| additional_options | 추가입력 옵션 |
| bundle_additional_options | 세트상품 추가입력 옵션 |

### Create order item options   cafe24

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
| product_bundleRequired | 세트상품 여부 |
| additional_options | 추가입력 옵션 |
| additional_options 하위 요소 보기     additional_option_nameRequired추가입력옵션명 additional_option_valueRequired추가입력 옵션 값 |
| bundle_additional_options | 세트상품 추가입력 옵션 |
| bundle_additional_options 하위 요소 보기     variant_codeRequired품목코드 additional_options Array    additional_options 하위 요소 보기     additional_option_name추가입력옵션명Required additional_option_value추가입력 옵션 값Required |

```bash
Create order item options        Create order item options       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Edit order item options   cafe24

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
| additional_options | 추가입력 옵션 |
| additional_options 하위 요소 보기     additional_option_nameRequired추가입력옵션명 additional_option_valueRequired추가입력 옵션 값 |

```bash
Edit order item options        Edit order item options       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
