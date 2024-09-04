# GPTScan

## 描述

使用ChatGPT进行逻辑漏洞检测。

## 如何使用

1. 安装依赖，

- 需要Python 3.10+
- 安装依赖：`pip install -r requirements.txt`

2. 运行GPTScan

例如，我这边源码存放于`/source`目录，则运行命令为：

```shell
python3.10 main.py -s /sourcecode -o /sourcecode/output.json -k OPEN_AI_API_KEY_xxxxxxxxxxxxx
```

3. 查看输出

输出结果位于`-o`参数指定的位置，在上例中位于`/sourcecode/output.json`。

## 支持的项目类型

目前支持的项目类型有：
- 单文件，即一个sol文件
- 多文件，即一个目录下有多个sol文件，不包括其它外部依赖
- 常见的框架项目，如truffle，hardhat，brownie等

经测试的框架有：
- hardhad
- truffle
- brownie

注意，这个项目不包含编译环境，如Node.js等，需要自行安装。

## 数据集

论文中用于评估GPTScan的数据集，如下：
1. Web3Bugs: [https://github.com/MetaTrustLabs/GPTScan-Web3Bugs](https://github.com/MetaTrustLabs/GPTScan-Web3Bugs)
2. DefiHacks: [https://github.com/MetaTrustLabs/GPTScan-DefiHacks](https://github.com/MetaTrustLabs/GPTScan-DefiHacks)
3. Top200: [https://github.com/MetaTrustLabs/GPTScan-Top200](https://github.com/MetaTrustLabs/GPTScan-Top200)


