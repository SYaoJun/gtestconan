# conan
## 简介
C/C++包管理工具
## 环境
- Ubuntu 22.04
## 安装
```bash
pip3 install conan
conan --version
``` 
## 查看远程仓库
```bash
conan remote remove conancenter
conan remote add conancenter https://center.conan.io
conan remote list
```
## 生成默认配置
```bash
conan profile detect
```
## 安装依赖和编译命令
```bash
mkdir build
conan install . --output-folder=build --build=missing
cd build
cmake .. -DCMAKE_TOOLCHAIN_FILE=conan_toolchain.cmake -DCMAKE_BUILD_TYPE=Release
cmake --build .
```