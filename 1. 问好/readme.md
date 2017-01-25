# 1. 问好

示例输出

```shell
What is your name? Brian
Hello, Brian, nice to meet you!
```

约束
- 输入、字符串链接和输出这几个部分要分开

挑战
- 不使用任何变量，编写一个新版本的程序。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  <h1>what is your name?</h1>
  <input type="text" placeholder="请输入您的名字">
  <button type="button" id="btn">确定</button>
  <p id="content"></p>
  <script>
    var btn = document.getElementById('btn')
    var content = document.getElementById('content')

    function sayHello (name) {
      var result = "Hello, " + name + ", " + "nice to meet you!"
      return result
    }
    btn.onclick = function() {
      var name = document.getElementsByTagName('input')[0].value
      var str = sayHello(name)
      content.innerText = str
    }
  </script>
</body>
</html>

```