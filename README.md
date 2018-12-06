## eliminate duplicates for ArrayObject
```javascript
/**
* created by Chanphy on 2018.12.06
*/
  let arr1 = [{id:1},{id:2}],
      arr2 = [{id:1},{id:3}],
      wholeItems = [...arr1, ...arr2];
  let resultArr = [wholeItems[0]];
  for (let item of wholeItems) {
    let itemIdStr = `"id":${item.id}`;
    let resultArrStr = JSON.stringify(resultArr);
    if(!resultArrStr.includes(itemIdStr)){
      resultArr.push(item);
    }
  }
  console.log(resultArr);
```
