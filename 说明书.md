# DEBATE
试问哪一个学创的工作人员不想拥有一个炫酷的计时桌面！它来了，它来了，这就是你所需要的辩论赛html页面，只需要简单的打开ZZU_DTS.html，你就可以拥有一个高颜值的辩论赛管理系统。
### 以往的辩论赛计时系统缺点
- 输入较长辩题/学院名称时文字排版难看
- 背景界面太老了，画质模糊
### 介绍
- 可配置 ：
支持自定义流程，可自由添加/删除辩论赛环节;  css/main.css为字体、位置的设置，该网页所有内容都可以配置.
- 动画  ：
支持炫酷的页面切换动画效果,目前只设置了一个，配置文件为css/animation.css
- 为什么要使用HTML？
HTML网页界面可以完美兼容Mac和Windows系统，可以在任意终端上使用该程序。
### 配置
可对js/main.js中开头的debate对象进行配置，达到自己想要的效果，下面是默认的debate配置：
``` JavaScrip
var debate = {
	title : "ZZU校辩论赛",//主页头部标题
	positive : "正方：工作中遇到坏人要以牙还牙",//正方观点
	negative : "反方：工作中遇到坏人还是不跟TA一般计较",//反方观点
	startback : "images/start.jpg",//主页背景图片，你可以放置图片到images文件夹下，再在这里使用。
	end : "完毕",//结束页感谢语，可以改成别的东西，我懒得想了，就写了个“完毕”
	endback : "images/start.jpg",//结束页背景图片
	animationTime : 0.5,//页面切换动画时间（单位秒）
	startAnimation : {//主页页面切换动画，可在css/annimation.css中进行定义，再在此处使用。
		centerToLeft : "centerToLeft",// 向左移出屏幕的动画，此处配置的动画可在css/annimation.css中找到，是一个平移的动画。
		leftToCenter : "leftToCenter"
	},
	endAnimation : {//结束页页面切换动画
		rightToCenter : "rightToCenter",// 向右移入屏幕的动画。
		centerToRight : "centerToRight"
	},
	pages : [// 辩论赛流程页（数组），一般一个流程定义为一个页面，也就是此数组的一个元素。
		{
			title : "正方开篇立论",//流程页title
			desc : "正方：ABC学院",//流程的描述语。
			back : "images/back.jpg",//流程页背景图片
			timers : [//流程页计时器（数组）
				{
					time : 210//计时器秒数
				}
			],
			animation : { //流程页动画
        leftToCenter : "leftToCenter", //从左移入屏幕的动画
        centerToRight : "centerToRight", // 其它自行理解
        rightToCenter : "rightToCenter", 
        centerToLeft : "centerToLeft" 
      }
		},
		{
			title : "反方盘问",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 90
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "反方开篇立论",
			desc : "反方：XYZ学院",
			back : "images/back.jpg",
			timers : [
				{
					time : 210
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "正方盘问",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 90
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "正方驳论",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 150
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "反方驳论",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 150
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "对辩",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 120
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "正方质询",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 150
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "反方质询",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 150
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "正方质询小结",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 120
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "反方质询小结",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 120
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "自由辩论",
			desc : "上方倒计时为正方，下方倒计时为反方",
			back : "images/back.jpg",
			timers : [
				{
					time : 240
				},
				{
					time : 240
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "反方总结陈词",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 240
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		},
		{
			title : "正方总结陈词",
			desc : " ",
			back : "images/back.jpg",
			timers : [
				{
					time : 240
				}
			],
			animation : {
				leftToCenter : "leftToCenter", 
				centerToRight : "centerToRight",
				rightToCenter : "rightToCenter",
				centerToLeft : "centerToLeft"
			}
		}
	]
}
```
### 注意
必须配置动画效果，因为在设置动画时，配置了：
``` css
animation-fill-mode : forwards;
```
该配置意思为，当动画结束时，保持动画时结束的状态，也就是在动画里配置了从left:0%到left:100%,那么当动画结束时，动画影响的元素的left就是100%。

### 关于默认流程
- 见赛制表.txt  