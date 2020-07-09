### 时间复杂度
公式法

公式法可以说是计算递归函数复杂度最方便的工具，当递归函数的时间执行函数满足如下的关系式时，我们可以利用公式法：T(n) = a×T(n/b) + f(n)。


其中，f(n) 是每次递归完毕之后额外的计算执行时间。例如，在归并排序中，每次递归处理完两边的数组后，我们需要执行合并的操作，那么这个操作的执行时间就是 f(n)。



当参数 a、b 都确定的时候，光看递归的部分，它的时间复杂度就是：O(n^logba)。



由于时间复杂度求的是上界（upper bound)，通过对比递归部分的时间复杂度和 f(n) 的大小关系，得出最后的整体时间复杂度。牢记以下三种情况和相应公式：



    当递归部分的执行时间 nlog(b)a 大于 f(n) 的时候，最终的时间复杂度就是 O(n^logba)。

    当递归部分的执行时间 nlog(b)a 小于 f(n) 的时候，最终的时间复杂度就是 f(n)。

    当递归部分的执行时间 nlog(b)a 等于 f(n) 的时候，最终的时间复杂度就是 O(n^logba)logn。