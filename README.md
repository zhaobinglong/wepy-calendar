# wepy-canlendar

一款微信小程序的日历组件,可用于订单订票等业务，选择入住退房时间，出发返程时间

## Screenshots


## 开始
cnpm install
wepy build --watch


```
import calendar from '../components/calendar

<calendar :visible.sync="calendarVisible"  :value.sync="time" @hanleConfirm.user="hanleConfirm" color="#05c8d3"></calendar>
  data = {
    calendarVisible: false,
    time: '2018-04-11'
  }
  components = {
    calendar
  }
  methods = {
    showcalendar () {
      this.calendarVisible = true
    },
    hanleConfirm (e) {
      console.log(e)// 导出数据
    }
  }


```
最后导出的数据很友好:
```
// 导出一个object
{
    day:27,
    formatDay:'2018-05-27',
    month:5,
    weekCh:'周日',
    year: 2018
}

```

## API

### wepy-calendar props

<table class="table table-bordered table-striped">
    <thead>
    <tr>
        <th style="width: 80px;">name</th>
        <th style="width: 50px;">type</th>
        <th style="width: 30px;">default</th>
        <th>description</th>
    </tr>
    </thead>
    <tbody>
        <tr>
          <td>visible</td>
          <td>Boolean</td>
          <td>false</td>
          <td>控制dialog的显示</td>
        </tr>
        <tr>
          <td>value</td>
          <td>String(YYYY-MM-DD)</td>
          <td>moment().format('YYYY-MM-DD')</td>
          <td>日历初始值</td>
        </tr>
        <tr>
          <td>hanleConfirm.user</td>
          <td>自定义事件</td>
          <td>必填</td>
          <td>点击确定按钮触发的钩子</td>
        </tr>
        <tr>
          <td>color</td>
          <td>rgb rgba等(css里的颜色值都可用)</td>
          <td>black</td>
          <td>日历主色</td>
        </tr>
    </tbody>
</table>



## License

wepy-calendar is released under the MIT license.
