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
<a name="2097"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="readme_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>分析：</b></div><div>这个题相对来说有一定的难度：</div><div>我们就借用剑指offer上面的递归解法分析：</div><div>查找子结构可以分为两步走：</div><div>（1）在A中找与B的根相同的节点；其实这一步就是遍历A;遍历一棵树比较简洁的就是用递归；</div><div>所以我们就可以写出如下的代码：（这就相当于先序遍历）</div><div><img src="readme_files/Image [1].png" type="image/png" style="height:auto;" width="598"/></div><div>如果找到了一个节点与B的根节点相同，那么就进入第二步：</div><div>如果当前节点的值不等于B的根节点，那么就去看A的左子树，还没有就去找A的右子树；如果都没有找到，就return false；</div><div><br/></div><div>（2）第二步就是看以A的当前节点为根的子树与B的结构是否相同；这一步我们也可以用递归的思想：</div><div><img src="readme_files/Image [2].png" type="image/png" style="height:auto;" width="599"/></div><div><br/></div><div><b>下面我们就来完整地实现一下这道题目：</b></div><div><img src="readme_files/Image [3].png" type="image/png" style="height: auto;"/></div></span>
</div></body></html> 