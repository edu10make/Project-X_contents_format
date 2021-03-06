# 2. Description : 프로젝트 기술 문서

### 개요

하나의 프로젝트는 여러 개의 미션들로 구성됩니다</br>

'프로젝트 기술 문서'에서는 프로젝트를 구성하는 미션들과 미션들에 포함되어야 하는 내용을 기술합니다.



### 목차 

![슬라이드2](https://user-images.githubusercontent.com/68315073/116506685-b5c6ea00-a8f8-11eb-951a-3cd795057bfd.PNG)
'프로젝트 기술 문서'에서 하나의 미션 포맷은 다음의 항목을 포함합니다.

| 순번 | 항목                                         | 변수형   | 크기        |
| ---- | :------------------------------------------- | -------- | ----------- |
| 2.1  | id                                           | `숫자`   | `단일 변수` |
| 2.2  | 미션의 주제                                  | `문자열` | `단일 변수` |
| 2.3  | 미션을 해결하기 위한 키워드                  | `문자열` | `배열`      |
| 2.4  | 미션에 대한 설명                             | `문자열` | `배열`      |
| 2.5  | 미션을 달성했을 때 달성할 수 있는 역량       | `숫자`   | `배열`      |
| 2.6  | 미션 수행후 산출해야하는 결과물              | `문자열` | `배열`      |
| 2.7  | 미션 종료 후 학습 성과를 확인할 수 있는 퀴즈 | `문자열` | `배열`      |


<br><br>
## 2.1 id : 고유번호
미션을 구분하기 위해 입력하는 각 미션의 `id(고유 번호)`입니다. </br>

미션의 `id(고유번호)`는 n자리 `숫자`로 구성되며, 서로 다른 미션은 동일한 `id`를 가질 수 없습니다.</br>

미션 `id(고유번호)`는 한 Project에서 미션이 진행되는 순서대로 1부터 오름차순으로 부여됩니다.

### 예시


```json
"id": 2
```

> 해당 미션의 `id(고유번호)`는 '2'입니다. 즉, 프로젝트를 진행하게 되면 두 번째로 수행하는 미션입니다. 

<br><br>
## 2.2 subject : 미션 제목

`미션 제목`을 `문자열`로 기입합니다. </br>

미션 전체 내용을 함축할 수 있는 문장이나 키워드를 입력합니다. </br>

`미션 제목`을 통해 미션의 내용을 대략적으로 파악할 수 있습니다. 

### 예시

```json
"subject": "숫자 추출하기1"
```

> 해당 `미션 제목`은 "숫자 추출하기1"입니다.

<br><br>
## 2.3 keywords : 키워드

해당 미션에 사용해야 하거나 해당 미션과 연관 있는 기술들을 작성합니다.</br>

키워드를 작성할 때에는 각각의 `키워드`를 문자열로 작성하며, `키워드`가 여러 개일 경우 `배열`로 작성합니다.  

### 예시

```json
"keywords": ["Open CV", "Affine", "PerspectiveTransform"]
```

> 학생들은 해당 미션을 수행할 때, 'Open CV', 'Affine', 'PerspectiveTransform'이라는 `키워드`를 검색해보고 도움을 얻을 수 있습니다. 

<br><br>
## 2.4 explanation : 설명

미션에 대한 구체적인 `설명`을 작성합니다. </br>

각각의 `설명`은 `문자열`로 작성하며, 한 미션의 `설명`이 여러 문장일 경우, 각각의 문장을 `문자열`로 변환하여 `배열`에 기입합니다. </br>

미션 `설명`을 통해 학생들은 미션의 내용을 구체적으로 파악할 수 있습니다.</br>

미션 `설명`을 통해 학생들은 미션에서 요구하는 바를 파악할 수 있습니다.

### 예시

```json
"explanation": [
            "먼저, 이미지를 회전시키고 왜곡을 보정하는 등의 과정을 거친다.",
            "수정한 이미지에서 미터 값이 변화하는 부분을 잘라낸다."
        ]
```

<br><br>
## 2.5 objects : 목적

모든 미션의 `목적`은 미션을 수행하는 학생이 특정한 기술을 경험하게 하기 위함입니다. </br>

따라서 프로젝트의 `목적`에는 프로젝트를 수행하고 나면 경험할 수 있는 역량을 작성합니다. </br>

모든 `목적`은 [tech skill 역량명세서 - 경험리스트](https://github.com/edu10make/Project-X_contents_format/tree/main/3.%20Source/2.%20Tech_Skill)를 보고 해당되는 역량의 `id`를 `숫자`로 기입합니다. </br>

만약, 한 미션의 `경험(목적)`이 여러 개일 경우, 각각의 `경험(목적)`을 `문자열`로 변환하여 `배열`에 기입합니다. </br>

예를 들어, 어떤 미션을 통해  "센서를 통해 들어오는 연속된 데이터를 처리"를 경험할 수 있다면,  [tech skill 역량명세서 - 경험리스트](https://github.com/edu10make/Project-X_contents_format/tree/main/3.%20Source/2.%20Tech_Skill)에서 경험 : "센서를 통해 들어오는 연속된 데이터를 처리할 수 있다"의 `id`가 '1'인 것을 확인한 후 `object`에 '1'을 기입합니다.</br>

추후에 **경험 리스트의 확장**이 필요하다면 [tech skill 역량명세서 - 경험리스트](https://github.com/edu10make/Project-X_contents_format/tree/main/3.%20Source/2.%20Tech_Skill)를 업데이트한 이후 추가된 경험의 `id`를 기입합니다. </br>

### 예시

``` json
"objects": [3, 4, 16, 18, 41, 87]
```

> 해당 미션을 통해 경험할 수 있는 역량은 다음과 같습니다. 

| id   | 카테고리                                                | 경험                                                         |
| ---- | ------------------------------------------------------- | ------------------------------------------------------------ |
| 3    | Data분석(데이터 추출 및 가공 역량)                      | 데이터베이스의 데이터를 추출해 가공할 수 있다                |
| 4    | Data분석(데이터 추출 및 가공 역량)                      | 이미지, 영상 데이터의 포맷을 변경하고 메타 데이터를 생성할 수 있다 |
| 16   | Data분석(데이터 추출 및 가공 역량)                      | 수집된 데이터의 형식을 동일하게 맞출 수 있다                 |
| 18   | Data분석(데이터 추출 및 가공 역량)                      | 수집된 데이터에서 불필요한 차원을 제거할 수 있다             |
| 41   | Data분석(데이터 관련 리터러시 및 데이터 특성 파악 역량) | 탐색적 자료 분석을 통해, 데이터의 특성을 파악할 수 있다.     |
| 87   | AI모델개발(이미지관련 지식 이해력)                      | OpenCV 라이브러리만을 사용해서 이미지 뷰어(Crop, 흑백화, Zoom 등의 기능 포함)를 만들 수 있다. |


<br><br>
## 2.6 result : 결과물

학생들이 미션 완료 후 산출해야 하는 `결과물`에 작성합니다.  </br>

`결과물`을 통해 학생들은 자신이 미션에서 어떤 결과물을 산출해야 하는지 명확하게 알 수 있습니다.</br>

### 예시

``` json
"result": ["training 이 끝난 model 을 읽어서 실시간으로 취득한 미터 이미지를 인식하는 파이썬 코드","Digital twin meter"]
```

> 해당 미션이 종료된 후 학생들은 결과물 코드와 만든 Digital twin meter를 제출해야 합니다. 

<br><br>
## 2.7. quiz : 퀴즈

학생이 미션을 제대로 수행했는지 확인할 수 있는 퀴즈를 작성합니다. </br>

`퀴즈`는 각 미션마다 **선택적으로** 들어갑니다. 따라서 한 미션에는 `퀴즈`가 존재할 수도 있고 없을 수도 있습니다. </br>

`퀴즈`는 `객체`로 이루어진 `배열`이며 하나의 `퀴즈`는 다음과 같은 항목으로 구성됩니다.  

- `class` : 해당 질문을 통해 물어볼 수 있는 학습 분야입니다. 만약 "Data Extracting"이 들어간다면, 해당 질문은 데이터 추출에 관한 질문입니다.
  `문자열`로 작성합니다. 

- `item` : 질문 문항을 `문자열`로 작성합니다. 

- `answer` : 질문에 대한 정답을 `문자열`로 작성합니다. 

### 예시

``` json
"quiz": [
            {
                "class": "Data Extracting",
                "item": "OpenCV 에서 이미지의 XY 좌표체계와 수학시간에 사용하는 X - Y 좌표를 비교해서 설명하라.",
                "answer": "Y 방향이 아래쪽으로 향한다."
            },
            {
                "class": "Data Extracting",
                "item": "이미지의 crop 을 위한 좌표는 어떻게 찾아내는가?",
                "answer": "OpenCV imshow 에서 click 마우스콜백이벤트의 파라미터로 주어지는 x, y 좌표를 프린트하는 프로그램을 간단히 만들 수 있다."
            }
        ]
```

> 해당 미션에는 "Data Extracting"에 관해 물어보는 퀴즈가 2개 존재합니다. 

| `class` : 학습 분야 | `item` : 질문 문항                                           | `answer` : 정답                                              |
| ------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Data Extracting     | OpenCV 에서 이미지의 XY 좌표체계와 수학시간에 사용하는 X - Y 좌표를 비교해서 설명하라. | Y 방향이 아래쪽으로 향한다.                                  |
| Data Extracting     | 이미지의 crop 을 위한 좌표는 어떻게 찾아내는가?              | OpenCV imshow 에서 click 마우스콜백이벤트의 파라미터로 주어지는 x, y 좌표를 프린트하는 프로그램을 간단히 만들 수 있다. |

<br><br>
