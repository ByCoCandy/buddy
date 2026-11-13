<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/7a512fdd834547c08fd03cd5b578a93c.jpg" width="80%" style="border-radius:20px" />
</div>

<p align="center"><b>BUDDY · 桌面与随身电子挂件</b></p>

<p align="center"><b>一只放桌边能触摸眨眼、背出门能“吃”蓝牙信号升级、丢了还能亮名片的小挂件</b></p>

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
  <a href="#-二创与折腾指南">二创指南</a> &nbsp;|&nbsp;
  <a href="#-社区交流与开源说明">社区与协议</a> &nbsp;|&nbsp;
  <a href="#-彩蛋">彩蛋</a>
</p>

---

## 📖 项目简介

写代码或看书累了摸摸它的后背，它会眯起弯眼冒爱心、亮起双侧暖光哼小调；一直连拍逗急了还会竖起眉头生闷气。出门把它挂在书包或钥匙扣上，它会悄悄收集路过的蓝牙信号当“糖果”攒经验升级；万一背包或钥匙忘在外面，手机离远了后路人轻碰一下背部，就能亮出你的像素联系名牌。

为了方便大家轻松复刻搓出一只，**BUDDY** 没有用难焊的密脚芯片和满板零碎阻容，而是采用**定制双面底板 + 常用成品小模块“叠汉堡”**的设计——全机一共只有 **8 种器件（合计 9 个零件）**。

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
      <b>🌐 零代码网页刷机</b><br />
      免装编译环境与烧录软件，连上电脑浏览器点一下即可一键烧录。
    </td>
    <td width="25%">
      <b>🎁 自用送人都讨喜</b><br />
      外壳与市售半透小眼镜可自由撞色搭配，连上网页自己捏脸、调光、画名牌。
    </td>
  </tr>
</table>

- 🧠 **主控** — ESP32-C3 SuperMini（RISC-V · BLE 5.0，邮票孔直接贴焊在底板）
- 📺 **屏幕** — 0.96" OLED 单色屏（SSD1306 · 128×64 I2C）
- 👆 **交互** — TTP223 背部隐藏触摸感应 + 侧发声贴片无源蜂鸣器
- 🌈 **灯光** — 2020 WS2812B 独立双氛围彩灯 × 2
- 🔋 **供电** — TP4056 Type-C 充放保护 + 3.7V `102030` 软包锂电 + 侧拨开关
- 🖨️ **结构** — 3D 打印低多边形机身外壳 + 市售成品迷你装饰小眼镜
- 🔓 **开源与固件说明** — 电路原理图与嘉立创 EDA 专业版工程（`.epro2` / Gerber）、3D 打印机身外壳模型（`.stp` / `.3dm` / `.blend`）按 `CC BY-NC-SA 4.0` 完全开源（也可配合开源 **[Bit-Eye-Lib](https://github.com/ByCoCandy/Bit-Eye-Lib)** 自写固件免费折腾）；官方闭源养成固件免费开放**网页一键刷机与 5 秒装机硬件自检**（先确认屏幕/灯光/蜂鸣器/触摸焊接无误再激活），完整功能采用**单机激活制**（第 1 台起按单机购买激活码，一机一码永久绑定芯片硬件 ID，重刷固件无需重复购码，含后续全部无线 OTA 新玩法）。**允许售卖 DIY 散料包、打印外壳与搭载官方正版已激活固件的成品（须保留 `BUDDY · CoCandy` 署名并如实说明激活规则），严禁刷入其他非官方固件商业售卖本项目的设计与外壳。**

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/21c52d77b2a74f8aa79383d280011c89.png" width="82%" style="border-radius:16px" />
</div>
<p align="center"><sub>▲ 结构三视图（机身左右外壳为 3D 打印件，头顶小眼镜为市售成品迷你装饰眼镜）</sub></p>

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
      <b>🎭 4 套性格与触摸声光反馈</b><br />
      内置<b>元气、机敏、温柔、沉稳</b> 4 套性格预设。背部隐藏式触摸配合左右双彩灯和蜂鸣器小曲，轻抚会眯眼撒娇回应，连拍逗急了还会竖眉抗议。
    </td>
    <td width="50%">
      <b>🎨 网页实时捏脸与双灯混色</b><br />
      连上网页端拖动滑块，屏幕上的眼睛宽高、圆角、斜率与左右双灯颜色都会实时跟着变，每个人都能调出不一样的脸。
    </td>
  </tr>
  <tr>
    <td width="50%">
      <b>📡 出门“吃”蓝牙信号养成进化</b><br />
      挂包出门时自动扫描周围的蓝牙广播信号（可识别手机、耳机、手环及另一只 Buddy 等 32 类信号图鉴）攒进糖罐。投喂升级有<b>可爱治愈、灵猫幻星、几何晶核</b>三条路线共 12 阶瞳孔与光环形态，并逐步解锁全部 <b>32 种</b>动态表情。
    </td>
    <td width="50%">
      <b>🛡️ 环境记忆安心地点与防丢狗牌</b><br />
      可记录「家」与最多 2 个常驻安心地点（共 3 处，如工位、工作室），在这些地点断开手机蓝牙不会误亮名牌，回到家后首次轻触还会弹出 <code>🏠 回家啦~</code> 问候；外出一旦蓝牙断连超时即切入防丢锁屏，路人轻触背部即亮屏 20 秒展示 <code>128×64</code> 像素联系名牌（支持邮箱默认生成、文字排版、二维码与手绘涂鸦）。
    </td>
  </tr>
  <tr>
    <td colspan="2">
      <b>🌙 自动对时与夜间免打扰</b>：连过一次网页即可自动同步时间，支持调节自动息屏时长（<code>5 ~ 120 秒</code>）、4 档提示音量（静音 / 轻柔 / 适中 / 清脆）与夜间安静时段自动关灯静音，放床头也不晃眼。
    </td>
  </tr>
</table>

### 2. 背部隐藏单键怎么玩？（交互速查）

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/4003674799b4483c9d49a8538df120b6.png" width="82%" style="border-radius:20px" />
</div>

全机没有外露机械按键，所有日常操作都通过**挂绳孔与小尾巴之间的背部隐藏触摸区**（外壳内侧紧贴 `TTP223`）完成：

| 手势操作 | 触发效果 |
| :---: | :--- |
| **单击轻点** (`< 0.3s`) | 随机触发当前性格互动眼神、双侧彩灯与音效（有待领经验时自动吃下） |
| **轻按抚摸** (`0.3 ~ 0.8s`) | 手指在背部稍停片刻，眯起弯眼配合轻柔呼吸灯撒娇回应 |
| **双击背部** | 查看当前等级进度，吞下收集到的蓝牙广播信号攒经验升级 |
| **三击 / 连续快拍** | 三击触发专属性格彩蛋；连拍积攒兴奋度，按性格递进触发冒爱心、眯眼笑或竖眉生气等反应 |
| **长按 `0.8s`** | 呼出**横向轮盘快捷菜单**（菜单内**短按**切换功能项，**长按 `0.8s`** 环形进度条确认调节音量/亮度/性格/进化路线或立即休眠） |
| **防丢锁屏下轻触** | 亮屏 20 秒展示机主联系名牌（快速三击背部可解锁退出防丢模式） |

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

除嘉立创打样的双层 PCB 底板与一块 `3.7V` `102030` 软包锂电池外，仅需采购以下常见器件：

| 位号 | 器件名称 | 数量 | 选型规格与购买避坑提醒 |
| :---: | :--- | :---: | :--- |
| **U1** | ESP32-C3 SuperMini 开发板 | `1` | Type-C 接口，邮票孔直接平贴焊在底板上，**千万不要焊排针** |
| **U5** | TP4056 Type-C 锂电充电保护板 | `1` | 带 `B+ / B- / OUT+ / OUT-` 焊盘与过充过放保护（对照采购图选常见标准款） |
| **H1** | 0.96 寸 OLED 显示屏 (SSD1306) | `1` | 4 针 I2C 单色屏（配 `1×4P 2.54mm` 排针焊接），**买前务必核对线序：`VCC - GND - SCL - SDA`** |
| **U2** | TTP223 触摸按键模块 | `1` | 常见红色电容触摸小板（`VCC / I/O / GND`） |
| **SW1** | SK12D07V 系列 2档3脚 侧拨开关 | `1` | 卧式弯脚插件（工程封装为 `SK12D07VG5`，同封装 `VG4` 等亦可；焊时尽量往板内靠紧） |
| **LED1, LED2** | 2020 WS2812B 幻彩 RGB 灯珠 | `2` | `SMD 2020` 贴片封装（如 `WS2812B-2020`，体积小建议多买两颗备用） |
| **BUZ1** | 侧发声贴片无源蜂鸣器 | `1` | 贴片电磁式无源蜂鸣器，谐振约 `2.7 kHz`（工程型号 `HYG-9025A`，同焊盘兼容 `SMD9032` 侧发声款） |
| **Q2** | AO3400A N沟道 MOS 管 | `1` | `SOT-23` 贴片封装（实物常见丝印 `A10T` / `X0DV`），用于驱动蜂鸣器 |

### 2. 电池、外壳打印与装饰眼镜说明

- 🔋 **软包锂电池**：使用型号 **`102030`** 的 `3.7V` 带保护板软包锂电池（下方左图实拍为 `650mAh`，买时认准 `102030` 规格，偏大将无法合上外壳）。
- 🖨️ **3D 打印机身外壳**：使用左右半壳 `left.stp`、`right.stp` 模型直接切片打印即可（常规 PLA / PETG 等耗材均可，低多边形折面棱角清晰）。
- 👓 **装饰小眼镜（淘宝识图购买）**：头顶的半透小眼镜**不是 3D 打印件**，直接保存下方右图用**淘宝拍照识图（拍立淘）**就能搜到同款成品迷你小眼镜，半透质感好又不容易断。

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
    <td><sub><b>▲ 电池参考</b>：型号 <code>102030</code>（3.7V · 650mAh 带保护板软包锂电）</sub></td>
    <td><sub><b>▲ 小眼镜参考</b>：非打印件，保存此图去淘宝“拍立淘”识图即可</sub></td>
  </tr>
</table>

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

1. **焊正面贴片与主控**：依次焊好 2 颗 `2020 WS2812B` 灯珠、`AO3400A` MOS 管、侧发声蜂鸣器、`ESP32-C3 SuperMini`（邮票孔平贴上锡）以及侧拨开关。
2. **焊背面 TP4056 充电板**：将 `TP4056` 模块按“Type-C 口略微外探”的位置贴焊在主板背面对应焊盘上。
3. **接好触摸板、电池与屏幕**：用细软硅胶线焊接 `TTP223` 触摸模块（装壳时卡在背部上方内侧斜槽里）和锂电池正负极，再通过 `4P` 排针将 `0.96 寸 OLED` 焊到主板 `3V3 / GND / SCL / SDA`。
4. **先通电、再合壳**：**合盖前务必先拨动开关通电试一下**，确认屏幕点亮正常，再把 `102030` 电池夹在中间理顺导线（可参考下方花絮剖面图），扣合左右外壳、架上小眼镜即大功告成！

---

## 🚀 固件烧录与使用

<div align="center">
  <img src="https://image.lceda.cn/oshwhub/pullImage/7dbaf9e58b894c9d9404cae65407579e.png" width="88%" style="border-radius:16px" />
</div>

> ⚡ **USB 插线前必看（对应 PCB 正面丝印提示）**：  
> 若已焊接锂电池，**用数据线连接内部 `ESP32-C3` 的 Type-C 口供电或刷机前，务必先将侧边电源开关拨至「关」**，防止 USB `5V` 倒灌至电池供电端！日常充电请插外壳底部露出的 `TP4056` Type-C 口。

<table align="center" width="100%">
  <tr>
    <td width="50%">
      <b>1️⃣ 网页一键有线刷机（免装驱动软件）</b><br /><br />
      用电脑 <b>Chrome / Edge</b> 浏览器直接打开在线烧录页：<br />
      👉 <a href="https://home.cocandy.com.cn/flash" target="_blank"><b>https://home.cocandy.com.cn/flash</b></a><br /><br />
      确认<b>侧边电源开关已拨到「关」</b>后，将数据线<b>插在内部 <code>ESP32-C3</code> 的 Type-C 口上</b>（背面 <code>TP4056</code> 的口仅供电不走数据；若未识别可按住 <code>BOOT</code> 键再插线），选中 Buddy 点击烧录即可自动刷入。
    </td>
    <td width="50%">
      <b>2️⃣ 5 秒硬件自检与单机激活</b><br /><br />
      首次刷完开机自带<b>免费装机自检引导</b>：先观察蜂鸣器与双灯闪烁、按屏幕提示<b>长按背部触摸区 5 秒</b>测通硬件（确认焊接零翻车后再激活）。<br /><br />
      随后在电脑或安卓 Chrome / Edge（iOS 可下载 Bluetooth Browser）打开 <a href="https://home.cocandy.com.cn" target="_blank"><b>home.cocandy.com.cn</b></a> 连接蓝牙 <code>Buddy-XXXXXX</code>，按单机使用在 <a href="https://store.cocandy.com.cn" target="_blank"><b>商店主页</b></a> 购买的激活码一键绑定（第 1 台起一机一码永久绑定芯片硬件 ID，重刷固件无需重复购码，且永久包含后续无线 OTA 新功能）。
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

## 🎨 二创与折腾指南

开源仓库同时提供了可直接制板的 PCB 工程（`.epro2` / Gerber）、可直接打印的 `.stp` 实体，以及完整的 **Rhino (`.3dm`) 建模源文件**与 **Blender (`.blend`) 渲染工程**，留足了改装空间，欢迎按自己的想法随便折腾：

### 1. 结构外观与周边配件二创
- **拓展形态配件**：基于外壳 `.3dm` / `.stp` 模型，可以很容易地衍生设计出**桌面磁吸底座**、**显示器顶部挂架**、**书包肩带快拆背夹**或**车载出风口卡扣**。
- **换装与造型魔改**：修改头顶与背部特征面，比如把小尾巴改成猫耳、恶魔角、发条钥匙，或者定制不同框型的可替换配件。
- **耗材与透光玩法**：机身内部左右两侧各有一颗高亮 `2020 WS2812B` 彩灯——除了常规白色 PLA，非常推荐试试**半透明 PETG / 透明光敏树脂 / 夜光或温变耗材**打印外壳，让内部呼吸彩灯直接透壳漫反射出来，或是用丙烯颜料给低多边形折面手涂撞色。

### 2. 自研开源固件折腾（当成掌上迷你开发板玩）
去掉官方固件限制看本质，这块板子就是一套自带**锂电充放管理 + `128×64 OLED` + 左右双路 RGB 灯 + 电容触摸键 + 无源蜂鸣器 + `ESP32-C3`（Wi-Fi & BLE 5.0）** 的超袖珍掌上开发终端。

`ESP32-C3 SuperMini` 外设引脚与 PCB 丝印位号对应关系如下：

| 外设模块（PCB 位号） | 功能信号 | ESP32-C3 引脚 | 备注说明 |
| :--- | :--- | :---: | :--- |
| **0.96" OLED (`H1` · SSD1306)** | `I2C SDA` | `GPIO10` | 4 针 I2C 单色屏（`128×64`），对应底板 `SDA` |
| **0.96" OLED (`H1` · SSD1306)** | `I2C SCL` | `GPIO20` | 对应底板 `SCL`（排针丝印 `3V3 - GND - SCL - SDA`） |
| **TTP223 触摸模块 (`U2`)** | `TOUCH I/O` | `GPIO3` | 默认高电平有效（触摸输出高电平） |
| **左侧氛围灯 (`LED2`)** | `WS2812B DIN` | `GPIO21` | 屏幕正面视角左侧（对应 PCB 丝印 **`LED2`**，独立单总线） |
| **右侧氛围灯 (`LED1`)** | `WS2812B DIN` | `GPIO0` | 屏幕正面视角右侧（对应 PCB 丝印 **`LED1`**，独立单总线非级联） |
| **贴片无源蜂鸣器 (`BUZ1`)** | `PWM 驱动` | `GPIO1` | 经 `AO3400A` (`Q2`) NMOS 驱动，谐振约 `2.7 kHz` |

对照上方引脚表，你可以直接用 **Arduino / PlatformIO / ESP-IDF** 从零写自己的固件，搭配我们开源的 **[Bit-Eye-Lib](https://github.com/ByCoCandy/Bit-Eye-Lib)** 表情渲染库，能轻松改出很多有意思的小玩意：
- **🍅 桌面番茄钟 / 久坐提醒器**：摸一下后背开启 25 分钟专注倒计时，到点双灯呼吸闪烁 + 蜂鸣器提醒。
- **📊 Wi-Fi 迷你状态监视屏**：利用 `ESP32-C3` 自带的 2.4GHz Wi-Fi 拉取天气、GitHub Star 数、B 站粉丝数或家用服务器在线状态。
- **⌨️ 蓝牙无线小宏键（BLE HID）**：模拟蓝牙键盘/多媒体键，放在手边摸一下一键静音麦克风、切歌或锁屏。
- **🕹️ 单键像素小游戏机**：在 `128×64` 屏幕上跑自己写的 Flappy Bird、小恐龙跳仙人掌或电子木鱼。

如果你做出了好玩的外壳改件或自研开源固件，欢迎去 GitHub 提 Issue / PR 贴出你的仓库链接，我们可以直接收录展示在 README 里！

---

## 💬 社区交流与开源说明

### 🔄 持续更新与维护
- **☁️ 玩法与固件持续上新**：正在开发中的**单键迷你小游戏**、**蓝牙近距寻物**，以及更多性格小动作、表情包与网页端新功能都会陆续推送。
- **📲 现有硬件免拆壳 OTA 升级**：现在复刻焊好的机器**不需要改板，也不用拆壳插线**——后续有新固件时，直接打开 **[home.cocandy.com.cn](https://home.cocandy.com.cn)** 蓝牙连上设备，点一下即可无线升级。

### 🤝 交流与仓库地址
- **🐧 QQ 交流群**：**`1042593321`**（复刻拼单、焊接刷机答疑、固件更新通知、晒图吹水都可以进群一起聊）
- **🐙 GitHub 开源仓库**：👉 **[https://github.com/ByCoCandy/buddy](https://github.com/ByCoCandy/buddy)**
  （同步完整 3D 模型源文件、PCB 工程与 GPIO 引脚文档；求个 **Star ⭐**，遇到 Bug 或有新功能点子可直接提 **Issue**）
- **📸 复刻答疑与晒图**：焊接、刷机或装壳时遇到任何问题可在下方评论区留言；搓出成品的小伙伴非常欢迎**返图晒出你的外壳/眼镜撞色搭配和专属捏脸**！

> 📄 **开源协议、单机激活与散料 / 成品售卖说明**
> - **基础开源协议**：本项目的电路原理图、PCB 制板文件、3D 外壳模型与图文文档采用 **`CC BY-NC-SA 4.0`** 协议开源，欢迎个人 DIY 复刻与非商业二创分享（也可配合开源 **[Bit-Eye-Lib](https://github.com/ByCoCandy/Bit-Eye-Lib)** 自写固件免费折腾）。
> - **官方固件单机激活**：官方预编译固件与在线网页服务闭源并保留全部权利。**[home.cocandy.com.cn/flash](https://home.cocandy.com.cn/flash)** 免费开放 USB 一键刷机与 5 秒装机硬件自检；解锁完整养成系统、网页实时捏脸与终身无线 OTA 升级采用**单机激活制**（第 1 台起按单机在 **[商店主页](https://store.cocandy.com.cn)** 购买激活码，一机一码永久绑定芯片硬件 ID，同一芯片重刷无需重复购码）。
> - **散料包与成品售卖许可（绑定官方固件生态）**：**允许个人或第三方店铺售卖 DIY 散件物料包、3D 打印外壳及组装好的 BUDDY 成品**——商品页须醒目标注 `BUDDY · CoCandy` 原作署名；组装成品须烧录官方正版固件并完成单机激活后交付，散件包须向买家如实说明官方固件需单机激活（或自写开源固件）。**严禁将本项目的 3D 外壳、PCB 设计或其衍生外观搭载任何非官方（第三方/自改）固件进行商业售卖**。非官方直营渠道售出的散件或成品，其器件品质、焊接做工、电池安全与退换货售后均由对应卖家自行负责，官方仅提供在线网页与固件更新支持。

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
