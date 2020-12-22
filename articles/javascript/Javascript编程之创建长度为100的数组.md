## 实现方法一：循环赋值

```
var arr1 = new Array(100);
for(var i = 0;i < arr1.length;i++){
    arr1[i] = i;
}
console.log(arr1);
```

## 实现方法二：push方法实现

```
var arr2 = new Array();
for(var i = 0;i < 100;i++){
    arr2.push(i);
}
console.log(arr2);
```

## 实现方法三：while

```
var arr3 = new Array();
var i = 0;
while(i < 100){
    arr3.push(i);
    i++;
}
console.log(arr3);
```

## 实现方法四：do while

```
var arr4 = new Array();
var i = 0;
do{
    arr4.push(i);
    i++;
}while(i<100)
console.log(arr4);
```

## 实现方法五：

```
var arr5 = Object.keys(Array.apply(null, {length:100})).map(function(item){
    return +item;
});
console.log(arr5);
```

## 实现方法六：

```
var arr6 = Array.from({length:100}, (v,k) => k);
console.log(arr6);
```

## 实现方法七：

```
var arr7 = Array.from(Array(100), (v,k) =>k);
console.log(arr7);
```

## 实现方法八：

```
var arr8 = new Array(100).keys();
console.log(Array.from(arr8));
```

## 实现方法九： 

```
var arr9 = [];
var i = 0;
var timer = setInterval(function(){
    arr9[i] = i++;
    if(i>=100){
        clearInterval(timer);
        console.log(arr9);
    }
},1);
```

## 实现方法十：

```
var arr = [];
var i = 0;
function MakeArray(num){
    if(i < num){
        arr[i] = i++;
        MakeArray(num);
    }
    return arr;
}
console.log(MakeArray(100));
```

## 实现方法十一：

```
var arr11 = new Array(100).toString().split(',').map(function(item,index){
    return index;
});
console.log(arr11);
```