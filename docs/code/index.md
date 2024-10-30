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
