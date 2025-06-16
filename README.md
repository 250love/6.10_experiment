实验环境搭建与启动指南



1\. 创建实验环境





```
conda create -n experiment python==3.12


conda activate experiment


pip install -r requirements.txt
```

2\. 手动更换程序根目录



### 需修改的文件及路径说明&#xA;



*   **rule\_application.py**

    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **run\_model.py**（位于 model\_train/TECHS\_main 目录）
    添加根路径：


    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **generate\_feature.py**（位于 model\_train\TempValid\_main 目录）
    添加根路径：


    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **learn.py**

    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **experient.py**



```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   第 38 - 47 行添加根路径：


*   第 86 - 92 行添加根路径：


<!---->

*   **TempValid.py**

    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **evaluate.py**

    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```



*   **apply.py**

    添加根路径：




```
import sys


sys.path.append('/root/autodl-tmp/6.10整理实验/')  # 替换为你的项目根目录路径
```

3\. 启动实验



启动实验时，需通过命令行传入关键参数，具体命令格式及参数说明如下：




```
\# 启动实验的命令模板


python experient.py \\


&#x20;   \--model \[模型名称] \  # 从以下模型中选择其一


&#x20;   \--dataset icews14    # 固定数据集名称


\# 可选择的模型列表：


\- TempValid

\- TECHS

\- TLogic

\- TR-Rules
```

4\. 实验环境配置





| 硬件 / 软件&#xA; | 配置详情&#xA;                                             |
| ------------ | ----------------------------------------------------- |
| GPU&#xA;     | 3090 24G&#xA;                                         |
| CPU&#xA;     | 14 vCPU Intel(R) Xeon(R) Gold 6330 CPU @ 2.00GHz&#xA; |
| CUDA&#xA;    | 12.4&#xA;                                             |
| Pytorch&#xA; | 2.5.1&#xA;                                            |

### 注意事项&#xA;



*   根目录路径需根据实际项目路径修改`/root/autodl-tmp/6.10整理实验/`部分


*   启动命令中`--model`参数需从提供的列表中选择其一，删除示例说明文字


> （注：文档部分内容可能由 AI 生成）
>
