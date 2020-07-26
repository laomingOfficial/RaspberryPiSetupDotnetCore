### Step 1 
https://dotnet.microsoft.com/download/dotnet-core 
SDK Linux ARM32 

### Step 2 
```
#安裝dotnet core SDK & Runtime + debug
sudo mkdir -p /usr/bin/dotnet
sudo tar zxf dotnet-sdk-*.tar.gz -C /usr/bin/dotnet
sudo mkdir -p /usr/bin/vsdbg
curl -sSL https://aka.ms/getvsdbgsh | sudo bash /dev/stdin -r linux-arm -v latest -l /usr/bin/vsdbg
sudo rm dotnet-sdk-*.tar.gz

#設置Environment Path
export DOTNET_ROOT=/usr/bin/dotnet
export PATH=$PATH:/usr/bin/dotnet
cat > dotnet-exports.sh <<EOF
export DOTNET_ROOT=/usr/bin/dotnet
export PATH=$PATH:/usr/bin/dotnet
EOF
sudo mv dotnet-exports.sh /etc/profile.d

#創建project 文件夾
mkdir ~/Projects
mkdir ~/Projects/helloworld
```

### Step 3 
https://drive.google.com/file/d/1Ht1UP08pFfToObTgdjW-zTm11i0jxX-8/view?usp=sharing