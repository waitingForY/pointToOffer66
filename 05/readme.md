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
<a name="1973"/>

<div>
<span><div>题目描述如下：</div><div><img src="剑指offer之从尾到头打印链表_files/Image.png" type="image/png"/></div><div>这道题目也是一个比较常规，简单的题目；</div><div>首先复习一下链表（单链表）的知识（常识）：</div><div>（1）要会写单链表的节点结构（就是上面给出的节点结构）；</div><div>（2）要知道单链表的特点：要找到下一个节点就必须通过上一个节点来找，只要记住这一点就知道了单链表只能顺序访问，不能随机访问（链表的存储是随机的，但访问是顺序的）；</div><div>（3）有关链表的题目（不管是双向链表还是单向链表），最好都要画图来理清思路；</div><div>（4）链表的题目多结合递归的思想来作（有递归时，多想到用栈这种数据结构来考虑）；</div><div>这道题目就用到了递归的思想（栈的思想）</div><div>下面我们就给出递归思想写出的完整代码：</div><div>（尤其要注意的是，递归的时候不能把条件写反了）</div><div><img src="剑指offer之从尾到头打印链表_files/Image [1].png" type="image/png"/></div><div><img src="剑指offer之从尾到头打印链表_files/Image [2].png" type="image/png"/></div><div>下面我们就可以用栈的思想来写出完整的代码：</div><div>这里我们用c++来实现，（利用c++stl中的stack来实现栈）</div><div>完整代码如下：（main函数与上面的main函数一样）</div><div><img src="剑指offer之从尾到头打印链表_files/Image [3].png" type="image/png"/></div></span>
</div></body></html> 