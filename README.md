# vue-droplist
vue项目的下拉框
## 介绍
vue-droplist是一款小型的下拉框
## 使用

### 安装
cnpm install vue-droplist --save

### 组件中导入
import DropList from 'vue-droplist'

### 注册组件
```js
components: {
  DropList
}
```

### data里设置配置信息
```js
data() {
  configData : {
    position: {  // 设置显示位置，position
      top: '', 
      right: '',
      bottom: '',
      left: ''
    },
    width: '40%', // 设置宽度
    list: [ // 设置下拉列表数据和对应的点击事件
      {text: '修改资料', action: this.updateUserInfo},
      {text: '更换主题', action: this.updateTheme},
      {text: '退出账号', action: this.signOut}
      ...
    ]
}
```

### html
```html
    <drop-list :config="configData" ref="droplist"></drop-list>
```

### 使用
默认点击其他区域和选中列表会自动隐藏，无需手动隐藏
#### 显示
    this.$refs.droplist.show()
#### 隐藏
    this.refs.droplist.hidden()

### 效果
![Image text](https://github.com/ClmPisces/vue-droplist/blob/master/egimg.png)