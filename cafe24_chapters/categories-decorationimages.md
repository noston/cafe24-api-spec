# CATEGORIES DECORATIONIMAGES


## Categories decorationimages

```json
Endpoints    GET /api/v2/admin/categories/{category_no}/decorationimages
PUT /api/v2/admin/categories/{category_no}/decorationimages
```

```json
GET /api/v2/admin/categories/{category_no}/decorationimages
PUT /api/v2/admin/categories/{category_no}/decorationimages
```

### Categories decorationimages property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| category_no | 분류 번호 |
| use_menu_image_pc | 분류 PC 메뉴 이미지 사용여부 T : 사용함 F : 사용안함 |
| menu_image_pc | 분류 PC 메뉴 기본 이미지 |
| menu_over_image_pc | 분류 PC 메뉴 오버 이미지 |
| use_top_image_pc | 분류 PC 상단 이미지 사용여부 T : 사용함 F : 사용안함 |
| top_images_pc | 분류 PC 상단 이미지 |
| use_title_image_pc | 분류 PC 타이틀 이미지 사용여부 T : 사용함 F : 사용안함 |
| title_image_pc | 분류 PC 타이틀 이미지 |
| use_menu_image_mobile | 분류 모바일 메뉴 이미지 사용여부 T : 사용함 F : 사용안함 |
| menu_image_mobile | 분류 모바일 메뉴 기본 이미지 |
| use_top_image_mobile | 분류 모바일 상단 이미지 사용여부 T : 사용함 F : 사용안함 |
| top_images_mobile배열 최대사이즈: [3] | 분류 모바일 상단 이미지 |
| use_title_image_mobile | 분류 모바일 타이틀 이미지 사용여부 T : 사용함 F : 사용안함 |
| title_image_mobile | 분류 모바일 타이틀 이미지 |

### Retrieve decoration image settings by category   cafe24

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
Retrieve decoration image settings by category        Retrieve decoration image settings by category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update decoration images of a product category   cafe24

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
| category_noRequired | 분류 번호 |
| use_menu_image_pc | 분류 PC 메뉴 이미지 사용여부   T : 사용함 F : 사용안함 |
| menu_image_pc | 분류 PC 메뉴 기본 이미지 |
| menu_over_image_pc | 분류 PC 메뉴 오버 이미지 |
| use_top_image_pc | 분류 PC 상단 이미지 사용여부   T : 사용함 F : 사용안함 |
| top_images_pc배열 최대사이즈: [3] | 분류 PC 상단 이미지 |
| use_title_image_pc | 분류 PC 타이틀 이미지 사용여부   T : 사용함 F : 사용안함 |
| title_image_pc | 분류 PC 타이틀 이미지 |
| use_menu_image_mobile | 분류 모바일 메뉴 이미지 사용여부   T : 사용함 F : 사용안함 |
| menu_image_mobile | 분류 모바일 메뉴 기본 이미지 |
| use_top_image_mobile | 분류 모바일 상단 이미지 사용여부   T : 사용함 F : 사용안함 |
| top_images_mobile배열 최대사이즈: [3] | 분류 모바일 상단 이미지 |
| use_title_image_mobile | 분류 모바일 타이틀 이미지 사용여부   T : 사용함 F : 사용안함 |
| title_image_mobile | 분류 모바일 타이틀 이미지 |

```bash
Update decoration images of a product category        Update decoration images of a product category Disable all PC decoration images of the category Update the PC and mobile decoration image of the category       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
