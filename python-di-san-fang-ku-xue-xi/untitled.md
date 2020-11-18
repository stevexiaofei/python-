# numpy+scipy

## numpy常用API汇总

| API | desp |
| :--- | :--- |
|  `numpy.ravel`\(_a_, _order='C'_\) | Return a contiguous flattened array |
|  `numpy.vstack`\(_tup_\) | 如果为1d array，则长度需要一致，如果为多维array，则除第一维外，其他维度的长度需要一致 |
|  `numpy.stack`\(_arrays_, _axis=0_, _out=None_\) | 讲一个array的list沿着某个新维度拼接成一个新的array，默认新维度为axis 0，array list 中的每个array的shape需要一样。 |
|  `numpy.concatenate`\(_\(a1_, _a2_, _...\)_, _axis=0_, _out=None_\) | 讲一个array的list沿着某个维度拼接成一个新的array， 除了参数中指定的维度外， array list中的array的其他维度需要一样。 |



