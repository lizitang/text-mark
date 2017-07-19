# jsTextOperation
网页文本选中高亮，关键字搜索高亮

文本编辑元素中的文本选择（Input, TextArea） 

document.activeElement() 方法

https://developer.mozilla.org/en-US/docs/Web/API/Document/activeElement
 
跨标签文本选择 

Selection 对象，window.getSelection() 方法

https://developer.mozilla.org/en-US/docs/Web/API/Selection

http://www.cnblogs.com/rainman/archive/2011/02/27/1966482.html

#### 写了一个更简单的方法：
	```
		function TextHighlight() {
	    	if(!lock){
	    		return false;
	    	}
	    	var sel = window.getSelection();
			var span = document.createElement("span");
	        span.style.background = "yellow";
			sel.getRangeAt(0).surroundContents(span);
			lock=false;
  		}
	```

