# PRODUCTS VARIANTS INVENTORIES


## Products variants inventories

```json
Endpoints    GET /api/v2/admin/products/{product_no}/variants/{variant_code}/inventories
PUT /api/v2/admin/products/{product_no}/variants/{variant_code}/inventories
```

```json
GET /api/v2/admin/products/{product_no}/variants/{variant_code}/inventories
PUT /api/v2/admin/products/{product_no}/variants/{variant_code}/inventories
```

### Products variants inventories property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| variant_code형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 품목코드 시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않는다. |
| use_inventory | 재고 사용여부 해당 품목에서 재고 관리를 사용할 것인지 여부. 해당 품목에 재고 관리를 사용할 경우 재고 수량을 입력할 수 있다. 재고 관리를 사용하지 않을 경우 해당 상품은 재고와 관계 없이 판매할 수 있으며, 재고 수량, 재고수량 체크 기준, 품절 표시 여부를 사용할 수 없다. T : 사용함 F : 사용안함 |
| important_inventory | 중요재고 여부 해당 재고를 중요하게 관리하는지 여부. 쇼핑몰에서는 검색을 하기위한 구분 데이터로 사용한다. A : 일반재고 B : 중요재고 |
| inventory_control_type | 재고 수량체크 기준 재고 수량을 어느 시점에 차감할 것인지 여부. 무통장 입금처럼 결제 시점과 주문 시점이 다른 경우 재고를 차감하는 기준을 다르게 설정할 수 있다.  주문 기준 : 주문한 시점에 재고 차감. 무통장 입금의 경우 입금 완료가 되지 않아도 재고를 차감한다. 결제 기준 : 결제한 시점에 재고 차감. 무통장 입금의 경우 입금 완료가 된 다음 재고를 차감한다. A : 주문기준 B : 결제기준 |
| display_soldout | 품절표시여부 재고가 다 판매되었을 경우 해당 품목을 품절로 표시할 것인지 여부. 품절로 표시되면 주문을 할 수 없다. 모든 품목이 품절이 될 경우 해당 상품에 품절 아이콘이 표시된다. "표시안함" 선택시 재고가 다 판매되어도 주문이 가능하며 재고가 마이너스(-)로 표기된다. T : 품절표시 사용 F : 품절표시 사용안함 |
| quantity | 수량 해당 품목에 판매가 가능한 재고 수량. 재고 수량은 주문 또는 결제시 차감되며, 품절 표시를 위하여 체크된다. |
| safety_inventory | 안전재고수량 |
| origin_code | 출고지 코드 |

### Retrieve inventory details of a product variant   cafe24 youtube

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
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 품목코드   판매 수량을 검색할 품목 코드 |

```bash
Retrieve inventory details of a product variant        Retrieve inventory details of a product variant Retrieve inventories with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product variant inventory   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호.   DEFAULT 1 |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| variant_codeRequired형식 : [A-Z0-9]글자수 최소: [12자]~최대: [12자] | 품목코드   시스템이 품목에 부여한 코드. 해당 쇼핑몰 내에서 품목 코드는 중복되지 않는다. |
| use_inventory | 재고 사용여부   해당 품목에서 재고 관리를 사용할 것인지 여부. 해당 품목에 재고 관리를 사용할 경우 재고 수량을 입력할 수 있다. 재고 관리를 사용하지 않을 경우 해당 상품은 재고와 관계 없이 판매할 수 있으며, 재고 수량, 재고수량 체크 기준, 품절 표시 여부를 사용할 수 없다.   T : 사용함 F : 사용안함 |
| important_inventory | 중요재고 여부   해당 재고를 중요하게 관리하는지 여부. 쇼핑몰에서는 검색을 하기위한 구분 데이터로 사용한다.   A : 일반재고 B : 중요재고 |
| inventory_control_type | 재고 수량체크 기준   재고 수량을 어느 시점에 차감할 것인지 여부. 무통장 입금처럼 결제 시점과 주문 시점이 다른 경우 재고를 차감하는 기준을 다르게 설정할 수 있다.  주문 기준 : 주문한 시점에 재고 차감. 무통장 입금의 경우 입금 완료가 되지 않아도 재고를 차감한다. 결제 기준 : 결제한 시점에 재고 차감. 무통장 입금의 경우 입금 완료가 된 다음 재고를 차감한다.   A : 주문기준 B : 결제기준 |
| display_soldout | 품절표시여부   재고가 다 판매되었을 경우 해당 품목을 품절로 표시할 것인지 여부. 품절로 표시되면 주문을 할 수 없다. 모든 품목이 품절이 될 경우 해당 상품에 품절 아이콘이 표시된다. "표시안함" 선택시 재고가 다 판매되어도 주문이 가능하며 재고가 마이너스(-)로 표기된다.   T : 품절표시 사용 F : 품절표시 사용안함 |
| quantity | 수량   해당 품목에 판매가 가능한 재고 수량. 재고 수량은 주문 또는 결제시 차감되며, 품절 표시를 위하여 체크된다. |
| safety_inventory | 안전재고수량 |
| origin_code | 출고지 코드 |

```bash
Update a product variant inventory        Update a product variant inventory Update inventoies of the variant to sold out       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
