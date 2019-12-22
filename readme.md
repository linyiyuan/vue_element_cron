## 安装

该项目是由 [ldy](https://gitee.com/lindeyi) 作者编写，该项目是由从作者项目下直接转载，非原创

项目地址：

*   [https://github.com/linyiyuan/vue_element_cron](https://github.com/linyiyuan/vue_element_cron)

首先我们将该项目本地克隆下来，然后将 `src/components` 里面的两个文件 `cron.vue`, `cron` 复制到我们的项目中的`components`中即可。


## 使用方式

在我们需要使用到该插件的页面中去引入该插件, 并注册

```javascript
import cron from '@/components/cron'

export default {
name: "App",
components: {
  cron
},
....
```

然后我们在指定显示组件的地方粘贴下以下代码：

```HTML
<el-form-item style="margin-top: -10px; margin-bottom:0px;">
          <span style="color: #E6A23C; font-size: 12px;">corn从左到右（用空格隔开）：秒 分 小时 月份中的日期 月份 星期中的日期 年份</span>
          <cron v-if="showCronBox" v-model="cronParams"></cron>
</el-form-item>
        <el-form-item label="cron表达式">
          <el-input size="medium" v-model="cronParams" auto-complete="off" placeholder="请填写cron表达式">
            <el-button slot="append" v-if="!showCronBox" icon="el-icon-arrow-up" @click="showCronBox= true" title="打开图形配置"></el-button>
            <el-button slot="append" v-else icon="el-icon-arrow-down" @click="showCronBox= false" title="关闭图形配置"></el-button>
          </el-input>
</el-form-item>
```

然后我们同样需要在`data` 数据块中加上以下数据即可：

```javascript
data() {
  return {
    cronParams: null,
    showCronBox: false,
  }
}
```

## 页面演示

![页面一](http://images.linyiyuan.top/cron1.png)

![页面二](http://images.linyiyuan.top/cron2.png)

![页面三](http://images.linyiyuan.top/cron3.png)

![页面四](http://images.linyiyuan.top/cron4.png)

