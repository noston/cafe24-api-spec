# PRODUCTS SEO


## Products seo

```json
Endpoints    GET /api/v2/admin/products/{product_no}/seo
PUT /api/v2/admin/products/{product_no}/seo
```

```json
GET /api/v2/admin/products/{product_no}/seo
PUT /api/v2/admin/products/{product_no}/seo
```

### Products seo property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| meta_title | 브라우저 타이틀 해당 상품의 상품 상세 페이지의 Title 태그에 표시되는 정보. Title 태그는 브라우저에 표시되는 정보로 검색엔진에서 검색시 가장 기본적인 정보이다. |
| meta_author | 메타태그1 : Author 해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. author 메타 태그에는 해당 상품을 제조한 사람 또는 등록한 사람을 기입한다. |
| meta_description | 메타태그2 : Description 해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. description 태그에 검색 결과 페이지에서 검색 결과 아래에 표시될 간략한 정보를 입력할 수 있다. |
| meta_keywords | 메타태그3 : Keywords 해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. keyword 태그에 해당 상품이 검색되었으면 하는 검색 키워드를 입력할 수 있다. |
| meta_alt | 상품 이미지 Alt 텍스트 상품 이미지에 표시되는 Alt 텍스트 정보. Alt 텍스트를 입력해놓으면 검색엔진에서 이미지 검색시 검색될 가능성이 높아지며, 브라우저에서 이미지 대신 해당 텍스트를 출력할 수 있어 웹 접근성에도 유리하다. |
| search_engine_exposure | 검색 엔진 노출 설정 해당 상품을 검색엔진에 노출할 것인지 설정. '노출안함'으로 설정할 경우 해당 상품이 검색엔진에 노출되지 않는다. T : 사용함 F : 사용안함 |

### Retrieve a product's SEO settings   cafe24 youtube

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

```bash
Retrieve a product's SEO settings        Retrieve a product's SEO settings       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update product SEO settings   cafe24 youtube

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
| product_noRequired | 상품번호   시스템에서 부여한 상품의 번호. 상품 번호는 쇼핑몰 내에서 중복되지 않는다. |
| meta_title | 브라우저 타이틀   해당 상품의 상품 상세 페이지의 Title 태그에 표시되는 정보. Title 태그는 브라우저에 표시되는 정보로 검색엔진에서 검색시 가장 기본적인 정보이다. |
| meta_author | 메타태그1 : Author   해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. author 메타 태그에는 해당 상품을 제조한 사람 또는 등록한 사람을 기입한다. |
| meta_description | 메타태그2 : Description   해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. description 태그에 검색 결과 페이지에서 검색 결과 아래에 표시될 간략한 정보를 입력할 수 있다. |
| meta_keywords | 메타태그3 : Keywords   해당 상품의 상품 상세 페이지의  태그에 표시되는 정보. keyword 태그에 해당 상품이 검색되었으면 하는 검색 키워드를 입력할 수 있다. |
| meta_alt | 상품 이미지 Alt 텍스트   상품 이미지에 표시되는 Alt 텍스트 정보. Alt 텍스트를 입력해놓으면 검색엔진에서 이미지 검색시 검색될 가능성이 높아지며, 브라우저에서 이미지 대신 해당 텍스트를 출력할 수 있어 웹 접근성에도 유리하다. |
| search_engine_exposure | 검색 엔진 노출 설정   해당 상품을 검색엔진에 노출할 것인지 설정. '노출안함'으로 설정할 경우 해당 상품이 검색엔진에 노출되지 않는다. |

```bash
Update product SEO settings        Update product SEO settings Update the product's search engine exposure to hidden       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
