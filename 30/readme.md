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
<a name="2195"/>

<div>
<span><div><b>题目描述：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><b>这个题目有两种解法：</b></div><div>首先我们来看一下，一种可以改变原始数组的方法，这个方法的思想就是利用partition的方法来实现的。</div><div>（1）也就是我们以第k个元素为分界点，比他小的就放在左边，大的就放在右边</div><div>（2）我们一直调用partition，知道partition的返回值为k-1</div><div><b>代码如下：</b></div><div><img src="readme_files/Image [1].png" type="image/png" style="height: auto;"/></div><div><br/></div><div>这个题还有另外一种解法：</div><div>就是利用堆，建立一个k个节点的大顶堆，。。。。</div><div>这个算法可以用于海量数据，且不改变原来的数据；</div></span>
</div></body></html> 