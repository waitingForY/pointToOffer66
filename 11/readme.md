<html>
<head>
  <title>Evernote Export</title>
  <basefont face="微软雅黑" size="2" />
  <meta http-equiv="Content-Type" content="text/html;charset=utf-8" />
  <meta name="exporter-version" content="Evernote Windows/302292 (zh-CN); Windows/10.0.10586 (Win64);"/>
  <style>
    body, td {
      font-family: 微软雅黑;
      font-size: 10pt;
    }
  </style>
</head>
<body>
<a name="2043"/>

<div>
<span><div><b>题目描述：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>分析：</b></div><div>这个题看似简单，但是要考虑全面（包括指数是否为负，0，正的情况），还要考虑到程序的执行效率；</div><div>这就需要认真重新审视这个题目了；</div><div><br/></div><div>这个题目考虑到效率，我们可以分为指数为偶数和指数为奇数来考虑，</div><div>（1）如果指数为偶数那么就只需要算指数的二分之一的指数，然后再平方；比如要算n的8次方，那么就只需要算n的4次方，在平方；</div><div>（2）如果指数为奇数，同样的道理，只需要算指数的二分之一，然后平方，只是最后还要在乘一次低数；</div><div>（3）为了提过效率，指数的二分之一，我们用位移运算来表示（向右移表示除2）；</div><div>（同时要判断指数的奇偶性，我们也用位运算来做，也就是看最后一位是否为1，所以我们利用指数去与上Ox1，如果结果为1，表示为奇数，如果结果为0表示为偶数）</div><div><br/></div><div>有了上面的分析我们就可以写出如下的代码了：</div><div><img src="readme_files/Image [1].png" type="image/png" style="height:auto;" width="576"/></div><div><img src="readme_files/Image [2].png" type="image/png" style="height:auto;" width="499"/></div><div><br/></div></span>
</div></body></html> 