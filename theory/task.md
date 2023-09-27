const arr = [10, 12, 15, 21];

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
