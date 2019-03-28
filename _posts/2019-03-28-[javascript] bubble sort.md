---
title: "[javascript] bubble sort"
date: 2019-3-28 10:23:00 -0400
categories: javascript algorithm
---

# 자바스크립트 버블정렬


첫 포스팅을 자바스크립트에 관한 글이 되었네요 .
요즘 알고리즘을 해야겠다는 생각이 되어 버블정렬을 한번 구현해봤어요.
ㅎㅎ 
근데 정말 알고리즘을 신경을 안써서 그런지 1시간이나 걸렸네요.
정말 머리가 굳어가는 느낌입니다. 매일매일 하나씩 해야겠네요.

정말 간단하게
버블 정렬은 배열의 n의 값과 n+1의 값을 비교 하여
더큰 값을 뒤로 보내는 정렬입니다.

```javascript
const getSortedArr = (arr) =>{
    const arrLength = arr.length;
    for(let index in arr){
        for(let sIndex=0;sIndex<arrLength;sIndex++){
            if(sIndex <arrLength-1){
                const value = arr[sIndex];
                const nextValue = arr[sIndex+1];
                if(value>nextValue) {
                    let empty = 0;
                    empty = value;
                    arr[sIndex] = nextValue;
                    arr[sIndex+1] = empty;
                }
            }
        }
    }
    return arr;
}

console.log(getSortedArr([4,5,1,9,10,13,21,2,3]));
```

결과 
```
[ 1, 2, 3, 4, 5, 9, 10, 13, 21 ]
```
* * *

코드의 질은 정말 떨어지네요
좀더 노력해서 깔끔한 코드를 짜야겠어요.

다음은 제스트를 써서 테스트 해보는 포스팅을 해볼게요. 
