시그모이드를 취하면 값은 플러스 이면 1이고 마이너스면 0 이다.
오차 값이 작아진다는것은 미분값이 0 에 가까워 진다는 것이다.
시그모이드 함수를 미분하면 0.25의 기울기를 가진 그래프가 나온다.

편미분 = 라운드 기호로 표시
해당되는 변수에 대해서만 미분 하는것을 편미분이라고 한다.

오차역전파 = 매트릭스의 곱셈
편미분을 거치는 복잡한 수학 과정이지만, 편미분을해서 나온 결과는 선형대수 매트릭스의 곱셈으로 귀결이 된다는것이 오차역전파이다. 그래서 계산을 빠르게 수행할 수 있다.

렐루 - ReLU(Rectified Linear Unit)
Rectified: 정유기 - 밧데리 충천할때 사용되는것

아담: 경사하강법을 발전시킨 고급 경사하강법이다.

## 딥러닝 발전 계기

오차역전파와 렐류의 발견으로 인해 딥러닝이 폭발적으로 발전하게 된다.

## 딥러닝 프로세스

딥러닝 과정

- 입력층
- 은닉층: 렐루
- 출력층: 시그모이드, 소프트맥스

출력층 분류

- 이진분류: 시그모이드
- 다중분류: 소프트맥스
  - onehot-encoding, softmax, categoricalentrype

## 모델 설정

실행환경

```
loss='binary_crossentropy' # 이진분류
loss='categorical_crossentropy' # 다중분류
optimizer='adam'
metrics=['accuracy']
```

## 모델 실행

```
model.fit(X_train, y_train, validation_split=0.2, epochs=200, batch_size=50)
```

- 훈련 데이터: x_train, y_train
- 검증 데이터: validation_split
- 전체 반복 횟수: epochs
- 한번에 처리하는 데이터의 갯수: batch_size=50
