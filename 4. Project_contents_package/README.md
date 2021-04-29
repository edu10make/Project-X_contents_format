

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

# 3. learning_resource : 프로젝트 학습 리소스
![슬라이드3](https://user-images.githubusercontent.com/68315073/116506694-b8c1da80-a8f8-11eb-9aee-8a8563d0add1.PNG)

# 4. assessment : 프로젝트 평가 요소
![슬라이드4](https://user-images.githubusercontent.com/68315073/116506696-bb243480-a8f8-11eb-8622-765469590e38.PNG)
