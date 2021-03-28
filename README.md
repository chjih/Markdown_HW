# ***GitHub Flavered Markdown (GFM) 사용 방법***

<br>

# 1. Tables(extention)

- 표를 추가하려면 세 개 이상의 하이픈 (---)을 사용 -> 각 열의 헤더 생성
- 파이프(|)를 사용 -> 각 열 구분
- 헤더 행 

### *예)*

```

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

```

### *<출력 결과>*

| Syntax      | Description |
| ----------- | ----------- |
| Header      | Title       |
| Paragraph   | Text        |

- 셀 너비는 다를 수 있음 -> 출력은 동일하게 보임

## - **Alignment (정렬)**

- 하이픈의 왼쪽 or 오른쪽 or 양쪽에 콜론(:) 추가 -> 텍스트 왼쪽, 오른쪽, 가운데로 정렬할 수 있음
- 헤대 행 = 셀 수의 구분 기호 행 ( 아닐 시 테이블이 인식 되지 x )

### *예)*

```

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

```

### *<출력 결과>*

| Syntax      | Description | Test Text     |
| :---        |    :----:   |          ---: |
| Header      | Title       | Here's this   |
| Paragraph   | Text        | And more      |

## - **Formatting Text in Tables (표에서의 텍스트 포멧팅)**

- table 내에서 텍스트 포멧 가능
- ex) 링크, 코드 (코드 블록이 아닌 백틱(`)사용) 및 강조 표시
- 제목(title), 인용구(blockqoutes), 리스트(list), 수평 규칙(horizontal rules), 이미지 또는 HTML 태그 추가 불가능

## - **Excaping Pipe Characters in Tables (표에서의 이스케이프 문자)**

- HTML 문자코드((&#124;)를 사용하여 표에서 파이프(|) 문자를 표시 할 수 있음

<br>
<br>
<br>

# 2. **분리 코드 블록 (Fenced Code Blocks)**

- 줄을 들여 쓰지 않고 코드 블록 생성하려면 '분리 코드 블록 (Fenced Code Blocks)' 사용  
코드 블록 앞뒤의 줄에 세 개의 백틱(```)혹은 물결(~~~) 사용

### *예)*

```

{
"firstName": "John",
"lastName": "Smith",
"age": 25
}

```
  
### *<출력 결과>*

{
"firstName": "John",
"lastName": "Smith",
"age": 25
}

<br>
<br>
<br>

# 3. **구문 강조(Syntax Highlighting)**

- 이 기능 사용 시 작성된 언어에 대해 색상 강조 표시 추가 가능
- 분리코드 블록 앞의 백틱 옆에 언어 지정
- ex) ```json

## *<출력 결과>*

```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```

<br>
<br>
<br>

# 4. **작업 리스트 항목 (Task list items)**

- 사용 시 확인란이 있는 항목 목록을 만들 수 있음
- 확인란 선택하려면 x를 대괄호 사이에 추가해야함 -> ([x])
- 작업 목록은 중첩 가능
- HTML에서는 \<input type="checkbox">

### *예)*

```

- [x] Write the press release
- [ ] Update the website
  - [ ] bar 
- [ ] Contact the media

```

### *<출력 결과>*

- [x] Write the press release
- [ ] Update the website
  - [ ] bar
- [ ] Contact the media

<br>
<br>
<br>

# 5. 취소선 (Strikethrough)

- 추가 강조 유형
- 두개의 물결표(\~~)로 묶인 텍스트

### *예)*

```

~~Hi~~ Hello, world!

```

### *<출력 결과>*

~~Hi~~ Hello, world!

<br>
<br>
<br>

# 6. 자동 링크 (Autolinks)

- 많은 markdown 프로세서는 자동으로 URL을 링크로 변환함
- 대괄호를 사용하지 않고도 자동으로 링크로 바뀜

### *예)*

```

http://www.naver.com/

```

### *<출력 결과>*

http://www.naver.com/

<br>
<br>
<br>

# 7. 허용되지 않는 원시 HTML

- GFM은 태그 필터 확장을 활성화함
- HTML 출력을 렌더링할 때 다음 HTML 태그가 필터링 됨

<br>

- \<tilte>
- \<textarea>
- \<style>
- \<xmp>
- \<iframe>
- \<noembed>
- \<noframes>
- \<script>
- \<plaintext>

<br>

- 필터링은 '<'을 '&lt;'로 대체하여 수행됨
- 이 태그들은 특히 HTML이 고유한 방식으로 해석되는 방법을 변경할 때 선택 됨
- 일반적으로 다른 렌더링되 MARKdown 컨텐츠의 맥락에서 바람직하지 않음

<br>

- 다른 모든 HTML 태그는 그대로 유지
