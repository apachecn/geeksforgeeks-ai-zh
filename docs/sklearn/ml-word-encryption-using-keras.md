# ML |使用 Keras 的文字加密

> 原文:[https://www . geesforgeks . org/ml-word-encryption-use-keras/](https://www.geeksforgeeks.org/ml-word-encryption-using-keras/)

机器学习是当今科技市场最受欢迎的领域之一。学习如何教你的系统自己做一些特定的事情是非常有趣的。今天，我们将借助像 Tensorflow 和 Numpy 这样的库，在发现机器学习方面迈出第一小步。我们将创建一个具有一个神经元的神经结构，它在生活中的唯一目的是通过遵循一个特定的模式将我们输入的字符变成其他字符，该模式的示例由我们存储在机器将从中学习的样本数据中。

**使用的库:**

*   张量流:从[这里](https://www.tensorflow.org/install)学习安装张量流*   NumPy: Learn to install numpy from [here](https://numpy.org/)

    **代码:导入库**

    ```
    # importing libraries
    import tensorflow as tf
    import numpy as np 
    from tensorflow import keras
    ```

    我们还将使用 Keras，这是用 Python 编写的神经网络库，并预先添加在 Tensorflow 库中。

    **模型的工作:**
    给定示例的目的是从用户处获取输入代码，然后对其进行加密，这样在不知道其密钥的情况下，没有人能够理解它。这里我们将逐个字符地查看消息，并用给定字符的 ASCII 值 1 + ASCII 值替换它。但首先，我们将创建一个神经结构来为我们做这样的工作。我们将在这里称之为模型，并使用 Keras 定义它。这里`keras.Sequential`定义我们的模型将是顺序的或者模型是层的线性堆叠，然后我们将定义层的种类(我们将使用密集连接的神经网络(NN)层)与我们想要的层数或单位。最后，我们将给出我们想要的神经元数量作为 input_shape，并将编译带有优化器和损失的模型。优化器和损失是帮助我们的模型朝着正确方向工作的两个函数。损失将计算由我们的模型做出的预测的误差，优化器将检查该误差，并将模型向误差减小的方向移动。

    **代码:创建顺序模型**

    ```
    # creating the simplest neural structure with only 
    # one layer and that only have one neuron
    model = keras.Sequential([keras.layers.Dense(units = 1, 
                                                 input_shape =[1])])

    # compiling model with optimizer to make predictions and 
    # loss to keep checking the accuracy of the predictions
    model.compile(optimizer ='sgd', loss ='mean_squared_error')
    ```

    在这之后，我们将指定我们的训练数据为 Numpy 数组，该数组将 x 的所有值连接到相应的 y，然后我们将使用`model.fit`在给定的数据上训练我们的模型。在这里，Epochs 将指定我们的模型处理训练数据的次数，以使用 Loss 和 Optimizer 提高其准确性。

     **代号:**

    ```
    # here we will give sample data with which program 
    # will learn and make predictions on its basis
    xs = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 
                  dtype = float)
    ys = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11], 
                  dtype = float)

    # we will fit the data in the model and the epochs
    # is the number of times model will run sample data to
    # increase its accuracy
    model.fit(xs, ys, epochs = 1000)
    ```

    最后，我们将从用户那里获取输入，并使用元组函数将其分解为字符，然后我们将所有这些字符保存到一个列表中。现在，我们将创建一个 for 循环，并在我们的模型中一次发送一个字符来进行预测，并将打印所有的预测，以便它们一起形成一个加密的消息，在您知道它的密钥之前，它不容易理解。

    **代码:**

    ```
    # taking input from user
    code = input("code is: ")
    n = len(code)

    # dividing the input message into its characters
    c = tuple(code)
    d = list(c)

    # predicting the output for each character and printing it
    for i in range(0, n):
        s = ord(d[i]) 
        x = model.predict([s])
        print(chr(x), end ="")

    ```

    **完成实施–**

    ```
    # importing libraries 
    import tensorflow as tf
    import numpy as np 
    from tensorflow import keras

    # creating the simplest neural structure 
    # with only one layer and that only have one neuron
    model = keras.Sequential([keras.layers.Dense(units = 1, 
                                                 input_shape =[1])])
    # compiling model with optimizer to make predictions and 
    # loss to keep checking the accuracy of the predictions
    model.compile(optimizer ='sgd', loss ='mean_squared_error')

    # here we will give sample data with which program will learn 
    # and make predictions on its basis
    xs = np.array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10], dtype = float)
    ys = np.array([1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11], dtype = float)

    # we will fit the data in the model and the epochs is number of
    # times model will run sample data to increase its accuracy
    model.fit(xs, ys, epochs = 1000)

    # taking input from user
    code = "Vaibhav Mehra writing for GeeksforGeeks"
    n = len(code)

    # dividing the input message into its characters
    c = tuple(code)
    d = list(c)

    # predicting the output for each character and printing it
    for i in range(0, n):
        s = ord(d[i]) 
        x = model.predict([s])
        print(chr(x), end ="")
    ```

    **输出:**

    ```
    Wbjcibw!Nfisb!xsjujoh!gps!HffltgpsHfflt

    ```