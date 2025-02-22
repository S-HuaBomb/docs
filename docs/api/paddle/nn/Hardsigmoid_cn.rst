.. _cn_api_nn_Hardsigmoid:

Hardsigmoid
-------------------------------

.. py:function:: paddle.nn.Hardsigmoid(name=None)

Hardsigmoid激活层。sigmoid的分段线性逼近激活函数，速度比sigmoid快，详细解释参见 https://arxiv.org/abs/1603.00391。

.. math::

    Hardsigmoid(x)=
        \left\{
        \begin{aligned}
        &0, & & \text{if } x \leq -3 \\
        &1, & & \text{if } x \geq 3 \\
        &x/6 + 1/2, & & \text{otherwise}
        \end{aligned}
        \right.

其中，:math:`x` 为输入的 Tensor

参数
::::::::::

    - **name** (str，可选) - 具体用法请参见 :ref:`api_guide_Name`，一般无需设置，默认值为 None。

形状：
::::::::::
    - input：任意形状的Tensor。
    - output：和input具有相同形状的Tensor。

代码示例
::::::::::

COPY-FROM: paddle.nn.Hardsigmoid