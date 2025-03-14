# fridaUiTools

fridaUiTools是一个界面化整理脚本的工具。新人的练手作品。参考项目ZenTracer，觉得既然可以界面化，那么应该可以把功能做的更加完善一些。跨平台支持：win、mac、linux

功能缝合怪。把一些常用的frida的hook脚本简单统一输出方式后，整合进来。并且将自己觉得常用的功能做成界面调用的。还想动态获取一些信息默认的直接展示。后续会根据自己实战的经验。不断完善这个工具。

##  Hook脚本如下（附加进程前使用）

> * 整合r0capture
> * 整合jnitrace
> * java层的加解密相关自吐
> * ssl pining（整合DroidSSLUnpinning）
> * 模糊匹配函数进行批量hook（整合ZenTracer）
> * native的sub函数批量hook（参数统一方式打印。所以输出只能做参考）
> * stalker的trace（整合sktrace）
> * 整合frida_hook_libart
> * 脱壳相关（整合frida_dump、FRIDA-DEXDump、fart）
> * 自定义脚本添加
> * patch汇编代码 


## 调用功能如下（附加进程后使用）

> * fart主动调用
> * DUMPDex主动调用
> * dump打印指定地址
> * dump指定模块
> * wallBreak整合

## 应用信息

附加成功时将一些信息带出来给界面展示。目前仅将module列表和class列表展示出来。可以查询函数以及符号

## 日志说明

### 1、操作日志

是对软件操作的所有输出日志。

### 2、输出日志

所有js返回的日志都在输出日志。并且保存在logs目录中

### 3、当前hook列表

当前勾选的hook脚本列表展示。可以保存，方便以后直接加载使用。



## 应用部分界面

![image-20210710125622863](./img/image-20210624204848522.png)

![image-20210710130420705](./img/image-20210710130116100.png)

![image-20210710130555333](./img/image-20210710130509193.png)

![image-20210710130631452](./img/image-20210710130631452.png)

![image-20210710130712969](./img/image-20210710130712969.png)

![image-20210710130905757](./img/image-20210710130905757.png)

![image-20210723161040549](./img/image-20210723161040549.png)



## 使用说明

软件里面有很多地方用到了缓存数据。缓存数据是附加一次进程后，保存下来的module和class列表。这样方便智能的检索。所以一般第一次使用的时候，先附加一次目标进程，就有缓存数据可以使用了。

fart如果第一次使用，需要在上传与下载菜单栏中点击上传fart的so。

软件目前应该还存在很多瑕疵和bug。我会在实用中慢慢修补。

## 新增功能

> frida-server14.2的自动上传到手机
>
> frida-server的启动
>
> 自定义脚本功能
>
> fart的dump结果下载
>
> 增加patch功能
>
> 应用信息显示（adb shell dumpsys取出来的数据）
>
> hookEvent（app的所有控件的点击事件hook）
>
> cmd切换（有些设备是需要adb shell su 0来使用su权限的，有些是adb shell su -c。这里为了通用，可以自己切换）
> 
> 增加模拟器启动frida-server的支持
>
> 增加下载当前apk功能
>
> 增加fart的bin文件修复
>
> 增加stalker的整理，将stalker输出的日志整理成更方便阅读的格式
## 感谢

* [jnitrace](https://github.com/chame1eon/jnitrace)
* [r0capture](https://github.com/r0ysue/r0capture)
* [ZenTracer](https://github.com/hluwa/ZenTracer)
* [DroidSSLUnpinning](https://github.com/WooyunDota/DroidSSLUnpinning)
* [frida_dump](https://github.com/lasting-yang/frida_dump)
* [FRIDA-DEXDump](https://github.com/hluwa/FRIDA-DEXDump)
* [FART](https://github.com/hanbinglengyue/FART)
* [sktrace](https://github.com/bmax121/sktrace)
* [Wallbreaker](https://github.com/hluwa/Wallbreaker)
