## metric

### p * r

可以使用$$precision * recall$$作为评判标准，同时考虑了$$p, r$$

$$P(Y=1)$$代表真实的正样本比例，但是我们不知道正样本的比例，因为$$U$$数据集中也有$$P$$；$$P(f(x)=1)$$代表模型预测的正样本比例，这个是根据模型预测的结果就可以得到的

实践中，我们使用下面的公式来作为$$pr$$的比较

$$\frac{pr}{P(Y=1)} = \frac{r^2}{P(f(x)=1)}$$

由于$$P(Y=1)$$正样本概率是一个固定值，所以作为分母不会影响最后的比较。然后左边可以推导到右边，我们根据右边的公式计算出metric，来比较模型。

$$p = P[Y=1|f(x)=1], r = P[f(x)=1|Y=1]$$代入上式即可完成推导，另外，$$r$$是可以估算的，而$$p$$是无法估算的

