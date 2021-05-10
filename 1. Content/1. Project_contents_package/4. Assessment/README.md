# 4. Assessment : 프로젝트 평가 요소

### 개요

![Untitled Diagram_](https://user-images.githubusercontent.com/68315073/117620469-78414700-b1ab-11eb-9cc0-24ec48d98417.png)


하나의 Asessment Directory는 여러 개의 JSON파일을 담고 있습니다. <br><br>

하나의 JSON파일은 1개의 미션에 대한 평가 항목들이 정의되어 있습니다. <br><br>

따라서 Assessment Directory 안에는 프로젝트에 존재하는 미션의 개수만큼 JSON파일이 존재합니다. <br><br>

LMS는 Assessment Directory에 존재하는 JSON파일들을 읽어와 평가 화면에 평가 항목들을 나열합니다. <br><br>

최종적으로 평가 항목들이 나열된 평가 화면에서 평가자들은 평가를 진행합니다. 

![image](https://user-images.githubusercontent.com/68315073/117620331-5f389600-b1ab-11eb-9ac1-03c7c6843c93.png)


### 목차

![슬라이드4](https://user-images.githubusercontent.com/68315073/116506696-bb243480-a8f8-11eb-8622-765469590e38.PNG)

> Assessment의 항목과 코드 연결

## 4.1 id : 고유번호

평가 항목을 구분하기 위해 입력하는 각 평가 항목의 식별자입니다. </br></br>
평가 항목의 `id(고유번호)`는 1 ~ 2자리 `숫자`이며, 하나의 미션 내에서 서로 다른 평가 항목은 동일한 `id`를 가질 수 없습니다.</br></br>
평가 항목의`id(고유번호)`는 한 1부터 오름차순으로 부여됩니다. 

### 예시

``` json
"id": 3
```

> 해당 평가 항목은 프로젝트 M의 N번째 미션의 3번째 평가 항목입니다. 

## 4.2 item : 평가 문항

학생의 미션 수행을 평가할 수 있는 문항을  `문자열`을 사용하여 1줄의 문장으로 작성합니다. 

### 예시

```json
"item": "image를 웹센서에서 문제 없이 load했나요?"
```

## 4.3 class : 평가 항목의 분류

해당 평가 문항이 어떠한 분야의 지식을 평가하는지 작성합니다.<br><br>

만약 `평가 항목의 분류`가 "Data Extracting"이라면, 해당 평가 문항은 학생의 데이터 추출 능력에 대해 평가합니다.

### 예시

```json
"class": "Data Extracting"
```

## 4.4 type : 문항 유형

해당 평가 문항을 평가하는 방법에 대해 서술합니다.<br>

<br>

가능한 평가 방법은 다음과 같습니다. 

- `radio` : 여러 개의 보기 중 하나만 선택할 수 있는 방법입니다. 
- `checkbox` : 여러 개의 보기 중 다수의 항목을 선택할 수 있는 방법입니다.
- `text` : 단답식 평가를 위한 평가 방법입니다.
- `textarea` : 서술형 평가를 위한 평가 방법입니다. 

### 예시

``` json
"type": "radio"
```

> 해당 평가 문항은 radio 유형이며 보기 중 하나를 선택합니다. 

![image](https://user-images.githubusercontent.com/68315073/117620726-b8082e80-b1ab-11eb-9025-481bbfcfed6d.png)


```json
"type": "checkbox"
```

> 해당 평가 문항은 checkbox 유형으로 다음 보기 중 해당되는 항목을 모두 선택할 수 있습니다.  

![image](https://user-images.githubusercontent.com/68315073/117620747-bd657900-b1ab-11eb-9915-fa7d1dfc2bce.png)


```json
"type": "textarea"
```

> 해당 평가 문항은 서술형 평가를 요구합니다. 

![image](https://user-images.githubusercontent.com/68315073/117620763-c0f90000-b1ab-11eb-8e0c-b4f038ee5ba2.png)


## 4.5 option : 선택 항목

`4.4 type`에서 평가 방법으로 `radio`나 `checkbox`를 선택했다면, 선택할 수 있는 보기들을 `option` 배열로 작성합니다. 

### 예시 

``` json
"option": [
            "예",
            "아니오"
        ]
```

> 해당 평가 문항은 "예" 와 "아니오" 중 선택하는 2지 선다 문제입니다.

![image](https://user-images.githubusercontent.com/68315073/117620930-f7367f80-b1ab-11eb-8121-017c0a1f03de.png)

<br><br>
