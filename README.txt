<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Document</title>
    <script src="../at.js"></script>
</head>
<body>
    <div id="app"></div>
    <script type="text/html" id="module">
        {{myname}}
        {{gender}}
        {{@tag}}
    </script>
    <script>
    let obj = {
        myname:"张鹏",
        gender:"男",
        tag:"<h3>我是傻缺</h3>"
    }

    let myhtml = template("module",obj);
    console.log(myhtml);
    //将渲染好的模板数据内容添加到页面容器
    .querySelector("#app").innerHTML = myhtml;
    </script>
</body>
</html>
