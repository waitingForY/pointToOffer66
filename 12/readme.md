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
<a name="2051"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>分析：</b></div><div>这道题目看似简单，但是有一个陷阱；</div><div>这个陷阱就是，没有告诉这个n到底是多大，有可能这个n位数很大，int等类型根本就没办法存下，所以我们就要考虑大数的表示方法了；</div><div>一种很自然而然的想法就是用字符串来表示这些数；</div><div><br/></div><div>有了这点认识之后，我们要考虑如何表示，如何在这个字符串上加1，如何判断达到了最大，如何输出？</div><div>（1）下面先来看一下如何表示：</div><div>我们可以用一个n+1长度的字符串（因为最后还会有一个‘\0’表示结束）；初始化为‘0’；</div><div>（2）再来看一下如何实现加一，已经如何判断已经达到了最大；</div><div>要实现字符串表示的整数加一，我们是从最后一位开始加一的，判断是否有进位，如果某一位没有发生进位就没有必要循环下去，所以就要有个循环整个字符串（从后向前）</div><div>那么如何快速判断达到了最大了，看第一位是否发生了进位，如果发生了，那么就已经达到了最大，没必要继续下去了</div><div>（3）再来看一下如何打印这个字符串表示的整数呢？</div><div>为了符合我们表示整数的习惯，所以那些以0开头的整数都要去掉开头的0，</div><div>所以我们从第一个不为0的位置开始先后打印；</div><div><br/></div><div>有了上面的分析之后，我们就可以写下完整的代码了！</div><div><img src="readme_files/Image [1].png" type="image/png" style="height: auto;"/></div><div><img src="readme_files/Image [2].png" type="image/png" style="height: auto;"/></div></span>
</div></body></html> 