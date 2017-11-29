# 主要功能
### 匿名聊天
分析:取消表单默认提交功能;   
获取内容发送到服务器;   
服务器广播给所有客户端;  
客户端接收到消息放入消息列表;
### 具名聊天
当客户端连接上服务器的时候,第一次说的话作为用户名;    
### 实现私聊功能
点击用户的用户名,在输入框出现@用户名,后面输入的信息只有被@的人才能看到    
在客户端,需要对用户名添加点击事件,做@用户名显示在输入框的功能;       
@用户名 后面的内容截取传送到服务器;      
服务端对接收到的信息做判断,如果带有@符号,那么此信息是私聊信息,不再广播,而是找到对应客户端,发送
##  实现消息持久化,打开聊天室显示最近20条聊天记录 
公共的消息,在广播之前先存入数据库;    
打开聊天室即建立连接之后,就发射自定义事件,从数据库中获取20条记录,传入客户端,客户端绑定上页面   
## 实现分房间聊天功能
进入房间1后,讲的话只有在房间1才能看见,其他房间及原本的"大厅"无法看见;   
对进入房间的客户端做记录,在广播之前先判断客户端是否在房间内,若在房间内,则在房间内广播;       
## 实现删除聊天记录功能   

## 技术栈
socket.io + mongodb/mongoose + bootstrap +express +ES6

## 项目运行
```
npm install
```