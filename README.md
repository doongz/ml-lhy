# Machine Learning

## Introduction

- 所属大学：國立台灣大學
- 授课老师：李宏毅
- 先修要求：熟练掌握 Python
- 编程语言：Python
- 课程难度：🌟🌟🌟🌟
- 预计学时：80 小时
- 学年：Spring 2022

李宏毅老师是国立台湾大学的教授，其风趣幽默的授课风格深受大家喜爱，并且尤其喜欢在 PPT 中插入宝可梦等动漫元素，是个非常可爱的老师。

这门课挂着机器学习的牌子，但其课程内容之广实在令人咋舌，其作业一共包含 15 个 lab，分别是 Regression、Classification、CNN、Self-Attention、Transformer、GAN、BERT、Anomaly Detection、Explainable AI、Attack、Adaptation、 RL、Compression、Life-Long Learning 以及 Meta Learning。可谓是包罗万象，能让学生对于深度学习的绝大多数领域都有一定了解，从而可以进一步选择想要深入的方向进行学习。

大家也大可不必担心作业的难度，因为所有作业都会提供助教的示例代码，帮你完成数据处理、模型搭建等，你只需要在其基础上进行适量的修改即可。这也是一个学习别人优质代码的极好机会，大家需要水课程大作业的话，这里也是一个不错的资料来源。

## Resources

- 课程网站：https://speech.ee.ntu.edu.tw/~hylee/ml/2022-spring.php
- 课程视频：https://www.youtube.com/playlist?list=PLJV_el3uVTsPM2mM-OQzJXziCGJa8nJL8
- 课程作业：15 个 lab，几乎覆盖了主流深度学习的所有领域，参见课程网站
- 参考书籍：《Dive into Deep Learning》https://d2l.ai/

## Notes

### Lecture 1: Introduction of Deep Learning

介绍了些本门课可以学到的东西

### Lecture 2: What to do if my network fails to train

为什么参数越多，越容易 overfit

训练集不好

<img src="./images/image-20230108182217458.png" alt="image-20230108182217458" style="zoom:50%;" />

<img src="./images/image-20230108183339463.png" alt="image-20230108183339463" style="zoom:50%;" />

<img src="./images/image-20230108183422655.png" alt="image-20230108183422655" style="zoom:50%;" />

<img src="./images/image-20230108215257508.png" alt="image-20230108215257508" style="zoom:50%;" />

Optimization Fails

<img src="./images/image-20230210205926945.png" alt="image-20230210205926945" style="zoom:50%;" />

<img src="./images/image-20230210211430195.png" alt="image-20230210211430195" style="zoom:50%;" />

为什么 small batch 的效果要好，因为在另一个损失函数中就不是 critical point

<img src="./images/image-20230210211810177.png" alt="image-20230210211810177" style="zoom:50%;" />

<img src="./images/image-20230210211756412.png" alt="image-20230210211756412" style="zoom:50%;" />

<img src="./images/image-20230210212251337.png" alt="image-20230210212251337" style="zoom:50%;" />

<img src="./images/image-20230210214209299.png" alt="image-20230210214209299" style="zoom:50%;" />

<img src="./images/image-20230210214409150.png" alt="image-20230210214409150" style="zoom:50%;" />

Tips for training: **Adaptive Learning Rate**

<img src="./images/image-20230210221116963.png" alt="image-20230210221116963" style="zoom:50%;" />

客制化的 learning rate

<img src="./images/image-20230211214337185.png" alt="image-20230211214337185" style="zoom:50%;" />

<img src="./images/image-20230211214403013.png" alt="image-20230211214403013" style="zoom:50%;" />

### Lecture 3: Image as input

cnn

<img src="./images/image-20230205125441972.png" alt="image-20230205125441972" style="zoom:50%;" />

<img src="./images/image-20230205131700429.png" alt="image-20230205131700429" style="zoom:50%;" />

<img src="./images/image-20230205132102613.png" alt="image-20230205132102613" style="zoom:50%;" />

<img src="./images/image-20230205132131344.png" alt="image-20230205132131344" style="zoom:50%;" />

深度学习好在哪

ReLU 进行叠加 + 常数可代表任何方程

<img src="./images/image-20230108223304383.png" alt="image-20230108223304383" style="zoom:50%;" />

<img src="./images/image-20230108223414917.png" alt="image-20230108223414917" style="zoom:50%;" />

<img src="./images/image-20230108230226158.png" alt="image-20230108230226158" style="zoom:50%;" />

<img src="./images/image-20230108232105650.png" alt="image-20230108232105650" style="zoom:50%;" />

### Lecture 4: Sequence as input

<img src="./images/image-20230205135807348.png" alt="image-20230205135807348" style="zoom:50%;" />

<img src="./images/image-20230205142626232.png" alt="image-20230205142626232" style="zoom:50%;" />

step-1 从 a_i 得到 q k v 的矩阵

<img src="./images/image-20230205143344853.png" alt="image-20230205143344853" style="zoom:50%;" />

step-2 K 和 Q 的矩阵乘 得到 A 矩阵

<img src="./images/image-20230205143822509.png" alt="image-20230205143822509" style="zoom:50%;" />

step-3 V 和 A 的矩阵乘得到 O 矩阵

<img src="./images/image-20230205144116182.png" alt="image-20230205144116182" style="zoom:50%;" />

并发能力由硬件提供，整个过程需要训练的是 q k v 的 weight 矩阵

<img src="./images/image-20230205144211354.png" alt="image-20230205144211354" style="zoom:50%;" />

<img src="./images/image-20230205151409655.png " alt="image-20230205151409655" style="zoom:50%;" />

<img src="./images/image-20230205151633597.png" alt="image-20230205151633597" style="zoom:50%;" />

self-attention vs CNN

- CNN 是 self-attention 的特例，CNN 的 receptive field 是固定的，self-attention 的 receptive field 是可变的，甚至是全图，甚至是可以训练的
- 训练集小的时候 CNN 效果好些，在大训练集上 self-attention 效果更好

<img src="./images/image-20230205152152888.png" alt="image-20230205152152888" style="zoom:50%;" />

self-attention vs RNN

- RNN 中的输入是有距离的（第一个输入在最后面的计算时慢慢会被遗忘），self-attention 中所有的输入都是平等的
- RNN 只能一个一个去算，self-attention 可以并行计算

### Lecture 5: Sequence to sequence

<img src="./images/image-20230207233649899.png" alt="image-20230207233649899" style="zoom:50%;" />

encoder

<img src="./images/image-20230207233738684.png" alt="image-20230207233738684" style="zoom:50%;" />

decoder

<img src="./images/image-20230208221948200.png" alt="image-20230208221948200" style="zoom:50%;" />

<img src="./images/image-20230208222141298.png" alt="image-20230208222141298" style="zoom:50%;" />

<img src="./images/image-20230208223416137.png" alt="image-20230208223416137" style="zoom:50%;" />

<img src="./images/image-20230208225443220.png" alt="image-20230208225443220" style="zoom:50%;" />

training

<img src="./images/image-20230208231147154.png" alt="image-20230208231147154" style="zoom:50%;" />

Tips

<img src="./images/image-20230208231422408.png" alt="image-20230208231422408" style="zoom:50%;" />

Scheduled Sampling

<img src="./images/image-20230208234349083.png" alt="image-20230208234349083" style="zoom:50%;" />

各式各樣的 Attention

<img src="./images/image-20230210204520913.png" alt="image-20230210204520913" style="zoom:50%;" />

<img src="./images/image-20230210204627492.png" alt="image-20230210204627492" style="zoom:50%;" />

<img src="./images/image-20230210204753892.png" alt="image-20230210204753892" style="zoom:50%;" />

通过改变矩阵乘的顺序来降低计算量

<img src="./images/image-20230210204834366.png" alt="image-20230210204834366" style="zoom:50%;" />

<img src="./images/image-20230210204924461.png" alt="image-20230210204924461" style="zoom:50%;" />

### Lecture 6: Generation

<img src="./images/image-20230212171042161.png" alt="image-20230212171042161" style="zoom:50%;" />

<img src="./images/image-20230212171908913.png" alt="image-20230212171908913" style="zoom:50%;" />

<img src="./images/image-20230212173910051.png" alt="image-20230212173910051" style="zoom:50%;" />

风格迁移

<img src="./images/image-20230212213444288.png" alt="image-20230212213444288" style="zoom:50%;" />

<img src="./images/image-20230212214109109.png" alt="image-20230212214109109" style="zoom:50%;" />

### Recent Advance of Self-supervised learning for NLP

BERT: https://leemeng.tw/attack_on_bert_transfer_learning_in_nlp.html

<img src="./images/image-20230219213117374.png" alt="image-20230219213117374" style="zoom:50%;" />

<img src="./images/image-20230219213733819.png" alt="image-20230219213733819" style="zoom:50%;" />

<img src="./images/image-20230219214255436.png" alt="image-20230219214255436" style="zoom:50%;" />

<img src="./images/image-20230219214731632.png" alt="image-20230219214731632" style="zoom:50%;" />

...

<img src="./images/image-20230219215149932.png" alt="image-20230219215149932" style="zoom:50%;" />

<img src="./images/image-20230219215547329.png" alt="image-20230219215547329" style="zoom:50%;" />

<img src="./images/image-20230219220128778.png" alt="image-20230219220128778" style="zoom:50%;" />

### Lecture 7: Self-supervised learning for Speech and Image

1. Generative Approaches

<img src="./images/image-20230221224028165.png" alt="image-20230221224028165" style="zoom:50%;" />

<img src="./images/image-20230221224043308.png" alt="image-20230221224043308" style="zoom:50%;" />

<img src="./images/image-20230221224310876.png" alt="image-20230221224310876" style="zoom:50%;" />

<img src="./images/image-20230221224413124.png" alt="image-20230221224413124" style="zoom:50%;" />

2. Predictive Approach

<img src="./images/image-20230221225039622.png" alt="image-20230221225039622" style="zoom:50%;" />

3. Contrastive Learning

<img src="./images/image-20230221225737652.png" alt="image-20230221225737652" style="zoom:50%;" />

<img src="./images/image-20230221230258071.png" alt="image-20230221230258071" style="zoom:50%;" />

### Lecture 8: Auto-encoder/ Anomaly Detection

<img src="./images/image-20230222220243772.png" alt="image-20230222220243772" style="zoom:50%;" />

<img src="./images/image-20230222220925680.png" alt="image-20230222220925680" style="zoom:50%;" />

<img src="./images/image-20230222223433760.png" alt="image-20230222223433760" style="zoom:50%;" />

### Lecture 9: Explainable AI

<img src="./images/image-20230224224032047.png" alt="image-20230224224032047" style="zoom:50%;" />

<img src="./images/image-20230224225532342.png" alt="image-20230224225532342" style="zoom:50%;" />

<img src="./images/image-20230224230356847.png" alt="image-20230224230356847" style="zoom:50%;" />

### Lecture 10: Attack

白盒攻击：知道模型和模型参数，输入的图片作为参数进行训练，既能让输出为另一个东西，同时也和原图片还很相同

<img src="./images/image-20230227230142745.png" alt="image-20230227230142745" style="zoom:50%;" />

<img src="./images/image-20230227230901029.png" alt="image-20230227230901029" style="zoom:50%;" />

<img src="./images/image-20230227232352463.png" alt="image-20230227232352463" style="zoom:50%;" />

黑盒攻击：不知道模型，用同一个数据集训练一个模型，对自己的模型进行攻击，那么训练好的输入图片，对要攻击的模型同样有效

<img src="./images/image-20230228223103633.png" alt="image-20230228223103633" style="zoom:50%;" />

<img src="./images/image-20230228225418185.png" alt="image-20230228225418185" style="zoom:50%;" />

<img src="./images/image-20230228230428890.png" alt="image-20230228230428890" style="zoom:50%;" />

<img src="./images/image-20230228231122088.png" alt="image-20230228231122088" style="zoom:50%;" />

<img src="./images/image-20230228231305462.png" alt="image-20230228231305462" style="zoom:50%;" />

### Lecture 11: Adaptation

<img src="./images/image-20230302225233152.png" alt="image-20230302225233152" style="zoom:50%;" />

<img src="./images/image-20230302230041993.png" alt="image-20230302230041993" style="zoom:50%;" />

### Lecture 12: Reinforcement Learning

### Lecture 13: Network Compression

### Lecture 14: Life-long Learning

### Lecture 15: Meta Learning
