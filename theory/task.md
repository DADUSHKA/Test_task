const arr = [10, 12, 15, 21];

for (let i = 0; i < arr.length; i++) {
  setTimeout(function() {
    console.log(arr[i] > 13 != 0 ? `Good: ${arr[i]}` : `Bad: ${arr[i]}`)
  }, 3000);
} 
// Данный код выводит четыре строчки: Bad: undefined
// Переменная, в ходе работы цикла, последовательно принимает значения 0, 1, 2, 3, 4, 
// причём, последнее значение оказывается сохранённым в ней и после выхода из цикла. 
// В массиве имеется четыре элемента, с индексами от 0 до 3, поэтому, попытавшись обратиться к arr[4], мы и получаем undefined. 


for (let i = 0; i < arr.length; i++) {
  setTimeout(function() {
    console.log(arr[i] > 13 != 0 ? `Good: ${arr[i]}` : `Bad: ${arr[i]}`)
  }, 3000);
}

for (var i = 0; i < arr.length; i++) {
  setTimeout(function(ii) {
    return function() {
      console.log(arr[ii] > 13 != 0 ? `Good: ${arr[ii]}` : `Bad: ${arr[ii]}`);
    }
  }(i), 3000);
}
