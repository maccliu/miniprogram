# 全局样式

`app.wxss`文件存放全局样式。

## 宽度

### 传统12栏宽度系列

类名：`.w-*`

```css
.w-1  {width: 8.333333%;}
.w-2  {width: 16.666666%;}
.w-3  {width: 25%;}
.w-4  {width: 33.333333%;}
.w-5  {width: 41.666666%;}
.w-6  {width: 50%;}
.w-7  {width: 58.333333%;}
.w-8  {width: 66.666666%;}
.w-9  {width: 75%;}
.w-10 {width: 83.333333%;}
.w-11 {width: 91.666666%;}
.w-12 {width: 100%;}
```

### 5栏宽度系列

类名：`.w-5-*`

```css
.w-5-1 {width: 20%;}
.w-5-2 {width: 40%;}
.w-5-3 {width: 60%;}
.w-5-4 {width: 80%;}
.w-5-5 {width: 100%;}
```

## 组件

### .badge

```css
.badge {
  position: absolute;
  display: block;
  top: 0;
  right: 15rpx;
  min-width: 30rpx;
  line-height: 30rpx;
  font-size: 24rpx;
  border-radius: 15rpx;
  background-color: red;
  color: white;
  text-align: center;
}
```

> 1. 记得要设置 `badge` 的父元素的 `position: ...` 属性。


### .footer 固定页脚

scss代码

```scss
$footer-height: 100rpx;   // 页脚的高度

/* 页脚 */
.footer {
  position: fixed;
  bottom: 0;
  height: $footer-height;
  width: 100%;
  box-sizing: border-box;
  background-color: #eee;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

/* 页脚的占位 */
.footer-space {
  box-sizing: border-box;
  width: 100%;
  height: $footer-height;
}

/* 页脚项目 */
.footer-item {
  height: $footer-height;

  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;

  /* 按钮模式 */
  &.button {
    text-align: center;
    font-size: 28rpx;
    line-height: 40rpx;
    color: #009b72;

    /* 主按钮模式 */
    &.primary {
      color: #fff;
      background-color: #009b72;
    }
  }
}
```

> 备注：
> 1. 因为`.footer`是固定在页面页脚的，所以主体内容部分要加上对应的占用空间`.footer-space`，不然最底下的内容会被页脚挡住了。


css代码

```css
/* 页脚 */
.footer {
  position: fixed;
  bottom: 0;
  height: 100rpx;
  width: 100%;
  box-sizing: border-box;
  background-color: #eee;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
}

/* 页脚的占位 */
.footer-space {
  box-sizing: border-box;
  width: 100%;
  height: 100rpx;
}

/* 页脚条目 */
.footer-item {
  height: 100rpx;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  position: relative;
}
.footer-item.button {
  text-align: center;
  font-size: 28rpx;
  line-height: 40rpx;
  color: #009b72;
}
.footer-item.button.primary {
  color: #fff;
  background-color: #009b72;
}

```
