# CATEGORIES SEO


## Categories seo

```json
Endpoints    GET /api/v2/admin/categories/{category_no}/seo
PUT /api/v2/admin/categories/{category_no}/seo
```

```json
GET /api/v2/admin/categories/{category_no}/seo
PUT /api/v2/admin/categories/{category_no}/seo
```

### Categories seo property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| category_no | 분류 번호 |
| search_engine_exposure | 검색 엔진 노출 설정 T : 사용함 F : 사용안함 |
| meta_title | 브라우저 타이틀 |
| meta_author | 메타태그1 : Author |
| meta_description | 메타태그2 : Description |
| meta_keywords | 메타태그3 : Keywords |

### Retrieve SEO settings by category   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 읽기권한 (mall.read_category) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| category_noRequired | 분류 번호 |

```bash
Retrieve SEO settings by category        Retrieve SEO settings by category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update a product category SEO   cafe24

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품분류 쓰기권한 (mall.write_category) |
| 호출건수 제한 | 40 |
| 1회당 요청건수 제한 | 1 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| shop_no | 멀티쇼핑몰 번호   DEFAULT 1 |
| category_noRequired | 분류 번호 |
| search_engine_exposure | 검색 엔진 노출 설정   T : 사용함 F : 사용안함 |
| meta_title | 브라우저 타이틀 |
| meta_author | 메타태그1 : Author |
| meta_description | 메타태그2 : Description |
| meta_keywords | 메타태그3 : Keywords |

```bash
Update a product category SEO        Update a product category SEO Update the categories's search engine exposure to hidden Update the categorie's title and meta tags       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
