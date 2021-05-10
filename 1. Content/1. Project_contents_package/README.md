# 콘텐츠 포맷 명세서

### 개요

교육을 진행하기 위해 개발한 교육용 콘텐츠의 **표준화된 포맷**을 **정의**합니다.</br>
개발한 교육용 콘텐츠를 **표준화된 포맷**으로 변환하여 저장해두었다가 필요에 따라 **콘텐츠를 LMS시스템에 탑재하여** 교육을 진행합니다. </br>

### 용어 설명

![Untitled Diag11ram (2)](https://user-images.githubusercontent.com/68315073/117391473-f5aa5480-af2a-11eb-9078-836cc2644173.png)
</br>

- `콘텐츠` : 학생들의 학습 진행을 위해 개발된 학습 자료를 의미합니다. 
- `프로젝트` : 콘텐츠 표준 포맷에 맞춰 정형화된 콘텐츠를 의미합니다. 하나의 프로젝트는 N개의 미션으로 구성됩니다.
- `미션` : 프로젝트를 구성하는 단위입니다. 프로젝트를 진행하는 학생은 프로젝트를 구성하는 N개의 미션을 모두 해결함으로써 프로젝트를 완수할 수 있습니다.
- `숫자` : JSON에서 나타낼 수 있는 숫자의 종류는 다음과 같습니다.
    - 1. 정수(integer)

    - 2. 실수(fraction)

    - 3. 지수(exponent)
- `문자열` : JSON에서 문자열(string)이란 일련의 연속된 문자의 집합을 의미합니다. 이러한 문자열은 큰따옴표("") 안에 유니코드 문자들의 나열로 구성됩니다.

### 콘텐츠 포맷 제작 목적

- 대학 등 각급 학교, 교육 사업자, 산업체에서 콘텐츠 표준 포맷을 사용하여 자신들만의 새로운 교육 콘텐츠를 만들고 개발한 콘텐츠를 LMS에 탑재하여 사용할 수 있도록 하기 위함입니다.
- 각기 다른 기관에서 개발한 콘텐츠를 표준화하여 저장해 두었다가, 추후에 다른 기관에서 해당 콘텐츠를 다시 사용하는 등 **콘텐츠의 재사용성**을 높이기 위함입니다.
- 해당 포맷을 적용한 다양한 교육 콘텐츠를 개발하여 **콘텐츠 마켓**을 형성할 수 있도록 하기 위함입니다. </br>

### 콘텐츠 포맷 명세서 작성 목적

- 콘텐츠를 개발하는 사용자가 콘텐츠를 표준 포맷으로 전환하는 것을 돕기 위함입니다. 
- 콘텐츠 포맷을 구성하는 각각의 항목을 정의하고 설명하기 위함입니다. 
- 콘텐츠 포맷을 구성하는 각각의 항목의 존재 이유에 대해 설명하기 위함입니다. 

### 콘텐츠 표준 포맷의 구성

콘텐츠 포맷은 크게 **'6개의 파트'** 로 구성됩니다.

| 순번 |     파일 이름     |  형식   |                             설명                             |
| :--: | :--------------- | :-----: | :---------------------------------------------------------- |
|  1   |    [Definition](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/1.%20Definition)     | `.json` |         프로젝트 전체를 포괄하는 정보를 기입합니다.          |
|  2   |    [Description](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/2.%20Description)    | `.json` |     프로젝트를 구성하는 각각의 미션에 대해서 기입합니다.     |
|  3   | [Learning Resource](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/3.%20Learning_Resource) | `.json` | 학생들이 프로젝트를 수행하기 위해 참고할 수 있는 학습 리소스에 대해 기입합니다. |
|  4   |    [Assessment](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/4.%20Assessment)    | `폴더`  | 학생들의 미션 수행을 평가할 수 있는 항목들과 기준에 대해 기입합니다. |
|  5   | [Assessment_Guide](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/5.%20Assessment_Gude)  |  `.md`  | 평가자들이 미션을 수행한 학생들을 평가할 때, 참고할 수 있는 문서입니다. |
|  6   |     [Data_File](https://github.com/edu10make/Project-X_contents_format/tree/main/1.%20Content/1.%20Project_contents_package/6.%20Data_File)     | `.tar`  | 학생들이 프로젝트를 수행할 때 필요한 데이터 파일을 제공하는 압축 파일입니다. |

