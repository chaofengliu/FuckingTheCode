# Activity
## 一、Activity的生命周期

### 1、正常情况下的生命周期

正常情况下的生命周期是指在有用户参与的情况下，Activity所经过的生命周期的改变

1)onCreate
表示Activity正在被创建，这是Activity生命周期的第一个方法，一般在这个方法里可以进行一些初始化工作，比如调用setContentView去加载界面布局资源、初始化Activity所需的数据


2)onRestart
表示Activity正在重新启动，当当前Activity从不可见重新变为不可见状态时，onRestart就会被调用。


3)onStart
表示Activity正在被启动，即将开始，这时Activity已经可见了，但是还没有出现在前台，还无法和用户进行交互。


4)onResume
表示Activity已经可见了，并且出现在前台并开始活动。

5)onPause
表示Activity正在停止，然后接着onStop就会被调用


6)onStop
表示Activity即将停止，可以做些稍微重量级回收工作，但是不能太耗时


7)onDestory
表示Activity即将被销毁，这是Activity生命周期最后一个回调方法，我们可以进行一些回收工作和最终的资源释放


Activity生命周期的切换过程
![生命周期](https://github.com/chaofengliu/FuckingTheCode/blob/main/Android/%E5%9F%BA%E7%A1%80%E7%9F%A5%E8%AF%86/Activity/Activity%E7%94%9F%E5%91%BD%E5%91%A8%E6%9C%9F.jpeg)

具体说明：

1)针对特定Activity，第一次启动

onCreate->onStart->onResume


2)当用户打开新的Activity或者切换到桌面的时候

onPause->onStop

如果新Activity采用了透明主题，当前Activity不会回调onStop

3)当用户再次回到原Activity时 

onRestart->onStart->onResume

4)当用户按back键回退时

onPause->onStop->onDestory

5)当Activity被系统回收后再次打开，生命周期方法回调和1)一样

6)从整个生命周期来说，onCreate和onDestory是配对的，代表Activity的创建和销毁，并且只可能有一次调用；从Activity是否可见来说，onStart和onStop是配对的，这两个方法可能被调用多次；从Activity是否在前台来说，onResume和onPause是配对的，这两个方法可能被调用多次。


### 2、异常情况下的生命周期
异常情况下的生命周期是指Activity被系统回收或者由于当前设备的Configuration发生改变从而导致Activity被销毁重建所经历的生命周期

1）


2）


## 二、Activity的启动模式

## 三、IntentFilter的匹配规则
