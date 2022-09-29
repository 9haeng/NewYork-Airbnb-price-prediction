# NewYork Airbnb price prediction
-----
![image](https://user-images.githubusercontent.com/70729822/193022076-255eeb2b-fa5b-4994-8ccd-576561b835b8.png)
전 세계적으로 위드 코로나가 시작된 이후로 사람들은 기다렸다는 듯이 다시 여행을 다니기 시작했습니다.

현 시점에서 여행 이라는 키워드가 화제되고 있는 만큼,여행 관련 서비스하면 빼놓을 수 없는 에어비앤비.

에어비앤비 데이터셋을 이용해 숙박 관련 데이터를 통한 숙박 가격을 예측하는 모델을 만들어보겠습니다.


## 프로젝트 목표
----
`범주형, 숫자형 feature`를 활용해 숙박 가격 예측

## 프로젝트 과정
- 데이터 탐색 및 전처리
    - 결측값, 중복값
    - 범주형 features
    - 숫자형 features
    - 상관성 확인
- 모델 학습
    - Baseline
        - 다양한 `Regressor`를 활용한 모델 생성과 `Hyper parameter tuning`
        - 모델 평가 및 `Feature importance`
    - 성능 개선
        - Data scaling
            - 모델 재 평가 및 `Feature importance`
    - `Voting Regressor`
----
![image](https://user-images.githubusercontent.com/70729822/193022992-08b89625-04fc-4ded-8f56-1ebdfd1695a4.png)
![image](https://user-images.githubusercontent.com/70729822/193023027-124931ea-c78c-445a-ac9b-301597276300.png)
![image](https://user-images.githubusercontent.com/70729822/193023083-33ca8205-dc26-49ae-ba05-273b0dcf2571.png)
- 시각화를 통한 `EDA`
![image](https://user-images.githubusercontent.com/70729822/193023200-a7d7d816-b630-4094-a2c6-69078c382f69.png)
- 다양한 `Regression` 모델 학습 결과 시각화
![image](https://user-images.githubusercontent.com/70729822/193023212-41063b9e-7e26-4472-b326-1621456feab3.png)
- `Regression` 별 `Feature importance`

![image](https://user-images.githubusercontent.com/70729822/193023640-d4534797-08eb-4b50-b5c9-91b35c305805.png)
- 최적의 모델이 가장 잘못 예측한 케이스 확인




## 결론 및 후기
----
다양한 `Regressor`와 `GridSearchCV`를 통한 하이퍼 파라미터 튜닝으로 각 모델들을 학습해 보았습니다.

성능을 평가하자면 최종 모델의 성능이 우수하다고 생각하지 않습니다.

그러나 이 머신러닝 프로젝트를 통해 각 모델별로 **어떤 특성**을 **얼만큼 중요시** 여기는지, 

즉 숙소의 가격을 결정 짓는 주 요소들이 무엇인지 `Feature importance`를 통해 확인할 수 있었던 점이 좋았습니다.  

예측 가격과 실제 가격의 차이가 큰 숙소 정보를 직접 확인하고, 해당 숙소와 비슷한 성격을 띈 숙소의 평균 가격을 확인해 본 결과,

`모델이 가격을 터무니없이 잘못 예측한 케이스`를 `모델의 정확도가 낮아 잘못 예측했다` 라고 해석하기 보다, 

`해당 숙소의 가격이 비슷한 성격을 띈 숙소의 평균 가격을 벗어난 케이스` 라고 결론 지을 수 있을 것 같습니다.

**그렇기 때문에,**


숙박 가격이라는 타겟은 주어진 데이터 내 특성과 비슷한 숙소와의 가격 경쟁으로만 결정지어지는 것이 아니라, 숙소 **호스트마다 다른 가격 책정요소**가 있기 때문에 이를 예측하는 정확도를 일정선 이상으로 높이는 것은 힘들다고 생각합니다.


감사합니다.

