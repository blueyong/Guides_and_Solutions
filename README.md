记录开发中的一些问题：
20190324：
 1.tensorflow安装：
	1.1 在Anaconda+python3.6下安装完成tensorflow后，import tensorflow as tf报错：
	Microsoft Windows [版本 6.1.7601]
版权所有 (c) 2009 Microsoft Corporation。保留所有权利。

C:\Users\sam>python
Python 3.6.5 |Anaconda, Inc.| (default, Mar 29 2018, 13:32:41) [MSC v.1900 64 bi
t (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> import tensorflow as tf
Traceback (most recent call last):
  File "C:\Users\sam\Anaconda3\lib\site-packages\tensorflow\python\pywrap_tensor
flow.py", line 58, in <module>
    from tensorflow.python.pywrap_tensorflow_internal import *
  File "C:\Users\sam\Anaconda3\lib\site-packages\tensorflow\python\pywrap_tensor
flow_internal.py", line 28, in <module>
    _pywrap_tensorflow_internal = swig_import_helper()
  File "C:\Users\sam\Anaconda3\lib\site-packages\tensorflow\python\pywrap_tensor
flow_internal.py", line 24, in swig_import_helper
    _mod = imp.load_module('_pywrap_tensorflow_internal', fp, pathname, descript
ion)
  File "C:\Users\sam\Anaconda3\lib\imp.py", line 243, in load_module
    return load_dynamic(name, filename, file)
  File "C:\Users\sam\Anaconda3\lib\imp.py", line 343, in load_dynamic
    return _load(spec)
ImportError: DLL load failed with error code -1073741795

During handling of the above exception, another exception occurred:


安装环境

C:\Users\sam>python --version
Python 3.6.5 :: Anaconda, Inc.

C:\Users\sam>conda list tensorflow
# packages in environment at C:\Users\sam\Anaconda3:
#
# Name                    Version                   Build  Channel
tensorflow                1.13.1                   pypi_0    pypi
tensorflow-estimator      1.13.0                   pypi_0    pypi

C:\Users\sam>conda --version
conda 4.6.7

你的CPU可能看起来缺少AVX指令。

参考一个关于如何解决这个问题的指南，供将来参考。

https://github.com/tintinmovie/Guides_and_Solutions/blob/master/Tensorflow%20-%20No%20module%20named%20'_pywrap_tensorflow_internal'.md

依照上面的方案解决了，并且使用了比较新的版本
https://github.com/fo40225/tensorflow-windows-wheel



