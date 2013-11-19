yuliao_nlp
==========
备忘2：
首先在原始的数据中保留带有“省”“市”“县”“区”的微博，保存到weiboout中，记做match001-out,match002-out...match547-out.
保存在D:\Weibo-data\省市县分词\weiboout-shixian\；而后需要用editplus把文件编码转换成UTF-8,覆盖原来的文件。

而后对match*-out进行分词，而后计算词频，结果保存在D:\Weibo-data\省市县分词\weibooutcome
记做fenci001-out fenci002-out.....

而后用replace pinoneer把fenci*-out文件merge成为一个文件，记做fencioutcome.txt
放在D:\weibooutdata\matchdata-shixian文件夹下。

而后我们对fencioutcome.txt转码为UTF-8，记做fencioutcome-utf8.txt

而后我们用该文件与五百姓氏的简繁体进行对照，留住对照之后的词语，记做fenciname.txt

把fenciname.txt中所有的空格变成制表符，记做fenciname-tab.txt;

将fenciname-tab导入到stata，去除那些重复的单词，只保留一个id即可，记做fenciname-simple.txt

之后将其导入到excel，用len函数计算字数，按照字数排序，记做fenciname-quan.xlsx

而后去除单字以及大于等于5字数的单词，保存为fenciname-simple.xlsx



备忘3：
原始数据保存在D:\Weibo-data\splitted.文件名是weibo001, weibo002....weibo547.txt

而后我们对其进行分词，计算词频。输出到D:\Weibo-data\全面分词\weiboout-newest，记做weibo001-out.....


而后用replace pinoneer把weibo*-out文件merge成为几个文件（merge为一个文件太大了，所以分成几个），存储在D:\weibooutdata\Originaldata
每一个文件都有一个ANSI与UTF-8版本。

而后我们用这些文件与五百姓氏的简繁体一一进行对照，留住对照之后的词语。记做weiboout×，文件找不到了，应该是删除了。

之后把这些文件merge到一起，记做allname.txt 放在D:\weibooutdata\matchdata


所以如果我们在备忘2之中找到的单词，如果我们希望知道其在每天出现的频次等，可以反过来回溯到allname.txt中。
