- 👋 Hi, I’m @Bokiiqq
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Bokiiqq/Bokiiqq is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
  // 1.获取元素
    // const uname = document.querySelector('input')
    // 2.获取值 获取表单里面的值 用的  表单 .value 
    // console.log(uname.value)   // 电脑
    // console.log(uname.innerHTML) // innertHTML; 得不到表单的内容
    // 3.设置表单的值
    // uname.value = ''
    // console.log(uname.type);
    // uname.type= 'password'
    / 1. a 模块制作 要给 5个链接绑定鼠标经过事件
    // 1.1 获取 a 元素 
    const as = document.querySelectorAll('.tab-nav a')
    // console.log(as) 
    for (let i = 0; i < as.length; i++) {
      // console.log(as[i])
      // 要给 5个链接绑定鼠标经过事件
      as[i].addEventListener('mouseenter', function () {
        // console.log('鼠标经过')
        // 排他思想  
        // 干掉别人 移除类active
        document.querySelector('.tab-nav .active').classList.remove('active')
        // 我登基 我添加类 active  this 当前的那个 a 
        this.classList.add('active')

        // 下面5个大盒子 一一对应  .item 
        // 干掉别人
        document.querySelector('.tab-content .active').classList.remove('active')
        // 对应序号的那个 item 显示 添加 active 类
        document.querySelector(`.tab-content .item:nth-child(${i + 1})`).classList.add('active')
