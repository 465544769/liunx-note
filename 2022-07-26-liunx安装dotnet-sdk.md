## 在线安装
```
yum install dotnet-sdk-6.0
```

如果报 找不到包就只能离线安装了

## 离线安装(不推荐)
从官方下载压缩包，然后解压
```
wget https://download.visualstudio.microsoft.com/download/pr/0e83f50a-0619-45e6-8f16-dc4f41d1bb16/e0de908b2f070ef9e7e3b6ddea9d268c/dotnet-sdk-6.0.302-linux-x64.tar.gz
```

配置环境变量（好像是一次性的，不知道为什么过一会dotnet --info 就用不了了）
```
DOTNET_FILE=dotnet-sdk-6.0.302-linux-x64.tar.gz
export DOTNET_ROOT=$(pwd)/.dotnet

mkdir -p "$DOTNET_ROOT" && tar zxf "$DOTNET_FILE" -C "$DOTNET_ROOT"

export PATH=$PATH:$DOTNET_ROOT
```