# 一些能在weex/web多端跑的组件
欢迎大家PR

## 图片组件smartImg
1. 支持weex/web
2. 支持在目标图片加载失败时，展示默认图片
demo:
```
    <SmartImg class="smartImg" 
        :imgUrl="targetImgUrl" 
        :defaultUrl="defaultImgUrl">
    </SmartImg>
```