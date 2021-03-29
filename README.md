### 机械革命umi air2黑苹果OpenCore引导 
OC引导来源于[@cmbs2019](https://www.cmbs-soft.com/oc-10th-2-8-0/)，感谢作者的无私分享。

原OC引导目前不支持HDMI输出，所以我就改了下以支持HDMI输出。这里只提供我修改后的config.plist文件，完整OC引导请点击原作者ID到其博客下载。修改内容如下：
* 修改SMBIOS为MacBookPro15,2(低压U)
* 添加一些缓冲帧参数

##### 已知问题
* 目前需要在开机前插上HDMI线才能有输出并且支持热插拔。
将SMBIOS换成原来的MacBookPro15,3可以开机后再插线，不过得第二次插拔才能识别并且有画面输出，而且再次拔出线时系统状态栏和显示设置依然会有外接显示器的相关设置，简单讲就是系统依然会停留在外接显示器的状态。

##### 注意事项
下列kext升级后可能会导致相关设备无法使用
- RealtekRTL8111.kext
- VoodooI2C.kext
- VoodooI2CHID.kext