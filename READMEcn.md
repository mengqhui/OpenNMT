OpenNMT 详细介绍
OpenNMT 是一个由 Harvard NLP (哈佛大学自然语言处理研究组) 开源的 Torch 神经网络机器翻译系统。



OpenNMT 系统设计简单易用，易于扩展，同时保持效率和最先进的翻译精确度。

特性：

简单的通用接口，只需要源/目标文件。

快速高性能GPU训练和内存优化。

提高翻译性能的最新的研究成果。

可配对多种语言的预训练模型（即将推出）。

允许其他序列生成任务的拓展，如汇总和图文生成。

快速开始：

OpenNMT 包含三个命令

1) 数据预处理

th preprocess.lua -train_src data/src-train.txt -train_tgt data/tgt-train.txt -valid_src data/src-val.txt -valid_tgt data/tgt-val.txt -save_data data/demo

2) 模型训练

th train.lua -data data/demo-train.t7 -save_model model

3) 语句翻译

th translate.lua -model model_final.t7 -src data/src-test.txt -output pred.txt
