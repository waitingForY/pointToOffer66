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
<a name="1915"/>

<div>
<span><div><b>关于单利模式这里我们不以剑指offer的面试题二作为例子，</b></div><div><b>这里我用一个纯c++实现的一个单利模式的写法：</b></div><div><b>15、static与单例模式</b></div><div>（1）单例模式的概念就是，在一个程序中不论调用多少次公共访问接口，整个程序中只会有一个实例存在；</div><div>（2）单利模式的实现由很多种方式，但是要注意几点本质：</div><div>一、构造函数只能调用一次，且必须要保证这个实例能够被正常的析构；</div><div>二、要能够保证不能够被拷贝和赋值，这就要求要将拷贝构造函数和赋值运算符声明为私有的；</div><div>三、为了实现单例模式，必须将构造函数声明为私有的，然后提供一个公有的访问接口；</div><div>四、为了保证这个公有的接口中只调用一次构造函数，我们可以这样干，声明一个局部的静态对象，然后返回他，这样既能保证只调用一次构造函数，也能保证正常的析构；</div><div>当然还有其他的方式；这里给出两种实现方式：</div><div>（1）这也是一种最简单的方式，但是他不是线程安全的；</div><div>class Single</div><div>{</div><div>     public:</div><div>          static Single&amp; getSingle()</div><div>          {</div><div>               static Single single;</div><div>               return single;</div><div>          }</div><div>          ~Single();</div><div>     private:</div><div>          Single(const Single&amp; other);</div><div>          Single&amp; operator=(const Single&amp; other);</div><div>}</div><div><br/></div><div><br/></div><div>（2）</div><div>class Single</div><div>{</div><div>     public:</div><div>          static Single* getSingle()</div><div>          {</div><div>               if(single_==NULL)</div><div>               {</div><div>                         single_=new Single;</div><div>               }</div><div>               return single;</div><div>          }</div><div>          ~Single();</div><div>     private:</div><div>          Single(const Single&amp; other);</div><div>          Single&amp; operator=(const Single&amp; other);</div><div>          static Single* single_;</div><div>}</div><div>但是第二种方式不能够正常的析构这个实例；那么还必须提供一个析构的方式；</div><div>一种方式就是定义一个函数来free掉</div><div>static void free（）</div><div>{</div><div>     if（single_！=NULL）</div><div>          delete single_;</div><div>}</div><div><br/></div><div>但是这种方式有点别扭，我们不知道何时释放好；</div><div>这里我们可以用另外一种方式，定义一个嵌套类来实现释放</div><div>class Single</div><div>{</div><div>     public:</div><div>     class Garbo</div><div>     {</div><div>          ~Garbo（）</div><div>          {</div><div>               if（single_!=NULL）</div><div>                    delete single_;</div><div>          }</div><div>     }</div><div>          static Single* getSingle()</div><div>          {</div><div>               if(single_==NULL)</div><div>               {</div><div>                         single_=new Single;</div><div>               }</div><div>               return single;</div><div>          }</div><div>          ~Single();</div><div>     private:</div><div>          Single(const Single&amp; other);</div><div>          Single&amp; operator=(const Single&amp; other);</div><div>          static Single* single_;</div><div>          static Garbo garbo;</div><div>}</div><div>在类的外面要定义式声明garbo</div><div>Single::Garblo Single::garbo;</div><div><br/></div></span>
</div></body></html> 