day1
第一节课：
        JavaScript简介：
        1、什么是JavaScript？
            官方：JavaScript是一种基于对象和事件驱动的客户端脚本语言。是嵌入到HTML中的。
                换句话说JavaScript是运行在客户端的嵌入式脚本语言
                
        2、JavaScript的组成部分 (ECMA 欧洲计算机制造商协会)
            ECMAScript-262（语法规范）   //ECMA-262  js的核心：变量声明 函数 语句 if
            document object model //DOM   文档对象模型   页面元素  div h2
            Browser object model  //BOM   浏览器对象模型
            版本：ES4 ES6
                
        3、javaScript的基本特点：（理解）
            是一种解释性的脚本语言，（代码不进行预编译）（记忆）
            主要用来向HTML页面加入交互行为
            可以直接嵌入 HTML 页面，但写成单独的js文件有利于结构和行为的分离
            
        4、JavaScript特性（了解）
            a)不同于服务器端脚本语言，例如PHP与ASP，JavaScript主要被作为客户端脚本语言在用户的浏览器上运行，不需要服务器的支持
            b)跨平台、容易上手，随着引擎如V8和框架如Node.js的发展，及其事件驱动及异步IO等特性，JavaScript逐渐被用来编写服务器端程序
            c)所有主流浏览器都支持JavaScript
            d)目前，全世界大部分网页都使用JavaScript

        5、JavaScript可以实现什么效果（作用）（了解）
            a)嵌入动态文本于HTML页面
            b)对浏览器事件作出响应
            c)读写HTML元素
            d)在数据被提交到服务器之前验证数据
            e)检测访客的浏览器信息
            f)控制cookies，包括创建和修改等
             
        4、在HTML中如何去使用JavaScript（js代码放在哪里）
            内嵌脚本：在head或body中使用<script type="text/javascript">写入js代码</script>
            外部文件：<script src="路径/文件名.js" type="text/javascript"></script>
            执行顺序：从上到下依次执行
            位置：body 或head
        
    第二节课：了解JavaScript的基础语法
    
        1、什么是标识符？
            在js中所有的可以由自己自主命名的都可称为是标识符，例如
            变量名 函数名 属性名或则函数的参数（你自己的名字就是你的标识，能让他认识你）
            
        2、标识符的命名规则：
            由字母、数字、下划线_ 或 $组成
            不能以数字开头，区分大小写
            不能使用关键字、保留字等作为标识符。
            建议驼峰命名规则，第一个字母小写、其他单词的首字母大写。
        3、输出的三种方式：
            alert('内容') 弹出框 警示框
            document.write("内容");页面内输出
                注意：如果遇到div标签，以字符串方式输出（浏览器识别标签，例如识别一级标题）
            控制台输出（打印输出）console.log（"内容"）;  
            举例说明：问是否命名正确;
        4、JavaScript注释：
            html:
            css:  // /**/，。
            注释的作用：
            JavaScript 不会执行注释。
            - 我们可以添加注释来对 JavaScript 进行解释，提高代码的可读性。
            也可以使用注释来阻止一行或多行代码执行 
            js: //   /**/

        5、JavaScript语句和分号（了解）
            JavaScript语句向浏览器发出的命令，语句的作用是告诉浏览器该做什么。
            下面的语句JavaScript语句向id= "demo"的HTML元素输出文本"HRlloWord"
            document.getElementById("demo").innerHTML = "HelloWord"

            分号：分号用于分隔 JavaScript 语句。
                通常我们在每条可执行的语句结尾添加分号。
                使用分号的另一用处是在一行中编写多条语句
                分号是可以省略的，在JavaScript中，用分号结束语句是可选的；
        
        6、什么是变量？
            JavaScript变量可用于存放值（x=5）和表达式（z=x+y)的占位符，
            变量可以使用短名称（x,y)，也可以使用描述性更好的名称（age,sum）等命名，

        7、定义（声明）变量的关键字是：var
            语法：var 变量名
        8、变量的赋值
            声明的同时赋初始值  var 变量名 = 初始值
            先声明后赋值   var 变量名    变量名 = 值

        9、变量的相关规则：   
            区分大小写
            定义多个变量之间用,隔开  var a=5,b=10;
            变量赋值：后写的值覆盖先写的值
            变量的赋值：把右侧的运算结果赋给左侧的变量；
            c = a+b;
            var 声明的变量叫做显示声明
            没有var声明的变量 直接赋值，叫隐式声明，是一个全局变量。
            
            ECMAScript的变量时松散类型,松散类型，可以用来保存任何类型的数据
            换句话说：变量本身是没有类型的，变量的类型是由变量的值决定的。


    第三节课：掌握基础数据类型

       1、 数据类型：
               5种基本类型：
                    Number类型 （数值类型） 10 34.00 52.00
                    String类型 （字符串类型） "123456"
                    Boolean类型 (布尔类型)  true false
                    undefined类型 （未定义类型） 
                    null类型 （空类型） null 也叫空对象指针；
               1种复杂类型：
                    Object 对象类型 （引用类型）
                    var obj = {} ;//对象字面量 
                    var obj = new Object(); //构造模式
        2、判断数据类型的关键字:typeof用来表示表达式的数据类型的字符串
                语法：typeof 变量名  或则
                     typeof（变量名）
                功能：检测变量类型的返回值
                返回值："number" "string" "boolean" "undefined" "object" "function"

        3、数据类型介绍：
            3.1、undefined类型 (未定义类型),表示，变量不含有值
                该类型只有一个值：即特殊的undefined
                var a;
                1)变量定义未赋值 ：值是undefined  返回类型：undefined;
                2)变量没有定义（没有声明） ： 值：报错 ； 返回类型：undefined；

            3.2、null：可以通过将一个变量的值设置为null，来清空变量。
                var a=123;a=null >null;
                1)null值表示一个空对象指针；
                2)如果定义的变量准备在将来用于保存对象，那么最好将改变的量初始化为null，而不是其他值。
                3）null是一种特殊的object类型；
                说明：undefined 值时派生自null值，所以undefined == null的结果是true
            3.3、Number：表示整数和浮点数
                    整数：1,2,3
                    浮点数：.1,0.4
                    极大数字：123e5  //12300000  科学计数法
                    极小数字：123e-5  //0.00123 
                    注意：保存浮点型的数值需要的内存空间比整形大两倍，因此ECMAScript,会讲能转化为整型的浮点数值自动转化为整型，如12.0
                    说明：浮点型的数值最高精度为17位小数，而我们口算中，可能不会精确，
                    所以在判断时要注意考虑到这个问题
                    eg:alert(0.1+0.2);
                NaN：即非数值（Not a Number）是一个特殊的数值。这个数值用于表示一个本来要返回数值的操作数未返回数值的情况(这样就不会抛出错误了)。
                    例如，在其他编程语言中，任何数值除以 0都会导致错误，从而停止代码执行。但在 ECMAScript中，任何数值除以 0会返回 NaN ，因此不会影响其他代码的执行。
                    var box = 0/0;

                    说明：
                        1）NaN不是一个数值，但他是一个number
		                2）任何涉及NaN的操作（例如NaN/10）都会返回NaN。
		                3）NaN与任何值都不相等，包括NaN本身。
                        var a = NaN + 1  //NaN
                        console.log(NaN  == NaN)  //false;

            3.4、string类型：用 "" ''包含的内容
                    注意："" '' 具有对称性 成对出现
                    var str= "1610B"
                    也可以在字符串中使用引号，只要不匹配包围字符串的引号即可
                    var str = '<div class = 'box'>123</div>'
                    字符串的属性：length 表示长度
                        变量名.length 返回变量的长度，类型是一个数值类型
                    空字符 "" '' 的长度为0；
                  

            3.5、Boolean 布尔类型 用于表示真假的类型，即true表示真，false表示假
            3.6、Object对象类型
                var timer = null
                timer 的值时null 空对象指针
                timer 的类型为object
                object:对象，只是带有属性和方法的特殊数据类型，
                        对象有花括号分隔，在括号内部，对象的属性以名称和值对的形式 (name : value) 来定义。属性由逗号分隔
                        对象字面量方式定义：var aa={name:"王五"，age:"23",sex:"男"，sayName: function(){
                alert(this.name);
                }}
                        构造函数的方式定义：var aa = new Object()

                            为对象添加属性和方法：aa.name = "张三"；
                            
                        对象属性的两种寻址方式：
                        var b = aa.sex;
                        var c = aa["age"]  //中括号方式访问的必须是字符串
                对象数组：arr[{name:"王五"，age:"23",sex:"男"},{name:"赵柳",age:"45",sex:"女"}]
                访问：arr[0].name;
            说明：var a = function(){}; typeof a;  返回值时"function";
    
    第四节课：

        1.数据类型的转换
            1）转换为布尔类型：
                Boolean(变量)
                数值转换为布尔： 非0 数字都是true ；0和NaN 是 false
                字符串转换为布尔 非空字符串都是true ； "" 是false   
                undefined 转换为布尔为 false 
                null转换为布尔为 false

                也就是说：转换为false的有哪些类型：0  NaN  ""  undefined null
                
            2)转换为number类型：
                有3个函数可以把非数值转换为数值：Number()、parseInt()和parseFloat()其中Number()可以用于任何数据类型，
                而parseInt()和parseFloat()则专门用于把字符串转换成数值。

                字符串转换为number的规则：
                    1.只包含数值的字符串，会直接转数值，如果包含前导0，即自动去掉。

                        alert(Number('456')); //456
                        alert(Number('070')); //70
                    2.只包含浮点数值的字符串，会直接转成浮点数值，如果包含前导和后导0，即自动去 掉。

                        alert(Number('08.90')); //8.9

                    3.如果字符串是空，那么直接转成成0。

                        alert(Number('')); //0

                    4.如果不是以上三种字符串类型，则返回NaN。

                        alert(Number('Lee123'); //NaN
                        Number("123sfsda");  //NaN

                布尔转换为number   true:1   false:0
                undefined ：NaN (易错)
                null : 0;

            3)字符串有两个方法。专门转化字符串为数字的：
                parseInt(字符串)	转化为整数     
                parseFloat(字符串)	转化为浮点数
                从第一位开始截取到符合条件的数字

                截取：截取不到结果是NaN.

                parseInt('') NaN
                parseFloat('') NaN
                Number('')   0

                


            4)  isNaN(变量)   返回值是布尔值 true false 
                功能：用来检测是否是非数字
                
                      非数字为true
                      是数字为false

            true: NaN  undefined  "abdee"   
              Number(变量)如果结果是NaN 就true.
                              转化为数字 false .


        isNaN("123abc")   Number("123abc")==NaN   isNaN(NaN)
        isNaN（123）  false
        是NaN？

        !isNaN()  
        不是NaN  true
        是   false

        如果是NaN   返回true
        如果不是NaN  返回false;   123是NaN  false

        var a = 123
        String();   //String(a)
        toString()  //a.toString();
        

五、运算符：
    算术运算符：
        加法：
            数字+数字 = 数字
            数字+NaN = NaN
            数字+字符串=字符串；  //字符串拼接
            数字+null=数字   //null转换为数字是0；
            熟悉+undefined= NaN   //undefined 转换为数字是NaN
            数字+true/false=数字  
            字符串+任何=字符串
        说明：+它既是算术运算符有事字符串运算符，即，它即可做加法运算，又可以做拼接

        减法：
        乘法：
        除法/：
        求模%： 求余数
    总结：
    +   
        a.只要一端是字符串 ，就拼接字符串
   		b.一端是数字 ，另外一端是true,false,NaN ,null,undefined
   		   则Number()之后，做加法。加不出来就是NaN

    - *  /  %  无论何时都是转化为数字，做减法，减不出来NaN.
    
        累加（递增）：++
            ++a与a++都是对a进行递增的过程
            区别：
	            ++a先返回递增之后的a的值（即先加再运算）

	            a++先返回a的原值，再返回递增之后的值（先运算后加）

        递减：-- 同理

逻辑运算符：
    && || ！
    逻辑与 &&：都为真才能为真
        '123' && 'abc' &&   4==5
        
        逻辑与：遇到第一个假，就停下啦，返回第一个假值；
                如果都为真，则返回最后一个

    逻辑或 ||：都为假才能为假

        逻辑或：遇到第一个真，就停下啦，
                如果都是假，则返回最后一个假值
    
    逻辑非 ！：返回值布尔值
        	!5  首先把5转boolean(5) 在取反
        	!4<=0  false<=0

关系运算符（比较运算符）>  >=  <  <=  ==   ===  ！=   ！==  

    返回值都是boolean类型。
        1)两端都是数字直接比较 。
        2)一端是数字，另外一端不是数字，把不是数字的转化为数字进行比较。
        3)如果一端是布尔值，另一端不管是什么，先把布尔转数字。 
        4)如果两端都是字符串.则按照Ascii码值比较。

    == != === !==也叫作相等运算符：
        == 相等 != 不等     先转化为相同类型，再比较
        === 全等    !== 不全等	 不转化，直接比较
        返回值都是boolean类型。
    			 1）两端都是数字或者字符串，直接比较。
                    "abc"=='bcd'  4==5
    			 2）一端是布尔值，先把布尔转为数字。 
    		     3) 一端是数字，一端是字符串，把字符串转化数值。
    		     4) undefined  null NaN  不转化直接比较。

    		     	undefiend 不等任何值   
    		     	null 不等任何值
    		     	NaN  不等任何值
    		     	null==undefined true
    		     	NaN==NaN  false
