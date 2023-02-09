## Double DQN
DQN의 문제점: target value가 특정 조건에서 overestimate됨<br><br>
![image](https://user-images.githubusercontent.com/121830114/217928649-50e014cb-1bbc-4689-b225-7d51235bdf60.png)<br><br>
Q learning 기반 알고리즘은 TD targe을 이용하기 때문에 target value를 Q-function을 이용해 추론하는 과정이 포함됨<br>
이 과정에서 max operation이 target value의 overestimation을 일으킴 -> Double DQN에서는 actio의 seleection과 evaluation을 분리하여 직접적인 max Q를 통해 현재 state의 가치를 추정하는 것을 방지
![image](https://user-images.githubusercontent.com/121830114/217929560-af412dd0-ac6f-4f42-8553-c1239ec5ac91.png)
![image](https://user-images.githubusercontent.com/121830114/217929600-de5fc986-7cc5-4a05-b7ee-3037d26ba28d.png)

### Overestimate란?
target value의 overestimation은 action-value Q(s, a)의 에러 때문에 발생
target value는 항상 증가시키는 방향으로 overestimation이 일어남

### DQN과 Double DQN의 overestimation error
![image](https://user-images.githubusercontent.com/121830114/217930048-57b7f7a0-0c09-421c-82e0-bb3acca1be5e.png)

## 실습

