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
<a name="2013"/>

<div>
<span><div><b>题目描述如下：</b></div><div><img src="（7）剑指offer之用两个栈实现队列_files/Image.png" type="image/png" style="height: auto;"/></div><div><br/></div><div><b>下面来分析一下这个题目：</b></div><div><br/></div><div>总的来说这个题目是一个比较简单的常规题目；</div><div><b>（1）首先要定义出这个自定义队列的数据结构（这里我们用c++的类来实现）</b></div><div>class Mqueue</div><div>{</div><div>     public：</div><div>          Mqueue（）；</div><div>          ~Mqueue（）；</div><div>          void appendTail（const int&amp; element）；</div><div>          int deleteHead（）；</div><div>     private：</div><div>          stack&lt;int&gt;stack1;</div><div>          stack&lt;int&gt;stack2;</div><div>}</div><div><b>（2）这个队列我们主要就是要实现入队列appendTail方法以及出队列deleteHead方法；</b></div><div><b>（3）有了这些准备之后，我们就来分析一下这两个方法的具体实现思路：</b></div><div>1&gt;appendTail方法：</div><div>因为我们有两个栈结构，我们的入队列的方法就直接将元素push到其中一个栈的栈顶就ok了；这个方法还是比较简单，不用考虑太多；</div><div>2&gt;deleteHead方法：</div><div>这个出队列的方法就要比较复杂了：</div><div>我们必须要考虑到队列的特点（是先进先出的FIFO），因为我们栈的特点是先进后出，所以我们在出队列的时候不能直接将stack1的栈顶弹出；</div><div>而我们必须要利用stack2来过渡一下，从stack2中去弹出元素；</div><div>那么具体怎么过渡呢？</div><div>首先：如果stack2为空的话就要去看stack1是不是为空，如果stack1不为空就要将stack1中的<b>所有</b>元素压到stack2中；</div><div>其次，如果stack2不为空，就直接弹出stack2的栈顶元素就可以了；</div><div><br/></div><div>接下来我们就来实现一下这两个函数：</div><div>void appendTail（const int&amp; element）</div><div>{</div><div>     stack1.push（element）；</div><div>}</div><div><br/></div><div>int deleteHead（）</div><div>{</div><div>     if（stack2.size()&lt;=0）</div><div>     {</div><div>          while（stack1.size()&gt;0）</div><div>          {     </div><div>               int tmp=stack1.top();</div><div>               stack1.pop();</div><div>               stack2.push(tmp);</div><div>          }</div><div>     }</div><div>     if(stack2.size()==0)</div><div>     {</div><div>          printf(&quot;empty queue\n&quot;);</div><div>          exit();    </div><div>     }</div><div>     int head=stack2.top();</div><div>     stack2.pop();</div><div>     return head;</div><div>}</div></span>
</div></body></html> 