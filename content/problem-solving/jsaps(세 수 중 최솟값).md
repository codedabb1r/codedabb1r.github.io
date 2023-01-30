---
emoji: 🧑🏻‍💻
title: 세 수 중 최솟값
date: '2023-01-26 23:00:00'
author: Ken
tags: jsaps javascript problem-solving
categories: PS
---

## 문제 설명

100이하의 자연수 A, B, C를 입력받아 세 수 중 가장 작은 값을 출력하는 프로그램을 작성하세요.

## 제한 사항

정렬을 사용하면 안됩니다.

## 입출력 예

| a, b, c  | answer |
| -------- | ------ |
| 6, 5, 11 | 5      |
| 1, 1, 2  | 2      |

## 나의 풀이

```javascript
function solution(a, b, c) {
	let answer;
	if(a < b) answer = a;
	else answer = b;
	if(c < answer) answer = c; 
	return answer;
}
```

## 알게 된 것

1. if 조건문을 통해 a와 b의 크기를 구한 뒤 젤 작은 수를 c와 비교 후 최종적으로 가장 작은 수를 판별하였다.

2. 처음에 Math.min() 함수를 통해 문제를 해결했지만, 이런 식으로 풀면 문제 해결 능력 향상에 전혀 도움이 되지 않을 거 같아 (이 문제를 만든 사람이 본다면 X욕을...) 하드코딩을 하더라도 최대한 바닐라로 구현했다. 😭

   ```javascript
   function solution(a, b, c) {
     let answer;
     return answer = Math.min(a, b, c);
   }
   ```

## 참고

* https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Math/min

---