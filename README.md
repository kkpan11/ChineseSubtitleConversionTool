# 繁体简体字幕转换工具

## 简介
此工具可将字幕文件中的简体中文与繁体中文进行相互转换，并且可以指定目录进行批量转换。

## 下载
- 开发版本：[ChineseSubtitleConversionTool.exe](https://github.com/xiaoxinpro/ChineseSubtitleConversionTool/raw/master/ChineseSubtitleConversionTool/bin/Debug/ChineseSubtitleConversionTool.exe)

- 稳定版本：[繁体简体字幕转换工具 Releases](https://github.com/xiaoxinpro/ChineseSubtitleConversionTool/releases)

- 其他版本：[繁体简体字幕转换工具 for 吾爱破解【小歆】](https://github.com/xiaoxinpro/ChineseSubtitleConversionTool/releases/download/V0.3.0.42/ChineseSubtitleConversionTool.52pojie.zip)

## 使用说明

![界面](https://github.com/xiaoxinpro/ChineseSubtitleConversionTool/blob/master/Image.png)

### 普通转换
可以直接将字幕文件拖拽到软件中，自动读取字幕文件内容，点击“转为简体”或“转为繁体”完成转换，点击“保存”按钮可以输出保存。

### 批量转换
可以直接将含有字幕的文件夹拖拽到软件中，选择转换的格式，填写输出的文件名样式，点击“开始转换”即可完成转换。

批量转换使用多线程技术，转换过程UI不卡顿，其他功能可正常同步使用，方便并快捷。

> 需要注意当目标“文件名”与源文件或已存在文件同名时会覆盖掉已有文件，请注意备份源字幕文件。

批量转换将自动获取该目录下的全部字幕文件（包括ASS、SSA、SRT、LRC、TXT），其他格式文件不会读取。

#### 输入编码说明
此功能针对`BIG5`或`GBK`等编码的文件输出乱码的问题，通过修改对应的输入文件编码，解决乱码的问题。

默认建议使用`UTF-8`，适用大多数的输入文件。

#### 输出编码说明
无特殊要求不要修改此选项，选择错误将导致输出文件乱码。

默认建议使用`UTF-8`，适用大多数视频播放器。

#### 文件名样式说明
批量转换使用的是文件名样式替换掉替换符，替换符使用`{}`包裹，已有替换符如下：

- `{name}` 源文件名称（不包含路径与扩展名）

- `{exten}` 源文件扩展名，必须存在的替换符

- `{num}` 文件序号，将列表中的序号使用在文件名中

文件名样式中除替换符以外的字符将原样输出，需要注意所有字符必须符合文件名规范，且不能存在重复的文件名，否则将出现保存异常。

> 如果要使用源文件名替换掉旧的字幕文件可输入：`{name}{exten}`

如果文件名样式格式存在问题，文件名样式文本框背景为红色，且不可进行转换。

### 转换选项
此配置全局有效，针对普通转换与批量转换输出结果；启用不同转换选项输出的效果略有不同，可根据需要进行选择。

#### 快速转换
采用常用模板算法，快速输出转换结果，无语义转换功能，适合大量简单的语句转换。

#### 优化古文字转换
在快速转换的基础上优化古文字显示，主要应用场景是在含有古文字字符的文本中，转换速度仅次于快速转换。

默认勾选该选项，该模式下与快速转换效率相差无几，有效避免快速转换结果出现`??`的BUG。

当不勾选该选项时，文本中包含的古文字有可能会被转换成`??`。

#### 高精度转换
采用Office组件实现的繁简转换功能，可根据语义输出转换结果，转换速度较慢，适合需要明确语义的使用场景。

使用此选项必须已安装Office组件，否则此选项不可用。

## 捐赠
如果您觉得此工具对你有帮助，欢迎给予我们一定的捐助来维持项目的长期发展。

### 支付宝扫码捐赠

![支付宝扫码捐赠](https://github.com/xiaoxinpro/xxjzWeb/blob/master/Public/Home/i/alipay.png)

### 微信扫描捐赠

![微信扫描捐赠](https://github.com/xiaoxinpro/xxjzWeb/blob/master/Public/Home/i/wechat.png)