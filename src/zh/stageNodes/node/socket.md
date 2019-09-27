---
sidebar: auto
sidebarDepth: 2
---

## socket
 Socket是应用层与TCP/IP协议族通信的中间软件抽象层，它是一组接口。在设计模式中，Socket其实就是一个门面模式，它把复杂的TCP/IP协议族隐藏在Socket接口后面，对用户来说，一组简单的接口就是全部，让Socket去组织数据，以符合指定的协议。
 
 前端代码
 
 
```

<script src="https://cdn.bootcss.com/react/16.8.6/umd/react.development.js"></script>

<script src="https://cdn.bootcss.com/react-dom/16.8.6/umd/react-dom.development.js"></script>

<script src="https://cdn.bootcss.com/babel-standalone/6.26.0/babel.js"></script>

<script src='https://cdn.bootcss.com/socket.io/2.2.0/socket.io.js'></script>

<script src="https://cdn.bootcss.com/axios/0.18.0/axios.js"></script>

<body>
    <div id='box'></div>
    <script type="text/babel">
         let {Component}=React;
         let socketObj=io.connect("http://localhost:9090")
         class Index extends Component{
             render(){
                 return (
                     <div>
                         <button onClick={this.sendCli} >点击</button>
                     </div>
                 )
             }
             sendCli=()=>{
                 axios.get("http://localhost:9090/getList").then(res=>{
                     console.log(res.data)
                 })
             }
             componentDidMount() {
                socketObj.on("getCount",(res)=>{
                    console.log(res)
                })
             }
         }
         ReactDOM.render(<Index/>,document.getElementById('box'))
    </script>
</body>
```

后端代码


```
const express = require("express")
const app = express()
let globalSocket = null;
app.get("/getList", (req, res) => {
    globalSocket.emit('getCount', 5)
    res.writeHead(200, {
        "Access-Control-Allow-Origin": "*"
    })
    res.end("ppp")
})
const server = app.listen(9090, () => {
    console.log("server is running at 9090")
})
let io = require("socket.io").listen(server);
io.sockets.on("connection", (socket) => {
    globalSocket = socket
    console.log("socket已连接")
})
```

