# 疯狂填词

创建一个简单的疯狂填词程序，提示用户输入一个名词、一个动词、一个形容词和一个副词，然后将这些词插入到所创建的故事中。

实例输出
```shell
Enter a noun: dog
Enter a verb: walk
Enter an adjective: blue
Enter an adverb: quickly
Do you walk your blue dog quickly? That's hilarious!
```

约束

- 在程序中使用一条输出语句。

- 如果所用语言支持字符串插入或替换，则使用它来构造输出。

挑战

- 向程序中添加更多输入，扩展故事。

- 实现一个带有分支发展的故事，可以根据问题的答案来确定如何构造故事。在第4章的问题中，你将进一步探索这个概念。

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>疯狂填词</title>
</head>
<body>
  <input type="text" placeholder="enter a noun">
  <input type="text" placeholder="enter a verb">
  <input type="text" placeholder="enter a adjective">
  <input type="text" placeholder="enter a adverb">
  <button type="button" id="btn">确定</button>  
  <p id="content"></p>


  <script>
    var btn = document.getElementById('btn')
    var content = document.getElementById('content')
    var inputs = document.getElementsByTagName('input')

    btn.onclick = function() {
      var str = `do you ${inputs[1].value} your ${inputs[2].value} ${inputs[0].value} ${inputs[3].value}? That's hilarious!`
      content.innerHTML = str
    }
  </script>
</body>
</html>

```