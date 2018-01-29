# python
python学习笔记

此笔记为nlp入门所记，来自Natural Language Processing with Python


day one
nlp   python自然语言处理方面的应用
(1) 关于NLTK入门
    1. 安装NLTk   pip install nltk  
    2. 安装NLTK自带书本  import nltk 
                        nltk.download()  ## 选择book  里面会有9个英文text文本
                        
    3. 常用函数
         ！ 搜索文本 函数名为：concordance  text1.concordance("monstrous")   # 前面需import nltk  此搜索文本函数会搜索出text1中所有含monstrous的句子
         ！ similar 函数   例如 text1.similar("monstrous")   # 会在text1中找出类似于monstrous用法的词  例如 the monstrous picture and the few picture 他会找出few这个词。
         ！ 函数common_contexts 可以研究两个或者两个以上的词共同的上下文  例如 text2.common_contexts(["monstrou","very"])  在text2中找出monstrous和very相同的上下文
         ！ dispersion_plot 自动检测文本中特定的词(大致位置，词的数目)   # text4.dispersion_plot(["citizens","democracy"])可以找出text4中citizens出现的位置，词频并以离散图的形式表示出来。每一竖线代表一个单词，每一行代表整个文本。
         ！ generate   生成类似文本？？？   text3.generate()  # 会产生类似于text3中的风格的文本  它重用了源文本中常见的词和短语，收集词序列的统计信息，进而执行
       
    4.计数词汇
         ！ len(text3)  44764  # 当成是一个列表来处理  会统计词+标点 
         ！ sort(set(text3))  2789  # set对text3进行处理 可以计算text中有多少不同的词   ## set 之后还是存在标点符号
         ！ count  计算一个词在文本中出现次数 text3.count("smote") 5
         
