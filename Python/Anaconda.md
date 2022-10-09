# 一、镜像源

##  显示所有源

```bash
conda config --show-sources
```

##  删除源

```bash
conda config --remove channels 地址
```
# 二、虚拟环境

##  1. 创建虚拟环境

```bash
conda create -n test python=3.8.5
```

##  2. 激活虚拟环境

```bash
conda activate test
```

##  3. 删除虚拟环境

```bash
conda remove -n test --all
```

##  4. 查看所有虚拟环境

```bash
conda info -e
```
# 三、创建32位虚拟环境

##  1. 在 base 环境下执行

```bash
set CONDA_FORCE_32BIT=1
```

## 2. 创建虚拟环境

必须指定python版本, 不然创建不了32位虚拟环境

```bash
conda create -n win32 python=3.8.5
```

## 3. 查看是否为 32 位

```python
import platform

print(platform.architecture())
```
