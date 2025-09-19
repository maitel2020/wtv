

# 原因
1. 定位自家使用
2. 曾开通电信IPTV，想看的台却没有
3. 稳定的IPTV直播源太难有了，一失效或者播放卡顿，就老是兴师问罪
4. CCTV_Viewer挺好的，但是不符合操作习惯，而且节目源无法自制


# 节目单测试地址
[https://raw.githubusercontent.com/maitel2020/wtv/refs/heads/main/channels.json](https://raw.githubusercontent.com/maitel2020/wtv/refs/heads/main/channels.json)
# 台标测试地址
[https://github.com/maitel2020/wtv/raw/refs/heads/main/logo.zip](https://github.com/maitel2020/wtv/raw/refs/heads/main/logo.zip)


# 界面
![主界面](image/1.webp)
![节目列表](image/2.webp)
![设置列表](image/3.webp)

# 功能说明
1. 单按确认键则弹出节目列表，长按确认键或者菜单键则弹出设置列表，上下翻台，数字选台
2. 列表配置
	* 列表订阅：本项目不提供节目来源，格式参考channels.json
	* EPG订阅：内置EPG订阅源，不想另行设置则点击确定即可
	* 台标订阅：本项目不提供台标来源，压缩包名称必须为logo.zip
3. 其他设置
	* 启动页图片：内置每日必应壁纸订阅源，不想另行设置则点击确定即可
4. X5设置
	- 官方路线：
		* 优点：从腾讯服务器下载内核，下载速度有保障
		* 缺点：有时会获取失败，以及部分机型无法下载
	- 其他路线：
		* 优点：所有机型均可下载，根据系统自动下载对应的32位/64位内核
		* 缺点：下载路线需要开发者维护，速度也无法保障，即便安装成功，但有些机型会存在内核没有开启的问题，需要在“官方路线”中手动开启，即“内核已被禁用”改成“内核未被禁用”
# 其他说明
1. 只支持5.0及以上
2. 支持arm64-v8a、x86、armeabi-v7a、x86_64
3. 系统内核播放过程中存在突然卡住不动的问题，X5内核暂时没发现此问题
4. 直播视频一定要来自源网站，使用iframe类似嵌套的直播网站，则无法全屏
5. 暂不开源，不收集任何隐私



## 目前问题
1. 使用uniapp x开发，弹出列表、切换列表会出现卡顿问题，配置越低越明显
2. 节目列表出现闪烁问题，使用canvas渲染，因为并非一次性渲染全部内容，而是切换一次就重新渲染一次


## 测试机型
荣耀V10、DBB3 PRO、TCL电视、夜神模拟器

## 参考
1. CCTV_Viewer
2. mytv-android
3. 酷9
