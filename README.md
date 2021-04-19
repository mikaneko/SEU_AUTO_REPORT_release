# SEU_AUTO_REPORT_release
## Southeast University Auto Health Report

### 东南大学健康打卡

使用selenium webdriver尽可能还原真人的打卡操作（request也太危险了吧）

`atarashichiaki@hotmail.com`



> 开发开源地址：  socket版shell端打卡服务器地址:
>
> `https://github.com/mikaneko/SEU_AUTO_REPORT_cloud-verison`



- 重要：需要安装chrome浏览器，内置的chromedriver版本为89，如果你的chrome浏览器版本过高，可以在如下地址下载相应版本的chromedriver，覆盖`tool/chromedriver.exe`，或者修改`config/general.cfg`中的webdriver目录

  `http://npm.taobao.org/mirrors/chromedriver/`

  `http://chromedriver.storage.googleapis.com/`

- 声明：find elements 部分采自 StephenHoo



- a开头的版本均为短期测试版，需要authencode。
- 开源代码，仅供学习与交流，不盈利，不承担任何法律和道德风险。
- 用户知悉协议，应在配置文件`userconfig/eula.cfg`中阅读相关协议，并选择确认。


### 使用方法详解

*（供a202104版本）*

1. 将zip格式`seu_report_group_xxxxxxx.zip`压缩文件解压

2. 运行`seu_report_group_xxxxxxx.exe`程序，此时会生成配置文件。

3. 下面开始讲解所有配置文件，配置文件的目的是提高普适性。

4. 记事本打开`userconfig/authen.cfg`，更改NULL，填入authencode（authencode.txt在本项目的主页）

5. 记事本打开`userconfig/eula.cfg`，阅读条约，填入confirm

6. 记事本打开`config/general.cfg`，

   report_url 可填`https://newids.seu.edu.cn/authserver/login?service=http://ehall.seu.edu.cn/qljfwapp2/sys/lwReportEpidemicSeu/*default/index.do`

   webdriver_addr 可填 `./tool/chromedriver.exe`

7. 记事本打开`userconfig/email_settings.cfg`，根据注释填入信息，启用或禁用，仅支持SSL。

8. 运行`seu_report_group_manager_xxxxxxx.exe`，根据提示添加和删除用户信息

9. 此时脚本已经配置完毕！

10. 脚本可以单次运行，也可以挂着24小时不间断运作，不用脚本时候，记得把encdata目录删除干净

11. 有未知问题，<u>先在log目录下查看错误内容，根据提示解决</u>，或提交问题至`atarashichiaki@hotmail.com`

### 版本更新内容
#### a202104_r
1. 优化所有功能，模块化所有功能。

2. 启动自检，第一次启动全部创建所有配置文件，增加错误后的短暂停留提示

3. 增加<u>每位用户创建打卡日志</u>，便于统计*（将来会添加周报和月报功能，通过邮件发送）*

4. 增加<u>email邮件通知打卡</u>功能*（实验性功能，可在`userconfig/email_settings.cfg`中进行设置，仅支持SSL）*

#### a202103
1. 重写代码，优化速度

2. log模块，debug模块，配置文件模块建立

### 当前版本不足
1. 效率和多线程
2. 异常处理
3. 用户数据加密（防君子，不防小人）

### 测试人员
1. BUGATTI
2. CHIAKI