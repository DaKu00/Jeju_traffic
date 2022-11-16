# [제주 도로 교통량 예측]
</br>

- 기간: 2022.10.19 - 2022.11.02

- 팀원: 3명


- 문제 정의 : 제주도 내 주민등록인구와 입도객의 증가에 따라 교통량 역시 증가하고 있는데 늘어난 교통량은 제주도의 큰 문제로 대두되고 있다.

- 목표 : 제주도 도로 교통량 예측을 통한 교통 체증 완화


# Project Details
</br>

### 데이터 : https://dacon.io/competitions/official/235985/overview/description

![image](https://user-images.githubusercontent.com/85794900/202253717-8ab56701-80ec-432d-9402-4c96a94c454d.png)

test 데이터에는 target이 없어 train 데이터 4,701,217개로 진행

### 진행 과정

![image](https://user-images.githubusercontent.com/85794900/202248793-f2c771ab-ebcd-459b-865b-102186c490e7.png)

### feature 선정


![image](https://user-images.githubusercontent.com/85794900/202249379-e51d840c-94a5-43e9-925c-4e10614fa37b.png)

### Model

- LightGBM을 이용해 예측 진행
  
  정형 데이터에서 좋은 성능을 냄
  
  적은 데이터로는 과적합이 될 수 있으나 현재 프로젝트는 데이터가 많아 과적합 우려가 없음
  
  빠른 학습 속도로 많은 데이터를 학습할 때 

- MAE를 통해 성능 평가
  
  평균절대 오차로 예측값을 측정하여 오차값이 줄어드는 것을 직관적으로 확인하기 위함


# Result
</br>

### feature importance

![image](https://user-images.githubusercontent.com/85794900/202257049-675d330b-0a9d-4d71-b84c-a31286a9a720.png)

### 예측값

![image](https://user-images.githubusercontent.com/85794900/202257296-c7e887bc-3ac9-4e40-a697-8977aead2605.png)

