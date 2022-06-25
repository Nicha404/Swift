# Swift

***   
   
## reduce    
 
```swift   
let sum = [1, 2, 3, 4].reduce(0) { $0 + $1 } 
```

0은 sum의 초기값을 말한다. reduce는 파라미터가 2개인데 0이 $0로 가고 배열의 첫번째 값이 $1로 간다. 그리고 그 두 수의 합은 다시 $0가 되고 배열의 두번째 값이 $1이 된다. 그렇게 끝까지 돌아가면 10이라는 결과가 나온다.

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

sort는 기본적으로 원본 배열을 정렬한다.
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

## Int 

```swift
let a: Int = 17
print(a / 5)
// 3
```

***

## dictionary

```swift
var dict: [String: Int] = [:]

dict["d"] = 3
dict.updateValue(4, forKey: "f")

print(dict)
// ["f": 4, "d": 3]

var dict: [[Int]: [Int]] = [:]
dict.updateValue([3, 3], forKey: [3, 3])

print(dict)
//[[3, 3]: [3, 3]]
```
***

## 배열 최빈값

```swift
let items = [1, 1, 1, 2, 2, 2, 2, 3, 3, 4]
let mappedItems = items.map { ($0, 1) }
let counts = Dictionary(mappedItems, uniquingKeysWith: +)
print(counts.max(by: { $0.value < $1.value })!.key)
// 2

let str = Dictionary(items.map { ($0, 1) }, uniquingKeysWith: +)
print(str.max(by: { $0.value < $1.value })!.key)
// 2

```

***

## 인덱스로 스트링 자르기

```swift
var s = "Swift"
var i = s.index(s.startIndex, offsetBy: 2)
s = String(s[s.startIndex...i])
print(s) // Swi
```

***

## sort 메커니즘

https://greendreamtrre.tistory.com/406

sort는 버블 정렬식으로 두 수를 비교하여 점차 뒤로 움직인다.

```swift
var failure: [Int: Float] = [1: 1, 2: 2, 4: 3, 3: 2]
print(failure.sorted(by: <).sorted(by: { $0.value > $1.value }).map { $0.key })
// [4, 2, 3, 1]
```
이런식으로 이중 sort도 가능하다. 일단 1234로 정렬한 뒤 value값에 따라 두 수를 버블 정렬식으로 비교하면 value값을 내림차순으로 정렬하면서도 value값이 같다면 key 값은 오름차순이 된다.

***

## 진수 변환

```swift
var n = 123
let binary = String(n, radix: 2)
```

***

## zip

zip은 두 개의 시퀀스로 구성된 시퀀스쌍을 만든다.

```swift
let words = 1...4
let numbers = 1...4

for (word, number) in zip(words, numbers) {
    print("\(word): \(number)")
}

1: 1
2: 2
3: 3
4: 4
```
***

## inout

https://hyunsikwon.github.io/swift/Swift-Inout-01/

***

## guard let

https://jud00.tistory.com/entry/오늘의-Swift-지식-if-let-과-guard-let의-차이는

***

## Set

```swift
var a: Set<Int> = [1, 2, 3]
a.remove(1)

print(a) // [2, 3]
```

You can remove specific numbers in Set

***

## enumerate 예

```swift
let a = "try hello world"
let b = a.components(separatedBy: " ").map { $0.enumerated().map { ($0.element, $0.offset) } }
print(b)
// [[("t", 0), ("r", 1), ("y", 2)], [("h", 0), ("e", 1), ("l", 2), ("l", 3), ("o", 4)], [("w", 0), ("o", 1), ("r", 2), ("l", 3), ("d", 4)]]
```

***

## 2차원 배열 map

```swift
var a = [["T", "r", "Y"], ["H", "e", "L", "l", "O"], ["W", "o", "R", "l", "D"]]
print(a.map { $0[0] })
//["T", "H", "W"]
```

***

## 2차원 배열

```swift
var a = [[2, 2, 3], [3, 3], [34]]

print(a.filter { $0[0] * 2 == 4 }) // [[2, 2, 3]]
print(a.flatMap { $0 }) // [2, 2, 3, 3, 3, 34]
```

***

## 2차원 배열 선언 방식

```swift
var arrTwoDimension = [[Int]]()
```
왼쪽에서 선언하니까 배열 추가할때 빈 배열이 생김. 그냥 오른쪽에서 선언하자. 왜 그런지는 더 알아봐야겠음.

***

## switch continue
switch문에서 continue 써도 for문 하나를 건너뛴다.

***













  





