# Lesson 1 Greeting Program
功能：接收一个名字参数并输出问候语。
环境：Ubuntu，已安装 g++ 和 cmake。
## 编译
方式一，在 main.cpp 所在目录执行：
```bash
g++ -std=c++17 -Wall -g main.cpp -o hello
```
运行方式一生成的程序，可执行文件是 `./hello`。
方式二，使用 CMake：
```bash
cmake -S . -B build
cmake --build build
```
也可以在构建目录中用 Make：
```bash
mkdir -p build && cd build
cmake ..
make -j4
cd ..
```
运行方式二生成的程序，可执行文件是 `./build/hello`。
## 运行
用方式一编译后：
```bash
./hello Alice
./hello "RM Vision"
```
分别输出 Welcome, Alice! 和 Welcome, RM Vision!。
用方式二编译后，把上面的 ./hello 换成 ./build/hello 即可。
## 错误输入
```bash
./hello
./hello Alice Bob
```
都应显示 Usage: ./hello <name>，退出状态为 1。
正常运行的退出状态为 0。
