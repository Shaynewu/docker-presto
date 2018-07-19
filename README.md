# Docker Presto

使用 docker-compose 启动 hive 及 prest。用于搭建测试使用的 presto 环境。

使用 [big-data-europe/docker-hive](https://github.com/big-data-europe/docker-hive) 仓库中的文件进行一键启动。

## install

> bash ./install.sh

## start

> (cd lib && docker-compose up -d)

## etc

### 数据

搭建完后，presto 中没有数据。根据业务需求准备模拟数据，建表并导入数据。

### 导入方案

1. 在 hive 层操作，使用 beeline 进行命令行的操作。
2. 在 hive 层操作，使用 hive client 进行操作。ps：目前支持最好的是 python 的 PyHive。
3. 在 presto 层进行操作，建表、然后使用 insert 语句进行插入。ps：这里可以使用 JS 实现，但可行性并未验证。