1. 这是ictclas中使用到的字典文件。
   从吕震宇的SharpICTCLAS-1.0中获取。
   与中科院的ictclas for linux版本中附带的字典不一样，本版本应该更详细一些。

   感谢两位前辈！

2. stopwords.txt 与 engstopwords.txt两个文件由原来的GBK编码转成了UTF-8编码。

3.  连同lucene对索引的optimize，处理速度： 581M/3292s = 176K/s，因为词典中短句较多.
   ChineseAnalyzer对普通文章的长句的分词速度大约是76K/s，ICTCLAS的google group中有人实现了15K/s的速度，
    他认为基本可用，看来我的分词程序可用程度更高：）

4. analysis-data下面必须有有bigramdict.dct coredict.dct stopwords_utf8.txt这三个文件。
   bigramdict.mem coredict.mem是上面两个dct文件的内容经过处理得到，
   他们可以直接载入内存，因此节省了每次都解析处理dct的时间（约10s），
   第一次运行时会自动生成mem文件，因此第二次运行时会快很多。
//!   
