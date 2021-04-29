

# 1. definition : 프로젝트 정의 및 역량
![슬라이드1](https://user-images.githubusercontent.com/68315073/116506676-b19acc80-a8f8-11eb-9339-092d257d9f21.PNG)
- 프로젝트의 id, 주제, 목적 등 프로젝트의 기본적인 정보에 대해 기입합니다.
- 특정 Level이나 Mission에 국한되는 정보가 아닌 프로젝트 전반적인 정보를 기입합니다.
- 이 파일은 Project-X 학습 관리 시스템(LMS)가 읽어 사용자로 하여금 Web상에서 프로젝트에 대한 정보를 확인할 수 있도록 합니다. 

## 1.1 id
```json
"id" : 10025
```

- 프로젝트를 구분하기 위해 각 프로젝트의 고유 번호를 입력합니다.<br>
- 프로젝트의 고유번호는 4자리 숫자로 구성되며, 서로 다른 프로젝트는 동일한 고유번호를 가질 수 없습니다.

## 1.2 title 
```json
"title": "미터기 읽기"
```
프로젝트의 이름을 입력합니다. 

## 1.3 estimation_time
```json
"estimated_time":50
```
- 커리큘럼을 만들려면 이 **프로젝트를 수행하는데 걸리는 시간**을 알아야 합니다.
- 해당 프로젝트를 수행하는데 걸리는 시간을 작성합니다.

## 1.4 class
```json
"class": [
        "AI/Data분석/Edu4",
        "AI/모델개발/Edu4",
        "AI/AIOps/Edu4",
        "Back-end/Edu4"
    ]
 ```
 - 프로젝트가 어떤 분야, 어떤 주제로 뭘 만들려하는 것인지 알게 해줍니다. <br>
 - 프로젝트의 적정 레벨을 **string 배열**로 입력합니다. 
 - PSI에서 제공하는 **'tech skill 역량명세서 - 수준 구분'** 의 양식에 맞춰 작성합니다. 
 
 ## 1.5 story
 ```json
 "story": "https://github.com/edu10make/Project-X_contents_format/blob/junseok/Project/story/no_show.md"
 ```
 - 프로젝트 스토리가 있는 링크를 기술합니다. 
 
 ## 1.6 object
 ```json
 "objects": {
        "main_object": "수도 계량기의 숫자를 읽어서 웹서버에 보여주는 digital twin기능을 구현하라, 실시간 분석 및 액튜에이션 확장기능 개발",
        "detailed_objects": ["현장에 설치된 계량기의 이미지 데이터를 취득하라",
            "계량기 숫자 부분의 이미지 추출하라",
            "클라우드 서비스를 이용하여 추출한 이미지에서 문자를 인식하라",
            "머신러닝 알고리즘을 탐색하여 기반으로 사용할 알고리즘을 선택하라",
            "수천 장 이미지를 갖고 각각의 사진에 레이블링을 어떻게 할 지 기술적으로 궁리하라",
            "파이썬 툴을 사용하여 수천 장 이미지를 적절한 하나의 데이터 화일로 구성하라",
            "몇 장의 표본에 대해 머신러닝 Training을 진행할지에 대한 판단기준 세워라",
            "인식한 숫자를 웹서버에 표기하는 digital twin meter를 구현하라"
        ]
    }
 ```
 - 프로젝트의 목적에 대해 작성합니다. 
 - `main_object`는 프로젝트 전체를 관통하는 하나의 목표입니다. 프로젝트가 해결하고자 하는 문제나 프로젝트가 끝났을 때 학생들이 만들어 낼 결과물을 기술합니다.
 - `detailed_objects`는 `main_object`를 달성하기 위한 프로젝트 세부 목표입니다.
 
## 1.7 skills
```json
"skills": {
        "require": [
            "Fundamentals > Python Programming > Python Basics",
            "Fundamentals > Python Programming >  Numpy",
            "Fundamentals > Python Programming > Pandas"
        ],
        "acquire": [
            "Deep Learning > Neural Networks > Activation Functions",
            "Deep Learning > Neural Networks > Understanding Nerual Networks",
            "Deep Learning > Architectures > CNN",
            "Deep Learning > Traning > Optimizers",
            "Deep Learning > Tools > TenosorFlow"
        ]
    }
```
- 프로젝트와 관련된 역량을 작성합니다.
- `require`에는 프로젝트를 수행하기 위해 필요한 역량을 작성합니다. 선수 프로젝트 등을 기입할 수 있습니다.
- `acqure`에는 프로젝트를 수행하고 나면 얻을 수 있는 역량입니다. 이 프로젝트를 통해 달성할 수 있는 학습 성과들을 기입합니다.


# 2. description : 프로젝트 기술 문서
![슬라이드2](https://user-images.githubusercontent.com/68315073/116506685-b5c6ea00-a8f8-11eb-951a-3cd795057bfd.PNG)
- 하나의 프로젝트는 여러 개의 미션들로 구성됩니다.
- 프로젝트 기술 문서에서는 프로젝트를 구성하는 미션들과 미션들에 포함되어야 하는 내용을 기술합니다.
- 각 미션은 다음의 항목을 포함합니다.
	- id
	- 미션의 주제
	- 미션을 해결하기 위한 키워드
	- 미션에 대한 설명
	- 미션을 달성했을 때 달성할 수 있는 역량
	- 미션 수행후 산출해야하는 결과물
	- 미션 종료 후 학습 성과를 확인할 수 있는 퀴즈
## 2.1 id
```json
"id": 2
```
- 서로 다른 미션을 구분하기 위한 고유 번호 입니다.

## 2.2 subject
```json
"subject": "숫자 추출하기1"
```
- 미션의 제목을 간단하게 설명합니다. 
- 학생들은 미션의 제목을 보고 미션의 내용을 파악할 수 있습니다.

## 2.3 keywords
```json
"keywords": ["Open CV", "Affine", "PerspectiveTransform"]
```
- 학생들이 미션을 수행하면서 참고할 수 있는 기술들을 배열로 작성합니다.
- 각각의 기술들을 단어 단위로 입력합니다. 

## 2.4 explanation
```json
"explanation": [
            "먼저, 이미지를 회전시키고 왜곡을 보정하는 등의 과정을 거친다.",
            "수정한 이미지에서 미터 값이 변화하는 부분을 잘라낸다."
        ]
```
- 구체적인 미션 수행 방향에 대해 작성합니다.
- 학생들은 미션 설명을 보고 제시된 문제를 구현할 수 있습니다. 

## 2.5 objects
``` json
"objects": [3, 4, 16, 18, 41, 87]
```
- 미션을 달성했을 때 달성할 수 있는 역량을 경험을 중심으로 기술합니다.
- 따라서 각 항목은 PSI에서 제공하는 **tech skill 역량명세서 - 경험리스트**를 참고하여 기술합니다.
- **tech skill 역량명세서 - 경험리스트**의 항목 중 해당 미션 수행 후 달성할 수 있는 역량을 찾아 해당 역량의 **no.**를 `int형 숫자`로 기술합니다.

## 2.6 result
``` json
"result": ["코드"]
```
- 미션 완료 후 산출해야 하는 결과물을 작성합니다. 
- 해당 항목을 통해 학생들은 자신이 미션에서 어떤 결과물을 산출해야 하는지 명확하게 알 수 있습니다.

## 2.7
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
- 학생이 미션을 제대로 수행했는지 확인할 수 있는 quiz이다. 
- `quiz`는 각 mission마다 **선택적으로** 들어갑니다. 따라서 `quiz`가 없는 mission이 존재할 수 있습니다. 
- `quiz`는 다음의 항목으로 구성됩니다. 
	- `class` : 해당 질문을 통해 물어볼 수 있는 학습 분야입니다. 만약 "Data Extracting"이 들어간다면, 해당 질문은 데이터 추출에 관한 질문입니다.
	- `item` : 질문 문항입니다.
	- `answer` : 질문에 대한 정답입니다. 

# 3. learning_resource : 프로젝트 학습 리소스
![슬라이드3](https://user-images.githubusercontent.com/68315073/116506694-b8c1da80-a8f8-11eb-9aee-8a8563d0add1.PNG)

# 4. assessment : 프로젝트 평가 요소
![슬라이드4](https://user-images.githubusercontent.com/68315073/116506696-bb243480-a8f8-11eb-8622-765469590e38.PNG)
