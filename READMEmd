# AutoCheckin 学习通自动签到

**！！！支持普通签到，手势签到，二维码签到，拍照签到，位置签到**
学习通自动签到，针对早起不能学生，**需要自行提供参数**。

**已知cookie的有效时间为一个月，请放心使用**

**登录方式**：首次登录使用二维码登录，登录成功后，自动保存cookie，**下次无需重新登录**

## 一、参数修改：

### 1.课程参数：

```python
   course_list = [
        {
            'name':  # 你的姓名
            'url':  # 课程的任务页面/活动首页
            'course_name':  # 课程名称，用于单课程签到指令和提示输出
        }
    ]
```


### 2.位置信息

```python
    address = {
        "latitude": "-1",  # 纬度
        'longitude': "-1",  # 经度
        'addr': "",  # 位置名称
        'ifTiJiao': "0"  # 是否开启提交位置信息，'0'关闭, '1'开启
    }
```

### 3.拍照签到的图片

请在该文件的目录下存放名字为up_img.jpg的图片

如有拍照签到会自动上传该图片，**否则会自动上传wyz照片**！

## 二、执行代码方式

分所有课程检测和单课程检测：

- 单课程签到调用方法：

  ```bash
  python3 checkin.py course_name
  ```

  **curse_name为上面修改的参数中curse_list里的curse_name**

- 所有课程签到调用方法：

  ```bash
  python3 checkin.py
  ```

  检测所有课程是否有签到任务。慎用，使用次数过多可能会被学习通拉入黑名单。


##  三、让Python脚本定时启动

准备好定时启动的脚本auto.py

用root权限编辑以下文件

```bash
sudo vim /etc/crontab
```

在文件末尾添加以下命令

```
2 * * * * root /usr/bin/python3.5 ~/auto.py > ~/auto.log

```

以上代码的意思是每隔两分钟执行一次脚本并打印日志。

**三、crontab编写解释**

基本格式

```
# Example of job definition:
# .---------------- minute (0 - 59)
# |  .------------- hour (0 - 23)
# |  |  .---------- day of month (1 - 31)
# |  |  |  .------- month (1 - 12) OR jan,feb,mar,apr ...
# |  |  |  |  .---- day of week (0 - 6) (Sunday=0 or 7) OR sun,mon,tue,wed,thu,fri,sat
# |  |  |  |  |
# *  *  *  *  * user-name  command to be executed

```

**四、举例说明**

1、每分钟执行一次

```
* * * * * user command
```

2、每隔2小时执行一次

```
* */2 * * * user command (/表示频率)
```

3、每天8:30分执行一次

```
	
30 8 * * * user command
```

4、每小时的30和50分各执行一次

```
30,50 * * * * user command（,表示并列）
```

4、每个月的3号到6号的8:30执行一次

```
30 8 3-6 * * user command （-表示范围）
```

5、每个星期一的8:30执行一次

```
30 8 * * 1 user command （周的范围为0-7,0和7代表周日）
```









# ✌auto-sign-chaoxing

👴 整个自动签到，在家安稳睡觉。
## 技术栈

本项目使用 TypeScript Koa Puppeteer 实现。

## 开始

### 安装依赖

> 本项目使用 `yarn` 进行依赖管理

```bash
yarn install
```

### 开发调试

因为 nodemon + ts-node 会有各种奇怪的问题。

目前本项目采用 tsc -w + nodemon ./dist 进行调试。

分别在两个 terminal 中执行（别骂啦别骂啦 我知道这么做很憨）
```bash
tsc -w
yarn dev
```

### 使用方式

url: localhost:3000
path: '/'

Request Headers

Method: POST
Content-Type: application/json

Request Body
```json
{
	"username": "13800001234", // 账号：请使用手机号。不要使用学号！
	"password": "password" // 你的密码
}
```

## 部署上线

```bash
tsc
yarn start
```









# ChaoXingAutoSign
超星学习通-自动签到（ChaoXingAutoSign），原作者已经不更新，我修改了登录模块可以用了，但是目前手上没有课程给我签到，所以无法验证签到是否正常
# 设置环境变量/常用的变量

> settings--->secrets

## USERNAME
学习通的账号
## PASSWORD
学习通的密码
## sleepTime
获取到签到任务后，等待多少秒进行签到（防止签到过快），单位毫秒.

GitHub有一定延迟，所以可以不用设置sleepTime
## SENDKEY
sever酱微信推送的sendkey

[sever酱](https://sct.ftqq.com/)
## ADDRSS
位置签到所需的地址（不设环境变量的话，可以直接在代码中改为定值）
## ~~ENC（已废弃）~~

~~已经无需填写~~

由于enc已经不能从接口直接获得，需要自己手动填写，所以我觉得这个项目也没什么必要了

### 获取ENC
找一个兄弟，用微信扫一扫或者其他二维码扫描工具，扫描签到的二维码，会出现一串地址，你会看到有`enc=******* `,把等于号后的字符串复制进代码中即可

# 定时任务
actions启用Workflows

/.github/workflows/main.yml中的cron部分，去除schedule和cron前面的井号#

定时任务，每5分钟运行一次（UTC时间）
```
- cron: '*/5 * * * *'
```









# ⭐ ChaoxingSign | 超星学习通签到
PHP 版超星学习用自动签到，支持多用户签到，二次开发便捷！

`PHP 7.3` 测试通过，理应 `PHP 5.4` 及以上都能够使用

- 登录方式：

支持手机号码登录，暂时不支持学号登陆！！！

- 签到功能：

支持普通签到，手势签到，~~二维码签到~~，位置签到，拍照签到（无图片上传）

# 🎨 更新日志
<details open>
  <summary>2023/2/12</summary>
  
- 增加了docker-compose运行的支持，运行`run-docker.sh`即可完成一键部署
<details open>
  <summary>2022/12/23</summary>
  
- 增加Go-cqhttp推送，需要配置 config.php 文件
- 支持直接在config.php文件配置账号和密码（单用户使用）
- 默认设置了周六周日不签到
<details open>
  <summary>2022/08/29</summary>
  
- 修复无法登录的Bug
- 修复无法位置签到的Bug
- 调整了curl的实现方法，方便后期debug
</details open>
<details>
  <summary>2022/06/06</summary>
  
- 增加预签到
- 修复无法签到的Bug
</details>
<details>
  <summary>2022/04/27</summary>
  
- 新增 Bark 推送 
  > Bark API的末尾不需要添加 / 
- 修复获取课程失败导致签到失败的Bug 
- 优化签到效率 
</details>
<details>
  <summary>2021/03/21</summary>

- <a href="https://github.com/xiwangly2/ChaoxingSign/issues/6">#6</a> 升级为新版 Server 酱推送通道，原因：微信发布公告将在2021年4月底下线模板消息，故旧版推送通道将于 2021年4月 下线
    > 获取本源码后，请配置 `Config.php` 的相关配置
</details>

<details>
  <summary>2020/06/13</summary>

- 修复 <a href="https://github.com/xiwangly2/ChaoxingSign/issues/2">#2</a> 的问题，配置了 Server酱但不推送的问题
- 更改 判断时间区间的方法
- 添加 获取课程列表失败，重试2次以判断是API错误
</details>

<details>
  <summary>2020/05/27</summary>

- 修复 <a href="https://github.com/xiwangly2/ChaoxingSign/issues/1">#1</a>
- 更改 获取课程、签到 API
- 添加 手势、位置、二维码一键签到
- 添加 Server酱 微信推送，需要配置 `config.php` 文件
</details>

<details>
  <summary>2020/05/25</summary>

- 更改 登录接口，原接口已经失效
</details>

# 🎁 TODO
- [] 接入钉钉机器人 API

# 🧀 使用方法
1. 下载源码：

    直接下载：https://github.com/xiwangly2/ChaoxingSign/archive/master.zip
    
    克隆源码：`git clone https://github.com/xiwangly2/ChaoxingSign.git`

2. 🚀 运行
    1. 上传到**网站根目录**运行
    
        然后访问 `http://你的域名/main.php?account=你的超星账号&password=你的超星密码`
    
    2. 或者使用**命令行**运行
       ```
       php main.php -A "你的超星账号" -P "你的超星密码"
       ```

3. ⚙ 实现自动签到
    > 推荐大于等于 **10 分钟** 执行一次，避免出现异常
    > 
    > 我已经硬编仅能在每天的 08:00 ~ 22:00 之间运行，
    > 如果要取消或修改这一限制，请删除或注释
    > `main.php` 第 7~9 行
    1. 如果以**网页方式**运行，定时监控 `http://你的域名/main.php?account=你的超星账号&password=你的超星密码` 即可
    2. 如果使用**命令行方式**运行，添加 `crontab` 任务即可，具体添加 `crontab 任务` 方法可以网上搜。
    每天 早上8点到晚上22点之间，每10分钟签到一次 crontab 表达式：`0 */10 8-22 * * * *`

# √ 运行输出
签到成功：
```
正在签到：陈半仙@测试班级
[2020-06-13 11:44:14]签到成功

Server酱 消息推送成功
```

没有签到任务：
```
没有待签到的任务
```

# ❗ 注意
超星**可能**屏蔽了如 阿里云、腾讯云、百度云... 等 IDC IP 地址，故有可能出现未知的错误（我没测试，我仅在家庭宽带中测试成功）


> 本项目中使用到的 `Selector.php` 来自 [PHPSpider](https://github.com/owner888/phpspider) 











## 超星学习通自动签到  
<!-- 填上账号密码运行运行就好了,别忘记装模块   -->
支持学习通的所有签到  
支持server酱推送  
能自定义照片,地址以及名字  
用screen后台挂住就好了,断网的话可能会boom(一般不会断网⑧..)  
## 配置文件
1. "username":手机号 
2. "passwd":密码
3. "SCKEY":server酱的key
4. "name":老师那里显示的名字,无特殊需要默认就行
5. "address":地址信息
6. "latitude":经度,同上
7. "longitude":纬度,同上
8. "picname":同目录的图片名字
## 本地使用教程
1. python3环境
2. 安装模块: pip install requests
3. 在同目录下的conf.json中写入配置
4. 双击运行...
## 云函数使用教程
1. 去腾讯云创建一个云函数,目前测试广州好像不能用.其他地区可以.
2. 环境选择`Python 3.6`
3. 内存最低实测`64M`可以跑.
4. 时间看个人课程数量.详细解释看下面
5. 测试运行,成功后设定定时触发.关于如何设定Cron也可以看下面

#### 关于时间设定
<script type="text/javascript" src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=default"></script>

在`Serverless`版里面,所有课程扫描/签到一次就会停止,这样做是为了符合云函数的设计,同时也节省运行时间.  
最简单的估算办法就是:
* 签到或扫描的请求撑死不会超过2S,记为`x`
* 中间等待时间由`account.json`决定,记为`y`
* 课程数量,记为`z`
那么最后总时间应该是:   
$$z*(x+y)$$

绝大多数情况下这个请求时间可以直接忽略.

再懒人一点的话,可以直接在命令行运行并统计时间,参考Linux命令`time` 

#### 关于Cron设定
我们先来看一个例子

```
0 */10 8-12,14-18 * * 1-5
```

云函数的Cron跟Linux Cron非常相似,不过左边多了一个秒.  
以上Cron可以解释为: 

```
0 */10 8-12,14-18 * * 1-5
| |    |          | |  |
| |    |          | |  .------- 在周几     (周一到周五)
| |    |          | .---------- 在哪个月   (所有)  
| |    |          .------------ 在哪一天   (所有)
| |    .----------------------- 在几点     (8-12和14-18) 
| .---------------------------- 在第几分钟 (每隔10分钟)
.------------------------------ 在第几秒   (第0秒)
```
这是比较符合现在上课的情况的Cron,各位也可以根据这个列表进行自定义









<h1 align="center">超星学习通签到 - Universal Platform</h1>

**新版本正在施工中，预计支持 Linux、Windows、macOS、iPad、iPhone、Android、HarmonyOS 客户端全平台**

**支持 Docker 服务器部署，可选 termux、magisk module 运行**

**新版本技术栈：PC 和 Web 使用 Electron + Next.js + Node.js，移动端 Capacitor**

**支持多账号切换**

---

**实现的签到类型：** 普通签到（没必要用这个程序）、拍照签到（任选照片）、手势签到（不需要知道手势）、位置签到（任选位置）、二维码签到（无视十秒）、签到码签到（不需要知道签到码）

**注意：** 只能手动签到。自动签到后续看情况添加



## 截图

<img src="https://github.com/eric-gitta-moore/chaoxing-sign-app/raw/main/readme_static/1.gif" width="48%"/><img src="http://tva1.sinaimg.cn/mw690/008d89Swgy1h2qwwyva0vj30u01uo0xn.jpg" width="48%"/>

<img src="http://tva1.sinaimg.cn/mw690/008d89Swgy1h2qwwytag4j30u01uodna.jpg" width="48%"/><img src="http://tva1.sinaimg.cn/mw690/008d89Swgy1h2qwwzy6xvj30u01uoh2r.jpg" width="48%"/>

<img src="http://tva1.sinaimg.cn/mw690/008d89Swgy1h2qx2zkr9bj30u01uon00.jpg" width="48%"/>

## 使用

### 下载

+ [最新版下载地址](https://github.com/james-curtis/chaoxing-sign-app/releases)

### 登录

- 请使用 **手机号+密码登录** (和[i.chaoxing.com](http://i.chaoxing.com)的账号密码一致)

### 课程

- 列举了所有根目录下的课程（如果课程太多的话可能卡顿，建议新建文件夹，把已结束的课程放在文件夹里面）
- 点击课程图标可以跳转到活动页面的对应课程中

### 活动

1. 课程tab页
   - 这里排序方式是超星那边默认的排序，也就是 活动未结束优先，再按开始时间降序
2. **签到方式**
   + 点击签到图标所在的那一行都可以触发操作
3. 签到类型
   + **普通签到&手势签到&签到码签到：** 直接签到
   + **二维码签到：** 直接扫码、选择二维码文件、输入二维码内容、输入enc参数，任选一种
   + **位置签到：** 直接在弹出的地图中选择签到地点即可
   + **拍照签到：** 选择手机中的图片上传即可。也可以选择普通签到，此时不会上传图片，但是可以签到成功（教师端会有显示没有图片）

### 我的

+ 这里显示的信息是根据超星那边返回的html页面正则匹配出来的
+ 比较奇怪的是那边的html好像做了点手脚，有时候正则能匹配上有时候不行



## 画饼

- [ ] 自动签到

- [ ] 获取群聊签到，需要逆向app，用的是环信SDK

- [x] 对接阿里mPaaS扫码

## 开发

1. #### NPM包

   - crypto-js安装`npm i crypto-js` 

2. #### uni-app应用标识(AppID)需要重新获取一下

3. #### 地图使用的是高德地图，需要配置自己的appkey，配置教程[地图插件配置 - DCloud问答](https://ask.dcloud.net.cn/article/29)



## 逆向

1. [模拟超星网课 Android 客户端 · HonKit (hiczp.com)](https://www.hiczp.com/wang-luo/mo-ni-chao-xing-wang-ke-android-ke-hu-duan.html)



## 声明
- 本项目基于 **GPL-3.0** ，完全开源，免费，仅供技术学习和交流，开发者团队并未授权任何组织、机构以及个人将其用于商业或者盈利性质的活动。也从未使用本项目进行任何盈利性活动。未来也不会将其用于开展营利性业务。
- 个人或者组织，机构如果使用本项目产生的各类纠纷，法律问题，均由其本人承担。
- 如果您开始使用本项目，即视为同意项目免责声明中的一切条款，条款更新不再另行通知。
- 如有触及相关平台规定或者权益，烦请联系我们删除。


## Star History

<a href="https://star-history.com/#eric-gitta-moore/chaoxing-sign-app&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=eric-gitta-moore/chaoxing-sign-app&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=eric-gitta-moore/chaoxing-sign-app&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=eric-gitta-moore/chaoxing-sign-app&type=Date" />
 </picture>
</a>









<h1 align="center">🌿超星学习通签到🌿</h1>

![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Licence](https://img.shields.io/github/license/cxOrz/chaoxing-signin?style=for-the-badge)

基于 Nodejs 实现的一个命令行签到工具，在此基础上使用 React.js + Material UI + Koa 扩展成为 Web 项目。

**功能**： 普通签到、拍照签到、手势签到、位置签到、签到码签到、二维码签到，多用户凭据储存，IM 协议自动签到。

## 环境 💻

可在任意运行 [NodeJS](https://nodejs.org/en/) > v18.14 的平台签到，Windows、MacOS、Linux ... 

安卓手机上可以用 Termux 来运行NodeJS程序，[查看Termux教程](./apps/server/src/docs/termux.md) 。

苹果手机请查看 [高级](#高级-) 部分，通过这种方式来使用，当然这种方式也适用于其他。

## 部署 🛠

将仓库克隆到本地

```bash
git clone https://github.com/cxOrz/chaoxing-signin.git
```

进入项目文件夹，并安装依赖

```bash
cd chaoxing-signin
pnpm install
```

## 运行 ⚙

### 命令解释

根目录下：
- `pnpm dev`：运行Web开发服务器、后端接口；
- `pnpm build`：构建前端页面、转译后端代码；
- `pnpm start`：运行手动签到；
- `pnpm serve`：启动后端接口；
- `pnpm monitor`：启动监听模式，检测到签到将自动签上，无需人工干预；

apps/server 目录下：
- `pnpm build`：转译代码；
- `pnpm start`：运行手动签到功能，若有签到则手动完成，若无则退出程序；
- `pnpm serve`：启动接口；
- `pnpm monitor`：启动监听模式，检测到签到将自动签上，无需人工干预；

apps/web 目录下：
- `pnpm dev`：运行 Web 开发服务器；
- `pnpm build`：构建静态页面；

### 基本使用方式

进入 `apps/server` 目录下，执行以下步骤：

构建代码
```bash
pnpm build
```
构建完成，后续的运行直至下次变更代码，不需要再构建，可以直接运行
```bash
pnpm start
```

## 使用须知 📄

为了节约资源，只对2小时以内的活动签到。若同时有多个有效签到活动，只签最新发布的。将结束的课程移入其他文件夹，减少根目录的课程能够提高活动检测速度。

### 二维码签到

在运行之前需要做些准备，请找一位挚友，拍一张二维码的照片，识别二维码，得到一个字符串，复制其中的 `enc` 参数值，例如 `1D0A628CK317F44CCC378M5KD92`，询问时填入。若使用 UI 仓库的项目(查看`高级`)，可以直接选择图片并自动解析得到enc参数。如果遇到10s变换的二维码，参考 [#178](https://github.com/cxOrz/chaoxing-signin/issues/178)

### 位置签到

根据运行时的提示输入**经纬度**和**详细地址**，经纬度在这里获取 [百度拾取坐标系统](https://api.map.baidu.com/lbsapi/getpoint/index.html)，点击某位置，经纬度将出现在网页右上方，复制该值，询问时填入。详细地址样例：河南省郑州市中原区华中师范大学附属郑州万科城小学，该地址将显示在教师端。

### 拍照签到

需要事先准备一张用来提交的照片。浏览器访问超星云盘：https://pan-yz.chaoxing.com ，在根目录上传一张你准备的照片，命名为 `0.jpg` 或 `0.png` 。若使用 UI 仓库的项目(查看`高级`)，不需要上传云盘，可以直接选择图片提交签到。

### 普通签到&手势签到&签到码签到

没有需要准备的，直接运行即可。

### 监听模式

支持开启QQ机器人、邮件推送、pushplus推送；

**QQ 机器人**：根据 [go-cqhttp](https://docs.go-cqhttp.org/guide/quick_start.html) 文档，配置正向 WebSocket、QQ号、密码，并运行 go-cqhttp 程序，即可运行监听模式并启用该选项。

如需发送二维码让机器人识别并签到，请配置 `env.json` 的 `SecretId` 和 `SecretKey`，将使用腾讯云OCR进行识别和处理。

监听模式每次需要时启用 2 - 4 小时较为合适，最好不要挂着不关。

## 高级 🎲

除了简单的 `pnpm start` 来手动签到，也可以部署到服务器使用网页版本，别忘了这也是个 Web 项目。

- 前端界面，查看 [前端](/apps/web) 的详细说明。
- 后端服务，查看 [服务端](/apps/server) 的详细说明。

### 一键运行

方案一：根目录下执行 `pnpm dev` 将运行前后端服务，并在浏览器弹出项目首页，注意这是开发模式！

方案二：用提供的 Docker 镜像，运行后可通过 IP 访问。

```bash
docker pull ghcr.io/cxorz/chaoxing-signin:latest
docker run -d -p 80:80 -p 5000:5000 ghcr.io/cxorz/chaoxing-signin
```

> 出现问题？先仔细阅读相关说明，若仍无法解决请发 issue

### 展示

![](https://service-m9r7liw5-1252446325.bj.apigw.tencentcs.com/release/ui-start.png)
![](https://service-m9r7liw5-1252446325.bj.apigw.tencentcs.com/release/ui-config.webp)

## 贡献须知

> 由于作者精力有限，自 2023.6.10 起，本项目不再维护，欢迎热心同学们贡献代码。

发起 pr 之前务必先发起issue进行讨论，之后新建一个分支(以提供的功能命名），并在此分支完成你的代码即可提交 pr。

必要条件：
- 运行 `turbo run lint` 无错误出现，可以有警告
- 测试所有功能全部正常

## 免责声明

本项目仅作为交流学习使用，通过本项目加深网络通信、接口编写、交互设计等方面知识的理解，请勿用作商业用途，任何人或组织使用项目中代码进行的任何违法行为与本人无关。










# Superstar Checkin

超星学习通自动签到工具

[![GitHub package.json dependency version (prod)](https://img.shields.io/github/package-json/dependency-version/Clansty/Superstar-checkin/oicq/main)](https://github.com/takayama-lily/oicq)
[![discord](https://img.shields.io/static/v1?label=chat&message=discord&color=7289da&logo=discord)](https://discord.gg/WV8W25eH)

特色：

- 通过 IM 协议实时获取签到信息，而不是每隔一定时间请求服务器

- 包含 QQ 机器人，实时向指定的群通知程序状态

- 支持使用任何一张二维码进行二维码签到，即使二维码已经过期（直接在指定群内发送二维码即可）

## 功能（已实现部分）

- [x] 自动取 Cookie，过期自动更新

- [x] 支持通过学习通 IM 协议实时获取签到推送

- [x] 在群内发送提醒并自动签到

- [x] 通过 QQ 机器人接收群内发送的二维码实现二维码签到

  本功能只需要一张已过期的二维码就可以

- [x] 支持多用户共同签到

- [x] 根据课程设置签到经纬度以及位置名称

  请使用[此网页](https://api.map.baidu.com/lbsapi/getpoint/index.html)拾取坐标

- [x] 支持通过周次设定签到的地址，适用于实验课和正课在不同地点的情况

- [x] 手动签到

  机器人命令：`签到 {aid} [enc(二维码签到时)|courseId(位置签到时。不需要提交位置可以不填)]`

- [x] Docker 和 Docker Compose 部署

- [ ] 通过 REST API 设置课程信息

## 部署方法

### 使用 Docker Compose 部署

1. 下载 [docker-compose.yaml](https://github.com/Clansty/superstar-checkin/raw/main/docker-compose.yaml) 和 [config.example.yaml](https://github.com/Clansty/superstar-checkin/raw/main/config.example.yaml)，将它们放在一个文件夹中
2. 将 `config.example.yaml` 重命名为 `config.yaml`
3. 修改 `config.yaml` 中的配置项
4. `docker compose up`

### 使用 NixOS 部署

1. 在你的系统 Flake 中，引入本项目

    ```nix
    inputs.superstar-checkin.url = "github:clansty/superstar-checkin";
    ```

2. 在系统配置的某个 Module 中填写配置项（[查看示例](./config.example.nix)）
3. `nixos-rebuild switch`

可以使用 `systemctl status superstar-checkin` 来查看状态

### 手动部署

1. 安装 NodeJS 14 以上版本
2. `yarn install`
3. `cp config.example.yaml config.yaml` 并在 `config.yaml` 中填写配置项。配置文件中自带说明，请参考
4. `yarn build`
5. `yarn start`

提示：机器人使用的账号必须已经在 [oicq](https://github.com/takayama-lily/oicq) 框架上登录过

## 限制

（据说）学习通禁止腾讯云阿里云这种 IP 签到，所以需要部署在家庭宽带下









# XueXiTong

学习通小程序

## 功能

1. 支持签到方式支持：普通，图片，手势，定位
2. 支持查询作业、考试的信息（暂不支持云函数）
   - 作业：课程 作业 剩余时间
   - 考试：考试 剩余时间
3. 支持发送签到结果：
   - 邮件
   - sever酱
   - 钉钉机器人（自定义机器人）
4. 支持部署到云函数（兼容所有云函数）

## 安装

- conf.py 配置文件
- index.py 主程序
- auto_send.py 发送消息
- auto_sign.py 自动签到
- auto_note.py 查询作业等

### 配置文件

加:warning:的是必填内容的

- account: 手机号:warning:
- password: 密码:warning:
- long: 经度
- lat: 纬度
- address: 地址
- name: 打卡显示姓名:warning:
- img: 图片链接，用于图片打卡
- email: 接受邮件的邮箱地址
- mail_host: 邮箱服务器地址
- mail_user: 邮箱用户名（账号）
- mail_password: 邮箱密码（授权码）
- SCKEY: Server酱密钥
- dingding_hook: 钉钉机器人的hoke

账号和密码不确定可以先在[学习通官网](https://passport2.chaoxing.com/login?fid=&newversion=true&refer=https%3A%2F%2Fi.chaoxing.com)尝试以下，再输入

### 配置参考文档

- [网易邮箱获取授权码](https://help.mail.163.com/faqDetail.do?code=d7a5dc8471cd0c0e8b4b8f4f8e49998b374173cfe9171305fa1ce630d7f67ac21b8ba4d48ed49ebc)
- [server酱](https://sct.ftqq.com/)
- [钉钉机器人](https://open.dingtalk.com/document/robots/custom-robot-access)

## 云函数

- [腾讯云函数](https://github.com/morning-start/XueXiTong/wiki/%E8%85%BE%E8%AE%AF%E4%BA%91%E5%87%BD%E6%95%B0)
- [华为云函数](https://github.com/morning-start/XueXiTong/wiki/%E5%8D%8E%E4%B8%BA%E4%BA%91%E5%87%BD%E6%95%B0)

## 版权说明

该项目签署了 GPL 授权许可，详情请参阅 LICENSE.md










<h1 align="center">签到小工具</h1>

<p align="center">手动签到；自动签到；签到队列</p>

![](./docs/pictures/config.png)
![](./docs/pictures/task.png)


## 声明
- 本项目基于GPL-3.0，完全开源，免费，仅供技术学习和交流，开发者团队并未授权任何组织、机构以及个人将其用于商业或者盈利性质的活动。也从未使用本项目进行任何盈利性活动。未来也不会将其用于开展营利性业务。
- 个人或者组织，机构如果使用本项目产生的各类纠纷，法律问题，均由其本人承担。
- 如果您开始使用本项目，即视为同意项目免责声明中的一切条款，条款更新不再另行通知。
- 如有触及相关平台规定或者权益，烦请联系我们删除。


## 使用
### 登录
- 可以账号密码登录，也可以直接提供cookie
- 如果账号密码登录，登录成功之后，会自动同步cookie，不需要再操作
- 如果直接提供cookie，需要先验证cookie有效性，验证成功后，点击替换cookie即可
- 长期使用之后，可能会在某次登录后提示cookie失效，重复上述两步即可
  - 尚未实现过期后自动使用账号密码重新获取cookie

### 活动
- 获取课程之后，可以添加至队列，也可以手动进行签到

### 签到任务设置
- 一门课程建议只配置一个任务，但是可以为该任务配置多个上课时间
- 选择合适的上课周期(最好和实际学期一致，或者和该门课的周期一致)和上课时间(比如可以比实际上课时间提前半小时)，小工具会根据任务的周期和时间，自动优化整合时间范围，保证监控的效率和精确
- 建议选择较大的监控频率(至少60s)，不然会被屏蔽，而获取不到活动信息

### 签到队列
- 添加、编辑、修改队列之后，是即时生效的，不需要重启

### 日志
- 可以筛选日志等级
- 可以控制是否自动下滑













# xxtSign

> 版本号V2.2.0 更新日期2022.3.12
## 支持的签到类型
支持以下类型的自动签到 
- 普通签到
- 拍照签到
- 位置签到
- 手势签到
- 签到码签到

###### 二维码签到需要到微信小程序「炒饭云签」中进行手动签到
###### (无视二维码10秒刷新)

## 优点
除了二维码签到外均支持自动签到

允许用户自行设定各种参数,如签到名称|签到地点显示|签到经纬度|签到图片等

#### ==提供了多彩的控制台界面,让用户及时了解当前程序运行情况==
![多彩的控制台](http://qiniu.dancedj.cn/iShot2022-03-12%2021.33.35.png)

### ==支持多个账号同时运行监控任务==
![多个账号](http://qiniu.dancedj.cn/1647091800208.jpg)

分离配置文件与源代码,代码小白无需关心代码实现,只需要按要求修改配置文件即可运行

多种通知方式,让用户及时知道任务状态

![多种通知方式](http://qiniu.dancedj.cn/iShot2022-03-12%2021.37.10.png)

### ==**无经验小白可直接使用打包版本,无需安装python环境即可运行**==

## 使用方式
#### 源码运行
安装python环境

安装包
```python
pip install requests
pip install rich
```
修改配置文件

```
[全局配置]
#循环休眠时间,也就是多久运行一次
sleep:10
#每门课程只检测前N个活动 避免因课程活动太多而卡住
count:3
#同时运行的用户数量,增加用户数量需在下方复制一个[用户N]
usercount:1
[通知]
#Server酱通知Key,不填则为不使用
serverKey:
#Bark通知Key,不填则为不使用
barkKey:
[用户1]
#用户名/手机号
account: 
#用户密码
password: 
#签到姓名,必填
name: 炒饭
#图片签到图片ID,可自行抓包获取,或者在小程序[炒饭云签]中的个人设置进行获取
oid:
#位置签到显示地址
address:
#位置签到纬度,可在小程序[炒饭云签]中的个人设置进行地图选点获取(精确不会漂移)
lat:
#位置签到经度,可在小程序[炒饭云签]中的个人设置进行地图选点获取(精确不会漂移)
long:
```

运行即可
![运行即可](http://qiniu.dancedj.cn/iShot2022-03-12%2021.41.53.png)

#### 小白运行
修改配置文件

双击exe文件即可运行

## 配置文件说明
各个参数意义均在上文说明,这里要特别指出多用户情况
增加一个用户,就需要在配置文件中增加将这部分,其中的N即为当前用户编号(从1开始,1,2,3,4)

```
[用户N]
account: 
password: 
name: 
oid:
address:
lat:
long:
```
并且需要修改全局配置中的usercount参数为当前用户数量

```
[全局配置]
usercount:2
```












## 其他项目推荐

| 项目地址                                                | 开发语言   | 备注                                           |
| ------------------------------------------------------- | ---------- | ---------------------------------------------- |
| https://github.com/cxOrz/chaoxing-signin                | TypeScript | 基于 Nodejs 实现的一个签到命令行工具           |
| https://github.com/PrintNow/ChaoxingSign                | PHP        | 超星学习通课堂签到&健康打卡&多用户多任务&API   |
| https://github.com/Clansty/superstar-checkin            | TypeScript | 超星学习通自动签到工具，可以配合QQ机器人       |
| https://github.com/Wzb3422/auto-sign-chaoxing           | TypeScript | 超星学习通自动签到，梦中刷网课                 |
| https://github.com/Huangyan0804/AutoCheckin             | Python     | 学习通自动签到，支持手势，二维码，位置，拍照等 |
| https://github.com/LnYo-Cly/ChaoXingAutoSign            | python     | 学习通（超星）自动签到                         |
| https://github.com/yuban10703/chaoxingsign              | Python     | 超星学习通自动签到                             |
| https://github.com/SSmJaE/XueXiTonsSign_Electron        | TypeScript | 基于Electron，桌面端，GUI，签到队列            |
| https://github.com/w964522982/xxtSign                   | Python     | 学习通自动签到,普通\|拍照\|位置\|手势\|签到码  |
| https://github.com/eric-gitta-moore/chaoxing-sign-app   | TypeScript | 超星学习通全平台，多账号批量签到               |
| https://github.com/morning-start/XueXiTong              |	python	   | 学习通自动签到，支持普通，图片等 	    		|
| ------------------------------------------------------- | ---------- | ---------------------------------------------- |
