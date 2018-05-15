# udacity-commit P1
### 主要记录了Udacity中做的项目
- 画图部分老师给的优化建议，尽量不要有重复的代码，可以用循环实现 %config InlineBackend.figure_format = 'retina' 可以让图像更清晰一些
<pre><code> 
import matplotlib.pyplot as plt
# 使输出的图像以更高清的方式显示
%config InlineBackend.figure_format = 'retina'
# 调整图像的宽高
plt.figure(figsize=(16, 4))
for i, key in enumerate(['RM', 'LSTAT', 'PTRATIO']):
    plt.subplot(1, 3, i+1)
    plt.xlabel(key)
    plt.scatter(data[key], data['MEDV'], alpha=0.5)
</code></pre> 

- 补充一种判断属性关联度的方法

<pre> <code>
import seaborn as sns
sns.heatmap(data.corr(), annot=True)
</pre> </code>

#### numpy统计上常用的函数：<https://docs.scipy.org/doc/numpy/reference/routines.statistics.html> <p>

#### skearn对于常见的模型表现衡量方法也有详细的介绍<http://scikit-learn.org/stable/modules/model_evaluation.html>

#### 这里还有更多关于学习曲线的介绍：
<https://www.coursera.org/learn/machine-learning/lecture/Kont7/learning-curves> <p>
<http://scikit-learn.org/stable/auto_examples/model_selection/plot_learning_curve.html><p>
#### 华盛顿大学机器学习的课程详细讲了这个问题 <https://www.coursera.org/learn/ml-regression/home/week/3><p>
#### 维基百科对此偏差和方差有详细的解释 <https://en.wikipedia.org/wiki/Bias%E2%80%93variance_tradeoff><p>

- 交叉验证
sklearn 也有对 validation curve的介绍：<http://scikit-learn.org/stable/modules/learning_curve.html><p>
- k-fold

#### k-fold是将**训练集**分为k份，而不是数据集，注意这里的差别。<p>
#### 对于网格搜索算法和K折交叉验证，你可以参考这篇文章来帮助自己更好地理解：<https://zhuanlan.zhihu.com/p/25637642><p>
-关于敏感性分析
#### 关于敏感性分析更多的知识可以参考 <https://en.wikipedia.org/wiki/Sensitivity_analysis>
