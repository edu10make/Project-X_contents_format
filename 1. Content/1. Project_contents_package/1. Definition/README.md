# 1. Definition : 프로젝트 정의

### 개요

프로젝트의 id, 주제, 목적 등 프로젝트의 기본적인 정보를 기입함으로써 해당 프로젝트가 어떠한 프로젝트인지 정의합니다. <br><br>
특정 미션에 국한되는 정보가 아닌 프로젝트 전반적인 정보를 기입합니다.


### 목차

![슬라이드1](https://user-images.githubusercontent.com/68315073/116506676-b19acc80-a8f8-11eb-9339-092d257d9f21.PNG)

<br><br>
## 1.1 id : 고유번호

프로젝트를 구분하기 위해 각 프로젝트의 `id(고유 번호)`입니다. </br></br>
프로젝트의 `id(고유번호)`는 4자리 `숫자`로 구성되며, 서로 다른 프로젝트는 동일한 `id`를 가질 수 없습니다.</br></br>
프로젝트 `id(고유번호)`는 **Project-X의 프로젝트 순서 규칙**에 따라 각 프로젝트에게 할당됩니다. </br></br>
프로젝트 `id(고유번호)`는 프로젝트의 분야 혹은 난이도와 관련이 없습니다. 

### 예시

```json
"id" : 10025
```

> 해당 프로젝트의 `id`는 '10025'입니다. 

<br><br>
## 1.2 title : 제목

프로젝트의 `제목`입니다. </br></br>
프로젝트 전체를 함축할 수 있는 문장이나 키워드를 입력합니다. </br></br>
학생들은 수행할 프로젝트를 결정할 때, 프로젝트 `제목`을 통해 프로젝트의 대략적인 내용을 파악할 수 있습니다. 

### 예시

```json
"title": "미터기 읽기"
```

> 해당 프로젝트의 `제목`은 '미터기 읽기'입니다. 

<br><br>
## 1.3 estimation_time : 예상 소요시간

프로젝트를 수행하는데 예상되는 소요시간입니다. </br></br>
프로젝트 `예상 소요시간`은 `숫자`로 입력하며 `예상 소요시간`의 단위는 '일'입니다. </br></br>
실제로 해당 프로젝트를 학생들에게 학습시킬 때, `예상 소요시간`을 참고하여 프로젝트 수행 기간을 설정할 수 있습니다. 

### 예시

```json
"estimated_time":50
```

> 해당 프로젝트를 수행하는데 예상되는 소요 시간은 '50일'입니다. 

<br><br>
## 1.4 class : 분야 및 지식 수준

하나의 프로젝트는 복합적인 `분야`의 기술을 요구합니다. 예를 들어, '주어진 데이터를 시각화하여 Web화면에 출력'하는 미션은 `Front-end`분야의 지식과 `데이터 분석`분야의 지식을 요구합니다. 또한 각 `분야`별로 요구하는 수준이 다릅니다. </br></br>
따라서 프로젝트가 요구하는 `지식 수준`을 정의하기 위해서는 프로젝트가 지식을 요구하는 `분야`를 먼저 설정하고, 각 `분야`에서 요구하는 `지식 수준`을 정의해야 합니다. 

 프로젝트의 `분야`와 `지식 수준`을 `분야/지식 수준`의 형식으로 `문자열`로 입력합니다. </br></br>
 입력하는 프로젝트의 `분야`와 `지식 수준`은 PSI에서 제공하는 [**'tech skill 역량명세서 - 수준 구분'**](https://drive.google.com/file/d/1vOcfcDQvWGrcwZy681pAUfqYj5tk9NED/view?usp=sharing)을 참고하여 작성합니다. </br></br>
 해당 항목을 통해 학생들은 프로젝트를 시작하기 전, 프로젝트가 어떤 `분야`에 속해있으며 프로젝트에서 요구하는 `지식 수준`은 어느정도인지 파악할 수 있습니다. 

### PSI 수준 구분 - Front end & Back end

| 수준 |                          Front-end                           |                           Back-end                           |
| :--: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| Edu1 | UI구성 관련 일반지식을 이해하는 수준,하나의 화면 (또는 두개까지)안에서 해결할 수 있는 수준,기본적인 개발 환경을 이용할 수 있는 수준 | 프로그램 언어에 대한 기초 이론, 문법을 학습 하고 이해하는 수준으로, 코드를 작성(CRUD)하고 적절한 결과를 출력 하거나 기능이 동작 하도록 할 수 있음 |
| Edu2 |          Front-end 분야의 기초 지식을 이해하는 수준          |     여러 화면을 서로 연결하는 업무를 수행할 수 있는 수준     |
| Edu3 | "라이브러리의 종류를 알고, 검색하여 활용할 수 있는 수준, 튜닝/응용을 시도하는 수준 | 구현하고자 하는 또는 문제 해결에 필요한 정보와 지식이 어디에 있는지 알고 찾을 수 있는 수준 (know how/where)으로 Pure 프로그래밍을 통해 서버/클라이언트 프로그램 구현이 가능 |
| Edu4 | "단위 업무를 수행하기 위해 필요한 지식을 갖춘 수준, 2개 이상 소스를 조합하거나, 검색을 통해 응용할 수 있는 수준(자기 코드 개선, 성능 개선 가능) | 업무 도메인에 필요한 프로젝트의 생성(시작)과 개발이 가능한 수준으로,  다수의 프레임워크 기반의 프로젝트 구성과 연동 개발이 가능 |
| Edu5 | "Front-end 분야의 중급 전문 지식을 이해하는 수준, 전체 개발 프로세스 내에서 FE영역의 개발을 경험해 본 수준 | 고가용성, 확장성, 유연성 등 안정적 서비스 지원을 위한 백엔드 아키텍쳐에 대한 설계가 가능 하고 구현을 할 수 있는 수준으로, FE, BE, Data, Infrastructure 에 대한 전체 구조 설계와 요건 정의 등이 가능함 |
| Edu6 | Web Front-end 분야의 고급 전문 지식을 이해하는 수준 어느 정도의 현업 경험이 있거나, 창업 가능한 수준 | 각 업무 도메인 별 전문 지식을 이해하고 있으며, 서비스를 구성 하는 모든 항목들에 대해 분석/설계/정의/구축이 가능한 수준 |

### PSI 수준 구분 - AI

<table>
<thead>
  <tr>
    <th>수준</th>
    <th>Data분석</th>
    <th>AI모델개발</th>
    <th>AIOps</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Edu1</td>
    <td></td>
    <td>AI 모델 개발을 위해 필요한 지식/스킬 중 기초 지식</td>
    <td></td>
  </tr>
  <tr>
    <td>Edu2</td>
    <td>정형/비정형 데이터에 대한 지식을 이해하고, 필요한 데이터를 직접 탐색하여 수집, 가공할 수 있는 수준</td>
    <td colspan="2">AI 모델 개발을 위해 필요한 지식/스킬 중 상대적 난이도가 있는 지식</td>
  </tr>
  <tr>
    <td>Edu3</td>
    <td>포맷 변경하여 저장하거나, 도구를 사용하여 데이터를 빠르게 수집하고 데이터 특성에 따라 가공할 수 있는 수준</td>
    <td colspan="2">End to End Task를 수행하지는 못하지만 특정 단위 Task를 수행할 수 있는 수준</td>
  </tr>
  <tr>
    <td>Edu4</td>
    <td>데이터를 보고 통계적 추론, 규칙 탐색 등을 할 수 있는 수준</td>
    <td colspan="2">공개되어 있는 코드를 활용하여 End to End Task를 수행할 수 있는 수준</td>
  </tr>
  <tr>
    <td>Edu5</td>
    <td></td>
    <td>공개되어 있는 코드를 응용/튜닝하여 결과를 향상시킬 수 있는 수준<br><br>여러 모델을 쌓아서 새로운 모델을 만들고 학습 시킬 수 있는 수준</td>
    <td>모델이 멈추지 않도록 파이프 설계, 고가용성 인식 등 전체 운용이 가능한 수준</td>
  </tr>
  <tr>
    <td>Edu6</td>
    <td></td>
    <td>실무 경험을 바탕으로 모델/시스템 최적화가 가능한 수준</td>
    <td></td>
  </tr>
</tbody>
</table>


### 예시 

 ```json
"class": [
        "AI-Data분석/Edu4",
        "AI-모델개발/Edu4",
        "AI-Ops/Edu4",
        "Back-end/Edu4"
    ]
 ```


> 해당 프로젝트에서 요구하는 `분야` 별 `지식 수준`은 다음과 같습니다.  


| 분야        | 지식 수준 |
| ----------- | --------- |
| AI-Data분석 | `Edu4`    |
| AI-모델개발 | `Edu4`    |
| AI-Ops      | `Edu4`    |
| Back-end    | `Edu4`    |


<br><br>
 ## 1.5 story : 프로젝트 스토리

프로젝트와 관련된 현실의 문제를 작성하거나 창작한 이야기를 작성합니다. </br></br>
`프로젝트 스토리`는 `문자열`로 작성합니다. </br></br>
프로젝트 스토리를 작성하는 이유는 다음과 같습니다.

- 프로젝트를 수행하는 학생들의 흥미를 높임
- 해당 프로젝트를 수행함으로써 현실에 존재하는 문제를 프로그래밍을 통해 어떻게 해결할 수 있는지 파악하게 함
- 실생활에 존재하는 문제를 해결함으로써 실무과 이론의 간극을 좁힘

### 예시

 ```json
"story": "IoT 전문회사인 MeasureWare 사의 기반서비스는 현장에 설치되어 사용중인 전통적인 방식의 계량기(통신기능이 탑재되지 않은 계량기)의 미터 값을 실시간으로 읽어서 디지털화하여 digital-twin 형태로 형상화한다. 또한 이렇게 형상화된 digital-twin 을 기반으로 실시간 감시, 실시간 작동, 리스크 관리 등 다양한 고객맞춤형 서비스를 제공하는 회사이다. 이 회사는 자신들이 관리하는 계량기에 카메라를 부착하여 HTTP 를 통해 1 시간 간격의 실시간 이미지를 가져오는 기능을 구현하였고 대상 계량기를 확대하고 있다."
 ```

> 해당 프로젝트의 스토리 : 
> IoT 전문회사인 MeasureWare 사의 기반서비스는 현장에 설치되어 사용중인 전통적인 방식의 계량기(통신기능이 탑재되지 않은 계량기)의 미터 값을 실시간으로 읽어서 디지털화하여 digital-twin 형태로 형상화한다. 또한 이렇게 형상화된 digital-twin 을 기반으로 실시간 감시, 실시간 작동, 리스크 관리 등 다양한 고객맞춤형 서비스를 제공하는 회사이다. 이 회사는 자신들이 관리하는 계량기에 카메라를 부착하여 HTTP 를 통해 1 시간 간격의 실시간 이미지를 가져오는 기능을 구현하였고 대상 계량기를 확대하고 있다.

<br><br>
 ## 1.6 object : 목표

프로젝트의 `목표`를 `문자열`로 작성합니다. </br></br>
프로젝트의 `목표`은 주요 목표인 `main_object`와 세부 목표인 `detailed_objects`로 구분하여 작성합니다.

 - `main_object`는 프로젝트 전체를 관통하는 하나의 목표입니다. 프로젝트가 해결하고자 하는 문제나 프로젝트가 끝났을 때 학생들이 만들어 낼 결과물을 기술합니다.
 - `detailed_objects`는 `main_object`를 달성하기 위한 프로젝트 세부 목표입니다.

### 예시

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

 > 해당 프로젝트의 `목표`는 다음과 같습니다. 

| 구분        | 내용                                                         |
| ----------- | ------------------------------------------------------------ |
| `주요 목표` | 수도 계량기의 숫자를 읽어서 웹서버에 보여주는 digital twin기능을 구현하라, 실시간 분석 및 액튜에이션 확장기능 개발 |
| `세부 목표` | 현장에 설치된 계량기의 이미지 데이터를 취득하라              |
| `세부 목표` | 클라우드 서비스를 이용하여 추출한 이미지에서 문자를 인식하라 |
| `세부 목표` | 머신러닝 알고리즘을 탐색하여 기반으로 사용할 알고리즘을 선택하라 |
| `세부 목표` | 수천 장 이미지를 갖고 각각의 사진에 레이블링을 어떻게 할 지 기술적으로 궁리하라 |
| `세부 목표` | 파이썬 툴을 사용하여 수천 장 이미지를 적절한 하나의 데이터 화일로 구성하라 |
| `세부 목표` | 몇 장의 표본에 대해 머신러닝 Training을 진행할지에 대한 판단기준 세워라 |
| `세부 목표` | 인식한 숫자를 웹서버에 표기하는 digital twin meter를 구현하라 |

<br><br>
## 1.7 skills : 필요 역량과 달성 역량

프로젝트와 관련된 역량입니다. </br></br>
모든 역량은 [프로젝트 역량 기준표](https://github.com/edu10make/Project-X_contents_format/blob/main/3.%20the%20rest/source/MagicEcole%20Skills%20List.md)를 보고 해당되는 역량의 `id`를 기입합니다.</br></br> 
예를 들어, 어떤 프로젝트를 수행하기 위해 필요한 역량이 "Data Base 기초"라면 [프로젝트 역량 기준표](https://github.com/edu10make/Project-X_contents_format/blob/main/3.%20the%20rest/source/MagicEcole%20Skills%20List.md)에서 "Data Base 기초"의 `id`가 '00001'인 것을 확인한 후 `require`에 '00001'을 기입합니다.</br></br> 
추후에 **역량 리스트의 확장**이 필요하다면 [프로젝트 역량 기준표](https://github.com/edu10make/Project-X_contents_format/blob/main/3.%20the%20rest/source/MagicEcole%20Skills%20List.md)를 업데이트한 이후 추가된 역량의 id를 기입합니다. </br></br> 
프로젝트 역량은 프로젝트를 '수행하기 위해 필요한 역량'과 프로젝트를 수행했을 때 '달성할 수 있는 역량'으로 구분하여 작성합니다.

- `require`에는 프로젝트를 수행하기 위해 필요한 역량을 작성합니다. 선수 프로젝트 등을 기입할 수 있습니다.
- `acqure`에는 프로젝트를 수행하고 나면 얻을 수 있는 역량입니다. 이 프로젝트를 통해 달성할 수 있는 학습 성과들을 기입합니다.

### 예시

```json
"skills": {
        "require": [ 00100, 00101, 00102, 00104],
        "acquire": [
            30100,
	    30102,
            30200,
            30300,
            30402
        ]
    }
```

> 프로젝트를 수행하기 위해 필요한 역량과 프로젝트 종료 후 얻을 수 있는 역량은 다음과 같습니다. 

**필요 역량**
구분| id | 역량 |
|--|--|--|
| Python Programming | 00100|Python Basic|
| Python Programming |00101|	Numpy|
| Python Programming |00102| Pandas|
| Python Programming |00104|	Jupyter Notebooks|

**달성 역량**
구분| id | 역량 |
|--|--|--|
| Neural Networks |30100| Understanding Neural Networks |
| Neural Networks|30102| Activation Function |
| Architectures|30200|CNN|
| Training|30300|Optimizers|
| Tools|30402|TensorFlow|

> 즉, 해당 프로젝트를 수행하기 이전 학생은 다른 프로젝트를 통해 'Python Basic', 'Numpy', 'Pandas', 'Jupyter Notebooks' 역량을 갖고있어야 하며, 이 프로젝트가 종료되면 'Understanding Neural Networks', 'Activation Function', 'CNN', 'Optimizers', 'TensorFlow' 총 5가지 역량을 달성할 수 있습니다. 

<br><br>
## 1.8 projects : 선수 프로젝트와 추천 프로젝트

해당 프로젝트를 수행하기 전에 필수적으로 수행해야 할 `선수 프로젝트`와 해당 프로젝트를 완수했을 떄 이어서 수행할만한 `추천 프로젝트`입니다.</br></br>
`선수 프로젝트`와 `추천 프로젝트`는 프로젝트 `id`를 `숫자`로 입력합니다. 

- `require` : 해당 프로젝트를 수행하기 전 필수적으로 수행해야 할 프로젝트 `id`
- `acqure` : 해당 프로젝트를 완수했다면 이어서 수행할만한 프로젝트 `id`

### 예시

```json
"projects": {
        "require": [ 653,3840,1596 ],
        "acquire": [ 214, 315, 8739, 9498 ]
    }
```
> 해당 예제는 다음과 같은 연관 프로젝트를 갖습니다.  
 
**선수 프로젝트** 

| 프로젝트 id | 프로젝트 제목         |
| ----------- | --------------------- |
| 653         | 트윈 미터 개발 `예시` |
| 3840        | 뇌 CT분석2 `예시`     |
| 1596        | MNIST3 `예시`         |

**추천 프로젝트**

| 프로젝트 id | 프로젝트 제목       |
| ----------- | ------------------- |
| 214         | 블랙박스 `예시`     |
| 315         | 미터기 읽기2 `예시` |
| 8739        | 모션 인식 `예시`    |
| 9498        | 안면 인식 `예시`    |

> 즉 해당 프로젝트를 수행하기 이전에 학생들은 '트윈 미터 개발' 프로젝트, '뇌 CT분석2' 프로젝트, 'MNIST3' 프로젝트를 완수한 상태여야 합니다. 



<br><br>