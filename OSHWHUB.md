<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/7a512fdd834547c08fd03cd5b578a93c.jpg" width="80%" style="border-radius:20px" />
</div>

<p align="center"><b>BUDDY · 桌面与随身电子挂件</b></p>

<p align="center"><b>一只放桌边能摸头眨眼、背出门能“吃”蓝牙信号升级、丢了还能亮名片的小挂件</b></p>

<p align="center">
  <code>ESP32-C3</code> &nbsp;·&nbsp;
  <code>0.96" OLED</code> &nbsp;·&nbsp;
  <code>双 WS2812B 彩灯</code> &nbsp;·&nbsp;
  <code>TTP223 触摸</code> &nbsp;·&nbsp;
  <code>开放网页APP</code> &nbsp;·&nbsp;
  <code>仅 9 个零件</code>
</p>

<p align="center">
  <a href="#-项目简介">简介</a> &nbsp;|&nbsp;
  <a href="#-功能与玩法">功能玩法</a> &nbsp;|&nbsp;
  <a href="#-开放网页app">开放网页APP</a> &nbsp;|&nbsp;
  <a href="#-硬件材料与打印建议">材料与打印</a> &nbsp;|&nbsp;
  <a href="#-焊接与组装流程">组装避坑</a> &nbsp;|&nbsp;
  <a href="#-固件烧录与使用">在线刷机</a> &nbsp;|&nbsp;
  <a href="#-花絮">花絮</a> &nbsp;|&nbsp;
  <a href="#-彩蛋">彩蛋</a>
</p>

---

## 📖 项目简介

写代码或看书累了摸摸它的头，它会眯起弯眼冒爱心、亮起双侧暖光哼小调；一直连拍逗急了还会竖起眉头生闷气。出门把它挂在书包或钥匙扣上，它会悄悄收集路过的蓝牙信号当“糖果”攒经验升级；万一背包或钥匙忘在外面，手机离远了后路人轻碰一下头顶，就能亮出你的像素联系名牌。

为了让大家周末花一小时就能轻松搓出一只，**BUDDY** 没有用难焊的密脚芯片和满板零碎阻容，而是采用**底板 + 常用成品小模块“叠汉堡”**的设计——全机一共只有 **8 种器件（合计 9 个零件）**。

<table align="center" width="100%">
  <tr>
    <td width="25%">
      <b>💰 一杯奶茶成本</b><br />
      全套模块约二三十元，小尺寸双面板可直接用<b>嘉立创免费打样券</b>。
    </td>
    <td width="25%">
      <b>🔥 一把烙铁搞定</b><br />
      仅 <b>9 个零件</b>，无 QFN 超密引脚芯片，新手没有风枪也能焊。
    </td>
    <td width="25%">
      <b>🌐 零代码 10 秒刷机</b><br />
      免装编译环境与驱动软件，连上电脑浏览器点一下即可一键烧录。
    </td>
    <td width="25%">
      <b>🎁 自用送人都讨喜</b><br />
      外壳与市售半透小眼镜可自由撞色搭配，连上网页自己捏脸、调光、画名牌。
    </td>
  </tr>
</table>

- 🧠 **主控** — ESP32-C3 SuperMini（RISC-V · BLE 5.0，邮票孔直接贴焊在底板）
- 📺 **屏幕** — 0.96" OLED 单色屏（SSD1306 · 128×64 I2C）
- 👆 **交互** — TTP223 顶部触摸感应 + 侧发声贴片无源蜂鸣器
- 🌈 **灯光** — 2020 WS2812B 独立双氛围彩灯 × 2
- 🔋 **供电** — TP4056 Type-C 充放保护 + 3.7V 软包锂电 + 侧拨开关
- 🖨️ **结构** — 3D 打印低多边形机身 + 可拆卸装饰眼镜
- 🔓 **开源与售卖说明** — 硬件原理图、PCB、3D 打印机身外壳模型（STP / 3DM / BLEND）按 `CC BY-NC-SA 4.0` 开源；配套提供免费个人可烧录固件（固件闭源）与开放网页端。**允许售卖 DIY 散件物料包与搭载官方正版固件的组装成品（须保留署名），严禁刷入其他非官方固件商业售卖本项目的设计与外壳。**

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/21c52d77b2a74f8aa79383d280011c89.png" width="82%" style="border-radius:16px" />
</div>
<p align="center"><sub>▲ 结构三视图</sub></p>

---

## ✨ 功能与玩法

### 1. 已上线功能与实机画面

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/0c9eedb7d7ad4daeafc93db925117a39.png" width="82%" style="border-radius:20px" />
</div>
<p align="center"><sub>▲ 0.96" OLED (128×64) 实机部分表情、进化眼神、轮盘菜单与系统 UI 展示</sub></p>

<table align="center" width="100%">
  <tr>
    <td width="50%">
      <b>🎭 4 套性格与摸头声光反馈</b><br />
      内置<b>元气、暴躁、社恐、发呆</b> 4 套性格底脸。头顶隐藏式触摸配合左右双彩灯和蜂鸣器小曲，轻抚会眯眼撒娇冒泡，狂拍会炸毛微颤。
    </td>
    <td width="50%">
      <b>🎨 网页实时捏脸与双灯混色</b><br />
      连上网页端拖动滑块，屏幕上的眼睛宽高、圆角、斜率与左右双灯颜色都会实时跟着变，每个人都能调出不一样的脸。
    </td>
  </tr>
  <tr>
    <td width="50%">
      <b>📡 出门“吃”蓝牙信号养成进化</b><br />
      挂包出门时自动扫描周围的蓝牙广播信号攒进糖罐。投喂升级有<b>可爱治愈、灵猫幻星、几何晶核</b>三条路线共 12 阶瞳孔与光环形态，并逐步解锁全部 <b>32 种</b>动态表情。
    </td>
    <td width="50%">
      <b>🛡️ 常驻安全区与电子防丢狗牌</b><br />
      可记忆最多 3 个安全地点（如家里、工位），回到家还会弹出 <code>🏠 回家啦~</code> 问候并自动免打扰；外出一旦蓝牙断连超时即切入防丢锁屏，轻触亮出 <code>128×64</code> 像素联系名牌（支持邮箱默认生成、文字排版、二维码与手绘涂鸦）。
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <b>🌙 自动对时与夜间免打扰</b>：连过一次网页即可自动同步时间，支持调节屏幕休眠时长、4 档音量与夜间自动静音熄灯，放床头也不晃眼。
    </td>
  </tr>
</table>

### 2. 头顶单键怎么玩？（交互速查）

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/4003674799b4483c9d49a8538df120b6.png" width="82%" style="border-radius:20px" />
</div>

全机没有外露机械按键，所有日常操作都靠头顶一块隐藏触摸区完成：

| 手势操作 | 触发效果 |
| :---: | :--- |
| **单击 / 轻抚摸头** | 随机触发当前性格的互动眼神、双侧灯效与欢快音效 |
| **连续快拍狂撸** | 积攒兴奋度冒出满屏像素小爱心（暴躁性格拍急了会生气抗议） |
| **双击头顶** | 掏出糖罐“吃”掉收集到的蓝牙信号攒经验，触发吞咬与升级动画 |
| **长按头顶** | 呼出**横向轮盘快捷菜单**（单击切项调音量/亮度/性格/路线，长按 `0.8s` 环形进度条确认） |

### 3. 正在开发（后续直接通过网页无线 OTA 升级）

<table align="center" width="100%">
  <tr>
    <td width="50%">
      <b>🎮 单键迷你小游戏</b> &nbsp;<code>🛠 开发中</code><br />
      适配单触摸键与 128×64 屏幕的休闲小游戏，做好后支持网页端直接在线更新。
    </td>
    <td width="50%">
      <b>🧭 近距雷达找物体</b> &nbsp;<code>🛠 开发中</code><br />
      忘了钥匙或包塞在哪个角落时，用蓝牙信号强度近距寻物并让挂件声光呼应。
    </td>
  </tr>
</table>

---

## 📱 开放网页APP

不用专门装配套客户端，**电脑、安卓、iOS 全平台都能用**。直接在对应浏览器打开 **[home.cocandy.com.cn](https://home.cocandy.com.cn)** 就能通过 WebBLE 蓝牙直连设备，完成**捏脸调光、糖罐投喂进化、防丢名牌绘制、表情点播**以及**有线一键刷机与无线 OTA 升级**。

| 使用设备 | 推荐浏览器 | 支持能力说明 |
| :---: | :---: | :--- |
| **💻 电脑 (Windows / macOS)** | `Chrome` / `Edge` | 蓝牙直连全功能调参 + 无线 OTA + **USB 串口一键有线刷机** |
| **🤖 安卓 (Android)** | `Chrome` / `Edge` | 蓝牙直连全功能调参（捏脸、投喂、画名牌、无线 OTA） |
| **🍎 苹果 (iOS / iPadOS)** | **`Bluetooth Browser`** | 在 App Store 下载 **Bluetooth Browser** 后输入网址即可蓝牙直连（自带 Safari 不支持 WebBLE） |

<table align="center" width="100%">
  <tr align="center">
    <td width="33%"><img src="https://image.lceda.cn/oshwhub/pullImage/3380559e2542484791a97c4a6a581885.png" width="100%" style="border-radius:14px" /></td>
    <td width="33%"><img src="https://image.lceda.cn/oshwhub/pullImage/e194e4d20c1c4912914cf3967ea367f2.png" width="100%" style="border-radius:14px" /></td>
    <td width="33%"><img src="https://image.lceda.cn/oshwhub/pullImage/692ae154d3e64354800f1f94b2c3a66e.png" width="100%" style="border-radius:14px" /></td>
  </tr>
  <tr align="center">
    <td><sub><b>设备管理主页</b><br />蓝牙直连与多设备管理</sub></td>
    <td><sub><b>成长喂养</b><br />蓝牙信号糖罐投喂与三路线进化</sub></td>
    <td><sub><b>眼神与灯光 DIY</b><br />双灯独立配色、128×64 捏脸与表情点播</sub></td>
  </tr>
</table>

---

## 🧩 硬件材料与打印建议

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/626a595e4ae64c52a7d49f764bcd78f2.png" width="88%" style="border-radius:16px" />
</div>

### 1. 电路元器件清单（8 种共 9 个）

除嘉立创打样的 PCB 底板与一块 `3.7V` `102030` 软包锂电池外，仅需采购以下常见器件：

| 位号 | 器件名称 | 数量 | 选型规格与购买避坑提醒 |
| :---: | :--- | :---: | :--- |
| **U1** | ESP32-C3 SuperMini 开发板 | `1` | Type-C 接口，邮票孔直接平贴焊在底板上，**千万不要焊排针** |
| **U5** | TP4056 Type-C 锂电充电保护板 | `1` | 尺寸 `17.4 × 28 mm`，1A 带过充过放保护 |
| **H1** | 0.96 寸 OLED 显示屏 (SSD1306) | `1` | 4 针 I2C 接口（配 `4P` 排针焊接），**买前务必核对线序：`VCC - GND - SCL - SDA`** |
| **U2** | TTP223 触摸按键模块 | `1` | 常见红色小板（`VCC / I/O / GND`） |
| **SW1** | SK12D07V 2档3脚 侧拨开关 | `1` | 卧式侧拨，**拨杆长度选 4mm** |
| **LED1, LED2** | 2020 WS2812B 幻彩 RGB 灯珠 | `2` | `2.0 × 2.0 mm` 贴片封装（建议多买两颗备用） |
| **BUZ1** | 侧发声贴片无源蜂鸣器 | `1` | SMD `10.5 × 9 mm`，电磁式（谐振约 `2.7 kHz`） |
| **Q2** | AO3400A N沟道 MOS 管 | `1` | `SOT-23` 贴片封装（丝印常见 `X0DV` / `A10T`），用于驱动蜂鸣器 |

### 2. 外壳打印建议

- 🖨️ **机身外壳**：推荐 **哑光白 / 奶油白 PLA**（层高 `0.16mm`），低多边形折面在自然光下棱角非常干净（`102030` 软包锂电池与装饰小眼镜详见下一节底部实物参考图）。

---

## 🔧 焊接与组装流程

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/fa49ba09e2ad4267a5ad4e6caaa35a34.jpg" width="88%" style="border-radius:16px" />
</div>
<p align="center"><sub>▲ 焊接与装壳完整流程</sub></p>

组装顺序按下面 **4 步**走就行，动手前先看一眼这 **2 个装壳避坑重点**，能省掉返工拆焊的麻烦：

> ⚠️ **装机前必看：2 个结构避坑重点**
> - **避坑 1（开关往里靠）**：焊正面 `SK12D07V` 拨动开关时**尽量往 PCB 内侧靠紧**，留出合适的拨杆外露长度，防止装壳时顶住外壳。
> - **避坑 2（充电口往外探）**：背面 `TP4056` 带 Type-C 口的一端**必须超出 PCB 边缘一小节**（参照上图特写）！如果焊平齐或缩在板内，装壳后充电线插头会被外壳挡住插不到底。

1. **焊正面贴片与主控**：依次焊好 2 颗 `2020 WS2812B` 灯珠、`AO3400A` MOS 管、侧发声蜂鸣器、`ESP32-C3 SuperMini`（邮票孔平贴上锡）以及 `SK12D07V` 拨动开关。
2. **焊背面 TP4056 充电板**：将 `TP4056` 模块按“Type-C 口略微外探”的位置贴焊在主板背面对应焊盘上。
3. **接好触摸板、电池与屏幕**：用细软硅胶线焊接 `TTP223` 触摸模块（装壳时卡在头顶内侧斜槽里）和锂电池正负极，再通过 `4P` 排针将 `0.96 寸 OLED` 焊到主板 `3V3 / GND / SCL / SDA`。
4. **先通电、再合壳**：**合盖前务必先拨动开关通电试一下**，确认屏幕点亮正常，再把电池夹在中间理顺导线（可参考下方花絮剖面图），扣合左右外壳、架上小眼镜即大功告成！

> ⚠️ **关于眼镜和电池**
> - **软包锂电池**：使用 **`102030`** 规格 `3.7V` 带保护板软包锂电池（容量约 `650mAh`，尺寸 `10 × 20 × 30 mm`，买的时候注意核对尺寸，太大合不上外壳）。
> - **装饰小眼镜**：头顶的小眼镜**不是 3D 打印件**，直接保存下方右图用**淘宝拍照识图（拍立淘）**就能搜到同款成品娃用小眼镜，果冻半透质感好又不容易断。

<table align="center" width="100%">
  <tr align="center">
    <td width="50%">
      <img src="https://image.lceda.cn/oshwhub/pullImage/160b2e92e0154e3abf291b8e12af541a.png" width="100%" style="border-radius:14px" />
    </td>
    <td width="50%">
      <img src="https://image.lceda.cn/oshwhub/pullImage/778734b7b32642e68eaa7a1a8f54363e.jpg" width="100%" style="border-radius:14px" />
    </td>
  </tr>
  <tr align="center">
    <td><sub><b>▲ 电池参考</b>：型号 <code>102030</code>（3.7V · 650mAh 带保护板）</sub></td>
    <td><sub><b>▲ 小眼镜参考</b>：非打印件，保存此图去淘宝“拍立淘”识图即可</sub></td>
  </tr>
</table>

---

## 🚀 固件烧录与使用

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/7dbaf9e58b894c9d9404cae65407579e.png" width="88%" style="border-radius:16px" />
</div>

<table align="center" width="100%">
  <tr>
    <td width="50%">
      <b>1️⃣ 网页一键有线刷机（免装驱动软件）</b><br /><br />
      用电脑 <b>Chrome / Edge</b> 浏览器直接打开在线烧录页：<br />
      👉 <a href="https://home.cocandy.com.cn/flash" target="_blank"><b>https://home.cocandy.com.cn/flash</b></a><br /><br />
      注意数据线要<b>插在内部 <code>ESP32-C3</code> 的 Type-C 口上</b>（背面 <code>TP4056</code> 的口仅供电不走数据；若未识别可按住 <code>BOOT</code> 键再插线），选中 Buddy 点击烧录即可自动刷入。
    </td>
    <td width="50%">
      <b>2️⃣ 5 秒硬件自检与蓝牙连接</b><br /><br />
      首次刷完开机自带<b>装机自检引导</b>：观察蜂鸣器与双灯闪烁正常后，按屏幕提示<b>长按头顶触摸区 5 秒</b>即可通过自检。<br /><br />
      随后在电脑或安卓 Chrome / Edge（iOS 可下载 Bluetooth Browser 浏览器）打开 <a href="https://home.cocandy.com.cn" target="_blank"><b>home.cocandy.com.cn</b></a> 连接蓝牙 <code>Buddy-XXXXXX</code>，绑定后即可解锁全部自定义捏脸、名牌与云端备份。
    </td>
  </tr>
</table>

---

## 📸 花絮

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/a047505b1c614050b41a69dfaf5f0f76.jpg" width="76%" style="border-radius:16px" />
</div>
<p align="center"><sub>▲ 装机前桌面随手拍：还没塞进“五脏六腑”的初代试装壳</sub></p>

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/bb09600160e14c2a9c2654106b96d867.png" width="76%" style="border-radius:16px" />
</div>
<p align="center"><sub>▲ 合盖前内部实拍：从左到右依次是触摸板、软包电池、主板叠层与 OLED 屏幕</sub></p>

调板子装机时随手留了两张桌面照——别看一共就 9 个零件，真把触摸板、软包电池和三层板子严丝合缝塞进这颗小多边形脑袋里的时候，成就感还是非常足的（复刻理线时照着图中的位置摆最顺手）。

如果你也复刻了一只 **BUDDY**，非常欢迎在社区**返图晒出你的外壳/眼镜撞色搭配和捏脸眼神**！觉得好玩的话也欢迎点个**赞和收藏**支持一下 🙌

---

## 🔄 持续更新与优化

这个项目不会“发完即止”，后续会围绕现有硬件持续维护和迭代优化：

- **☁️ 玩法与固件持续上新**：正在开发中的**单键迷你小游戏**、**蓝牙近距寻物**，以及更多性格小动作、表情包与网页端新功能都会陆续推送。
- **📲 现有硬件免拆壳 OTA 升级**：现在复刻焊好的机器**不需要改板，也不用拆壳插线**——后续有新固件时，直接打开 **[home.cocandy.com.cn](https://home.cocandy.com.cn)** 蓝牙连上设备，点一下即可无线升级。

---

## 🎨 二创与折腾指南

本仓库同时提供了可直接制板的 PCB 工程、可直接打印的 `.stp` 实体，以及完整的 **Rhino (`.3dm`) 建模源文件**与 **Blender (`.blend`) 渲染工程**，留足了改装空间，欢迎按自己的想法随便折腾：

### 1. 结构外观与周边配件二创
- **拓展形态配件**：基于外壳 `.3dm` / `.stp` 模型，可以很容易地衍生设计出**桌面磁吸底座**、**显示器顶部挂架**、**书包肩带快拆背夹**或**车载出风口卡扣**。
- **换装与造型魔改**：修改头顶与背部特征面，比如把小尾巴改成猫耳、恶魔角、发条钥匙，或者定制不同框型的可替换配件。
- **耗材与透光玩法**：机身内部左右两侧各有一颗高亮 `2020 WS2812B` 彩灯——除了常规哑光白 PLA，非常推荐试试**半透明 PETG / 透明光敏树脂 / 夜光或温变耗材**打印外壳，让内部呼吸彩灯直接透壳漫反射出来，或是用丙烯颜料给低多边形折面手涂撞色。

### 2. 自研开源固件折腾（当成掌上迷你开发板玩）
去掉官方固件限制看本质，这块板子就是一套自带**锂电充放管理 + `128×64 OLED` + 左右双路 RGB 灯 + 电容触摸键 + 无源蜂鸣器 + `ESP32-C3`（Wi-Fi & BLE 5.0）** 的超袖珍掌上开发终端。

对照 **[GitHub](https://github.com/ByCoCandy/buddy)** 的 **GPIO 引脚分配表**，你可以直接用 **Arduino / PlatformIO / ESP-IDF** 从零写自己的固件，搭配我们开源的 **[Bit-Eye-Lib](https://github.com/ByCoCandy/Bit-Eye-Lib)** 表情渲染库，能轻松改出很多有意思的小玩意：
- **🍅 桌面番茄钟 / 久坐提醒器**：摸一下后背开启 25 分钟专注倒计时，到点双灯呼吸闪烁 + 蜂鸣器提醒。
- **📊 Wi-Fi 迷你状态监视屏**：利用 `ESP32-C3` 自带的 2.4GHz Wi-Fi 拉取天气、GitHub Star 数、B 站粉丝数或家用服务器在线状态。
- **⌨️ 蓝牙无线小宏键（BLE HID）**：模拟蓝牙键盘/多媒体键，放在手边摸一下一键静音麦克风、切歌或锁屏。
- **🕹️ 单键像素小游戏机**：在 `128×64` 屏幕上跑自己写的 Flappy Bird、小恐龙跳仙人掌或电子木鱼。

如果你做出了好玩的外壳改件或自研开源固件，欢迎提 Issue / PR 贴出你的仓库链接，我们可以直接收录展示在 README 里！

---

## 💬 社区交流与 GitHub

欢迎大家一起来玩、改外观、提脑洞：

- **🐧 QQ 交流群**：**`1042593321`**（复刻拼单、焊接刷机答疑、固件更新通知、晒图吹水都可以进群一起聊）
- **🐙 GitHub 仓库**：👉 **[https://github.com/ByCoCandy/buddy](https://github.com/ByCoCandy/buddy)**
  （整理同步 3D 模型、硬件工程文件等；求个 **Star ⭐**，遇到 Bug 或有新功能点子也可以直接提 **Issue**）
- **📸 复刻答疑与晒图**：焊接、刷机或装壳时遇到任何问题，也可以直接在本页下方评论区留言；搓出成品的小伙伴非常欢迎**返图晒出你的外壳/眼镜撞色搭配和专属捏脸**！
- 👍 觉得这个小挂件好玩的话，别忘了随手点个**赞和收藏**支持一下 🙌

> 📄 **开源协议与散料 / 成品售卖说明**
> - **个人 DIY 复刻**：电路、3D 外壳模型与文档遵循 `CC BY-NC-SA 4.0` 开源，个人自用可在网页端免费烧录激活。
> - **允许售卖散料包与官方固件成品**：欢迎大家在闲鱼/小店售卖 **BUDDY 的 DIY 散件物料包、3D 打印外壳以及组装好的成品**！商品页注明 `BUDDY · CoCandy` 原作信息即可；其中组装成品须**烧录官方正版固件并通过官方平台正规激活**（超出个人免费额度的批量激活可在 **[商店主页](https://store.cocandy.com.cn)** 获取授权配额）。**严禁将本项目的外壳、PCB 设计或其衍生外观刷入任何第三方/自改固件进行商业售卖**。
> - **售后说明**：非官方直营渠道售出的散件物料或代焊成品，其器件品质、焊接做工、电池安全与退换售后均由对应卖家自行负责，官方仅提供在线网页端与固件更新服务。

---

## 🍬 彩蛋

<p align="center">
  <a href="https://cocandy.com.cn" target="_blank"><b>✨ 彩蛋!!! 点击访问 CoCandy 主页 ✨</b></a>
</p>

<div align="center">
  <a href="https://cocandy.com.cn" target="_blank">
    <img src="https://image.lceda.cn/oshwhub/pullImage/15aeb272429848caa594ff229211e4e3.png" width="76%" style="border-radius:16px" />
  </a>
</div>

<p align="center">
  <a href="https://home.cocandy.com.cn" target="_blank">✨设备中心</a> &nbsp;·&nbsp;
  <a href="https://store.cocandy.com.cn" target="_blank">商店主页</a> &nbsp;·&nbsp;
  <a href="https://home.cocandy.com.cn/flash" target="_blank">烧录平台✨</a>
</p>
