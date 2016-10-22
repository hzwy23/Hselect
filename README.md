这个JS文件是对select标签的一个扩展，使得select能够支持树形下拉框

### 1.依赖关系：
   使用这段js代码之前，请先引入jQuery库。


### 2.使用示例代码：

```javascript
	$.getJSON("/api/data/jsonType",function(data){

		var arr = new Array();

	    $(data).each(function(index,element){

	        var ijs = {};

	        ijs.id = element.Busiz_id

	        ijs.text = element.Busiz_desc

	        ijs.upId = element.Busiz_up_id

	        arr.push(ijs)

	          
	    });

	    $("#SelectId").Hselect({

	        data:arr,

	        height:"29px",

	        border:"#ccc solid 1px"

	    });

	}
```


### 3.可供修改的参数：
```
    #待显示数据
	data: "",

	#提示框高度
    height:"26px",

    #提示框宽度
    width:"auto",

    #提示框边框属性
    border:"#000 solid 1px",

    #提示框字体大小
    fontSize:"13px",
    
    #提示框圆角大小
    borderRadius:"5px",

    #提示框背景色
    bgColor:"white",
            

    #下边这个参数，是树形下拉框中每一个选项的高度
    showLiHeight:"30px",

    #下边这个参数，是树形下拉框的最大高度
    showHeight:"230px",

    #下边这个参数，是树形下拉框中，边框属性
    showBorder:"#31708f solid 1px",

    #下边这个参数，是树形下拉框中，字体大小
    showFontSize:"14px",

    #下边这个参数，是树形下拉框中，隐藏或展示图标的颜色。
    iconColor:"#ff5763",
```

