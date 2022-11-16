# ds5-ml-repo-1

# 제주도 도로 교통량 예측
제주도 도민의 증가와 입도 여행객의 증가로 인한 교통체증 문제에 해결에 도움이 되고자 프로젝트를 진행
제주도 도로 정보 데이터를 통해 특정 구간에서의 평균 속도를 예측하여 교통체증 여부를 판별

## 1. 데이터
### - 데이콘에서 주최하는 '제주도 도로 교통량 예측 AI 경진대회'에서 제공하는 데이터를 사용
https://dacon.io/competitions/official/235985/data

### - 총24개의 컬럼이 있는 데이터의 2개의 컬럼을 추가하여 진행
  - 주말컬럼과 월컬럼을 추가
  - 주말컬럼에는 공휴일, 연휴을 포함시켜 휴일과 비휴일 형태로 구성
<img src="https://user-images.githubusercontent.com/87750521/202093281-3a33f059-6051-4c2d-ac4c-5aa2d5cf1e95.png" width="430" height="400"/>

### - 학습에 필요하지 않거나, 도움이 되지 않는다 판단되는 컬럼을 삭제
  - 빨간 박스로 체크된 컬럼을 drop하여 학습 진행
  - target컬럼은 학습 데이터에서 삭제하고 정답 데이터로서 학습에 사용
<img src="https://user-images.githubusercontent.com/87750521/202093609-79b5b954-8349-4127-95bd-e5921a80fc0b.png" width="230" height="400"/>

### - 데이터셋 설정
  - 데이콘에서 받은 데이터는 train데이터와 test데이터로 나뉘어 있지만 test데이터에는 target이 없어 모델의 성능을 평가하기 힘듦
  - train데이터를 나누어 test데이터로 사용
    - test데이터는 22년 8월 데이터, train데이터는 22년 8월 이전의 데이터
<img src="https://user-images.githubusercontent.com/87750521/202096392-e786d998-0ba0-49f2-b66f-6fb3f0515455.png" width="1000" height="300"/>




## 2. 모델
### LightGBM모델을 사용하여 머신러닝 진행
- 예측 알고리즘과 정형데이터에서 좋은 성능을 보임
- 학습 속도가 빨라 데이터 수가 많을 때 적합

### MAE를 사용하여 모델평가
- 평균절대 오차로 예측값을 측정하여 오차값이 줄어드는 것을 직관적으로 확인하기 위함


## 3. 하이퍼파라미터 튜닝
- max_depth, num_leaves, learning_rate, n_estimators 4개의 파라미터가 오차값에 큰 영향이 확인됨
- 4개의 파라미터튜닝만으로 MAE값이 5.04대에서 3.55대로 감소
<img src="https://user-images.githubusercontent.com/87750521/202098537-a8619390-01c6-4302-b86e-2836ca86d0a2.png" width="300" height="134"/>
<img src="https://user-images.githubusercontent.com/87750521/202098021-966239c3-ab48-427a-b49f-8df0c3bcb57e.png" width="400" height="45"/>

