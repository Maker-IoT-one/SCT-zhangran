# 算法推理

## 原生推理

- 先将自己在个人设备上的训练模型scp到昇腾上
    > 这个是我们在自己的设备上训练好后
    ```
    scp 文件 用户名@xxx.xxx.xxx.xxx:传输的路径
    ```
- 然后将推理部分的代码在昇腾上写一遍
    > 去掉训练部分
    ```python
    ......
    fut_pred = 60

    test_inputs = train_data_normalized[-train_window:].tolist()
    print(test_inputs)
    model.eval()
    ......
    ```
- 安装推理代码所需要的包
    ```
    pip install pandas
    ......
    ```
- 直接加载 
    ```
    python 推理文件.py
    ```

## ACL推理

- 持续更新中......