## k8s secret配置更新工具
### 下载k8s中的secret及对应的配置文件
```bash

./sconfig down ${config_file} ${namespace} ${secret_name}
```
*当前config_file支持`secrets.py` 及 `config.hcl` 两种*
执行以上命令后将在当前目录出现secret文件(`secret.json`) 及 配置文件(`secrets.py` 或 `config.hcl`)

### 更新secret中对应的配置文件  
1. 先修改`config_file`对应的配置文件
2. 执行下列脚本替换secret文件中的配置
```bash
./sconfig replace ${config_file}
```

### 更新k8s中的secret
```
./sconfig apply
```

test
