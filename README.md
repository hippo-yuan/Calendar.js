Calendar.js 跨平台万年历组件  
===    
Calendar.js 万年历组件，PC 移动端均适配的轻量级插件    
`大屏幕`下展示效果  
![PC端图片显示](https://github.com/hippo-yuan/Calendar.js/blob/master/image/GIF.gif)  
`移动端`下展示效果   
![移动端图片显示](https://github.com/hippo-yuan/Calendar.js/blob/master/image/mGIF.gif)  
#### [DEMO查看](http://hippo-yuan.github.io/Calendar.js/)  
功能列表  
------  
* 支持时间选择  
* 支持农历展示  
* 支持禁忌事宜
* 通过拖拽滑动切换日历显示内容    
* 对外提供良好的扩展接口  
* 支持移动端展示  
* 通过less，gulp构建   

使用方法  
------  
### 引入css, js, 并初始化日历对象   
```javascript  
<link rel="stylesheet" href="./build/calendar.css">
<script src="./build/calendar.js"></script>  
<script>
	var calendar = new Calendar();
</script>
```    
### 初始化配置信息  
```javascript  
var defaults = {
    //中文格式内容
    monthNames: ['一月', '二月', '三月', '四月', '五月', '六月', '七月', '八月' , '九月' , '十月', '十一月', '十二月'],
    dayNames : ['周日', '周一', '周二', '周三', '周四', '周五', '周六'],
    dayLongNames : ['星期日', '星期一', '星期二', '星期三', '星期四', '星期五', '星期六'],
    holiday : {
        "1-1" : "元旦",
        "2-2" : "湿地日",
        "2-14" : "情人节",
        "3-8" : "妇女节",
        "3-12" : "植树节",
        "3-15" : "消费者权益日",
        "4-1" : "愚人节",
        "4-22" : "地球日",
        "5-1" : "劳动节",
        "5-4" : "青年节",
        "5-12" : "护士节",
        "5-18" : "博物馆日",
        "6-1" : "儿童节",
        "6-5" : "环境日",
        "6-23" : "奥林匹克日",
        "6-24" : "骨质疏松日",
        "7-1" : "建党节",
        "8-1" : "建军节",
        "9-3" : "抗战胜利日",
        "9-10" : "教师节",
        "10-1" : "国庆节",
        "11-17" : "学生日",
        "12-1" : "艾滋病日",
        "12-24" : "平安夜",
        "12-25" : "圣诞节"
    },
    firstDay: 1,                // 从周一开始,计算
    weekendDays: [0, 6],        // 休息日为：周六, 周日
    dateFormat: 'yyyy-mm-dd',   // 打印格式, formatDate 对应
    limitDis : 80,              // 拖拽限制距离，当大于该距离时，触发页面切换
    weekHandler : "dayThead",   // 星期title内容所在类
    monthContainer : "dateUl",  // 日期内容所在容器类
    toolBar : "timeChoose",     // 工具条所在类
    parentNode : document.body, // 组件插入容器，默认body
};
```    
### 参数说明  
* `monthNames`: 月份展示信息(更改设置，即切换成其他语言)  
* `dayNames`: 每周信息内容  
* `holiday`: 节假日内容，系统已内置部分信息，参数为需要添加的内容  
* `firstDay`: 默认从周一开始计算  
* `weekendDays`: 休息日期，默认周六周日  
* `dateFormat`: 日期展示格式，默认"yyyy-mm-dd"  
* `limieDis`: 拖拽响应最短距离  
* `weekHandler`: 日历时间头部所使用类名  
* `toolBar`:　工具栏所使用的类  
* `parentNode`: 日历组件内容，渲染所在容器，默认document.body




