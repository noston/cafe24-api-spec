# PRODUCTS VARIANTS


## Products variants

```json
Endpoints    GET /api/v2/admin/products/{product_no}/variants
GET /api/v2/admin/products/{product_no}/variants/{variant_code}
PUT /api/v2/admin/products/{product_no}/variants/{variant_code}
PUT /api/v2/admin/products/{product_no}/variants
DELETE /api/v2/admin/products/{product_no}/variants/{variant_code}
```

```json
GET /api/v2/admin/products/{product_no}/variants
GET /api/v2/admin/products/{product_no}/variants/{variant_code}
PUT /api/v2/admin/products/{product_no}/variants/{variant_code}
PUT /api/v2/admin/products/{product_no}/variants
DELETE /api/v2/admin/products/{product_no}/variants/{variant_code}
```

### Products variants property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 상품 품목 코드 시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않음. |
| options | 옵션 |
| custom_variant_code최대글자수 : [40자] | 자체 품목 코드 사용자가 품목에 부여 가능한 코드. 재고 관리 등의 이유로 자체적으로 상품을 관리하고 있는 경우 사용함. |
| display | 진열상태 해당 품목을 진열할지 여부. 품목을 진열할 경우 상품 상세 또는 상품 목록에서 해당 품목을 선택할 수 있다. 품목이 진열되어있지 않을 경우 해당 품목이 표시되지 않으며 해당 품목을 구매할 수 없다. T : 판매함 F : 판매안함 |
| selling | 판매상태 해당 품목을 판매할지 여부. 진열은 되어있으나 판매는 하지 않을 경우 해당 품목은 "품절"로 표시되며 해당 품목을 구매할 수 없다. 품목이 "판매함" 상태여도 "진열안함"으로 되어있다면 해당 품목을 구매할 수 없다. T : 진열함 F : 진열안함 |
| display_order최소: [1]~최대: [300] | 진열 순서 |
| additional_amount | 추가금액 해당 품목을 구매할 경우, 상품의 판매가에 더하여 지불해야하는 추가 가격. |
| use_inventory | 재고 사용여부 T : 사용함 F : 사용안함 |
| important_inventory | 중요재고 여부 A : 일반재고 B : 중요재고 |
| inventory_control_type | 재고 수량체크 기준 A : 주문기준 B : 결제기준 |
| display_soldout | 품절표시여부 T : 품절표시 사용 F : 품절표시 사용안함 |
| quantity | 수량 |
| safety_inventory | 안전재고수량 |
| image | 품목 이미지 |
| inventories | 재고 리소스 품목의 재고 리소스 |
| duplicated_custom_variant_code | 자체품목코드 중복여부 T : 중복됨 F : 중복안됨 |
| product_no | 상품번호 상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |

### Retrieve a list of product variants   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| inventoriesembed | 재고 리소스   품목의 재고 리소스조회시 Embed 파라메터를 사용하여 조회할 수 있다.   ,(콤마)로 여러 건을 검색할 수 있다. |

```bash
Retrieve a list of product variants        Retrieve a list of product variants Retrieve variants with embed parameter Retrieve variants with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Retrieve a product variant   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 읽기권한 (mall.read_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 품목코드 |
| inventoriesembed | 재고 리소스   조회시 Embed 파라메터를 사용하여 조회할 수 있다. |

```bash
Retrieve a product variant        Retrieve a product variant Retrieve a product variant with fields parameter Retrieve a product variant with embed       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product variant   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 상품 품목 코드   시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않음. |
| custom_variant_code최대글자수 : [40자] | 자체 품목 코드   Youtube shopping 이용 시에는 미제공   사용자가 품목에 부여 가능한 코드. 재고 관리 등의 이유로 자체적으로 상품을 관리하고 있는 경우 사용함. |
| display | 진열상태   Youtube shopping 이용 시에는 미제공   해당 품목을 진열할지 여부. 품목을 진열할 경우 상품 상세 또는 상품 목록에서 해당 품목을 선택할 수 있다. 품목이 진열되어있지 않을 경우 해당 품목이 표시되지 않으며 해당 품목을 구매할 수 없다.   T : 진열함 F : 진열안함 |
| selling | 판매상태   해당 품목을 판매할지 여부. 진열은 되어있으나 판매는 하지 않을 경우 해당 품목은 "품절"로 표시되며 해당 품목을 구매할 수 없다. 품목이 "판매함" 상태여도 "진열안함"으로 되어있다면 해당 품목을 구매할 수 없다.   T : 판매함 F : 판매안함 |
| display_order최소: [1]~최대: [300] | 진열 순서   조합형 옵션 품목에 대해서만 사용 가능함 |
| additional_amount최소: [-2147483647]~최대: [2147483647] | 추가금액   해당 품목을 구매할 경우, 상품의 판매가에 더하여 지불해야하는 추가 가격. |
| quantity | 수량 |
| use_inventory | 재고 사용여부   T : 사용함 F : 사용안함 |
| important_inventory | 중요재고 여부   Youtube shopping 이용 시에는 미제공   A : 일반재고 B : 중요재고 |
| inventory_control_type | 재고 수량체크 기준   A : 주문기준 B : 결제기준 |
| display_soldout | 품절표시여부   T : 품절표시 사용 F : 품절표시 사용안함 |
| safety_inventory | 안전재고수량   Youtube shopping 이용 시에는 미제공 |

```bash
Update a product variant        Update a product variant Update a variant of the product to public Update a variant of the product to sold out       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update multiple product variants   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 100 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 상품 품목 코드 |
| custom_variant_code최대글자수 : [40자] | 자체 품목 코드 |
| display | 진열상태   T : 진열함 F : 진열안함 |
| selling | 판매상태   T : 판매함 F : 판매안함 |
| display_order최소: [1]~최대: [300] | 진열 순서   조합형 옵션 품목에 대해서만 사용 가능함 |
| additional_amount최소: [-2147483647]~최대: [2147483647] | 추가금액 |
| quantity | 수량 |
| use_inventory | 재고 사용여부   T : 사용함 F : 사용안함 |
| important_inventory | 중요재고 여부   A : 일반재고 B : 중요재고 |
| inventory_control_type | 재고 수량체크 기준   A : 주문기준 B : 결제기준 |
| display_soldout | 품절표시여부   T : 품절표시 사용 F : 품절표시 사용안함 |
| safety_inventory | 안전재고수량 |

```bash
Update multiple product variants        Update multiple product variants Update multiple variants of the product to public Update multiple variants of the product to sold out       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product variant   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 상품 품목 코드   시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않음. |

```bash
Delete a product variant        Delete a product variant       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
