# Lmembers_solution3

## 구매감소 고객 예측기반 매출 관리 솔루션 

### 프로젝트 절차 
#### 1. 유통업체의 고객 이용, 상품, 계열사, 매출, 구매상품, 경쟁사 이용 데이터 분석
#### 2. 변수 설정 
#### 3. 머신러닝 모델로 구매 감소 고객 예측 및 하이퍼 파라미터 튜닝
#### 4. 매출 방어 솔루션 제안

### 프로젝트 결과 
#### 1. 총 7개의 모델, 14개의 변수를 사용하여 모델링 진행 
#### 2. Decision Tree 사용 결과, 총 구매금액 증감율, 총 구매금액 평균, A방문횟수 평균을 중심으로 노드가 나뉘는 것을 확인하여 해당 변수가 중요도가 높음을 파악 
#### 3. GridSearch CV 활용, 하이퍼 파라미터 튜닝. test score 0.74 도출 
#### 4. 실루엣 분석, PCA, 엘보우 기법 진행. 군집을 3개로 분류한 점수가 0.381로 가장 높음.  총 3개의 제휴사 별 주 이용 고객으로 그룹으로 분류
#### 5. 솔루션 제안 
#### 5-1. 군집 1 대상 솔루션(단골 고객) : 
-> 단골 고객 대상 의류, 신규상품, 잡화 및 신발 상품 프로모션 및 할인 쿠폰 제공
#### 5-2. 군집 2 대상 솔루션(멤버십 가입률이 높은 고객)
-> 개인 맞춤 모바일 쿠폰 배포. 고객의 장바구니 분석 후 재구매율이 높은 상품 위주로 모바일 할인 쿠폰 제공
#### 5-3. 군집 3 대상 솔루션(식재료 구매를 위해 일상적으로 방문하는 고객)
-> PB 상품 별 무료 멤버십 개설. 구매율이 높은 PB상품 위주로 무료 멤버십 개설 후 구매 횟수가 많을 수록 추가 혜택 증정 


### 사용 모델 
#### XGBoost 
#### LightGBM
#### CatBoost
#### AdaBoost
#### Logistic Regression
#### Random Forest
#### Decision Tree 

### 변수 리스트 
> 1. 인구 통계학적 변수
>> 1) 성별 
>> 2) 멤버십 가입 여부 

> 2. 구매액 관련 변수 
>> 1) 회당 구매액 증감률
>> 2) 총 구매금액 평균
>> 3) 총 구매금액 증감율
>> 4) A사 구매금액 증감율
>> 5) B사 구매금액 증감율
>> 6) C사 구매금액 증감율

> 3. 상품 구매개수 관련 변수 
>> 1) A사 상품 구매개수 평균
>> 2) B사 상품 구매개수 평균
>> 3) C사 상품 구매개수 평균

> 4. 방문횟수 관련 변수 
>> 1) A사 방문 횟수 평균
>> 2) B사 방문 횟수 평균
>> 3) C사 방문 횟수 평균

