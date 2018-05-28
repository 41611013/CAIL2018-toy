# 2018中国“法研杯”法律智能挑战赛 CAIL2018

## 大赛官方网站
[2018中国‘法研杯’法律智能挑战赛](http://cail.cipsc.org.cn/index.html)

## 时间节点
- 第一阶段（2018.05.15-2018.07.14）:
 - ~ 6月 5日，基于Small数据的模型提交截至。向评测结果高于基准算法成绩的团队发布Large数据
 - ~ 6月12日，基于Large-test数据对前期模型进行重新评测刷榜
 - ~ 7月14日，最终模型提交截至。
- 第二阶段（2018.07.14-2018.08.14）:
 - 主办方根据一个月的新增数据对最终模型进行封闭评测

## Updates

### 2018-05-18 [feng]
- 数据文件太大，将文件夹从项目中删除
- 默认数据目录为`../data/CAIL2018-small-data`，见`util.py`文件`DATA_DIR`常量
- ~~使用清华中文分词工具[thulac-python](https://github.com/thunlp/THULAC-Python)~~
- thulac分词工具速度过慢，暂时使用jieba，后续可以考虑C++版本的各种分词工具
- **Notice**：法条预测中，有些案件对应多个法条
- 添加`util.py`文件
- 添加`preprocess.py`文件，对数据进行中文分词，整合json2csv文件函数
- 添加`stopwords.txt`文件，来源[GitHub · stopwords-iso/stopwords-zh](https://github.com/stopwords-iso/stopwords-zh)

### 2018-05-26  [feng]
- 使用jieba多线程分词
- 导入从[搜狗词库](https://pinyin.sogou.com/dict/)下载的法律词典
- 删除`CODE_OF_CONDUCT.md`文件
- 添加`dictionary/`文件夹，包含用户词典及由`.scel`(搜狗的用户词典文件)文件解码处理的代码
- 修正`util.py`中的24行的一处bug

### 2018-05-28  [feng]
- 重新组织代码结构，依照官方提供[svm_baseline](https://github.com/thunlp/CAIL2018/tree/master/baseline)代码
- 删除`preprocess.py`
- 添加`train.py`文件, `./predictor/`目录等

## 团队成员

Team name: 陈-冯-杨

陈子彧 [@mcorange1997](https://github.com/mcorange1997)

冯柏淋 [@FengBli](https://github.com/FengBli)

杨凌宇 [@Scott1123](https://github.com/Scott1123)
