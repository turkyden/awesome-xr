# Awesome XR

国内 AR VR 从业者交流

## WebVR

- 客户端 VR
- 浏览器 VR

使用 three.js 和 react.js 创建实时的多人 WebXR 体验

https://jamesmiller.blog/tag/extended-reality/

## WebAR

- ARKit
- 

[IOS 微信内置浏览器明明能开启摄像头为什么不支持 AR.js] - https://zhuanlan.zhihu.com/p/34580521

【跨平台移动Web AR的关键技术介绍及应用】https://www.w3.org/2021/07/chinese-ig-xr/slides/WebXR-yakun-huang.pdf

微信 IOS 兼容写法 `getUserMedia`：

```
//访问用户媒体设备的兼容方法
function getUserMedia(constraints, success, error) {

  if (navigator.mediaDevices.getUserMedia) {
    //最新的标准API
    console.log("navigator",navigator);
    navigator.mediaDevices.getUserMedia(constraints).then(success).catch(error);
  } else if (navigator.webkitGetUserMedia) {
    //webkit核心浏览器
    navigator.webkitGetUserMedia(constraints,success, error)
  } else if (navigator.mozGetUserMedia) {
    //firfox浏览器
    navigator.mozGetUserMedia(constraints, success, error);
  } else if (navigator.getUserMedia) {
    //旧版API
    navigator.getUserMedia(constraints, success, error);
  }
}
```

<img width="300" src="https://user-images.githubusercontent.com/24560160/194598238-02951753-7d7e-4768-8db6-672ffc080aeb.png">
