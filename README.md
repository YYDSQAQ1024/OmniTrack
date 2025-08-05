# OmniTrack
[![Version](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fomnitrack.ngup.eu.org%2Fapi%2Fversion&query=%24.version&label=Version&link=https%3A%2F%2Fomnitrack.ngup.eu.org%2F)](https://omnitrack.ngup.eu.org/)
===========

一个功能丰富并内置应用商店的Minecraft Web面板插件  
**[演示面板(账号密码随便填)](https://omnitrack.ngup.eu.org/?server=demo)**

**获取支持:**
- [QQ群](https://qm.qq.com/q/NrAST9Uqie) or 邮箱: admin@ngup.eu.org

**支持我们**
- [爱发电](https://afdian.com/a/lao_wang)

### 它能干什么？
1. 解除简幻欢限制(其他面板服也行)，解压、压缩文件无需排队，无需IP白名单就能登录，服务器运行时也能管理文件
2. 远程查看服务器状态
3. 远程安装、卸载插件
4. 远程管理、封禁、解禁玩家
5. 远程管理服务器文件
6. 查看服务器日志
7. 观察服务器的一举一动

下载
------
- [OmniTrack官网](https://omnitrack.ngup.eu.org/omnitrack) or [GitHub Release](https://github.com/YYDSQAQ1024/OmniTrack/releases/latest)

### 设备要求
前置插件：暂无  
环境要求：Java16以上  
最低版本：1.8  
已经测试的最高版本：1.21.8  

### 插件安装
1. 确认服务端环境符合设备要求
2. 下载插件文件
3. 将插件文件放入`/plugins`文件夹中
4. 重启服务器

使用
------
1. 默认端口号为`80`，请确保端口未被占用
如端口号被占用，请前往`/plugins/OmniTrack/config.yml`中修改`port`的值  
2. 访问面板`你的服务器IP:面板端口`，例:`111.222.11.22`  
3. 登录面板，默认账号`default`密码`OmniTrack`,登录后可前往设置修改账号和密码  
<img width="1919" height="878" alt="image" src="https://github.com/user-attachments/assets/b064e85b-e8d3-449b-9043-3add7fabf521" />

OTProxy
------
OTProxy是一个OmniTrack的附属插件，它允许您让服务器与面板共用同一个端口，使得单端口的面板服(如简幻欢)也能正常使用OmniTrack
### 下载
- [OmniTrack官网](https://omnitrack.ngup.eu.org/otproxy)

### 设备要求
前置插件：OmniTrack  
环境要求：Java16以上  

### 安装
1. 确保已安装OmniTrack
2. 下载插件文件
3. 将插件文件放入`/plugins`文件夹中
4. 打开`server.properties`,修改`server-port`的值，改成25585或者其他的，使其与服务器连接端口不同
5. 重启服务器
6. 端口`/plugins/OTProxy/config.yml`,修改`ProxyPort`的值，使其与服务器连接端口一致

### 一些问题及解决方法
Q：在使用时控制台有时会弹出红色错误怎么办？  
A：正常情况，无需在意  

Q：简幻欢修改端口后启动服务器端口又被改回去了怎么办？  
A：在服务器根目录(有启动脚本的文件夹)创建一个新的文件夹`server`，将所有服务端有关的文件(启动脚本除外)放入`server`文件夹中，修改位于`server`文件夹中的`server.properties`。打开启动脚本，在`${openjdk21} -Xms1024M -Xmx${maxmem}M -jar server-release.jar`的前面添加代码`cd server`，至此大功告成！开启服务器后，服务器根目录会出现一个server.properties文件，这个文件是面板生成的，不必理会。如要修改服务器参数，请前往`/server/server.properties`修改。  

API/插件开发
------
OmniTrack提供丰富的API接口，开发者可以通过接口实现在面板显示数据等用途  
[OmniTrack API](https://github.com/YYDSQAQ1024/OmniTrack-mvn)


