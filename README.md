# PCA算法的Matlab实现

* X : m行n列数据，每行为1个样本，每个样本维度为n
* dims : 目标维度
* Wlda : n行dims列投影向量
* PCA原理推导在我的个人博客 [www.liangtianming.com](http://www.liangtianming.com/2017/10/31/PCA/)
* 问题和讨论可以发到我的邮箱 tm.liang@outlook.com
* 2017.11.1

---

## 下面利用 *knn* 进行图像识别，检测PCA效果

* 训练集X : 120*1024, 每行为1个图像样本，每个样本维度为1024
* 训练集标签gptn : 1*120, 共有15类
* 测试集Y : 45*1024, 每行为1个图像样本，每个样本维度为1024
* 测试集标签gptt : 1*45,共有15类

---

* 原始数据:

  ![](https://raw.githubusercontent.com/Leungtamir/mymarkdownphoto/master/pca_img/v.png)

* 正确率:

  ![](https://raw.githubusercontent.com/Leungtamir/mymarkdownphoto/master/pca_img/w.png)

* 使用PCA降维到20维后的数据:

  ![](https://raw.githubusercontent.com/Leungtamir/mymarkdownphoto/master/pca_img/x.png)

* 正确率:

  ![](https://raw.githubusercontent.com/Leungtamir/mymarkdownphoto/master/pca_img/z.png)

**可见，PCA使数据从1024维降到20维，仅仅牺牲了 *4%* 左右的正确率，这对于不过分牺牲正确率的前提下，提高高维数据处理的效率，避免维数灾难，有着相当好的效果。**

* 使用PCA降维到70维时，正确率为:

  ![](https://raw.githubusercontent.com/Leungtamir/mymarkdownphoto/master/pca_img/y.png)

**和原始数据的识别正确率相同，因此PCA能把1024维数据降到70维并且保持正确率不变，对于本样本来说，70维是最好选择**
