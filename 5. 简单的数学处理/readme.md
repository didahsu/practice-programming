# 简单的数学处理

编写一个程序，提示用户输入两个数。打印这两个数的和、差、积及商，如示例输出所示。

```shell
What is the first number? 10
What is the second number? 5
10 + 5 = 15
10 - 5 = 5
10 * 5 = 50
10 / 5 = 2
```

约束

- 用户输入的值将会是字符串。确保在做数学运算之前将其转换成数值。

- 将输入和输出与数值转换及其他处理分开。

- 生成一条在适当的位置包含换行的输出语句。

挑战

- 修订这个程序，确保输入以数值形式提供。如否，不允许用户继续。

- 不允许用户输入负数。

- 将程序分解成处理计算的函数。你将在第5章中探索函数。

- 将该程序实现为图形用户界面程序，当任何值发生变化时，自动更新相关的值。


```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>简单的数学处理</title>
</head>
<body>
  <h1>What is the first number?</h1>
  <input type="text">
  <h1>What is the second number?</h1>
  <input type="text">
  <p id="content"></p>
  <script>
    var firstInput = document.getElementsByTagName('input')[0]
    var secondInput = document.getElementsByTagName('input')[1]
    var content = document.getElementById('content')

    function calculate(firstInput, secondInput) {
      var firstValue = parseInt(firstInput.value)
      var secondValue = parseInt(secondInput.value)

      return `${firstValue} + ${secondValue} = ${firstValue + secondValue}
              ${firstValue} - ${secondValue} = ${firstValue - secondValue}
              ${firstValue} * ${secondValue} = ${firstValue * secondValue}
              ${firstValue} / ${secondValue} = ${firstValue / secondValue}`
    }

    Array.from(document.getElementsByTagName('input')).forEach(input => {
      input.onchange = function() {
        content.innerText = calculate(firstInput, secondInput)
      }
    })

  </script>
</body>
</html>


```