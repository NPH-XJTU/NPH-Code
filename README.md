# XJTU-Identification-Model-for-NPH

<p align="center" style="color: red">本项目已完成全部开发，已获得计算机软件著作权，正在申请国家专利🎉</p>

## Quick Start

1. 下载本仓库并保持在`main`分支
2. 安装依赖:

    ```shell
    pip install -r requirements.txt
    ```

3. 从[这里](https://github.com/Orion-zhen/project-brain/releases)下载模型文件(`unet-ventricle.pth`和`unet-skull.pth`)
4. 把下载下来的模型文件放入仓库目录中的`./output`目录
5. 运行命令:

    ```shell
    python webui.py
    ```

6. 浏览器打开网址[127.0.0.1:7860](http://127.0.0.1:7860)
7. 开始体验!🤗

## Model Training

仓库里内置了649张打好标签的数据, 可供参考训练!😃

1. 复制训练参数配置文件:

    ```shell
    cp ./config/train_params.py.example ./config/train_params.py
    ```

2. 在`./config/train_params.py`中调整训练参数, 其中`CATEGORY`的值可以取`ventricle`(代表脑室识别)或`skull`(代表颅骨识别)
3. 开始训练:

    ```shell
    python train.py
    ```

    你可以运行`python train.py --help`查看更多可选命令行参数. 训练结果默认保存在`./output`文件夹内
4. 测试训练结果:

    ```shell
    python predict.py
    ```

## Developer's Message

The project is made by three undergraduates in Xi'an Jiaotong University

<a href="https://github.com/NPH-XJTU/NPH-Final/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=NPH-XJTU/NPH-Final" />
</a>
