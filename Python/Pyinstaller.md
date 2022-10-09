# 安装

```bash
pip install pyinstaller
```

# 打包

```bash
pyinstaller -F -w --clean --upx-dir=D:\Dev\upx-3.95-win64\upx.exe -i public\shooting_star.ico --key 1597530 main.py
```

主要参数

- `-F` 打包成单个可执行文件
- `-D` 打包成文件夹
- `-w` 不显示终端
- `--clean` 在构建之前，清理 PyInstaller 缓存并删除临时文件(多次打包会报错，最好清除缓存)
- `--upx-dir`  结合 UPX 压缩打包（--upx-dir=path/pux）
- `--key`  指定加密密钥来用 AES256 来混淆 Python 字节码（实际性能参见官方使用手册），需要安装 crypto 库
