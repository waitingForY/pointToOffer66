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
<a name="2059"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>分析：</b></div><div>这个题有明确的要求在时间复杂度为O(1)的情况下删除指定的节点；</div><div>根据单链表的特点，如果我们要删除某一个节点，就势必要找到他的前一个节点，然后把他的前一个节点接到删除节点的后面，那个结点点上；</div><div>但是这样做肯定会从头去找到删除节点的前一个节点，这样时间复杂度就变为O(n)了，所以这样做是不行的；</div><div><br/></div><div>那么我们换一个思维，既然没办法在O(1)的情况下找到前一个节点，那么我们可以在O(1)找到下一个节点，</div><div>所以我们不删除当前节点，而去改为删除下一个节点，而把下一个节点的值保存到当前节点，</div><div>这样不就达到了目的了吗？</div><div><br/></div><div>但是这个思路是有一个局限的，如果想删除最后一个节点，还是必须从头开始找到前一个节点，然后把前一个节点的next变为空，让后再free掉最后一个节点；</div><div><br/></div><div>这个题由于比较简单，我们这里就不给出代码实现了；</div><div><img src="readme_files/Image [1].png" type="image/png"/></div><div><img src="readme_files/Image [2].png" type="image/png"/></div></span>
</div></body></html> 