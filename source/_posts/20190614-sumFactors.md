---
title: 약수의 합
categories:
  - Algorithm
  - Programmers
  - Level1
tags:
  - Algorithm
  - Programmers
  - Level1
  - JavaScript
  - ES6
date: 2019-06-14 00:03:03
---

## 문제 설명
자연수 n을 입력받아 n의 약수를 모두 더한 값을 리턴하는 함수, solution을 완성해주세요.

<!-- more -->

## 제한 조건
- n은 0 이상 3000이하인 자연수입니다.

<br/>

## 입출력 예

| n | return |
| --- | --- |
| 12 | 28 |
| 5 | 6 |

<br/>


## 입출력 예 설명

입출력 예 #1<br/>
12의 약수는 1, 2, 3, 4, 6, 12입니다. 이를 모두 더하면 28입니다.<br/>

입출력 예 #2<br/>
5의 약수는 1, 5입니다. 이를 모두 더하면 6입니다.<br/>

### Solution

---

```javascript
function solution(n) {
    return new Array(n).fill(1).reduce((target, item, index) => {
        let el = item + index;
        
        !(n % el) && (target += el);
        
        return target;
    }, 0);
}
```