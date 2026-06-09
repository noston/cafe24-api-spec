# PRODUCTS OPTIONS


## Products options

```json
Endpoints    GET /api/v2/admin/products/{product_no}/options
POST /api/v2/admin/products/{product_no}/options
PUT /api/v2/admin/products/{product_no}/options
DELETE /api/v2/admin/products/{product_no}/options
```

```json
GET /api/v2/admin/products/{product_no}/options
POST /api/v2/admin/products/{product_no}/options
PUT /api/v2/admin/products/{product_no}/options
DELETE /api/v2/admin/products/{product_no}/options
```

### Products options property list

| Attribute | Description |
| --- | --- |
| shop_no | 멀티쇼핑몰 번호 멀티쇼핑몰 구분을 위해 사용하는 멀티쇼핑몰 번호. |
| product_no Required | 상품번호 상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |
| has_option | 옵션 사용여부 T : 사용함 F : 사용안함 |
| option_type | 옵션 구성방식 옵션을 사용할 경우, 옵션의 유형 표시  ● 조합형 : 옵션명을 기준으로 옵션값을 조합할 수 있음 ● 상품 연동형 : 옵션표시방식은 조합형과 유사하지만 필수옵션과 선택옵션을 선택할 수 있음. 옵션의 조합을 제한 없이 생성할 수 있음. ● 독립 선택형 : 독립적인 조건 여러개를 각각 선택할 수 있는 옵션으로 옵션 값이 조합되지 않고 각각의 품목으로 생성됨. T : 조합형 E : 연동형 F : 독립형 |
| option_list_type | 옵션 표시방식 조합형 옵션을 사용할 경우, 조합형 옵션의 유형 표시  * 조합 일체선택형 : 하나의 셀렉스박스(버튼 이나 라디오버튼)에 모든 옵션이 조합되어 표시됨 * 조합 분리선택형 : 옵션을 각각의 셀렉스박스(버튼 이나 라디오버튼)로 선택할 수 있으며 옵션명을 기준으로 옵션값을 조합할 수 있음  독립형이나 상품 연동형 옵션을 사용하고 있을 경우 S(분리형)로 입력됨. C : 일체형 S : 분리형 |
| option_preset_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 옵션세트 코드 상품연동형 옵션을 사용할 경우, 옵션 세트 코드 표시 |
| options | 옵션 |
| select_one_by_option | 옵션별로 한 개씩 선택 (독립형 옵션) 독립형 옵션을 사용할 경우, 하나의 옵션을 여러개 중복하여 선택할 수 없고 한개씩만 선택 가능함. T : 사용함 F : 사용안함 |
| option_preset_name | 연동형 옵션 세트명 상품연동형 옵션을 사용할 경우, 옵션 세트의 이름 표시 |
| use_additional_option | 추가입력 옵션 사용여부 T : 사용함 F : 사용안함 |
| additional_options | 추가입력 옵션 |
| use_attached_file_option | 파일 첨부 옵션 사용여부 T : 사용함 F : 사용안함 |
| attached_file_option | 파일 첨부 옵션 |

### Retrieve a list of product options   cafe24 youtube

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

```bash
Retrieve a list of product options        Retrieve a list of product options Retrieve options with fields parameter       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Create product options   cafe24 youtube

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
| has_option | 옵션 사용여부   T : 사용함 F : 사용안함 |
| option_type | 옵션 구성방식   옵션을 사용할 경우, 옵션의 유형 입력  ● 조합형 : 옵션명을 기준으로 옵션값을 조합할 수 있음 ● 상품 연동형 : 옵션표시방식은 조합형과 유사하지만 필수옵션과 선택옵션을 선택할 수 있음. 옵션의 조합을 제한 없이 생성할 수 있음. ● 독립 선택형 : 독립적인 조건 여러개를 각각 선택할 수 있는 옵션으로 옵션 값이 조합되지 않고 각각의 품목으로 생성됨.   T : 조합형 E : 연동형 F : 독립형 |
| option_list_type | 옵션 표시방식   조합형 옵션을 사용할 경우, 조합형 옵션의 유형 입력  * 조합 일체선택형 : 하나의 셀렉스박스(버튼 이나 라디오버튼)에 모든 옵션이 조합되어 표시됨 * 조합 분리선택형 : 옵션을 각각의 셀렉스박스(버튼 이나 라디오버튼)로 선택할 수 있으며 옵션명을 기준으로 옵션값을 조합할 수 있음  독립형이나 상품 연동형 옵션을 사용하고 있을 경우 S(분리형)로 입력됨.   S : 조합 분리선택형 C : 조합 일체선택형 |
| options | 옵션 |
| options 하위 요소 보기     option_nameRequired옵션명 option_value Array    option_value 하위 요소 보기     option_text옵션값Required option_image_file옵션 버튼 이미지 option_color컬러칩 색상    option_display_type옵션 표시방식S : 셀렉트박스 P : 미리보기 B : 텍스트버튼 R : 라디오버튼DEFAULT S |
| select_one_by_option | 옵션별로 한 개씩 선택 (독립형 옵션)   독립형 옵션을 사용할 경우, 하나의 옵션을 여러개 중복하여 선택할 수 없고 한개씩만 선택 가능함.   T : 사용함 F : 사용안함 독립형에만 존재 체크시 옵션별로 한개씩 선택 값 처리 |
| option_preset_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 옵션세트 코드 |
| option_preset_name | 연동형 옵션 세트명   상품연동형 옵션을 사용할 경우, 옵션 세트의 이름 입력 |
| use_additional_option | 추가입력 옵션 사용여부   T : 사용함 F : 사용안함 |
| additional_options | 추가입력 옵션 |
| additional_options 하위 요소 보기     additional_option_nameRequired추가입력옵션명 additional_option_text_lengthRequired추가입력옵션 길이제한1~30 50 100 200 required_additional_optionRequired추가입력옵션 필수 여부T : 필수 F : 선택DEFAULT T |
| use_attached_file_option | 파일 첨부 옵션 사용여부   T : 사용함 F : 사용안함 |
| attached_file_option | 파일 첨부 옵션 |

```bash
Create product options        Create product options Create combination type option of the product Create linked with product option of the product with creating new option preset Create linked with product option of the product with existing option preset Create independently selectable option of the product       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Update product options   cafe24 youtube

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
| option_list_type | 옵션 표시방식   조합형 옵션을 사용할 경우, 조합형 옵션의 유형 입력  * 조합 일체선택형 : 하나의 셀렉스박스(버튼 이나 라디오버튼)에 모든 옵션이 조합되어 표시됨 * 조합 분리선택형 : 옵션을 각각의 셀렉스박스(버튼 이나 라디오버튼)로 선택할 수 있으며 옵션명을 기준으로 옵션값을 조합할 수 있음  독립형이나 상품 연동형 옵션을 사용하고 있을 경우 S(분리형)로 입력됨.   S : 조합 분리선택형 C : 조합 일체선택형 |
| option_preset_code형식 : [A-Z0-9]글자수 최소: [8자]~최대: [8자] | 옵션세트 코드   상품연동형 옵션을 사용할 경우, 옵션 세트 코드 입력 |
| options | 옵션 |
| options 하위 요소 보기     option_nameRequired옵션명 option_value Array    option_value 하위 요소 보기     option_text옵션값Required option_image_file옵션 버튼 이미지 option_link_image옵션 연결 이미지 option_color컬러칩 색상    option_display_type옵션 표시방식S : 셀렉트박스 P : 미리보기 B : 텍스트버튼 R : 라디오버튼DEFAULT S |
| original_options | 수정되기전 옵션값 |
| original_options 하위 요소 보기     option_nameRequired옵션명 option_value Array    option_value 하위 요소 보기     option_text옵션값Required |
| select_one_by_option | 옵션별로 한 개씩 선택 (독립형 옵션)   독립형 옵션을 사용할 경우, 하나의 옵션을 여러개 중복하여 선택할 수 없고 한개씩만 선택 가능함.   T : 사용함 F : 사용안함 독립형에만 존재 체크시 옵션별로 한개씩 선택 값 처리 |
| option_preset_name | 연동형 옵션 세트명   상품연동형 옵션을 사용할 경우, 옵션 세트의 이름 입력 |
| use_additional_option | 추가입력 옵션 사용여부   T : 사용함 F : 사용안함 |
| additional_options | 추가입력 옵션 |
| additional_options 하위 요소 보기     additional_option_nameRequired추가입력옵션명 additional_option_text_lengthRequired추가입력옵션 길이제한1~30 50 100 200 required_additional_optionRequired추가입력옵션 필수 여부T : 필수 F : 선택DEFAULT T |
| use_attached_file_option | 파일 첨부 옵션 사용여부   T : 사용함 F : 사용안함 |
| attached_file_option | 파일 첨부 옵션 |

```bash
Update product options        Update product options Update option name and option value Update option name and option value of linked with product option Update option name, option value and required option of independetly selectable option       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```

### Delete a product option   cafe24 youtube

#### 기본스펙

| Property | Description |
| --- | --- |
| SCOPE | 상품 쓰기권한 (mall.write_product) |
| 호출건수 제한 | 40 |

#### 요청사양

| Parameter | Description |
| --- | --- |
| product_noRequired | 상품번호   상품의 고유한 일련 번호. 해당 쇼핑몰 내에서 상품 번호는 중복되지 않음. |

```bash
Delete a product option        Delete a product option       Request   cURL Java Python Node.js PHP Go  Copy         Response  Copy
```
