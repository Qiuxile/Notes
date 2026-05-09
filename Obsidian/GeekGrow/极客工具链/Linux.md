新建目录
```shell
mkdir <目录名>
```

新建文件
1. **`touch`** – 创建一个空文件（若文件已存在则更新其时间戳）
```shell
touch filename.txt
```
2. **`echo`** – 写入内容并创建文件
```shell
echo "Hello" > filename.txt
```
2. **`cat`** – 使用重定向创建文件
```shell
cat > filename.txt
```
（按 `Ctrl+D` 结束输入）
3. **`vi` / `vim` / `nano`** – 使用文本编辑器创建并编辑文件
```shell
vi/vim/nano filename.txt
```

其中最常用、最快捷的是 `touch`。