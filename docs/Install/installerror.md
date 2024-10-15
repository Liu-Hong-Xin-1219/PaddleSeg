# 安装错误应对文档

本文档包含了安装过程之中可能出现的错误.安装过程之中如果系统报错,请您先运行eiseg确认程序是否能够正常运行,如果能够正常运行,请记录报错信息并且暂时搁置此报错. 如果不能正常运行,则参考下面内容进行修复.

### module ‘cv2.dnn’ has no attribute ‘DictValue’
运行以下指令:
```shell
pip install --upgrade opencv-python==4.7.0.72 -i https://pypi.tuna.tsinghua.edu.cn/simple
```
运行以下指令后,系统可能仍然报错,报错信息大致意思是: opencv-python 4.7.0.72 不是paddlepaddle需要的版本.
请记录并且暂时忽略此报错.因为高版本的opencv能够兼容低版本的opencv,所以我们更新opencv-python到高版本之后, 程序仍然能够正常运行.

### RuntimeError: module compiled against ABI version 0x1000009 but this version of numpy is 0x2000000
请使用`python --version`检查你的python版本. 本程序要求的python版本为3.6~3.10, 这条报错意味着你的python版本不对.
请参考[新手指南](installfornewbe.md)进行合适版本python的安装,推荐安装的python版本为3.10或者3.8

### ImportError: numpy.core.multiarray failed to import
这可能是因为你没有安装numpy,或者你的numpy版本过低. 你可以使用`pip list` 来检查你的numpy版本. 你可以使用以下指令安装合适版本的numpy
```shell
pip install numpy==1.24.4 -i https://pypi.tuna.tsinghua.edu.cn/simple
```
### pip._vendor.urllib3.exceptions.ReadTimeoutError: HTTPSConnectionPool(host='....', port=443): Read timed out.
这是因为部分pip包的安装需要访问外网, 这一过程速度很慢,所以请尝试在安装指令之后加上以下指令使用国内的清华源进行安装.
`pip install numpy` -> `pip install numpy -i https://pypi.tuna.tsinghua.edu.cn/simple`
