# 구현할 기능 목록

## 예외 상황 (throw 문을 사용해 예외를 발생시킨 후 애플리케이션 종료)
- 예외 1: 게임 진행 상황에서 사용자가 3자리의 수를 입력하지 않은 경우(1, 2 ,4 ,5...자리)
- 예외 2: 게임 진행 상황에서 사용자가 3자리의 수를 입력했지만, 그 3자리의 수가 모두 다르지 않은 경우
- 예외 3: 게임 종료 후에 사용자가 1(재시작) 또는 2(종료) 외의 다른 숫자를 입력한 경우
- 예외 4: 게임 진행 상황, 게임 종료 후에 사용자가 입력해야 하는 부분에서 입력 없이 엔터를 친 경우

## 실행 결과 예시 (각 예외마다 다르게 예외를 처리할건지, 그냥 똑같이 예외를 처리할건지 정하기) => 똑같이 하기로 결정
- 예외 1(게임 진행 상황에서 사용자가 3자리의 수를 입력하지 않은 경우)의 예시
```
숫자 야구 게임을 시작합니다.
숫자를 입력해주세요 : 123
1볼 1스트라이크
숫자를 입력해주세요 : 14
[ERROR] 3자리의 수를 입력하지 않았습니다.
```

- 예외 2(게임 진행 상황에서 사용자가 3자리의 수를 입력했지만, 그 3자리의 수가 모두 다르지 않은 경우)의 예시
```
숫자 야구 게임을 시작합니다.
숫자를 입력해주세요 : 123
1볼 1스트라이크
숫자를 입력해주세요 : 144
[ERROR] 서로 다른 3자리의 수를 입력하지 않았습니다.
```

- 예외 3(게임 종료 후에 사용자가 1(재시작) 또는 2(종료) 외의 다른 숫자를 입력한 경우)의 예시
```
숫자 야구 게임을 시작합니다.
숫자를 입력해주세요 : 123
1볼 1스트라이크
숫자를 입력해주세요 : 145
1볼
숫자를 입력해주세요 : 671
2볼
숫자를 입력해주세요 : 216
1스트라이크
숫자를 입력해주세요 : 713
3스트라이크
3개의 숫자를 모두 맞히셨습니다! 게임 종료
게임을 새로 시작하려면 1, 종료하려면 2를 입력하세요.
3
[ERROR] 1 또는 2를 입력하지 않았습니다.
```

- 예외 4(게임 진행 상황, 게임 종료 후에 사용자가 입력해야 하는 부분에서 입력 없이 엔터를 친 경우)의 예시
```
숫자 야구 게임을 시작합니다.
숫자를 입력해주세요 : 123
1볼 1스트라이크
숫자를 입력해주세요 :
[ERROR] 아무런 숫자도 입력하지 않았습니다.
```