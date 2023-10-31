# PLSB：Point-Line-Surface-Body


此仓库记录一些经过检验的，用户喜爱的三维场景元素，目前包括：POI点、GIF动画。

## 生成 POI 点

通用的POI点解决方案：基于屏幕空间的UMG图形，基于emoji字体的图标。此demo使用了Google的开源字体Noto：https://fonts.google.com/noto/specimen/Noto+Emoji/glyphs ，该字体基本覆盖了所有emoji字符，用于展示信息类的场景对象。

```js
// 推荐接口格式：
ps.emitMessage(`
    -POI="✅"
    -title="POI标题"
    -color="R=1 G=1 B=1"
    -shape="2"
    -where="X=50000 Y=-1000 Z=0"
    -tag="标签"
`);
```

- POI：传入 Emoji 字符。
- title：POI 图标旁边展示的标题文字。（可以传空）
- color：POI 点的主题颜色，RGB模式。
- shape：0 菱形，1 圆形，2 圆角方形。
- where：XYZ坐标。
- tag：标签文本。
- plain：是否开启纯图标模式，并指定字体大小。（-plain=30）