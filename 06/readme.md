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
<a name="1985"/>

<div>
<span><div>题目描述如下：</div><div><img src="剑指offer之重建二叉树_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div>首先来回顾一下关于二叉树的一些知识：</div><div><b>（1）要会定义二叉树的节点结构：</b></div><div>struct BTreeNode</div><div>{</div><div>     int value；</div><div>     struct BTreeNode* left；</div><div>     struct BTreeNode* right；</div><div>}</div><div><br/></div><div><b>（2）要知道二叉树的三种遍历算法（先序，中序，后序），包括非递归，和递归的算法；</b></div><div>后面遇到相关题目在做详细讨论；</div><div><b>（3）针对这个题目：二叉树的重构问题是有条件的：必须知道两个遍历序列（且每个节点的值互不相同），另外一个就是这两个序列也是有要求你的；这两个序列中必须要有中序；</b></div><div><br/></div><div>下面我们就来看一下这个题目的解题思路：</div><div>（1）首先要知道在先序遍历序列中（根-&gt;左-&gt;右），第一个出现的一定是跟节点；在中序遍历序列中（左-&gt;根-&gt;右），找到根节点后，其左边的都是左子树，右边的都是右子树；</div><div>（2）第一步是在先序序列中找到根；让后在中序序列中找到根；</div><div>（3）第二步是在中序序列中求出左子树的长度（leftlen），也就是左子树有多少个节点（根的左边都是左子树），右子树的长度（rightlen）；</div><div>（4）接下来我们就知道了1&gt;在先序序列中leftlen这么长的序列就是左子树的先序遍历序列，后面的rightlen就是右子树的先序遍历序列；</div><div>                                      2&gt;在中序遍历序列根的前面就是左子树的中序遍历序列，根的后面就是右子树的中序遍历序列；</div><div>（5）接下来就可以递归调用分别对左右子树进行构造（条件是只要他们的序列长度大于0）</div><div><br/></div><div>更加上面的分析我们就很容易写出如下完整的代码了；</div><div><br/></div><div><br/></div></span>
</div></body></html> 