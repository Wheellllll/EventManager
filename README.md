
## 配置模块
> 这是一个简单的事件转发模块，目前仅支持string转发

### 安装
从 https://github.com/Wheellllll/ConfigManager/releases 下载最新的jar包添加到项目依赖里去

### 实例
```java
EventManager mEventManager = new EventManager();

//注册事件
mEventManager.addEventListener ("login" , new EventListener () {
    @Override
    public void run (HashMap <String, String> args) {
        //Do something

    }
});

//模拟触发事件
HashMap<String, String> args = new HashMap<>();
args.put("username", "admin");
args.put("password", "admin");
mEventManager.triggerEvent("login"); //触发login事件
```
