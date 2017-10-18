
# 1 简介
## 1.1 文档目的
　　编写此文档的目的是进一步定制软件开发的功能列表，希望能使本软件开发工作更具体。为了使用户、软件开发者及分析和测试人员对该软件的初始规定有一个共同的理解，它说明了本软件的各项功能需求，明确标识各项功能的具体含义，阐述实用背景及范围，提供客户解决问题或达到目标所需要的条件或权能，提供一个度量和遵循的基准。具体而言，编写软件需求说明的目的是为所开发的软件提出：
* 软件设计总体要求，作为软件开发人员、软件测试人员相互了解的基础
* 功能、性能要求，数据结构和采集要求，重要的接口要求，作为软件设计人员进行概要设计的依据；
* 软件确认测试的依据。

## 1.2 适用群体
本文档建议适用人员：
* 软件开发人员；
* 软件测试人员。

## 1.3 OSS平台使用群体
* 运营商：物联网运营群体，如：中科、联通；
* 企业客户：运营商发展的企业客户，借助OSS平台实现物联网功能的群体，如：自来水公司、燃气公司；
* 设备厂商：包括终端厂商和基站厂商，拥有硬件设备，无平台支持的群体。

# 2 首页

# 3 连接管理
![设备接入](https://github.com/systemcc/IMG/blob/master/%E8%AE%BE%E5%A4%87%E6%8E%A5%E5%85%A5.png)
## 3.1 企业应用管理
* 运营商发展的企业客户，进入设备接入前需添加相应的企业和应用，用于企业应用管理和维护。
* 默认显示“企业”标签，企业与应用管理可分别点击相应标签进行切换。
* 路径：连接管理>企业应用管理。

![企业应用管理](https://github.com/systemcc/IMG/blob/master/%E4%BC%81%E4%B8%9A%E5%BA%94%E7%94%A8%E7%AE%A1%E7%90%86.png)
### 3.1.1 创建企业
![创建企业](https://github.com/systemcc/IMG/blob/master/%E5%88%9B%E5%BB%BA%E4%BC%81%E4%B8%9A.png)

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|创建企业|按钮|弹出层显示如上图|||点击按钮弹出层显示“创建企业”弹出层|
|企业名称|单行输入框||1.必填项，50字符；2.中英文数字和()、-。||1.填写企业客户的企业名称；2.为空时提交，提示“不能为空”；3.存在非法字符时提交，提示“只能填写中英文、数字和()、-”；4.超过50字符不可输入。|
|企业地址|单行输入框||1.必填项，100字符；2.中英文数字和符号||1.填写企业客户的企业地址；2.为空时提交，提示“不能为空”；3.超过100字符不可输入。|
|提交并创建应用|按钮|关闭“创建企业”页面并切换至“应用”标签同时打开“创建应用”弹出层||详见企业名称和企业地址|1、提交企业信息并创建该企业的应用信息。|
|提交|按钮|关闭“创建企业”弹出层，返回企业列表||详见企业名称和企业地址|1、提交企业信息，并在企业列表中增加新的企业名称条目。|
|取消|按钮|关闭“创建企业”弹出层，返回企业列表|||取消创建企业信息的操作。|
### 3.1.2 企业管理列表
* 创建企业后，生成企业列表及其企业信息；
* 运营商可查看所有企业列表，企业客户和设备厂商仅可查看权限范围内的企业和应用。

![企业管理列表](https://github.com/systemcc/IMG/blob/master/%E4%BC%81%E4%B8%9A%E7%AE%A1%E7%90%86%E5%88%97%E8%A1%A8.png)

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|检索框|单行输入框||为空时不进行检索操作||1.输入企业名称进行检索，回车或点击“放大镜”图标执行检索操作；2.模糊检索|
|企业名称、企业地址|||||创建企业时填写的企业名称和企业地址信息|
|创建时间|||||1.点击“创建企业”弹出层，提交、提交并创建应用的时间；2.格式：2017-10-10 10:00。|
|APPID、AppKey|按钮|弹出层显示AppID和AppKey|||企业创建成功，系统自动分配APPID、AppKey|
|应用|按钮|页面切换至应用列表|||页面切换应用列表，默认检索条件为属于企业的所有应用。|
|管理员|按钮|页面跳转至账号列表|||页面条装置账号列表，默认条件为属于该企业的所有管理员列表。|
|最后修改人|||||显示最后修改企业信息的人员，第一次创建时显示为创建人|
|修改|按钮|弹出层显示修改企业页面|||点击“修改”按钮，弹出层显示修改企业页面，详见3.1.3修改/删除企业|
|删除|按钮|弹出层显示删除确认页面|||点击“删除”按钮，弹出层显示删除确认页面，详见3.1.3修改/删除企业|
|表格属性|||||1.每页显示20条数据；2.翻页功能。|
### 3.1.3 修改/删除企业
![修改企业]()

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|企业名称|单行输入框||必填项，50字符||修改企业名称|
|企业地址|单行输入框||必填项，100字符||修改企业地址|
|修改|按钮|修改成功关闭修改企业弹出层|||点击修改按钮，成功修改后，数据库保存修改后企业信息，同时上方显示绿色横幅提示“修改成功！”|
|取消|按钮|关闭修改企业弹出层|||点击取消按钮，关闭弹出层，无数据修改操作。|
![删除企业]()

* 点击“删除”按钮，显示如上图，进行删除确认操作，点击“确定”即可删除企业；点击“取消”则不进行删除操作。
* 当需删除的企业存在下级应用的时，无法删除企业，上方红色横幅提示“该企业存在下级应用，无法删除！”；点击右侧“×”可关闭提示横幅。

### 3.1.4 创建应用
* 应用属于企业，一个企业可创建多个应用。

![创建应用]()

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|创建应用|按钮|弹出层显示如上图|||点击“创建应用”按钮，显示“创建应用”弹出层|
|所属企业|检索下拉框||必选项|提交为空时，提示“请选择所属企业”|1.选择应用所属的企业，默认显示“请选择所属企业”，下拉框可模糊检索企业名称；2.如从企业管理列表中点击“应用”从而进入创建应用页面、或为创建企业后点击“提交并创建应用”进入创建应用页面的情况，“所属企业”字段默认显示为企业管理列表对应的企业名称和前一步操作创建的企业名称。|
|应用名称|单行输入框||1.必填项；2.中英文数字，50字符|提交为空时，提示“请填写应用名称”；提交输入非法字符时，提示“请输入中英文以及数字”|填写应用名称|
|选择地区|检索下拉框||1.必选项；|提交时为空，提示“请选择地区”|1.选项为全国所有省市，按照拼音的顺序排列，第一个选项均为“全部”；2.两个下拉框分别选择对应的省市及其下级市区；3.“省市”选择全部，同时“市区”自动选择“全部”。|
|应用类型|下拉框||必选项|提交为空时，提示“请选择应用类型”|选项为系统配置完成的，包含烟气传感、消防器材等，具体选项详见表格下方。|
|AppEUI|文字显示||||1.可唯一识别终端设备的应用服务供应商（即所有者）；2.CLAA规定AppEUI是64bits唯一识别码（平台显示16位16进制数）网络将根据此标识寻找终端对应的 APP 厂家的服务器，由 1位应用范围,5 位应用地区，以及2位应用类型，8位序列号组成。|
|设备最大连接数量|单行输入框||必填项，仅数字，5字符|提交为空时，提示“请填写设备最大连接数量”|该应用最多可申请终端设备的数量。|
* 应用类型选项：

|一级类型|二级类型|
|-------|-------|
|作物和农业生产相关服务||
|环境监控|空气、微粒监控|
||江河、湖泊、海洋、水监控|
||土壤环保监控|
||其他环保监控|
|林业和伐木业||
|消防类|消防器材|
||烟气传感|
||危险品|
||其他消防应用|
|渔业与水产业||
|水务类|集水、水处理、水供应|
||污水处理|
||井盖、器材管理|
||抄表类服务|
||其他水务类应用|
|热力类|燃气、蒸汽、热力供应|
||抄表类服务|
||井盖、器材管理|
||其他燃气、蒸汽、热力类服务|
|城市管理类|园区、社区、场所管理|
||公用设施、停车场、路灯管理|
||文物保护|
||其他城市管理类服务|
|交通类|陆路运输和管道运输|
||水上运输|
||储存和运输辅助|
||其他运输、物流及仓储服务|
|制造业|石油石化工业|
||机械加工|
||装备制造|
||食品加工|
||电子、通讯制造|
||其他制造行业服务|
|开采服务|煤炭开采|
||石油及天然气的开采|
||金属矿的开采|
||其他采矿和采石|
||其他开采服务
|电力服务|水、热力、新能源发电|
||输电|
||配电|
||变电|
||其他电力服务|
|其他农林应用||
### 3.1.5 应用管理列表

* 成功创建应用后，生成应用管理列表。
* 查看应用整体状况。

![应用管理列表]()

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|应用创建字段|||||显示创建的应用名称、所属企业、应用类型、AppEUI、资源连接方式、设备最大连接，均为创建应用时填写或选择的内容。|
|终端（已启用/总数）|按钮|当前页面跳转至终端列表|||1.显示内容为该应用包含的终端数量：已启用数量和申请的总数；2.由于应用创建初期尚未进行终端设备的申请，因此默认显示为0/0；3.点击数值，跳转至终端列表页面，默认检索条件为所选择的应用。|
|基站|按钮|当前页面跳转至基站列表|||1.显示内容为该应用的所有终端连接的基站数量（当前时间下所有终端上一次数据传输时所连接的基站数量）；2.点击数值，跳转至基站列表页面，默认检索条件为所选择的应用下终端。
|管理员|按钮|当前页面跳转至账号列表|||1.显示数值为当前应用的管理员数量；2.点击数值，跳转至账号列表，默认条件为所选择的应用。|
|分布|按钮|当前页面跳转至终端、基站分布页面|||分别进入终端和基站的分布查看页面，详见|
### 3.1.6 修改/删除应用
* 用于修改、删除已创建的应用。

![修改应用]()

　1、只能修改应用名称、设备最大连接数、资源连接方式，其他不可修改。
　2、点击“修改”，输入内容符合规范情况下修改成功，关闭修改应用弹出层（同时上方显示绿色提示横幅“修改成功”），数据库记录修改后的信息；点击“取消”，不执行修改操作，同时关闭修改应用弹出层。

![删除应用]()

1、点击“删除”按钮，显示如上图，进行删除确认操作，点击“确定”即可删除应用；点击“取消”则不进行删除操作。
2、当需删除的应用存在终端设备时，无法删除应用，上方红色横幅提示“该应用包含终端设备，无法删除！”；点击右侧“×”可关闭提示横幅。

# 4 运维管理
# 5 系统管理
## 5.1 菜单管理
* 用于菜单创建、修改和删除。
* 最多三级目录，一级目录为平台顶端主菜单，二三级目录为平台左侧纵向菜单。

![菜单管理]()
### 5.1.1 添加一级菜单
![添加一级菜单]()

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|添加一级菜单|按钮|显示“添加一级菜单”弹出层|||点击按钮添加一级菜单信息|
|序号|||||1.序号自动生成，初始状态添加第一个一级菜单，序号为1；顺序添加第二个一级菜单，序号为2；2.序号小的菜单排列显示靠前。|
|菜单名称|单行输入框||1.必填项；2.中英文，20字符|1.提交时为空，提示“请填写菜单名称”；2.提交时有非法字符，提示“仅能输入中文、英文”|填写菜单名称|
|菜单URL|单行输入框||1.非必填项；2.链接格式：英文、数字、符号，500字符||填写菜单URL表示点击该一级菜单可进入对应的功能页面，如无菜单URL，点击菜单名称无操作。|
|提交|按钮|成功则关闭添加一级菜单弹出层|||提交成功，表示添加菜单成功|
|取消|按钮|关闭添加一级菜单弹出层|||取消操作，不执行添加操作|

### 5.1.2 创建二级菜单
* 添加一级菜单后，点击对应一级菜单所在行的“+”用来添加其二级菜单。

![添加二级菜单]()

|元素名称|类型|跳转关系|校验规则|报错提示|元素样式和说明|
|-------|----|-------|-------|--------|-------------|
|一级菜单所在行的“+”|按钮|显示“添加二级菜单”弹出层|||点击按钮，用于添加该一级菜单所属二级菜单。|



### 5.1.3 创建三级菜单
![创建三级菜单]()


















# 6 文档中心
# 7 增值服务
