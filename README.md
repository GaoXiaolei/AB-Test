## AB-Test

本项目通过给定的包含新旧页面时间戳、转化率等信息的网站流量数据集，帮助公司分析是否应该设计新页面、保留原有网页或延长测试时间。

#### 第一部分 抽样分布

本部分建立假设如下：

零假设 H0 : Pnew ≤ Pold

备择假设 H1 : Pnew ＞ Pold

其中，Pnew及Pold分别指新页面与旧页面的转化率。

通过抽样分布计算P值为0.9，即中意味着，在Pnew ≤ Pold的条件下，出现样本中观察到实际差值的概率为0.9，这个值在新旧页面中没有区别。基于这个值无法拒绝零假设，新页面不比旧页面更好。

#### 第二部分 回归分析

此部分用建立逻辑回归的方法获取测试结果，与第一部分不同，回归的零假设为 Pold = Pnew，为双尾检验。

得到的P值为0.19，基于95%的置信区间，同样无法无法拒绝零假设，新页面不比旧页面更好。

接下来在模型中添加国家/区域信息，以及页面与国家/地区之间的相互作用关系，得到结论：

国家项与转化率、国家/地区之间的相互作用与转化率均没有显著的线性关系，不会对结果转化产生重大影响。
