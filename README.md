# Swift

***

## reduce 

```swift
let sum = [1, 2, 3, 4].reduce(0) { $0 + $1 } 
```

0은 sum의 초기값을 말한다. reduce는 파라미터가 2개인데 sum 값이 $0로 가고 배열의 첫번째 값이 $1로 간다. 그리고 그 두 수의 합은 다시 $0가 되고 배열의 두번째 값이 $1이 된다. 그렇게 끝까지 돌아가면 10이라는 결과가 나온다.

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

## sort() vs sorted()

sort는 기본적으로 원본 배열을 가지고 정렬한다.
```swift
var arr = [2, 24, 45, 36, 9]
arr.sort()
print(arr) // [2, 9, 24, 36, 45]

arr.sort(by: >)
print(arr) // [45, 36, 24, 9, 2]
``` 

sorted는 원본 배열은 건드리지 않고 사본을 만들어서 오름차순으로 정렬한 후 정렬된 요소를 반환해주는 방식이다. 내림차순 방식은 sort와 똑같다.

```swift
var arr = [2, 24, 45, 36, 9]
var sortedArr = arr.sorted()

print(arr) // 변함없음
print(sortedArr) // [2, 9, 24, 36, 45]
```

***

```swift
let a: Int = 17
print(a / 5)
// 3
```

***









 





