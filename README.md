#前端开发 第一次
## 1、作用域
### 浏览器在什么时候进入到作用域
1、当他看到script标签得时候进入作用域
2、当执行方法得时候（不是声明方法）
###进入了作用域发生了什么事情
   1、js预解析（未执行做准备）
     首先是在内存里面开辟一个空间
   2、是否有方法参数，有没有方法体，如果有var 有方法参数，就会被var和方法参数声明得变量赋值为一个undefined.
    如果有方法体，就会把整个方法存在那个空间里。
3、js执行
    js逐行执行，找有没有表达式，赋值 +-*/ = ++ --
    如果有表达式，就会修改js与解析里面得值。


    例子：
    1.js预解析
    2.a=undefined
    function a(){consoloe.log(a)}
    //方法得权重高
    

    遇到全局，里面得改，外面得也改，外面得改，里面得也改。


例子1：

	 window.onload = function(){
	            //1、
	            // console.log(a);
	            // var a = 1;
	            // console.log(a);
	            // function a(){console.log(2);}
	            // console.log(a);
	            // var a=3;
	            // console.log(a);
	            // function a(){console.log(4);}
	            // console.log(a);
	            // a();
		}

例子2：
	            
                // var a = 1;
	            // function fn1(){
	            //    console.log(a);
	            //    var a =2;
	            // }
	            // fn1();
	            // console.log(a);

例子3：

 			    var a = 1;
			    function fn1(a){
			       console.log(a);
			       var a =2;
			    }
			    fn1();
			    console.log(a);





