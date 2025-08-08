This will be a file introducing the theoretical principle of support vector machine.

SVM是监督学习(Supervised Learning) [^1] 中的一种算法，主要用于求解分类问题 [^2]。
分类问题最基本的想法就是基于训练集在样本空间中找到一个划分超平面 [^3] ，将不同类别的样本分开。但能将训练样本分开的划分超平面可能有很多，如下图所示，存在多个划分超平面将两类训练样本分开，应该选哪一条呢？实际上，我们应选择“正中间”的黄色线, 对局部扰动容忍性好, 鲁棒性(robust)高, 对未见示例的泛化能力最强。

![svm_classification](image\svm_classification.png)

用数学语言来讲，就是给定训练样本集 $$D=\{(x_1^a, x_1^b), (x_2^a, x_2^b), (x_3^a, x_3^b),……(x_m^a, x_m^b)\}, y_i \in \{-1,+1\}$$ , 





使得两类样本中**距离它最近的样本点距离最大**。

## Reference

[^1]: 在监督学习中训练数据既有 **特征(feature)** 又有 **标签(label)** ，通过训练，让机器可以自己找到特征和标签之间的联系，在面对只有特征没有标签的数据时，可以判断出标签。
[^2]: 分类(classification)问题指的是输出的数据类型是离散数据，回归（regression）问题指的是输出的是连续数据类型。
[^3]: 准确地讲，“一条线或者平面”被称作超平面（hyperplane）。超平面是指n维线性空间中维度为n-1的子空间。它可以把线性空间分割成不相交的两部分。比如二维空间中，一条直线是一维的，它把平面分成了两块；三维空间中，一 个平面是二维的，它把空间分成了两块。
![hyperplane](image\hyperplane.png)
图源：Hardin, D., Guyon, I., & Aliferis, C. F. (2011). A Gentle introduction to support vector machines in biomedicine. 



