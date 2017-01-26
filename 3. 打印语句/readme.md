# 打印语句
创建一个程序，提示用户输入一条引语及其作者。按照实例输出那样显示引语和作者。
实例输出
```shell
What is the quote? These aren't the droids you're looking for.
Who said it? Obi-Wan Kenobi
Obi-Wan Kenobi says, "These aren't the droids you're looking for"
```

约束

- 使用一条输出语句来生成该输出，使用适当的字符串转义技术来处理引语。
- 不要使用字符串插入和替换，要使用字符串连接

挑战
- 修改这个程序，不再提示用户输入语句，而是创建一个保存引语及其作者的结构，然后使用例子中的格式显示所有的引语。由映射(map)组成的数组会是个不错的选择。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>打印语句</title>
</head>
<body>
  <p id="content"></p>
  <script>
    var op = document.getElementById('content')
    op.innerText = "What is the quote? These aren't the droids you're looking for.\n" +
                   "Who said it? Obi-Wan Kenobi\n" +
                   "Obi-Wan Kenobi says, \"These aren't the droids you're looking for\""

  </script>
</body>
</html>
```