
因时间严重受限，进度难保，设计能力欠缺……等原因，在代码里写了很多临时的东东，如果以后需要维护可能会带来困惑，特记录如下。

所有的


1. formula.ml中，normalize函数中的TODO：有的带参系统中的参数只有一部分是对称的，这里假设带参系统的参数只能是intc，且不对称的参数只有(intc 0)一个，当然，这是不对的。正确的做法应该是修改typedef类型，除了Enum外还应该有Paramters类似的东东。当然并没有这么简单，还需要考虑更多，比如带参系统的参数不是数值类型的。

2. invFinder.ml中，minify_inv_inc假设系统只有一个类型作为参数，且通过NuSMV检查不变式时，参数值最大为3.

3. loach.ml中，limit_params_in_typedef只是一个权益之计。正确的做法应该是试探法，是的，相当麻烦。



