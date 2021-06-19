## 경사하강법(Gradient Descent)
- 모델이 학습하면서 가중치(w)을 갱신하는 데 무작정 갱신하는 것이 아니라 지정한 loss function을 최소화할 수 있는 방향으로 갱신.
- 그 방향을 제시하는 것이 loss function의 미분값인 gradient

## 배치(Batch) : 설정한 데이터 개수의 묶음 단위

## 에폭(Epoch) : 전체 데이터를 학습하는 횟수

## BDG(Batch Gradient Descent)
 - 한 번의 loss, gradient를 구하기 위해 전체 데이터를 다 넣어서 계산
 - 단점 : 데이터 수가 증가하면 계산, 시간 측면에서 효율적이지 않음

## SGD(확률적 경사 하강법, Stochastic Gradient Descent)
 - 매개변수를 갱신할 때 필요한 loss를 구하기 위해서 하나의 샘플을 추출하여 계산
 - 장점 : 수렴속도가 빠름
 - 단점 : global optima를 찾지 못할 수도 있고 노이즈에 약함

## Mini-Batch SGD
 - SGD와 BGD의 중간 방법으로 매개변수를 갱신할 때 필요한 loss를 구하기 위해 '적절한 batch size'를 통해 구함
 - 적절한 batch size에 대한 튜닝 혹은 의사결정이 필요

## 오차역전파(backpropagation)
 - 오차역전파는 신경망의 학습을 위해서 gradient(오차)를 output에서 input의 '순서로 전달해주는 것'
 - 전체 loss에 대한 gradient를 적용하는 것이 아니라 각 지점에 맞게 gradient를 적용하여 매개변수를 업데이트

## 최적화(Optimization) : 신경망 학습에서 loss function을 최소화하는 매개변수를 찾는 것
 - SGD : 일반적인 SGD 매개변수 갱신
 - Momentum : 기존 경사하강법에 관성을 추가한 것. 이전의 가던 기울기를 반영하여 더 빠르게 수렴
 - AdaGrad : 학습률 감소 전략 활용. 탐색하지 못한 곳은 빠르게 보고 학습하면서 탐색한 곳은 더 세세하게 보아 global optima 탐색. 학습을 하면서 학습률이 점차 감소되는 방식
 - RMSProp : AdaGrad가 학습이 지속되면서 학습률이 0에 가까워져 학습이 불가능한 문제를 해결하고자 나온 방법. 최근값들에는 큰 가중치, 이전 값들에 더 적은 가중치를 주어 급격하게 학습률이 감소하는 것을 방지할 수 있음
 - Adam : 딥러닝에서 optimizer로 가장 일반적으로 사용되는 기법. Adam은 모멘텀과 RMSProp을 결합한 느낌의 기법으로 모멘텀의 개념을 활용하면서 학습률을 조정하기 위해 지수가중평균을 적용한 것
 
# 손실함수(Loss function)
 - 일반적으로 회귀문제에서는 MSE, 분류문제에서는 Cross entropy error 활용.

# 가중치 초기화(Weight initialization)
 - 

