# PBL Contents Standard Format
![PBL Contents Standard Format_liner](https://user-images.githubusercontent.com/68315073/115686649-62064f00-a394-11eb-80f4-769dd1f406fb.png)

### 읽는 방법
- 타일에 따른 분류
	- 직사각형 한 개짜리 타일 : 단일 변수
	- 직사각형 두 개가 겹쳐진 타일 : 배열

- 색상에 따른 분류
	- `검정색` : `object`
	- `빨간색` : `boolean`
	- `초록색` : `string`
	- `파란색` : `int`

- 예시 -> '1. Basic - objects - detailed objects[]'는 직사각형 두 개가 겹쳐진 초록색 타일 : '프로젝트의 세부 목적'은 string 배열로 작성


## 0. Operation
```json
"Operation": {
    "period": {
      "self_paced": true,
      "start": 2021050313,
      "finish": 2021071324
    },

    "progress": {
      "select": "peer_learning",
      "option": ["self_learning", "peer_learning", "lecture"]
    },

    "matching": {
      "select": "random",
      "option": ["random", "designate", "select"]
    }
  }
```
프로젝트 운영을 위한 전반적인 내용을 결정한다.<br>
해당 챕터에서 결정해야 할 내용은 다음과 같다.
- `period` : 학습 기간
- `matching` : 평가자 매칭 방식

### 0.1 period
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트의 시작 시기, 끝나는 시기와 기간에 대한 옵션을 지정한다.
```json
    "period": {
      "self_paced": true,
      "start": 2021050313,
      "finish": 2021071324
    },
```
- `self_paced` : `boolean`변수가 인자로 들어가며 프로젝트가 'self-paced'방식으로 진행되는지 여부를 결정한다. 만약 `false`라면 Fixed schedule으로 프로젝트가 진행된다.
	- self-paced : 각 학생들의 수준 및 상황에 따라 각기 다른 속도로 미션을 수행하는 모델, 따라서 모든 학생들의 프로젝트 진행 상황과 종료 시점은 상이함
	- Fixed schedule : 고정된 일정에 맞춰서 모든 학생들이 동일한 스케쥴로 프로젝트를 수행하는 모델, 따라서 모든 학생들이 같은 속도로 프로젝트를 수행함
- `start` : 프로젝트의 예정 시작일 및 예정 시작 시간을 입력한다. 10자리 `int`형 변수이며 '연도(4자리)' + '월(2자리)' + '일(2자리)' + '시간(2자리)'로 구성된다.
- `finish` : 프로젝트의 예정 종료일 및 예정 종료 시간을 입력한다. 10자리 `int`형 변수이며 '연도(4자리)' + '월(2자리)' + '일(2자리)' + '시간(2자리)'로 구성된다.

따라서 위의 예시 프로젝트는 self-paced 방식으로 2021년 5월 3일 오후 1시부터 시작해서 2021년 7월 13일 오후 24시에 종료된다.



### 0.2 matching
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트 동료 평가자 방식을 결정한다. 
```json
"matching": {
           "select": 0,
           "option": [
               "request",
               "designate",
               "consent"
            ]
       }
```

- `option` : 'string 배열'로 가능한 프로젝트 진행 옵션들을 나열한다. 
	- request : A가 B에게 평가를 요청하면, B는 A의 평가를 진행 (평가 요청 거절 불가능)
	- consent : A가 B에게 평가를 요청하면, B가 A의 요청을 수락함으로써 평가 관계가 형성됨 (평가 요청 거절 가능)
	- designate : 멘토가 판단하여 학생들 간 평가 관계를 지정함
- `select` : - `select` : 가능한 `option`중 해당 프로젝트가 동료 평가자 선택 방식으로 선택한 option의 index를 기입한다. 

따라서 해당 프로젝트는 학생끼리의 '요청'방식을 통해서 평가 관계를 형성한다. 


## 1. Basic
```json
"Basic": {
    "id": 10023,
    "title": "환자 데이터 분석을 통한 No-Show 예측",
    "class": ["AI/Data분석/Edu4", "AI/모델개발/Edu4", "AI/AIOps/Edu4"],
    "story": "https://github.com/edu10make/Project-X_contents_format/blob/junseok/Project/story/no_show.md",
    "objects": {
      "main_object": "텍스트 데이터 분석 및 학습",
      "detailed_objects": [
        "데이터 저장 및 준비 등 데이터 전처리 과정을 경험할 수 있다.",
        "데이터를 자세하게 분석하고 해당 내용에 대해 설명할 수 있다.",
        "모델링을 경험해볼 수 있다."
      ]
    },
    "skills": {
      "require": ["python", "numpy", "pandas", "matplotlib"],
      "acquire": ["jupyter_notebook", "TensorFlow", "scikit-learn", "CNN"]
    }
  }
```
프로젝트의 id, 주제, 목적 등 프로젝트의 기본적인 정보에 대해 기입한다.<br>
또한 '프로젝트'에 대한 정보이기에 특정 Level이나 mission에 국한되는 내용이 아닌, 프로젝트 전반적인 정보를 기입한다는 점에 주의한다. 

### 1.1 id
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `int` | `필수` |

여러 개의 프로젝트를 구분하기 위해 각 프로젝트의 고유 번호를 입력한다.<br>
프로젝트의 고유번호는 4자리 숫자로 구성되며, 서로 다른 프로젝트는 동일한 고유번호를 가질 수 없다. 
```json
"id": 10023
```


### 1.2 title 
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `필수` |

프로젝트의 이름을 입력한다. 프로젝트 이름은 한 줄 이내의 핵심적인 내용을 담아, 제목만 보고도 프로젝트를 대략적으로 파악할 수 있도록 한다.
```json
"title": "환자 데이터 분석을 통한 No-Show 예측"
```


### 1.3 class

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `string` | `필수` |

['tech skill 역량명세서 - 수준 구분'](https://github.com/PSIConsulting/Project-X/blob/master/Competency%20Level.md)을 참고하여 프로젝트를 수준을 분류한다.

```json
"attribute": ["AI/Data분석/Edu4",
            "AI/모델개발/Edu4",
            "AI/AIOps/Edu4"
        ]
```


### 1.4 objects
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트의 목적을 주요 목적과 세부 목적으로 분리하여 입력한다. 
이 때, 프로젝트의 주요 목적은 프로젝트 전체를 관통하는 내용이 포함되어야 한다. 

```json
"objects": {
            "main_object": "프로젝트 메인 주제",
            "detailed_objects": ["데이터 저장 및 준비 등 데이터 전처리 과정을 경험할 수 있다.",
                "데이터를 자세하게 분석하고 해당 내용에 대해 설명할 수 있다.",
                "모델링을 경험해볼 수 있다."
            ]
        },
```

- `main object` : 프로젝트의 중추적인 목표를 'string 변수'로 입력한다. `main object`에는 프로젝트가 해결하고자 하는 문제나 프로젝트가 끝났을 때 학생들이 만들어 낼 결과물을 기술한다.
- `detailed objects` : 프로젝트의 세부적인 목표들을 'string 배열'로 입력한다. `main object`를 달성하기 위해 수행할 세부적인 목표들을 기술한다.


### 1.5 skills
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트를 수행하면 얻을 수 있는 기술을 입력한다. 
```json
"skills": {
      "require": ["python", "numpy", "pandas", "matplotlib"],
      "acquire": ["jupyter_notebook", "TensorFlow", "scikit-learn", "CNN"]
    }
```

- `require` : 프로젝트를 수행하기 위해 필요한 기술들을 나열한다.
- `acquire` : 프로젝트를 수행하면 얻을 수 있는 기술들을 나열한다. 

예를 들어, 프로젝트1을 시작하기 전 학생들은 python과 numpy, pandas, matpolib에 대해 학습을 진행한 상태여야 하며,<br>
프로젝트가 진행되는 동안 jupyter notebook, TensorFlow, scikit-learn, CNN에 대해 학습할 수 있다.



## 2. Levels
```json
  "Levels": [{
    "level": 2,
    "missions": [{
        "id": 1,
        "subject": "환자 데이터 분석",
        "keywords": [
        ],
        "explanation": [
        ],
        "result": ["코드", "데이터 분석 보고서", "데이터 분석 발표 동영상"],
        "objects": [11, 12, 14, 20, 21],
        "evaluation_method": {
          "auto": true,
          "online": true,
          "offline": false
        },
        "evaluation_standard": [
        ],
        "quiz": [
        ]
      },
      {
        "id": 2,
        "subject": "No Show 예측 모델 개발",
        "keywords": [
        ],
        "explanation": [
        ],
        "result": ["코드", "모델링 결과 발표 동영상"],
        "objects": [23, 151],
        "evaluation_method": {
          "auto": true,
          "online": true,
          "offline": false
        },
        "evaluation_standard": [
        ],
        "quiz": [
        ]
      }
    ]
  }],
 ```
하나의 프로젝트는 여러 개의 level들로 구성되고, 해당 목차에서는 하나의 레벨에 포함되어야 할 항목들을 기술한다. <br>
즉 `Levels`는 여러 개의 level로 이루어진 하나의 객체이다.

### 2.1 level
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `int` | `필수` |

해당 레벨을 `int`형 변수로 입력한다. 1 ~ 5까지의 정수만 입력할 수 있다.

```json
"level": 2
```
프로젝트 2의 경우 적정 level이 2임으로 int형 2를 입력한다. 

### 2.2 missions
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `필수` |

해당 레벨을 구성하는 미션들에 대한 정보를 작성한다.<br>
`missions`는 여러 개의 미션을 각각의 원소로 하는 객체 배열이다. 

#### 2.2.1 id
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `int` | `필수` |

한 레벨 안에 존재하는 여러 개의 미션을 구분하기 위해 각 미션의 고유 번호를 입력한다.

```json
"id": 1
```

#### 2.2.2 subject
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `필수` |

미션의 이름을 입력한다.

```json
"briefing": "환자 데이터 분석"
```

#### 2.2.3 keywords
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

미션을 수행하면서 참고할 수 있는 기술들을 배열로 기술한다. 

```json
"keywords": ["NumPy", "Pandas", "matplotlib", "seaborn", "data_analysis"]
```

#### 2.2.4 explanation
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

미션에 대한 설명을 기입한다.<br>
각각의 문장을 string타입으로 된 배열에 기입한다.<br>
학생들은 미션에 대한 설명을 보고 어떻게 미션을 진행해야 하는지 파악할 수 있다. 
```json
 "explanation": [
          "환자 데이터를 읽어오고 데이터를 전처리한다.",
          "이 때, 데이터에 존재하는 오타를 수정하고 데이터를 학습을 위한 데이터 타입으로 변환한다.",
          "필요하다면 학습을 위해 새로운 데이터를 생성해도 된다.",
          "이 후 데이터들을 분석 분석한 내용을 토대로 보고서를 작성하고 데이터 분석에 관한 발표 동영상을 만들어라"
        ]
```

#### 2.2.5 result

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `string` | `필수` |

미션이 종료되고 어떤 결과가 나와야 하는지 서술한다. `result`항목을 통해 학생들은 자신이 미션에서 어떤 결과물을 산출해야 하는지 명확하게 알 수 있다.

```json
"result": ["데이터 분석 보고서", "데이터 분석 발표 동영상"]
```

예를 들어, 해당 미션이 종료되고 나면 학생은 데이터 분석 보고서와 데이터 분석 발표 동영상을 제출해야 한다. 

#### 2.2.6 progress
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

미션을 어떤 방식으로 결정할 지 `option`의 항목 중에 선택한다. 
```json
"progress": {

            "option": [
                "self_learning",
                "peer_learning",
                "lecture"
            ],
	    "select": 0,
	    
        }
```

- `option` : 'string 배열'로 가능한 프로젝트 진행 옵션들을 나열한다. 
	- self_learning : 혼자서도 학습 리소스를 찾아가면서 학습이 가능한 콘텐츠 혹은 미션
	- peer_learning : 팀 콘텐츠의 경우 개인이 아니라 학습자들이 분담 또는 전체가 학습을 해야 진행이 가능해지는 콘텐츠 혹은 미션
	- lecture : 강의 형식으로 진행되는 미션
- `select` : 가능한 `option`중 해당 프로젝트가 진행 방식으로 선택한 option의 index를 기입한다. 

현재 `option`의 0번 index인 self_learning이 선택되었기 때문에 해당 미션은 self_learning 방식으로 진행된다. 

#### 2.2.7 objects


| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `int` | `필수` |

[PSI역량모델 - AI](https://drive.google.com/file/d/1t6cxIyztiAzTSFFtg-cF-Fmy8SBBntwT/view?usp=sharing)를 참고하여 해당 미션을 수행하고 난 후에 학생이 경험할 것으로 기대되는 항목 번호를 int형 배열에 집어 넣는다. 

```json
"objects": [11, 12, 14, 20, 21],
```

![image](https://user-images.githubusercontent.com/68315073/115672020-1482e580-a386-11eb-8a80-6c6d36acf576.png)<>
예를 들어, 해당 미션을 수행한 학생은 수집된 데이터의 속성을 결정하고 관련 내용을 정리할 수 있으며 수집된 데이터에서 잘못된 데이터를 찾아 수정 삭제할 수 있다.


#### 2.2.8 evlauation method

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `필수` |

해당 미션이 평가 방식으로 진행되는지 기입한다.<br>
하나의 미션은 3가지 평가 방식을 각각 선택적으로 적용할 수 있으며, 각각의 평가 방식은 `boolean`타입으로 기입한다. 

```json
"evaluation_method":{
                "auto":true,
                "online":true,
                "offline":false
            }
```

- `auto` : 자동 평가 방식
- `online` : 온라인 평가
- `offline` : 오프라인 평가

따라서 해당 미션은 자동 평가와 온라인 평가만 진행될 뿐, 오프라인 평가는 진행되지 않는다. 

#### 2.2.9 evaluation standard

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `필수` |

해당 미션을 모두 수행하고 미션을 평가하는 과정에서 어떤 기준으로 해당 미션을 평가해야할지 서술한다.<br>
`evaluation standard`는 여러 개의 평가 기준으로 이루어진 하나의 객체이다. 하나의 객체는 `item`, `class`, `type`, `option`으로 구성된다. <br>
또한 미션을 평가하는 방법(check box, radio button, 주관식 평가)도 `type`항목을 통해 입력 받는 방법을 선택함으로써 결정할 수 있다. 
<br>__해당 기준은 미션을 수행하는 학생에게는 공개되지 않으며, 이후에 미션을 평가할 멘토 혹은 동료에게만 공개됨__

```json
"evaluation_standard": [{
                    "item": "구글드라이브에 저장했는가?",
                    "class": "Data Store",
                    "tag": "input",
                    "type": "radio",
                    "option": [
                        "예",
                        "아니오"
                    ]
                },
                {
                    "item": "try except의 사용으로 데이터 엑세스 에러에 대처했는가?",
                    "class": "Data Store",
                    "type": "radio",
                    "option": [
                        "예",
                        "아니오"
                    ]
                },
                {
                    "item": "오타를 고쳤는가?",
                    "class": "Data Explore & Preprocess",
                    "type": "radio",
                    "option": [
                        "예",
                        "아니오"
                    ]
                }
	]
```

- `item` : 미션을 평가하는 기준이다. 'string 변수'로 입력한다.
- `class` : 해당 평가 기준으로 피평가자의 어떤 역량을 측정할 수 있는지 서술한다. 'string 변수'로 입력한다. 
- `type` : 평가자가 해당 미션을 평가하는 방법을 결정한다. 아래의 3가지 옵션 중에 결정하여 `type`에 기입한다. 
	- `radio` : 여러 개의 옵션 중 하나의 선택지만 선택할 수 있다. 
	- `check_box` : 여러 개의 옵션 중 다수의 선택지를 고를 수 있다. 
	- `text` : 주관식 평가를 위해 text형식으로 평가를 입력 받을 때 선택한다. 
- `option` : 만약 `type`에서 `radio` 혹은 `check_box`를 선택했다면, 선택할 수 있는 옵션들을 'string 배열'로 입력한다. 

#### 2.2.10 quiz


| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `선택` |

학생은 미션을 제출한 후 `quiz`를 수행함으로써 자신들이 미션을 제대로 수행했는지 평가받을 수 있다.<br>
`quiz`는 객체 배열으로써 하나의 `quiz`객체에는 학생이 '해당 미션을 통해 학습을 제대로 수행했는지'를 확인할 수 있는 질문을 기입한다. <br>
`quiz`는 미션마다 `optional`하게 들어갈 수 있다. 즉, `quiz`가 있는 미션도 있고 `quiz`가 없는 미션도 존재한다.<br>
`quiz`는 질문(`question`)과 그 질문이 속해 있는 학습분야(`class`) 그리고 답변(`answer`)으로 구성된다. 

```json
"quiz": [{
                    "class": "Data Explore & Preprocess",
                    "item": "판다스 데이터 프레임을 간단하게 요약해서 보여주며, 주로 데이터 타입을 확인할 때 사용하는 메소드는?",
                    "answer": "info() (sample(), describe()을 적었을 경우 점수 반만 부여)",
                },
                {
                    "class": "Data Explore & Preprocess",
                    "item": "열에 어떤 데이터들이 있는지 확인해 보고 싶을 때 사용하는 메소드는?",
                    "answer": "set(), unique() (둘중 하나만 적어도 정답)",
                },
                {
                    "class": "Data Analysis",
                    "item": "판다스 데이터의 개수를 세기 위해서 사용하는 메소드, 예를 들어 no show의 yes와 no의 개수를 세기위해서 어떤 메소드를 사용해야 하는가?",
                    "answer": "size()",
                }
	]
```
- `class` : 질문 분야를 기입한다. 즉, `item`문항이 어떤 분야의 지식을 물어보는 것인지 작성한다. 
- `item` : 질문의 내용을 작성한다.
- `answer` : 해당 문제에 대한 정답, 학생이 문제를 풀고난 후 학생에게 공개하거나 멘토에게만 공개한다.

## 3. Reference
```json
"Reference": {
    "answer_code": "https://github.com/edu10make/Project-X_/blob/main/Project1-Medical%20Analysis/001_Medical%20No%20Show/001_Medical%20No%20Show.ipynb",

    "evaluation_guide": "link",

    "forum" : "link",

    "data": [{
        "file_name": "brain.jpg",
        "explanation": "정상 뇌 사진 100 장, 뇌출혈 뇌 사진 100 장으로 이루어진 이미지 파일"
      },
      {
        "file_name": "labels.csv",
        "explanation": "뇌출혈 여부 데이터"
      }
    ],

    "resource": [{
        "subject": "Convolution Neural Network(합성곱 신경망)에 대한 일반적인 이해 (위키피디아)",
        "link": "https://en.wikipedia.org/wiki/Convolution_neural_network"
      },
      {
        "subject": "scikit-learn 에 대한 일반적인 이해 (위키피디아)",
        "link": "https://en.wikipedia.org/wiki/Scikit-learn"
      }
    ]
  }
```
프로젝트 전체적으로 참고할 수 있는 자료들을 작성한다. <br>
3.1 `answer code`, 3.2 `evaluation_guide`, 3.3 `forum` 3.4 `data`, 3.5 `resource` 다섯 가지 항목으로 구성된다.

### 3.1 answer code link

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

프로젝트의 예제 코드 링크가 'string 변수'로 들어간다. 

```json
"answer_code": "https://github.com/edu10make/Project-X_/blob/main/Project1-Medical%20Analysis/001_Medical%20No%20Show/001_Medical%20No%20Show.ipynb"
```

### 3.2 evaluation_guide

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

프로젝트의 평가 가이드에 대한 'string 변수'로 들어간다. 

```json
"evaluation_guide": "link",
```

### 3.3 forum

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

프로젝트 포럼에 대한 링크가 'string 변수'로 들어간다. 

```json
"forum" : "link",
```

### 3.4 data

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `선택` |

프로젝트에 사용되는 데이터 파일들이 있다면, 그 데이터 파일들에 대한 설명을 작성한다.<br>
`data`는 객체 배열이며 각각의 객체는 프로젝트에 사용되는 데이터 파일 하나 하나이다. 

```json
"data": [{
            "file_name": "Medical_no_show.csv",
            "explanation": "브라질 환자들의 병원 예약 정보와 예약 취소 여부에 대한 데이터"
        }]
```

- `file name` : 데이터 파일의 이름
- `explanation` : 해당 데이터 파일에 대한 설명

### 3.5 resource


| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `선택` |

학생들이 프로젝트를 수행하면서 참고할 수 있는 자료들을 기입한다. <br>
`resource`는 객체 배열으로써 각각의 객체는 하나의 참고자료의 링크와 그에 대한 설명이 들어간다. 

```json
"resource": [{
                "item": "Convolution Neural Network(합성곱 신경망)에 대한 일반적인 이해 (위키피디아)",
                "link": "https://en.wikipedia.org/wiki/Convolution_neural_network"
            },
            {
                "item": "scikit-learn 에 대한 일반적인 이해 (위키피디아)",
                "link": "https://en.wikipedia.org/wiki/Scikit-learn"
            }
        ]
```

- `item` : 참고 자료에 대한 설명
- `link` : 참고 자료 


