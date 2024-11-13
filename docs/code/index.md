# Linux常用命令
- **统计文件大小**
```bash
du -hd 1
```

- **统计文件数量**
```bash
tree | wc -l
```

- **统计子文件夹文件数量**
```bash
find . -type f -print | awk -F'/' 'NF>1 {print $(NF-1)}' | sort | uniq -c
```

# 常用conda env命令
- 激活环境
```bash
conda activate <env_name>
```
- 停用当前环境
```bash
conda deactivate
```
- 查看环境列表
```bash
conda env list
```
