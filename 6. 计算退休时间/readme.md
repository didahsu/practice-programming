# 计算退休时间

创建一个程序，确定用户还有多少年退休，并计算退休年份。
它应该提示用户输入当前年龄，以及想要退休的年龄，最终按如下例子这样显示输出。

示例输出
```shell
What is your current age? 25
At what age would you like to retire? 65
You have 40 years left until you can retire.
It's 2015, so you can retire in 2055.
```

约束

- 再次强调，在做任何数学运算之前，务必将输入转换成数值数据。

- 不要将当前的年份硬编码到程序中。通过所用编程语言从系统时间中获取。

挑战

- 处理程序返回负数的情况，提示用户已经可以退休了。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>计算退休时间</title>
</head>
<body>
  <h1>What is your current age?</h1>
  <input type="text">
  <h1>At what age would you like to retire?</h1>
  <input type="text">
  <button type="button">确定</button>
  <p id="content"></p>

  <script>
    var inputAge = document.getElementsByTagName('input')[0]
    var inputRetire = document.getElementsByTagName('input')[1]
    var content = document.getElementById('content')
    var btn = document.getElementsByTagName('button')[0]

    btn.onclick = function() {
      var currentAge = parseInt(inputAge.value)
      var retireAge = parseInt(inputRetire.value)
      var diff = retireAge - currentAge
      var nowYear = new Date().getFullYear()

      if (diff <= 0) {
        content.innerText = '您已经可以退休了！'
      } else {
        content.innerText = `You have ${diff} years left until you can retire.
                             It's ${nowYear}, so you can retire in ${nowYear + diff}.`
      }

      
    }

  </script>
</body>
</html>
```


