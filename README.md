app端的登陆，人脸识别，修改信息等，需要后台的部署。后台是在Eclipse开发，建议用eclipse运行，同时下载Spring Boot插件完成项目的部署；
部署后，后台的WebService也同时发布成功。
部署成功，访问http://localhost:8089/进入后台管理
用户在网页访问http://localhost:8089/netty/openserver后，在控制台看到websocket started，表示netty编写的网络服务器开启成功，通过这个
网络服务器可以通过WebSocket向网页推送消息。
车牌识别：点击app的用户头像，再点击拍照，拍的照片会通过WebService传输到后台，通过WebSocket把识别的车牌发到页面。
地址说明:在停车场账号首页main.jsp两个地址是摄像头的影像网址, 用ip摄像头(一款app)实现
         项目的端口为8089，netty服务器用了9999；app调用WebService接口直接访问pc端的ip地址，前提是手机开热点给手机，保证处于同一网段。
         netty服务器和WebSocket的交互使用localhost访问，前提是同一台电脑打开。否则映射到外网。

