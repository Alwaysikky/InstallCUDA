# InstallCUDA
Install CUDA in Ubantu1804 (Jan.2024)


有效的流程说明：
https://zhuanlan.zhihu.com/p/143429249

其中遇到一个public key invaild 问题，将官网安装的其中一句命令更改为：

$wget https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/cuda-wsl-ubuntu.pin
$sudo mv cuda-wsl-ubuntu.pin /etc/apt/preferences.d/cuda-repository-pin-600

$sudo apt-key del 7fa2af80
$sudo apt-key adv --fetch-keys http://developer.download.nvidia.com/compute/cuda/repos/ubuntu1604/x86_64/3bf863cc.pub
$ # sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/7fa2af80.pub

$ sudo add-apt-repository "deb https://developer.download.nvidia.com/compute/cuda/repos/wsl-ubuntu/x86_64/ /"
$ sudo apt-get update
$ sudo apt-get -y install cuda
