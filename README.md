# SEU_AUTO_REPORT_release
## Southeast University Auto Health Report

### 东南大学健康打卡

使用selenium webdriver尽可能还原真人的打卡操作

`atarashichiaki@hotmail.com`



> 开发开源地址：  socket版shell端打卡服务器地址:
>
> `https://github.com/mikaneko/SEU_AUTO_REPORT_cloud-verison`



- 重要：需要安装chrome浏览器


- a开头的版本均为短期测试版，需要authencode。


### 使用方法详解

*（供a202104版本）*

1. 将zip格式压缩文件解压

2. 运行`seu_report_group_xxxxxxx.exe`程序

3. 记事本打开`userconfig/authen.cfg`，更改NULL，填入authencode（authencode在本项目的主页）

   记事本打开`userconfig/eula.cfg`，阅读条约，填入confirm

   记事本打开`config/general.cfg`，report_url 可填`https://newids.seu.edu.cn/authserver/login?service=http://ehall.seu.edu.cn/qljfwapp2/sys/lwReportEpidemicSeu/*default/index.do`，webdriver_addr 可填 `./tool/chromedriver.exe`

9. 运行`seu_report_group_manager_xxxxxxx.exe`，根据提示添加和删除用户信息

10. 此时脚本已经配置完毕！

11. 脚本可以单次运行，也可以挂着24小时不间断运作，不用脚本时候，记得把encdata目录删除干净（简单加密，不防破密）

9. 有未知问题，<u>先在log目录下查看错误内容，根据提示解决</u>，或提交问题至`atarashichiaki@hotmail.com`

### 版本更新内容

   #### a202104

  1. 启动自检，第一次启动全部创建所有配置文件，增加错误后的短暂停留提示
  2. 增加<u>每位用户创建打卡日志</u>，便于统计
  3. 增加<u>用户数据加密</u>（防君子，不防小人）
  4. 增加<u>email邮件通知打卡</u>功能（实验性功能，可在`userconfig/email_settings.cfg`中进行设置）

   #### a202103

   1. 模块化所有功能，<u>重写代码</u>
   2. 使用authencode，以便更快的进行版本迭代
   3. log模块化初步，eula功能，log使用

### 当前版本不足
1. 效率和多线程
2. 异常处理

### 测试人员
1. BUGATTI
2. CHIAKI