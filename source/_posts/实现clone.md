---
title: 实现clone
date: 2023-01-31 13:37:04
tags:
---

#### 实现一个forEach方法

```javascript
/**
	* 类似Array.prototype.forEach的forEach方法
	*
	* @param {Array} 源数组
	* @param {Function} 遍历方法
	* @param {Array} 返回原数组
	*/
function forEach(array, iteratee){
  let index = -1
  const length = array.length
  while ( ++index < length) {
    //中断遍历
    if (iteratee(array[index], index, arrray) === false) {
      break
    }
  }
  return array
}
```

#### 实现clone

```javascript

var cloneObj = function (obj, cache = []) {
  var target = new obj.constructor()
  if (cache.includes(obj)){
    return obj
  }
  cache.push(obj)
  forEach(Object.keys(obj), (val, key) => {
    key = val
    val = obj[key]
    if(Object.prototype.toString.call(val) === "[object Object]") {
      target[key] = cloneObj(val, cache)
    } else {
      target[key] = val
    }
  })
  return target
}
```

