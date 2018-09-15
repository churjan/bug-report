# AI 名片

- 开启下拉刷新

    现在对应页面下的json里面添加

    ```js
        {
        "enablePullDownRefresh": true
        }
    ```

    下拉刷新那三个点默认是白色的，所以要在json成设置成暗色调，`"backgroundTextStyle": "dark",`

    事件用 `onPullDownRefresh` 监听