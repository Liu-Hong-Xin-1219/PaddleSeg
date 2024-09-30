# 安装错误应对文档

本文档包含了安装过程之中可能出现的错误.安装过程之中如果系统报错,请您先运行eiseg确认程序是否能够正常运行,如果能够正常运行,请记录报错信息并且暂时搁置此报错. 如果不能正常运行,则参考下面内容进行修复.

### module ‘cv2.dnn’ has no attribute ‘DictValue’
运行以下指令:
```shell
pip install --upgrade opencv-python==4.7.0.72
```
运行以下指令后,系统可能仍然报错,报错信息大致意思是: opencv-python 4.7.0.72 不是paddlepaddle需要的版本.
请记录并且暂时忽略此报错.因为高版本的opencv能够兼容低版本的opencv,所以我们更新opencv-python到高版本之后, 程序仍然能够正常运行.

