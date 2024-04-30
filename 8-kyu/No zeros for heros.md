## Numbers ending with zeros are boring.
**Instructions**

They might be fun in your world, but not here.

Get rid of them. Only the ending ones.

```JavaScript
1450 -> 145
960000 -> 96
1050 -> 105
-1050 -> -105
```
Zero alone is fine, don't worry about it. Poor guy anyway

---

### Solution

```JavaScript
function noBoringZeros(n) {
  let arr = n.toString().split(''); //перевести число в строку и разбить по символам
  for(let i = arr.length; i > 0; i--){ //пройтись циклом по массиву строки
      if (n == 0){
      return 0;
    } else if(arr[arr.length-1] == '0'){ //array.length возвращает размер массива, нумеруя элементы с единицы, а сам массив нумеруется с нуля, поэтому результат этой функции будет, фактически, на 1 больше реального размера. Если не вычесть единицу, то на последней итерации выйдем за пределы массива.
      arr.pop();
    }else {
    return +arr.join('') //меняем обратно на строку на число и соединяем
    }
  }
}
```
