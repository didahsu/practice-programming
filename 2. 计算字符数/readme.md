# 计算字符数
创建一个程序，提示用户输入字符串，然后输出这个字符串，以及其中的字符数。

示例输出
```shell
What is the input steing? Homer
Homer has 5 characters.
```
约束
- 确保输出中包含原始的字符串
- 使用一个输出语句来构造输出
- 使用所有编程语言中的一个内置函数来确定字符串的长度

挑战
- 如果用户什么都没输入、提示用户输入内容
- 使用图形用户界面实现改程序，在每次键盘按下是，更新字符字数信息。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>计算字符数</title>
</head>
<body>
  <h1>What is the input string?</h1>
  <input type="text" placeholder="请输入字符">
  <span id="prompt">请输入内容！</span>
  <p id="output"></p>
  <script>
    var oinput = document.getElementsByTagName('input')[0]
    var ospan = document.getElementById('prompt')
    var op = document.getElementById('output')

    oinput.onkeyup = function() {
      var num = oinput.value.length
      var text = oinput.value + " has " + num + " characters."
      if (num === 0) {
        ospan.innerText = "请输入内容！"
        op.innerText = ''
        return
      }
      ospan.innerText = ''
      op.innerText = text
    }
  </script>
</body>
</html>

```