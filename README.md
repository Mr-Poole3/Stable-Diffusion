
# Stable diffusion项目的部署
<h3>本教程已上传视频教程于哔哩哔哩<br>
网址：https://www.bilibili.com/video/BV1ah411K7Jp/
<br>
 <br>
 <br>
 <br>
部署Stable Diffusion前的准备

1. 检查电脑是否满足最低配置（显存至少4GB,只能是RTX或者10系以上GTX！，本地磁盘要求有15GB）

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

# Stable Diffusion插件—SadTalker

看到这儿里，你已经迫不及待想要在自己的电脑上面部署Stable Diffusion了，但是，我还发现了一个更有趣的模型——SadTalker，talker顾名思义，是一个说话的人，他的作用就是通过模型，将一张图片和一段音频合成为一个动态的视频。

## 前期准备

1. 安装python3.10.6.

2. 安装git.

3. 安装ffmpeg，详细教程：[如何在Windows上安装FFmpeg：15个步骤（带图片） (wikihow.com)](https://www.wikihow.com/Install-FFmpeg-on-Windows)

## 安装

1.得益于Stable Diffusion的插件属性，我们可以直接从其插件页进行克隆SadTalker的库，具体实现如下：

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/8e5b327b-342a-4999-97aa-1428ae262bd2)


下载完之后可以在installed处检查会出现sadtalker的标志，如果有就下载成功了，如果没有可能是因为网络原因，多试几次，如果不行那就上gitup下载，并把下载后的插件放到sd栏目中的，E:\stable-diffusion-webui_23-04-18\extensions文件中。

2.下载预训练模型

1. [sadtalker.zip - Google 云端硬盘](https://drive.google.com/file/d/1gwWh45pF7aelNP_P78uDJL8Sycep-K7j/view)

2. [gfpgan.zip - Google 云端硬盘](https://drive.google.com/file/d/19AIBsmfcHW6BRJmeqSFlG5fL445Xmsyi/edit)

​	需要魔法上网

​	百度网盘：

​	1.https://pan.baidu.com/share/init?surl=P4fRgk9gaSutZnn8YW034Q&pwd=sadt）

​	2.（https://pan.baidu.com/s/1kb1BCPaLOWX1JJb9Czbn6w?pwd=sadt）

两个预训练模型下载好后将这两个文件夹复制粘贴到你的SadTalker文件夹中去

![image](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/662ed403-c7e4-4315-88e0-a9a6679366d5)


![image-20230621142123399](C:\Users\28402\AppData\Roaming\Typora\typora-user-images\image-20230621142123399.png)


![tmpwqvcjocw__1-0-100](https://github.com/Mr-Poole3/Stable-Diffusion/assets/112788987/cca26f56-64e7-4033-ab75-1c431f990397)





5.大功成啦！！！现在导入你的图片和音频就能实现啦！！（大概3秒需要30s，这取决于你的GPU和是否安装CUDA)
后面我也会教大家如何基于Stable Diffusion来训练一个属于自己想要的风格的Lora模型   网址：


