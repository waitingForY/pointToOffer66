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
<a name="2075"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>分析：</b></div><div><br/></div><div>（1）这个题有一点技巧，如果想要快速的找到倒数第k个节点，（也就是只需遍历一遍就要求能够找出）</div><div>这样以来就可以利用两个指针来找，使得这两个指针的间隔为k，那么前面那个指针到达链表最后时，第二个指针所指的位置就是倒数第k个节点；</div><div><br/></div><div>（2）有了上面这个技巧之后，我们还必须考虑到这个题目的各种特殊情况，要考虑全面；</div><div>如果输入的k&lt;=0，或者k已经超过了整个链表的长度了，我们就应该抛出异常来；</div><div><br/></div><div>经过上面的分析，我们就不难写出如下完整的代码了：</div><div><img src="readme_files/Image [1].png" type="image/png" style="height:auto;" width="575"/></div></span>
</div></body></html> 