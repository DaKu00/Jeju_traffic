# ds5-ml-repo-1

# 제주도 도로 교통량 예측
제주도 도민의 증가와 입도 여행객의 증가로 인한 교통체증 문제에 해결에 도움이 되고자 프로젝트를 진행
제주도 도로 정보 데이터를 통해 특정 구간에서의 평균 속도를 예측하여 교통체증 여부를 판별

## 데이터
- 데이콘에서 주최하는 '제주도 도로 교통량 예측 AI 경진대회'에서 제공하는 데이터를 사용
https://dacon.io/competitions/official/235985/data

- 총24개의 컬럼이 있는 데이터의 2개의 컬럼을 추가하여 진행
<img src="https://user-images.githubusercontent.com/87750521/202093281-3a33f059-6051-4c2d-ac4c-5aa2d5cf1e95.png" width="430" height="400"/>


- 학습에 필요하지 않거나, 도움이 되지 않는다 판단되는 컬럼을 삭제
  - 빨간 박스로 체크된 컬럼을 drop하여 학습 진행
  - target컬럼은 학습 데이터에서 삭제하고 정답 데이터로서 학습에 사용
<img src="https://user-images.githubusercontent.com/87750521/202093609-79b5b954-8349-4127-95bd-e5921a80fc0b.png" width="230" height="400"/>

