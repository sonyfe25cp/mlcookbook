本章主要介绍跟分类有关的内容。

分类通常指的是将实例分成不同的类别。根据类别的不同，又分为二类分类（binary classification）和多类分类（multi-class classification）

分类是有监督学习的一种，采用对训练数据进行拟合，然后进行应用。

分类的应用场景有很多：

* 预测广告点击率，也就是区分点或者不点
* 探测欺骗
* 预测是否可以贷款
* 对图片、视频、声音等进行分类，通常都是多类分类
* 给新闻文章、网页或者其他东西打标签，这是另一类多类分类
* 探测垃圾邮件、垃圾评论或者其他行为
* 检测失败原因，如操作系统或者网络中的崩溃原因
* 对用户的购买商品或者服务进行预测排序


##模型分类

从分类算法上来讲，有很多种模型，如：线性模型、决策树、朴素贝叶斯模型等。线性模型相对简单，容易应用到大数据上。决策树是一种非线性的模型，但在大规模应用上有难度，对训练上比较敏感，应用效果较好。朴素贝叶斯模型更简单，但是它更加容易训练和并行化。不同的模型在合适的特征工程辅助下，都能得到合理的性能。一般用朴素贝叶斯作为对比的基线。

###线性模型

$y = f(w^t x)$

####逻辑回归

逻辑回归是个概率模型，它得到的结果是个概率，然后再通过跟阈值的对比，得到分类结果。

$function = \frac{1}{(1+exp(-w^tx))}$

损失函数：$log(1+exp(-yw^tx))$

####线性支持向量机

SVM是个判别模型，它得到的结果就是1或者-1。

###朴素贝叶斯模型

朴素贝叶斯是个概率模型，它得到的也是个概率。它假定每个特征对它的类别都有个独立的贡献，也就是p(y|x_i).于是，每个特征对类别的贡献可以通过统计的方法从数据集中直接计算得到，也就是条件概率；同样的，类别自身的先验概率也可以通过统计得到，即：p(y)。

###决策树

决策树模型是一种非概率模型，可以训练得到非线性特征和特征间关系。

它形成的是一棵树，叶子节点为类别结果，枝为特征。

