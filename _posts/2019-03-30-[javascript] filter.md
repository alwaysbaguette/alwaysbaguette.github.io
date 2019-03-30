---
title: "[javascript] filter"
date: 2019-3-30 14:20:00 -0400
categories: javascript 
---

# javascript filter


age 가 20 이상인 오브젝트를 리턴하는 필터함수를 만들었습니다.


```javascript 
    const list = [
        {id:1,name:'va',age:'10'},
        {id:2,name:'la',age:'20'},
        {id:3,name:'aa',age:'30'},
        {id:4,name:'bfba',age:'40'},
        {id:5,name:'sa',age:'50'},
        {id:6,name:'fa',age:'60'},
    ];

    const _above20 = (obj) =>{
        return obj.age>20 ;
    }

    const _filter = (list,pre) =>{
        return list.filter(x=>pre(x));
    }

    console.log(_filter(list,_above20));
```

결과값

```javascript
[ { id: 3, name: 'aa', age: '30' },
  { id: 4, name: 'bfba', age: '40' },
  { id: 5, name: 'sa', age: '50' },
  { id: 6, name: 'fa', age: '60' } ]
```

처음에 list를 선언햇을때 값들중에 age가 20 이상인 값들이  
출력이 되었네요 .

**_filter  함수**를 보시면 인자로 리스트 와 함수를 하나씩 받게되는데 받은 함수는 불린을 리턴하는 함수입니다. 

**_filter** 를 호출하는 곳을 보시면 제가 **_above20**이라는 함수를 넣었는데  
이렇게 넣었을경우 오브젝트의 age가 20보다 위일 경우 true를 리턴하면서 필터 함수에서 필터가 작동됩니다.

```javascript
const _filter = (list) =>{
    return list.filter(x=>x.age>20)
}
```

이렇게 작성할수도 있지만 이렇게 작성하게될 경우 필터함수는 재사용성이 없어지게되죠.


저렇게 함수를 받게 함으로서 **_filter** 함수는 재사용을 할수있는 함수가 되었습니다. 