# AI 名片

1. 开启下拉刷新

    现在对应页面下的json里面添加

    ```js
        {
        "enablePullDownRefresh": true
        }
    ```

    下拉刷新那三个点默认是白色的，所以要在json成设置成暗色调，`"backgroundTextStyle": "dark",`

    事件用 `onPullDownRefresh` 监听


    
1. openSetting 只能通过 button 组件调请

    `<button open-type="openSetting">`

1. `data-` 里卖弄自定义的值必须是小写的
    
    如果写成大小写的，例如 `customerId` 会被是被成 `customerid`

1. 获取用系统时间不能用 `new Date()`, 要用`getDate()`

1. swiper 组件要设置高度

```html
<swiper height="{{swiperHeight}}">
    <swiper-item>
        <view class="swiper-wrap"></view>
    </swiper-item>
</swiper>
```

```js
wx.createSelectorQuery()
    .selectAll('swiper-wrap')
    .boundingClientRect(rect => {
        console.log(rect)
        this.setData({
            swiperHeight: rect[0].height
        })
    })
    .exec()
```

通过动态判断 `swiper-wrap` 高度，并设置给 `swiper` 组件，这样就能动态设置swiper高度。



