# 5. Assessment Guide : 프로젝트 평가가이드

### 개요

피평가자가 제출한 미션을 평가하는 평가자(동료, 멘토)를 위한 평가 안내서입니다.<br>

콘텐츠를 제작한 사람은 `markdown`형식으로 `프로젝트 평가가이드`를 함께 작성합니다.<br>

`markdown`형식으로 작성된 `프로젝트 평가가이드`는 각 미션마다 `PDF`형식으로 변환되어 LMS에 업로드되며 평가자가 해당 문서를 읽고 평가를 진행합니다.<br>

<img src="https://user-images.githubusercontent.com/68315073/117620331-5f389600-b1ab-11eb-9ac1-03c7c6843c93.png" width="70%" height="70%">

물론 실제 평가는 LMS가 `프로젝트 평가 요소(4. Assessment)`를 읽어 구성한 평가 화면에서 진행하되, 평가자는 해당 화면에서 평가하기 전 `평가 가이드`를 읽고 평가해야할 방향을 결정합니다. <br>

> 평가사이트 운영 방법에 대해 더 자세히 알아보려면 [평가사이트 운영가이드](https://github.com/edu10make/Project-X_contents_format/blob/main/2.%20Operation/%ED%8F%89%EA%B0%80%EC%82%AC%EC%9D%B4%ED%8A%B8%20%EC%9A%B4%EC%98%81%EA%B0%80%EC%9D%B4%EB%93%9C_.pdf)를 참조

<br><br>


---

#  프로젝트 평가가이드 markdown 작성 예시
## 1️⃣ 미션 정보
### 평가 미션
|프로젝트ID|프로젝트 이름|미션 ID|미션 이름|
|:--------:|:----------:|:------:|:------:|
|2|뇌 CT 분석|1|CT이미지 분석

### 평가 방법 선택
|`코드 자동 평가`|&nbsp;`퀴즈`&nbsp;|&nbsp;`동료 평가`&nbsp;|`멘토 평가`|
|:--------:|:----------:|:------:|:------:|
||✅|✅||

### 미션 설명
-	구글드라이브에 환자 진료 데이터를 저장하고 구글 드라이브를 구글 Collaboratory에서 사용할 있도록 마운트하라.
-	그리고 데이터들을 다양한 그래프로 출력하여 분석한다. 이미지는 학습을 위해 128, 128 크기로 저장한다.
-	또한 학습을 위해 데이터를 train 80%, validation 10%, test 10%로 나누어라.
-	데이터 변환으로 추가데이터를 확보한다는 것은 train 과 validation 데이터를 가공하여 추가 데이터를 확보한다는 의미이다.
-	test 데이터는 가공할 이유가 없으므로 추가데이터 확보는 반드시 데이터를 train 과 test 로 구분하고 난 뒤에 train에 대해서만 가공한다.

### 결과물
- Image Data Generator의 발표 동영상

### 평가 항목
|구분|평가 항목|
|:--------:|:----------|
|`Data Store`|	1. try except의 사용으로 데이터 엑세스 에러에 대처했는가?|
|`Data Store`|	2. 구글드라이브에 저장했는가?|
|`Data Analysis`|	3. 그래프를 많이 만들어서 데이터 분석을 많이 할수록 높은 점수 부여|
|`Data Analysis`| 4. 이미지는 128, 128 크기로 저장했는가?|
|`Data Split`| 5. 데이터를 train, validation, test로 나누었는가? |
|`Image Data Generator`|	6. Image Data Generator를 사용하였는가?|
|`Image Data Generator`| 7. 발표를 잘할 수록 높은 점수 부여|

### 퀴즈 문항
|구분|문제|정답|
|:--------:|:----------|:-|
|`Data Analysis`|이미지를 pyplot에서 출력하기 위해서 사용하는 메소드는?|imshow()|
|`Data Split`|train_test_split을 사용할 때, 실행 시 마다 같은 학습 데이터를 얻고 싶다. 어떤 인자 값을 어떻게 해야 하는가?|random_state에 임의의 값을 넣어준다. 시드를 고정하기 때문에 실생 시마다 같은 학습 데이터를 얻는다.|
<br>
<br>

## 2️⃣ 평가자를 위한 평가 가이드
### 어떤 관점으로 학생의 미션을 평가해야 하는가?
 이번 미션에서 가장 핵심적인 부분은 주어진 데이터를 training set과 test set으로 구분하는 비율에 있다. 주어진 Data Set이 많지 않으므로 training set에 많은 data를 할당하면 test 결과를 신뢰할 수 없고, test set에 많은 데이터를 할당하면 좋은 모델을 만들 수 없다. 이 때, 이상적인 test set과 training set의 비율은 1:7 정도이다. 이 때, sklearn의 train_test_split model을 사용하지 않았음은 감점 요소가 아니다. 

### 출제자의 의도

이번 미션의 출제 의도는 데이터 분석과 관련된 라이브러리를 제대로 사용할 수 있는 가를 평가함에 있다. 

<br>
<br>

---


# 평가 가이드 PDF 변환 예시

<img src="https://user-images.githubusercontent.com/68315073/117905061-78f1ee80-b30d-11eb-8d33-caebdd26cbc2.png" width="50%" height="70%"><img src="https://user-images.githubusercontent.com/68315073/117905085-86a77400-b30d-11eb-9357-cfc9919d74fd.png" width="50%" height="70%">


[assessment_guide_2-1.pdf](https://github.com/edu10make/Project-X_contents_format/files/6462760/assessment_guide_2-1.pdf)

