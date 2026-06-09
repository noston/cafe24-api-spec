# CARTS SETTING


## Carts setting

```json
Endpoints    GET /api/v2/admin/carts/setting
PUT /api/v2/admin/carts/setting
```

```json
GET /api/v2/admin/carts/setting
PUT /api/v2/admin/carts/setting
```

### Carts setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| wishlist_display | 장바구니 관심상품 노출 여부 |
| add_action_type | 장바구니 담기 이후 액션 타입 |
| cart_item_direct_purchase | 담긴 상품 확인 및 구매 가능여부 |
| storage_period | 장바구니 저장 기간 설정 여부 |
| period | 설정할 저장기간 장바구니 저장기간은 1,2,3,4,5,6,7,8,9,10,14,30일 중 설정 가능 |
| icon_display | 장바구니 담기 아이콘 표시 여부 |
| cart_item_option_change | 장바구니에서 상품 옵션 변경가능 하도록 제공 여부 |
| discount_display | 장바구니에 할인 금액 표시 |

### Retrieve carts settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |

```bash
Retrieve carts settings        Retrieve carts settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/carts/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "cart": {        "shop_no": 1,        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/carts/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "cart": {        "shop_no": 1,        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}
```

### Update carts settings   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상점 읽기권한 (mall.read_store) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| wishlist_display | 장바구니 관심상품 노출 여부   T: 사용함 F: 사용안함 |
| add_action_type | 장바구니 담기 이후 액션 타입   M: 장바구니 페이지 바로 이동 S: 장바구니 페이지 이동 유무 선택 |
| cart_item_direct_purchase | 담긴 상품 확인 및 구매 가능여부   T: 사용함 F: 사용안함 |
| storage_period | 장바구니 저장 기간 설정 여부   T: 설정함 F: 설정안함 |
| period | 설정할 저장기간   장바구니 저장기간은 1,2,3,4,5,6,7,8,9,10,14,30일 중 설정 가능 |
| icon_display | 장바구니 담기 아이콘 표시 여부   T: 사용함 F: 사용안함 |
| cart_item_option_change | 장바구니에서 상품 옵션 변경가능 하도록 제공 여부   T: 사용함 F: 사용안함 |
| discount_display | 장바구니에 할인 금액 표시   T: 사용함 F: 사용안함 |

```bash
Update carts settings        Update carts settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/carts/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}'    Response  Copy     {    "cart": {        "shop_no": 1,        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}
```

```bash
curl -X PUT \  'https://{mallid}.cafe24api.com/api/v2/admin/carts/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}' \  -d '{    "shop_no": 1,    "request": {        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}'
```

```json
{    "cart": {        "shop_no": 1,        "wishlist_display": "T",        "add_action_type": "M",        "cart_item_direct_purchase": "T",        "storage_period": "T",        "period": "7",        "icon_display": "T",        "cart_item_option_change": "T",        "discount_display": "T"    }}
```
