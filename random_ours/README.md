#  语句分词presentation by: 向昕宇＆李虹霖 
## 实现算法：HMM 
数据集：人民日报 训练：测试=4：1 <br>
demo：自己一句话即可（不超过15个字） <br>
数据处理：<br>
```
cd data
在DemoData.txt_utf8中写入自己的demo语句
python data_load.py  # 载入训练，测试和demo语句
```
HMM：<br>
```
python hmm_model.py  # train+test+demo
#  如果感觉过慢，可以直接注释掉main中的test()
```
我运行的结果：<br>
```
HMM:
precision:0.87980196
recall:   0.84381022
fscore:   0.86143031
```
demo 展示：<br>
```
GT: 
随机过程 十分 有趣 尤其 是 隐马尔科夫 模型 
OURS: 
[['随', '机'], ['过', '程'], ['有', '点'], ['难', '度'], ['尤', '其'], ['是'], ['隐'], ['马', '尔'], ['科', '夫'], ['模', '型']]
```
BiLSTM+CRF pytorch实现 参考 [ChineseNER](https://github.com/buppt/ChineseNER)<br>
Hmm实现 参考 [HMM](https://github.com/ldanduo/HMM)<br>

