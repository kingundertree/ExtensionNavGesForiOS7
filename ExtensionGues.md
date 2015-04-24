###拦截iOS7 滑动返回手势

###效果图
见iOS7 系统自带原生手势滑动返回，但是控制区域在左侧10px位置，本demo支持viewController全部区域
![Mou icon](https://raw.githubusercontent.com/kingundertree/ExtensionNavGesForiOS7/master/extension.gif)

###github地址

https://github.com/kingundertree/ExtensionNavGesForiOS7

###主要功能
1. 模拟iOS手势滑动返回效果
2. 只支持iOS7 及以上版本
3. 此方法比较简单，而且系统提供的手势滑动效果更加细腻。但是采用NSRunloop截图系统事件，使用需谨慎。

###实现思路
1. iOS7 开始，系统提供手势滑动返回功能，但是操作区域有限
2. 设法截取系统手势事件，UINavgationController的interactivePopGestureRecognizer
3. 自定义UIPanGestureRecognizer并add到UINavgationController的view上
4. 截取interactivePopGestureRecognizer的target和action
5. 把interactivePopGestureRecognizer的target和action，赋给自定义的手势上即可

###使用方法
1. 继承ExtensionNav即可