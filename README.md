# GDUINavigationController-FDFullscreenPopGesture
================================================

# 导航控制器手势返回修正

## Method 
    无需导入头文件，直接将.h .m文件拖入项目目录 即可使用
 
![示例图](https://raw.githubusercontent.com/forkingdog/FDFullscreenPopGesture/master/Snapshots/snapshot0.gif)



#Usage
AOP, just add 2 files and no need for any setups, all navigation controllers will be able to use fullscreen pop gesture automatically.

To disable this pop gesture of a navigation controller:
```objc
  navigationController.fd_fullscreenPopGestureRecognizer.enabled = NO;
```
To disable this pop gesture of a view controller:
```objc
viewController.fd_interactivePopDisabled = YES;
```
Require at least `iOS 7.0.`

This opmiziation is enabled by default, from now on you don't need to call UINavigationController's

  -setNavigationBarHidden:animated: method, instead, use view controller's specific API to hide its bar:

![示例图](https://raw.githubusercontent.com/forkingdog/FDFullscreenPopGesture/master/Snapshots/snapshot1.gif)

```objc
- (void)viewDidLoad {
    [super viewDidLoad];
    self.fd_prefersNavigationBarHidden = NO;
}
```
And this property is NO by default.
