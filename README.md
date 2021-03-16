# SEU_AUTO_REPORT_release
## Southeast University Auto Health Report

### 东南大学健康打卡

使用selenium webdriver尽可能还原真人的打卡操作
`atarashiciaki@hotmail.com`

开发开源地址：

`https://github.com/mikaneko/SEU_AUTO_REPORT_cloud-verison`

### 使用方法详解
1. 将zip格式压缩文件解压

2. 运行seu_report_group_xxxxxxx.exe程序

3. 记事本打开userconfig/authen.cfg，更改NULL，填入authencode（authencode在本项目的主页）

4. 再次运行seu_report_group_xxxxxxx.exe程序

5. 记事本打开userconfig/eula.cfg，阅读条约，填入confirm

6. 再次运行seu_report_group_xxxxxxx.exe程序

7. 记事本打开config/general.cfg，report_url 可填`https://newids.seu.edu.cn/authserver/login?service=http://ehall.seu.edu.cn/qljfwapp2/sys/lwReportEpidemicSeu/*default/index.do`webdriver_addr 可填 `./tool/chromedriver.exe`

8. 再次运行seu_report_group_xxxxxxx.exe程序，并关闭

9. 运行seu_report_group_manager_xxxxxxx.exe，根据提示添加和删除用户信息

10. 此时脚本已经配置完毕！

11. 脚本可以单次运行，也可以挂着24小时不间断运作

12. 不用脚本时候，记得把encdata目录删除干净

13. 有未知问题，先在log目录下查看错误内容，提交bug，或提交至`atarashiciaki@hotmail.com`

### 当前版本不足
1. 用户数据加密

### 测试人员
1. BUGATTI

### 版本更新内容
#### a202103
1. 模块化所有功能，重写代码
2. 使用authencode，以便更快的进行版本迭代
3. log模块化初步
4. eula功能
5. log使用