# PRODUCTS ADDITIONALIMAGES


## Products additionalimages

```json
Endpoints    POST /api/v2/admin/products/{product_no}/additionalimages
PUT /api/v2/admin/products/{product_no}/additionalimages
DELETE /api/v2/admin/products/{product_no}/additionalimages
```

```json
POST /api/v2/admin/products/{product_no}/additionalimages
PUT /api/v2/admin/products/{product_no}/additionalimages
DELETE /api/v2/admin/products/{product_no}/additionalimages
```

### Products additionalimages property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| additional_image | 추가이미지 |
| product_no | 상품번호 |

### Create an additional product image   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| additional_imageRequired | 추가이미지   ● 최대요청건수 : 20개 ● 이미지 파일 용량 제한 : 5MB ● 한 호출당 이미지 전체 용량 제한 : 30MB |

```bash
Create an additional product image        Create an additional product image Try uploading over 20 additional images to a product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update an additional product image   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |
| additional_imageRequired | 추가이미지   ● 최대요청건수 : 20개 ● 이미지 파일 용량 제한 : 5MB ● 한 호출당 이미지 전체 용량 제한 : 30MB |

```bash
Update an additional product image        Update an additional product image Try updating over 20 additional images to a product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete an additional product image   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no최소값: [1] | 멀티쇼핑몰 번호   DEFAULT 1 |
| product_noRequired | 상품번호 |

```bash
Delete an additional product image        Delete an additional product image       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
