# 2021-1_Artificial-Intelligence-Thinking
2020년1학기_인공지능적사고와문제해결_숭실대학교AI융합학부전공  
It is a practical class of "Artificial Intelligence Thinking and Problem Solving," a subject of AI Convergence Department at Soongsil University.


### Week1_Lecture Introduction / Machine Learning Overview
1. 성적 평가 세부사항
	- 출석(10%), 수업 참여 점수(10%), 프로젝트 평가(40%), 기말 코딩테스트(40%)
2. 수업 교재
	- 파이썬머신러닝완벽가이드(권철민지음/위키북스)
3. 머신러닝 개요
	- 머신러닝 역사, 머신러닝 알고리즘의 분류, Python 머신러닝 생태계

### Week2_Python
1. Python(A)
 	- 파이썬 설치, 아나콘다 가상환경
 	- 주석(comment), 데이터 타입, 연산자(operator), 문자열, 조건문 if, 반복문, 출력과 입력, 함수(function)
2. Python(B)
 	- 컬렉션:리스트,튜플,딕셔너리,집합
 	- 모듈,패키지
  - 주피터 노트북(jupyter notebook)
  - 구글 Colab

### Week3_Numpy
1. ndarray
  	- 행렬을 위한 새로운 객체
2. data types
 	- ndarray는 하나의 데이터타입만 가질 수 있다
 	- 데이터 타입 변환: ndarray.astype(“목표타입”)
 	- arange(): python내장 range()와 비슷한 기능 수행  
 	- zeros(), ones(): 주어진 shape의 ndarray를 생성하되, 하나의 값 이용(0또는1)
 	- reshape()
 	- tolist()
3. indexing
  	-  주어진 ndarray에서 일부 데이터 세트나 특정 데이터만을 선택
  	- 특정한 데이터만 추출, 슬라이싱(slicing), 팬시 인덱싱(fancy indexing), 불린 인덱싱(boolean indexing)
4. 정렬
  	- np.sort(ndarray): 정렬된 새로운 ndarray를 리턴
  	- ndarray.sort(): 기존에 있는 ndarray객체를 정렬하며 리턴값 없음
  	- np.argsort(): 정렬된 행렬의 인덱스를 반환 (ndarray형으로 리턴)
5. 선형대수 연산
  	- 행렬곱:np.dot()
  	- 행렬전치:np.transpose()

### Week7_Evaluation
1. 정확도(Accuracy)
	- (예측 결과가 동일한 데이터 건수) / (전체 예측 데이터 건수)
	- 직관적인 모델 예측 성능
	- 데이터 분포에 따라 성능이 왜곡되어 나타날 수 있음
2. 오차 행렬(Confusion matrix)
	- 정답 클래스와 예측 클래스의 조합을 가지고 2X2 행렬을 만듦
3. 정밀도(Precision)와 재현율(Recall)
	- 정밀도 = TP / (FP + TP) → 스팸 메일 탐지 → __확실한 것만 찾자__
	- 재현율 = TP / (FN + TP) → 코로나 탐지 키트, 사기 탐지 → __웬만하면 다 찾자(조금 틀리더라도)__
	- 적용하려는 문제에 따라 어떤 성능을 최적화 할지 결정해야 함
	- 임곗값(threshold)에 따라 정밀도-재현율 트레이드오프(trade-off)가 생김
4. F1 스코어
	- 정밀도와 재현율을 결합한 스코어로, 어느 한 쪽으로 치우치지 않을때 높은 값을 가짐
5. ROC곡선과 AUC
	- 임곗값을 변경시키며 이진 분류 모델의 성능을 판단하는 그림
	- AUC: ROC Curve로 만들어지는 면적
	- sklearn.metrics.roc_curve(): roc curve 그리기
	- sklearn.metrics.roc_auc_score():이진 분류 모델의 대표적인 성능 지표로 활용
