# Sensitive Information Scanner

这是一个用 Go 语言编写的敏感信息扫描工具，可以扫描指定路径下的文件，查找用户名、密码和内网 IP 地址等敏感信息。

## 功能特性

- 支持指定扫描路径
- 支持指定并发线程数
- 支持将结果输出到 JSON 文件
- 支持扫描多种文件类型
- 支持扫描账号密码和内网 IP

## 用法

```bash
./sensitive-info-scanner -path /path/to/scan -workers 8 -output results.json -mode pass
```

### 参数说明

- `-path`: 扫描起始目录（默认当前目录）
- `-output`: 将扫描结果输出为 JSON 文件（可选）
- `-workers`: 并发线程数（默认 4）
- `-verbose`: 输出详细进度信息
- `-filetypes`: 扫描文件扩展名，多个逗号分隔（默认：.txt,.log,.conf,.ini,.xml,.json,.yml,.yaml,.sh,.py,.go,.java,.c,.cpp,.h,.hpp,.php,.js,.html,.htm,.css）
- `-mode`: 扫描模式，`pass`=账号密码，`ip`=内网IP，不指定则不扫描
- `-version`: 显示版本信息并退出
- `-h`, `--help`: 显示帮助信息

