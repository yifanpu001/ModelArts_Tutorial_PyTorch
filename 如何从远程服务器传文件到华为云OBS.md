__在服务器端，使用obsutil工具__ 
1. 下载和安装obsutil工具  
https://support.huaweicloud.com/utiltg-obs/obs_11_0003.html  

2. 准备环境（注册华为云账号，创建访问密匙等，已有账号和密匙的话可跳过）  
https://support.huaweicloud.com/utiltg-obs/obs_11_0004.html  

3.  进行初始化配置  
https://support.huaweicloud.com/utiltg-obs/obs_11_0005.html  
其中endpoint指OBS当前开通的区域和终端节点地址  

> 示例  
> 北京四：
> `./obsutil config -i=你的AK -k=你的SK -e=https://obs.cn-north-4.myhuaweicloud.com`
> 上海一：
> `./obsutil config -i=你的AK -k=你的SK -e=https://obs.cn-east-3.myhuaweicloud.com`

4. 配置成功后即可传输文件  
命令结构请见 https://support.huaweicloud.com/utiltg-obs/obs_11_0013.html  
上传示例请见 https://support.huaweicloud.com/utiltg-obs/obs_11_0028.html  

> 示例  
> 上传服务器中的文件ILSVRC2012_img_val.tar至华为云obs://d-cheap-net/datasets/  
> `./obsutil cp /home/imagenet/ILSVRC2012_img_val.tar obs://d-cheap-net/datasets/ `

> 上传服务器中的文件ILSVRC2012_img_train.tar至华为云obs://d-cheap-net/datasets/  
> `./obsutil cp /home/imagenet/ILSVRC2012_img_train.tar obs://d-cheap-net/datasets/ `   
> 传输意外中断后，继续传输  
> `./obsutil cp /home/imagenet/ILSVRC2012_img_train.tar obs://d-cheap-net/datasets/ -f`  
> 提示：出现 permission denied错误，可在指令前加sudo解决
