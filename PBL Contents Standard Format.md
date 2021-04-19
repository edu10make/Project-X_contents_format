# PBL Contents Standard Format

![PBL Contents Standard Format_map](https://user-images.githubusercontent.com/47736525/115193729-83163800-a127-11eb-8903-923be6f22a25.png)

## 1. Project
프로젝트 전체적인 내용에 대해 서술한다.

### id
| 형식 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `변수` | `int` | `필수` |

여러 개의 프로젝트를 구분하기 위해 각 프로젝트의 고유 번호를 입력한다.
프로젝트의 고유번호는 4자리 숫자로 구성되며, 서로 다른 프로젝트는 동일한 고유번호를 가질 수 없다. 


### title 
| 형식 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `변수` | `string` | `필수` |

프로젝트의 이름을 입력한다. 프로젝트 이름은 한 줄 이내의 핵심적인 내용을 담아, 제목만 보고도 프로젝트를 대략적으로 파악할 수 있도록 한다.

### levels

- `appropriate level` : 프로젝트의 적정 레벨을 'int 변수'로 입력한다. `appropriate level`를 통해 학생들은 해당 프로젝트의 난이도를 가늠할 수 있다.
- `detailed levels` : 프로젝트의 적정 레벨을 <span style="color:red">'string 배열'</span>로 입력한다. `detailed levels`는 PSI에서 제공하는 'tech skill 역량명세서 - 수준 구분'을 참고한다.

### objects
```JSON
"objects": {
            "main_object": "프로젝트 메인 주제",
            "detailed_object": ["데이터 저장 및 준비 등 데이터 전처리 과정을 경험할 수 있다.",
                "데이터를 자세하게 분석하고 해당 내용에 대해 설명할 수 있다.",
                "모델링을 경험해볼 수 있다."
            ]
        },
```

- `main object` : 프로젝트의 중추적인 목표를 'string 변수'로 입력한다. `main object`에는 프로젝트가 해결하고자 하는 문제나 프로젝트가 끝났을 때 학생들이 만들어 낼 결과물을 기술한다.
- `detailed objects` : 프로젝트의 세부적인 목표들을 'string 배열'로 입력한다. `main object`를 달성하기 위해 수행할 세부적인 목표들을 기술한다.

### skills

- `knowledge skills` : 프로젝트를 수행하는데 사용할 기술들을 간략하게 'string 배열'로 기술한다. 학생들은 `knowlege skills`을 미션을 수행할 때 키워드로 활용할 수 있고, 또한 `knowlege skills`를 통해 해당 프로젝트에서 어떠한 기술들을 다루는지 대략적으로 파악할 수 있다.  
- `tech skills` : 여러 개의 'tech skill'로 이루어진 객체 배열이다. 하나의 'tech skill'은 PSI에서 제공하는 'tech skill 역량명세서 - 경험리스트'의 항목으로 구성되어야 한다. 따라서  하나의 'tech skill'은 'tech skill 역량명세서 - 경험리스트'의 형식에 따라 아래와 같은 항목들을 포함한다. 

	- `class` : 'tech skill 역량명세서 - 경험리스트' 중 '카테고리'에 해당하는 내용을 'string 변수'로 입력한다.
	- `experience` : 'tech skill 역량명세서 - 경험리스트' 중 '경험'에 해당하는 내용을 'string 변수'로 입력한다.
	- `difficulty` : 'tech skill 역량명세서 - 경험리스트' 중 '난이도'에 해당하는 내용을 'string 변수'로 입력한다.

- soft skills : 여러 개의 'soft skill'로 이루어진 객체 배열이다. 하나의 'soft skill'은 PSI에서 제공하는 'soft skill 역량명세서 - 역량별 행동지표'의 항목으로 구성되어야 한다. 따라서 하나의 'soft skill'은 'soft skill 역량명세서 - 역량별 행동지표'의 형식에 따라 아래와 같은 항목들을 포함한다. 

	- `class` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '역량명'에 해당하는 내용을 'string 변수'로 입력한다.
	- `key word` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '키워드'에 해당하는 내용을 'string 변수'로 입력한다.
	- `action` : 'soft skill 역량명세서 - 역량별 행동지표' 중 '행동 지표'에 해당하는 내용을 'string 변수'로 입력한다.

## 2. Mission
하나의 프로젝트는 여러 개의 미션으로 구성되고, 해당 목차에서는 각 미션에 포함되어야 할 내용들을 기술한다.

### mission id
| 형식 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `변수` | `int` | `필수` |

한 프로젝트 안에서 여러 개의 미션을 구분하기 위해 각 미션의 고유 번호를 입력한다.

### breifing
| 형식 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `변수` | `string` | `필수` |

미션에서 수행할 내용을 단어나, 문장 단위로 간략하게 기술한다. 

### kewords
| 형식 | 변수형 | 필수 여부 |
|:---:|:---:|:----:|
| `배열` | `string` | `선택` |

미션을 수행하면서 참고할 수 있는 기술들을 배열로 기술한다. 

### mission object

- main objects
- detailed objects

	- item
	- optional

### result

### evaluation standard

- item
- class
- tag
- type
- option

### quiz

- class
- question
- answer

## 3. Reference

### answer code link

### data

- file name
- explanation

### resource

- item
- link



*XMind - Trial Version*
