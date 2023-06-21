# Stable diffusion项目的部署

## 部署Stable Diffusion前的准备

1. 检查电脑是否满足最低配置（显存至少4GB,只能是N卡！，本地磁盘要求有15GB）

*如何查看电脑显存？*

在Windows【开始】点鼠标右键，选择【任务管理器】，在【性能】一栏选择【GPU】查看“专用GPU内存”

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/19ed0615-7ce8-4c90-9f59-06e8238762eb)


<!--我的是RTX 3060 laptop,显存是6GB-->

## 下载必备环境

 1. Git 官方网址：[吉特 (git-scm.com)](https://git-scm.com/) 

    ![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/75fb3b85-5492-4c88-aa65-3fdaf3b2e090)

​       <!--注意版本号的对应关系-->

​	检查是否安装成功（图表3）：检查自己电脑有没有安装Git：【Win+R】唤出【运行】，输入“cmd”，回车，在命令行里输入：git --version

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/7e9736fa-ea79-4558-af7b-f1bb1cc5011c)

这样就说明安装成功了

​	

 	2.  Python   官方地址： [python.org](https://www.python.org/)      <!--部署此项目时用的是python3.10.6的版本-->

## Stable Diffusion仓库的获取

 1. 从Github库：[CompVis/稳定扩散：潜在的文本到图像扩散模型 (github.com)](https://github.com/CompVis/stable-diffusion)直接克隆其压缩包

 2. 通过git进行克隆：先git bush到你想下载的文件夹

   ![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/78b21b29-c21e-4868-883d-d3d25b14f241)


​	然后输入指令：

```
git clone https: //github.com/AUTOMATIC1111/stablediffusion-webui.git
```

​	3. 下载完成后，我们会得到这样一个文件夹

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/29bacaf5-7bc4-4848-9ba1-04d69b13ddc6)


## Stable Diffusion安装

​	1.双击运行此文件（在运行之前最好开启魔法网络！！因为在下载过程中会从huggingface上下载模型权重，没有魔法网络会导致权重或者相关库下载失败！！！（当然你不会魔法上网后面也会讲解，先运行第6步））

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/3095ccd2-b0e2-4336-be74-22664c0e4aea)

​	2.运行后，它会下载相关的环境以及模型权重（我是之前就下好了，所以画面不一样）

​	3.所有下载后，会弹出一串网址，直接摁住Ctrl然后单击网址就会进入web界面

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/fb7ed7d5-5713-4f78-91fe-a322ddefd5cb)


​	![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/40feb589-b08a-4bcf-aa14-ee9a2429b8f5)

## 利用模型权重进行图像生成

​	经过万般险阻，我们终于是来到了项目的界面

​	下面这栏可以选择你的模型权重，不同的模型对于输入的图像有着巨大的影响！！！

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/0c8ad7b4-f289-47a4-aa35-9f54154a0338)


   这一栏输入你的提示词
   
   ![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/92eac3a8-c0ae-4dc4-90cd-987e72b0273b)

这一栏输入你的反向提示词（不希望出现的）![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/895eec83-b440-4bfb-9b62-07c0377a679a)


下面的基本可以保持默认，width和height是图像的长宽，像素越高，所需显存越大**（显存低的电脑慎重尝试)**

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/e4149715-37f0-438a-883e-5e2e9f108042)

我们用Stable Diffusion 自带的v1-5-pruned-emaonly来举个例子：

输入提示词：***lake,mountain,train***

点击    **Generate**

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/714a47f8-83e4-40d5-aef0-6051d34c6f1d)

当下载完成后，我们返回web界面查看，得到：

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/006a5ef8-1c5b-4403-a98a-2f9d0710706d)


*然后你就可以开始尽情发挥自己的创作想法了！！！*

