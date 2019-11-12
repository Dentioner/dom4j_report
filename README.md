# dom4j源码阅读与简析

本文的dom4j版本为2.1.1，由[https://dom4j.github.io](https://dom4j.github.io/)所提供。

本文的内容不是dom4j具体源码实现的解析，也不是dom4j所涉及的算法设计的讨论，仅仅从程序设计的抽象角度进行简单分析。

由于本人水平有限，对java的了解也很浅薄，因此文章不免会出现各种错误，欢迎各位提出意见或建议。

参考资料：

\[1\] [https://www.cnblogs.com/sharpest/p/7877501.html](https://www.cnblogs.com/sharpest/p/7877501.html)

\[2\] [https://developer.mozilla.org/zh-CN/docs/Web/API/Document\_Object\_Model/Introduction](https://developer.mozilla.org/zh-CN/docs/Web/API/Document_Object_Model/Introduction)

\[3\] [https://github.com/dom4j/dom4j/wiki/FAQ](https://github.com/dom4j/dom4j/wiki/FAQ)

\[4\] [https://www.runoob.com/xml/xml-tutorial.html](https://www.runoob.com/xml/xml-tutorial.html)

\[5\] [https://wiki.jikexueyuan.com/project/xml/overview.html](https://wiki.jikexueyuan.com/project/xml/overview.html)

\[6\] [https://blog.csdn.net/chenweitang123/article/details/6255108](https://blog.csdn.net/chenweitang123/article/details/6255108)

\[7\] [https://blog.csdn.net/qq\_38254978/article/details/77870598](https://blog.csdn.net/qq_38254978/article/details/77870598)

\[8\] [https://www.tutorialspoint.com/java\_xml/java\_dom4j\_parser.htm](https://www.tutorialspoint.com/java_xml/java_dom4j_parser.htm)

\[9\] [https://segmentfault.com/a/1190000011332759\#articleHeader0](https://segmentfault.com/a/1190000011332759#articleHeader0)

\[10\] [https://dom4j.github.io/](https://dom4j.github.io/)

\[11\] [https://www.cnblogs.com/huanjianlin/archive/2013/04/03/2997303.html](https://www.cnblogs.com/huanjianlin/archive/2013/04/03/2997303.html)

\[12\] [http://www.saxproject.org/apidoc/org/xml/sax/InputSource.html](http://www.saxproject.org/apidoc/org/xml/sax/InputSource.html)

\[13\] [https://blog.csdn.net/wei\_zhi/article/details/52837635](https://blog.csdn.net/wei_zhi/article/details/52837635)

\[14\] [https://docs.oracle.com/middleware/11119/core/OCLAR/oracle/sdp/presence/integration/DocumentException.html](https://docs.oracle.com/middleware/11119/core/OCLAR/oracle/sdp/presence/integration/DocumentException.html)

\[15\] [http://www.saxproject.org/apidoc/org/xml/sax/EntityResolver.html](http://www.saxproject.org/apidoc/org/xml/sax/EntityResolver.html)

\[16\] [https://blog.csdn.net/zlb824/article/details/7462827](https://blog.csdn.net/zlb824/article/details/7462827)

\[17\] [https://dom4j.github.io/javadoc/1.6.1/org/dom4j/io/SAXContentHandler.html](https://dom4j.github.io/javadoc/1.6.1/org/dom4j/io/SAXContentHandler.html)

\[18\] [http://www.blogjava.net/DLevin/archive/2012/11/18/391545.html](http://www.blogjava.net/DLevin/archive/2012/11/18/391545.html)

\[19\] [https://www.runoob.com/dtd/dtd-tutorial.html](https://www.runoob.com/dtd/dtd-tutorial.html)

\[20\] [https://sbzeng.gitbook.io/fastjson/](https://sbzeng.gitbook.io/fastjson/)

\[21\] [https://2550688560.gitbook.io/dom4j\_guide/chapter1/jian-dan-shi-yong-dom4j](https://2550688560.gitbook.io/dom4j_guide/chapter1/jian-dan-shi-yong-dom4j)



