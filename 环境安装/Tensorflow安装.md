# 打开Anaconda Prompt

```
anaconda prompt
```

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/anacondaPrompt.png)

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/openAnacondaPrompt.png)

# 执行换源操作(国外的同学不需要执行，该操作只需要在安装好Anaconda之后执行一次，不要重复执行)

**依次执行下面四条语句**

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge

conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/msys2/

conda config --set show_channel_urls yes
```

# 创建虚拟环境

```
conda create -n tf2 python=3.8(如果遇到创建失败，一般是由于网络引起，多执行几次就好)
```

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/createEnvs.png)

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/createEnvsYes.png)

# 激活虚拟环境并安装tensorflow函数库

**在安装函数库之前，我们需要激活相应的虚拟环境**

```
conda activate tf2
pip install tensorflow-gpu(国外同学执行这条语句)
pip install tensorflow-gpu -i "https://mirrors.aliyun.com/pypi/simple"(国内同学执行这条语句，使用国内的阿里源)
```

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/activateEnvs.png)

# 测试安装是否成功

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/testInstalled.png)

# CUDA安装(如果本地没有GPU，就不用管这步了)

```
conda install cudatoolkit==10.1.243 cudnn
```

![](https://maoxianxin1996.oss-accelerate.aliyuncs.com/environment/tensorflow/installCuda.png)