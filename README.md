# Swift

***

## reduce 

```swift
let sum = [1, 2, 3, 4].reduce(0) { $0 + $1 }
```

0은 sum의 초기값을 말한다. reduce는 파라미터가 2개인데 sum 값이 $0로 가고 배열의 첫번째 값이 $1로 간다. 그리고 그 두 수의 합은 다시 $0가 되고 배열의 두번쨰 값이 $1이 된다. 그렇게 끝까지 돌아가면 10이라는 결과가 나온다.

***

## Optional

옵셔널 선언 시 ! 선언은 무엇인가?

```swift
let a: Int! = 234 // Optional<234>
let b: Int = 34

print(a + b)
// 268
```

! 선언은 ? 선언과 달리 연산 시 자동적으로 옵셔널이 풀린다.

***

## 2차원 배열

```swift
var arr = [[0, 3], [1, 9], [2, 6]]
print(arr[1][1]) // 9
```

***

## Substring

A slice of a string.

***

