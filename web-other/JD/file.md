# HTML5 File API 文件上传功能

## 图片上传兼容性测试
* 示例demo测试地址: http://testpdjm.jd.com/html/test/image-preview.html  (其它测试地址都有bug, 只保留这一个, 进行修改后可兼容大部分机型), 测试过程中发现问题都能通过修改代码解决;
* 设备共测试: 13台设备; 其中Android 10台, IOS 3台;
* Android中共测试 5个浏览器 默认浏览器/微信/UC浏览器/QQ浏览器/百度浏览器, 支持率 97%左右, 其中部分浏览器不支持打开相册;
* IOS共测试3个浏览器 safari浏览器/微信/UC浏览器, 支持率100%;  
### 具体如下

| 手机型号     | 默认浏览器      |    微信    |   UC浏览器     |  QQ浏览器     |百度浏览器    |
| :-------------| :-------------|:------------- |:------------- |:-------------|:------------- |
| 小米4C         | 全部支持            |全部支持        |/              |/             |/    |
| 三星Note2     | 支持(自定义样式时,不支持Demo2自定义样式)|全部支持           |全部支持      |/     |/    |
| 三星Note3     | 全部支持            |全部支持           |全部支持            |全部支持           |/    |
| 三星S5     | 全部支持            |全部支持           |全部支持            |全部支持           |/    |
| 华为Mate7     | 全部支持            |全部支持           |全部支持            |全部支持           |/    |
| 联想 S90-t     | 不能打开相册 |全部支持           |全部支持           |全部支持           |全部支持    |
| LG G4     | 全部支持           |全部支持           |全部支持            |/           |/    |
| 华为荣耀6     | 全部支持           |全部支持           |全部支持            |/           |/    |
| 华为荣耀     | 全部支持           |全部支持           |全部支持            |/           |/    |
| 红米Note     | 全部支持           |全部支持           |全部支持            |/           |/    |
| ipone6P     | 全部支持            |全部支持           |全部支持            |全部支持   |全部支持    |
| ipone6     | 全部支持            |全部支持           |/            |/           |/    |
| ipone5     | 全部支持            |全部支持           |全部支持            |/        |/    |



## 共测试3个 demo:
Demo1: http://www.cnblogs.com/dreamback/archive/2011/10/12/2208557.html 自定义上传按钮样式  
Demo2: http://testpdjm.jd.com/html/test/image-preview.html 自定义按钮样式过滤并预览图片  
Demo3: http://www.zhangxinxu.com/study/201109/html5-file-image-ajax-upload.html 默认按钮颜色, 可以预览图片, 及上传图片到服务器的完整示例  
