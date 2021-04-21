# PBL Contents Standard Format
![Project_w](https://user-images.githubusercontent.com/47736525/115352595-7f9bb300-a1f2-11eb-94ec-7ad24ca4cce7.png)



## 0. Operation
프로젝트 운영을 위한 전반적인 내용을 결정한다.<br>
해당 챕터에서 결정해야 할 내용은 다음과 같다.
- `period` : 학습 기간
- `progress` : 학습 진행 방식
- `matching` : 평가자 매칭 방식

### 0.1 period
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트의 시작 시기, 끝나는 시기와 기간에 대한 옵션을 지정한다.
```json
"period": {
            "self_paced":true,
            "start": 2021050313,
            "finish": 202105023
        }
```
- `self_paced` : `boolean`변수가 인자로 들어가며 프로젝트가 'self-paced'방식으로 진행되는지 여부를 결정한다. 만약 `false`라면 fixed timeline으로 프로젝트가 진행된다. 
- `start` : 프로젝트의 예정 시작일 및 예정 시작 시간을 입력한다. 10자리 `int`형 변수이며 '연도(4자리)' + '월(2자리)' + '일(2자리)' + '시간(2자리)'로 구성된다.
- `finish` : 프로젝트의 예정 종료일 및 예정 종료 시간을 입력한다. 10자리 `int`형 변수이며 '연도(4자리)' + '월(2자리)' + '일(2자리)' + '시간(2자리)'로 구성된다.

### 0.2 progress
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트의 진행 방식을 결정한다. 
```json
"progress": {
            "select": "peer_learning",
            "option": [
                "self_learning",
                "peer_learning",
                "lecture"
            ]
        }
```

- `option` : 'string 배열'로 가능한 프로젝트 진행 옵션들을 나열한다. 
- `select` : 가능한 `option`중 해당 프로젝트가 진행 방식으로 선택한 option을 기입한다. 

### 0.3 matching
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `객체` | `필수` |

프로젝트 동료 평가자 방식을 결정한다. 
```json
"matching": {
           "select": "random",
           "option": [
               "random",
               "designate",
               "select"
            ]

       }
```

- `option` : 'string 배열'로 가능한 프로젝트 진행 옵션들을 나열한다. 
- `select` : 가능한 `option`중 해당 프로젝트가 동료 평가자 선택 방식으로 선택한 option을 기입한다. 


## 1. Basic
프로젝트의 id, 주제, 목적 등 프로젝트의 기본적인 정보에 대해 기입한다.<br>
또한 '프로젝트'에 대한 정보이기에 특정 Level이나 mission에 국한되는 내용이 아닌, 프로젝트 전반적인 정보를 기입한다는 점에 주의한다. 

### 1.1 id
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `int` | `필수` |

여러 개의 프로젝트를 구분하기 위해 각 프로젝트의 고유 번호를 입력한다.<br>
프로젝트의 고유번호는 4자리 숫자로 구성되며, 서로 다른 프로젝트는 동일한 고유번호를 가질 수 없다. 


### 1.2 title 
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `필수` |

프로젝트의 이름을 입력한다. 프로젝트 이름은 한 줄 이내의 핵심적인 내용을 담아, 제목만 보고도 프로젝트를 대략적으로 파악할 수 있도록 한다.

### 1.3 attribute

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `string` | `필수` |

프로젝트의 적정 레벨을 <span style="color:red">'string 배열'</span>로 입력한다. `detailed levels`는 PSI에서 제공하는 'tech skill 역량명세서 - 수준 구분'을 참고한다.

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

프로젝트의 목적을 입력한다. 

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
            "knowledge_skill": ["Python", "Jupyter_Notebook", "TensorFlow", "NumPy", "Pandas", "scikit-learn", "CNN"],

            "tech_skills": [{
                    "class": "Data분석(데이터 처리 역량)",
                    "experience": ["수집된 데이터를 특정 포맷으로 가공하고 정렬할 수 있다",
                        "수집된 데이터에서 잘못된 데이터를 찾아 수정 삭제할 수 있다.",
                        "수집된 데이터에서 불필요한 차원을 제거할 수 있다."
                    ],
                    "difficulty": 2
                },
                {
                    "class": "Data분석(데이터 추론 역량)",
                    "experience": ["모집단으로부터 추출된 표본을 바탕으로 통계적 추론이 가능하다.",
                        "대용량의 자료에서 데이터의 관계, 패턴, 규칙을 탐색하고 활용할 수 있다.",
                        "모델링을 위한 성능 평가 지표를 정의하고 구현할 수 있다."
                    ],
                    "difficulty": 3
                }
            ],
            "soft_skills": [
	        {
                    "class": "비판적 사고",
                    "keyword": "핵심 정보 파악",
                    "action": "비판적 사고/핵심 정보 파악/다양한 정보나 아이디어를 무작정 수용하지않고 업무에 도움이 되는 것과 그렇지 않은 것을 구별할 수 있다."
                },
                {
                    "class": "비판적 사고",
                    "keyword": "근본 원인 규명",
                    "action": "비판적 사고/근본 원인 규명/문제 발생 시, 문제 해결을 위해 근본 원인을 해결할 수 있다."
                }
            ]
        }
```

- `knowledge skills` : 프로젝트를 수행하는데 사용할 기술들을 간략하게 'string 배열'로 기술한다. 학생들은 `knowlege skills`을 미션을 수행할 때 키워드로 활용할 수 있고, 또한 `knowlege skills`를 통해 해당 프로젝트에서 어떠한 기술들을 다루는지 대략적으로 파악할 수 있다.  
- `tech skills` : 여러 개의 'tech skill'로 이루어진 객체 배열이다. 하나의 'tech skill'은 PSI에서 제공하는 'tech skill 역량명세서 - 경험리스트'의 항목으로 구성되어야 한다. 따라서 하나의 'tech skill'은 'tech skill 역량명세서 - 경험리스트'의 형식에 따라 아래와 같은 항목들을 포함한다. 

	- `class` : 'tech skill 역량명세서 - 경험리스트' 중 '카테고리'에 해당하는 내용을 'string 변수'로 입력한다.
	- `experience` : 'tech skill 역량명세서 - 경험리스트' 중 '경험'에 해당하는 내용을 'string 변수'로 입력한다.
	- `difficulty` : 'tech skill 역량명세서 - 경험리스트' 중 '난이도'에 해당하는 내용을 'string 변수'로 입력한다.

- `soft skills` : 여러 개의 'soft skill'로 이루어진 객체 배열이다. 하나의 'soft skill'은 PSI에서 제공하는 'soft skill 역량명세서 - 역량별 행동지표'의 항목으로 구성되어야 한다. 따라서 하나의 'soft skill'은 'soft skill 역량명세서 - 역량별 행동지표'의 형식에 따라 아래와 같은 항목들을 포함한다. 

	- `class` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '역량명'에 해당하는 내용을 'string 변수'로 입력한다.
	- `key word` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '키워드'에 해당하는 내용을 'string 변수'로 입력한다.
	- `action` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '행동 지표'에 해당하는 내용을 'string 변수'로 입력한다.



## 2. Levels
하나의 프로젝트는 여러 개의 level들로 구성되고, 해당 목차에서는 하나의 레벨에 포함되어야 할 항목들을 기술한다. <br>
즉 `Levels`는 여러 개의 level로 이루어진 하나의 객체이다.

### 2.1 appropriate_level
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `int` | `필수` |

해당 레벨을`int`형 변수로 입력한다. 1 ~ 5까지의 정수만 입력할 수 있다.

```json
"appropriate_level": 2
```

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

#### 2.2.2 breifing
| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `필수` |

미션의 내용을 간략하게 브리핑하여 진행하는 학생들로 하여금 해당 미션의 내용을 파악할 수 있도록 한다.<br>
미션에서 수행할 내용을 단어나, 문장 단위로 간략하게 기술한다. 

```json
"briefing": "환자 데이터를 읽어오고 데이터를 전처리하고 분석하라, 분석한 내용을 토대로 보고서를 작성하고 데이터 분석에 관한 발표 동영상을 만들어라"
```

#### 2.2.3 kewords


| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

미션을 수행하면서 참고할 수 있는 기술들을 배열로 기술한다. 

```json
"keywords": ["NumPy", "Pandas", "matplotlib", "seaborn", "data_analysis"]
```



#### 2.2.4 mission object


| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `객체` | `필수` |

1) 미션의 목표, 2) 해당 목표의 분류와 3) 해당 목표가 필수적인지 선택적인지 여부를 기입한다.

```json
"objects": [{
                        "class": "Data Store",
                        "item": "구글드라이브에 환자 진료 데이터를 저장하고 구글 드라이브를 구글 Collaboratory 에서 사용할 있도록 마운트하라",
                        "optional": false
                    },
                    {
                        "class": "Data Explore & Preprocess",
                        "item": "주어진 환자 진료 데이터를 분석하기 위해 전처리를 진행하라",
                        "optional": false
                    },
                    {
                        "class": "Data Analysis",
                        "item": "전처리를 완료한 환자 데이터를 분석하라",
                        "optional": false
                    },
                    {
                        "class": "Data Explore & Preprocess",
                        "item": " 데이터에는 오타가 존재한다. 오타를 고쳐라.",
                        "optional": true
                    },
                    {
                        "class": "Data Explore & Preprocess",
                        "item": "학습을 위한 데이터 타입으로 변환하라. ",
                        "optional": false
                    }
	]
```

- `classs` : 미션의 목표를 포함하는 분류 기준을 입력한다. 
- `item` : 미션의 목표를 'string 변수'로 입력한다. 
- `optional` : 입력한 세부 목적이 optional한 것인지 혹은 필수적인 것인지 `boolean` type으로 입력한다. 만약 세부 목적이 'optional'하다면 `true`를 입력한다. 

#### 2.2.5 result

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `string` | `필수` |

미션이 종료되고 어떤 결과가 나와야 하는지 서술한다. `result`항목을 통해 학생들은 자신이 미션에서 어떤 결과물을 산출해야 하는지 명확하게 알 수 있다.

```json
"result": ["데이터 분석 보고서", "데이터 분석 발표 동영상"]
```

#### 2.2.6 evlauation method

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


#### 2.2.7 evaluation standard

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

#### 2.2.8 quiz


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
		    "type": "text"
                },
                {
                    "class": "Data Explore & Preprocess",
                    "item": "열에 어떤 데이터들이 있는지 확인해 보고 싶을 때 사용하는 메소드는?",
                    "answer": "set(), unique() (둘중 하나만 적어도 정답)",
		    "type": "text"
                },
                {
                    "class": "Data Analysis",
                    "item": "판다스 데이터의 개수를 세기 위해서 사용하는 메소드, 예를 들어 no show의 yes와 no의 개수를 세기위해서 어떤 메소드를 사용해야 하는가?",
                    "answer": "size()",
		    "type": "text"
                }
	]
```
- `class` : 질문 분야를 기입한다. 즉, `item`문항이 어떤 분야의 지식을 물어보는 것인지 작성한다. 
- `item` : 질문의 내용을 작성한다.
- `answer` : 해당 문제에 대한 정답, 학생이 문제를 풀고난 후 학생에게 공개하거나 멘토에게만 공개한다.
- `type` : 평가자가 해당 미션을 평가하는 방법을 결정한다. 아래의 3가지 옵션 중에 결정하여 `type`에 기입한다. 
	- `radio` : 여러 개의 옵션 중 하나의 선택지만 선택할 수 있다. 
	- `check_box` : 여러 개의 옵션 중 다수의 선택지를 고를 수 있다. 
	- `text` : 주관식 평가를 위해 text형식으로 평가를 입력 받을 때 선택한다. 
- `option` : 만약 `type`에서 `radio` 혹은 `check_box`를 선택했다면, 선택할 수 있는 옵션들을 'string 배열'로 입력한다. 

## 3. Reference
프로젝트 전체적으로 참고할 수 있는 자료들을 작성한다. <br>
3.1 `answer code link`, 3.2 `data`, 3.3 `resource` 세 개의 항목으로 구성된다.

### 3.1 answer code link

| 개수 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `단일` | `string` | `선택` |

프로젝트의 예제 코드 링크가 'string 변수'로 들어간다. 

```json
"answer_code_link": "https://github.com/edu10make/Project-X_/blob/main/Project1-Medical%20Analysis/001_Medical%20No%20Show/001_Medical%20No%20Show.ipynb"
```

### 3.2 data

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

### 3.3 resource


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

