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
<a name="2025"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="（8）剑指offer之旋转数组中的最小值_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>首先分析：</b></div><div>这个题目考查二分查找：</div><div>首先要弄清旋转数组的特点：</div><div><b>针对这个题目，由于是通过一个递增数组旋转而来的；所以这个旋转数组一定具备以下几个特点：</b></div><div>1&gt;整个数组被旋转位置分为两个递增的序列，前面递增的序列一定都大于后面递增的序列；</div><div>2&gt;整个数组的最小值一定位于后面递增序列的第一个元素；</div><div><br/></div><div><b>鉴于以上两个特点我们可以用二分查找来求解这个题；下面给出求解步骤；</b></div><div>1&gt;和二分查找一样利用两个指针：一个指针p1指向序列的第一个元素（也就是前面那个递增序列的最小值），两一个指针p2指向序列的最后一个元素（也就是后面那个递增序列的最大值）；</div><div>2&gt;如果p1的值比p2的值都大就继续向中间靠拢；</div><div>3&gt;p1,p2向中间靠拢的步长不是一步一步地靠拢的，而是求p1与p2的中间位置，把这个中间值与p1与p2进行比较，然后看：</div><div>如果中间值比p1还大，那么p1就移到这个中间位置上，如果这个中间位置的值比p2还小，那么就把p2向中间移动到中间位置来；</div><div>4&gt;如果p1，中间位置，以及p2这三个位置的值都相等，那么就必须要顺序查找（这里可以试想一个顺序查找的函数）</div><div>5&gt;最后p1，与p2就相差1，那么p2所指向的元素就是最小值；</div><div><br/></div><div>根据上面的分析，我们可以写出完整的代码了；</div><div><br/></div></span>
</div></body></html> 