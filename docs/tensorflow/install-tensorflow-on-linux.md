# 在 Linux 上安装 Tensorflow

> 原文:[https://www.geeksforgeeks.org/install-tensorflow-on-linux/](https://www.geeksforgeeks.org/install-tensorflow-on-linux/)

在本文中，我们将看到如何在 Linux 中安装 TensorFlow。这是一个完全开源的使用数据流图进行数值计算的库。

### **系统**要求 **:**

*   Python 3.6 到 3.8。
*   Pip 19.0 或更高版本。
*   Ubuntu 16.04 或更高版本。

### **分步安装:**

**步骤 1:** 为 python venv 模型创建一个虚拟环境。

```
sudo apt install python3-venv python3-dev
```

![](img/c4e7ca0b51379b726004e2cc6c039f56.png)

**步骤 2:** 创建 python 3 虚拟环境。

```
mkdir tensor
cd tensor/
python3 -m venv <virtual_environment_name>
```

![](img/6147404dfdf7e7b87cc477c264c10164.png)

**步骤 3:** 现在在虚拟环境中检查 pip 版本。

```
pip --version
```

![](img/d5590f894e0f059c03248db84c2bb5f6.png)

这里我们的 pip 是 9，因此我们需要使用升级来升级 pip:

```
pip install --upgrade pip
```

![](img/d62f9ccf951fe47e39a151273d546f53.png)

**步骤 4:** 使用 pip 安装 TensorFlow:

```
pip install --upgrade tensorflow
```

![](img/301523e56f47cf0ecd73cd7c863290af.png)

**第五步:**检查安装是否正确。

```
import tensorflow as tf
print(tf.__version__);
```

![](img/15c2c1a4135b95d4d44ea13c51378703.png)