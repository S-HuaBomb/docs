.. _cn_api_io_ChainDataset:

ChainDataset
-------------------------------

.. py:class:: paddle.io.ChainDataset

将多个流式数据集级联的数据集。

用于级联的数据集须都是 ``paddle.io.IterableDataset`` 数据集，将各流式数据集按顺序级联为一个数据集。

参数
::::::::::::

    - **datasets** (list of IterableDataset) - 待级联的多个数据集。

返回
::::::::::::
Dataset，级联后的流式数据集

代码示例
::::::::::::

COPY-FROM: paddle.io.ChainDataset
