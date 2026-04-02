## 04.01 vue3
- node_modules 所有依赖文件的包
- index.html静态文件夹
- src/assets 资源
###  setup方法是应用开发中的主方法
- vue 脚本文件要写在script 尖括号中
	~~~
	<script src="https://unpkg.com/vue@3.5.31/dist/vue.global.js"></script>
	~~~
 
## 04.02 Vue3
- 在VS code中安装Vue扩展包才能看到{{ }}中的代码颜色
- Vue的插值表达式{{}}中可以直接写JS
~~~
//Math是对象
//Math.floor(数字); 向下取整
//Math.random();随机返回(0,1),0~1中的一个数字 不包括1
<body>
    <div id="vue3Demo">
    <h1>{{message}}</h1>
    <p>The luckNumber is {{luckNumber}}</p>
    <p>The luckNumber is {{luckNumber%2==0?"even luckNumber":"odd luckNumber"}}</p>
    <p>{{luckNumbers}}</p>
    <p>{{employee.name}} is {{employee.age}} years old!</p>
    <p>Random Number  from:1-10:{{Math.floor(Math.random()*10)}}</p>
    //取0到9再减去1=-1~8
    <p>{{Math.floor(Math.random()*10-1)}}</p>
    </div>
</body>
~~~
- 在插值表达式中使用方法
~~~
//message.toLowerCase();
//message.toUpperCase();
<p>Random Number  from:1-10:{{getLuckNumer()}}</p>

 function getLuckNumer(){
                return Math.floor(Math.random()*10+1);
            }
~~~
### ref
- 使用ref前需要从视图导入
- 对ref变量值进行更新，对变量的value属性进行赋值
  ~~~
  const {ref}=Vue;
   let luckNumber=ref(7);
     function getLuckNumer(){
                 luckNumber.value=Math.floor(Math.random()*10+1);
                return Math.floor(Math.random()*10+1);
            }
  ~~~
