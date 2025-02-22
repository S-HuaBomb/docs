.. _cn_api_fluid_layers_sum:

sum
-------------------------------

.. py:function:: paddle.fluid.layers.sum(x)




该OP用于对输入的一至多个Tensor或LoDTensor求和。如果输入的是LoDTensor，输出仅与第一个输入共享LoD信息（序列信息）。

例1：
::
    输入：
    	input.shape = [2, 3]
    	input = [[1, 2, 3],
	      	  [4, 5, 6]]

    输出：
    	output.shape = [2, 3]
    	output = [[1, 2, 3],
	          [4, 5, 6]]
	
例2：
::
    输入：
	第一个输入：
    	    input1.shape = [2, 3]
    	    input1 = [[1, 2, 3],
	      	      [4, 5, 6]]
	
	第二个输入：
    	    input2.shape = [2, 3]
    	    input2 = [[7, 8, 9],
	              [10, 11, 12]]

    输出：
    	output.shape = [2, 3]
    	output = [[8, 10, 12],
	          [14, 16, 18]]

参数
::::::::::::

    **x** (Variable|list(Variable)) - 输入的一至多个Variable。如果输入了多个Variable，则不同Variable间的shape和数据类型应保持一致。Variable为多维Tensor或LoDTensor，数据类型支持：float32，float64，int32，int64

返回
::::::::::::
对输入 ``x`` 中的Variable求和后的结果，shape和数据类型与 ``x`` 一致

返回类型
::::::::::::
Variable


代码示例
::::::::::::

COPY-FROM: paddle.fluid.layers.sum