# PRODUCTS SETTING


## Products setting

```json
Endpoints    GET /api/v2/admin/products/setting
```

```json
GET /api/v2/admin/products/setting
```

### Products setting property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 |
| display_price_scope | 회원/비회원 가격표시 A : 모두 표시함 (회원+비회원) C : 회원만 표시함 |
| calculate_price_based_on | 판매가 계산 기준 S : 공급가 대비 마진율 A : 판매가 대비 마진율 P : 기본몰 판매가 B : 상품가 |
| price_rounding_unit | 판매가 계산 절사 단위 F : 절사안함 -2 : 0.01단위 -1 : 0.1단위 0 : 1단위 1 : 10단위 2 : 100단위 3 : 1000단위 |
| price_rounding_rule | 판매가 계산 절사 방법 L : 내림 U : 반올림 C : 올림 |
| auto_translation | 자동 번역 항목 사용여부 T:사용 F:사용안함 |
| translation_items | 자동 번역 항목 product_name : 상품명 summary_description : 상품요약설명 simple_description : 상품간략설명 description : 상품상세설명 category_name : 상품 분류 option : 옵션 material : 상품소재 |
| popular_search_keywords배열 최대사이즈: [10] | 인기검색어 |
| popup_menu | 팝업 메뉴 T : 사용함 F : 사용안함 |
| display_sub_category | 분류 리스트 표시 T : 사용함 F : 사용안함 |
| display_sub_category_detail | 하위분류 표시단계 상세설정 |
| display_product_count | 상품 수 표시 T : 사용함 F : 사용안함 |
| option_preview | 옵션 미리보기 기능 T : 사용함 F : 사용안함 |
| wishlist_registration | 관심상품 등록 기능 T : 사용함 F : 사용안함 |
| additional_image_action | 추가이미지 액션 C : 마우스 클릭 O : 마우스 오버 |
| image_effect | 상품이미지 효과 설정 T : 사용함 F : 사용안함 |
| image_effect_detail | 상품이미지 효과 상세설정 |

### Retrieve product settings   cafe24

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
Retrieve product settings        Retrieve product settings       Request   cURL Java Python Node.js PHP Go  Copy     curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'    Response  Copy     {    "product": {        "shop_no": 1,        "display_price_scope": "A",        "calculate_price_based_on": "P",        "price_rounding_unit": "1",        "price_rounding_rule": "U",        "auto_translation": "T",        "translation_items": [            "product_name",            "summary_description",            "simple_description",            "description",            "category_name",            "option",            "material"        ],        "popular_search_keywords": [            "New arrivals",            "Best sellers"        ],        "popup_menu": "T",        "display_sub_category": "T",        "display_sub_category_detail": {            "type": "S",            "visible_targets_by_depth": {                "category_depth_1": "category_depth_4",                "category_depth_2": "category_depth_4",                "category_depth_3": "category_depth_4"            }        },        "display_product_count": "T",        "option_preview": "T",        "wishlist_registration": "T",        "additional_image_action": "O",        "image_effect": "T",        "image_effect_detail": {            "type": "opacity",            "opacity_value": 10,            "border_color": "#ff0000",            "border_width": 1        }    }}
```

```bash
curl -X GET \  'https://{mallid}.cafe24api.com/api/v2/admin/products/setting' \  -H 'Authorization: Bearer {access_token}' \  -H 'Content-Type: application/json' \  -H 'X-Cafe24-Api-Version: {version}'
```

```json
{    "product": {        "shop_no": 1,        "display_price_scope": "A",        "calculate_price_based_on": "P",        "price_rounding_unit": "1",        "price_rounding_rule": "U",        "auto_translation": "T",        "translation_items": [            "product_name",            "summary_description",            "simple_description",            "description",            "category_name",            "option",            "material"        ],        "popular_search_keywords": [            "New arrivals",            "Best sellers"        ],        "popup_menu": "T",        "display_sub_category": "T",        "display_sub_category_detail": {            "type": "S",            "visible_targets_by_depth": {                "category_depth_1": "category_depth_4",                "category_depth_2": "category_depth_4",                "category_depth_3": "category_depth_4"            }        },        "display_product_count": "T",        "option_preview": "T",        "wishlist_registration": "T",        "additional_image_action": "O",        "image_effect": "T",        "image_effect_detail": {            "type": "opacity",            "opacity_value": 10,            "border_color": "#ff0000",            "border_width": 1        }    }}
```
