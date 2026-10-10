# ESP32-S3 Touch AMOLED 2.16 CRT 外壳 — STEP 与尺寸规格

这是适配 Waveshare ESP32-S3-Touch-AMOLED-2.16 的小型 CRT 风格外壳 **Fusion v50** 原生 BRep STEP 导出。全部尺寸单位为 **mm**。公开仓库只提供本版 STEP 和这份规格文档；独立零件 STEP 保留装配坐标。

## 文件

| 文件 | 内容 |
|---|---|
| [STEP/assembly-v50.stp](STEP/assembly-v50.stp) | 整机位置参考，17 个实体；包含前后壳、按钮、低矮底座、显示模块/PCB/螺母占位及间隔件。它不包含电池、喇叭占位或另两款底座。 |
| [STEP/parts/front-fascia.stp](STEP/parts/front-fascia.stp) | 一体前盖 |
| [STEP/parts/rear-shell.stp](STEP/parts/rear-shell.stp) | 后壳 |
| [STEP/parts/three-buttons-w.stp](STEP/parts/three-buttons-w.stp) | W 型三联按钮，设计为柔性材料件 |
| [STEP/parts/left-lower-pcb-spacer.stp](STEP/parts/left-lower-pcb-spacer.stp) / [left-upper](STEP/parts/left-upper-pcb-spacer.stp) / [right-lower](STEP/parts/right-lower-pcb-spacer.stp) / [right-upper](STEP/parts/right-upper-pcb-spacer.stp) | 四个 PCB 环形间隔件；这些不是旧版左右固定条 |
| [STEP/parts/low-glue-base.stp](STEP/parts/low-glue-base.stp) / [round-20deg-base.stp](STEP/parts/round-20deg-base.stp) / [three-foot-20deg-base.stp](STEP/parts/three-foot-20deg-base.stp) | 三款可选底座，每次只选一种 |

每个独立零件 STEP 含一个实体。STEP 文件由 Fusion 对同一已保存 v50 设计导出；整机 STEP 中的参考实体用于定位，不是打印件。

## 坐标与外形

- **X**：左右；**Y**：向上；**+Z**：朝屏幕。外壳前后方向为 Z。
- 前盖与后壳合并外包围盒：**X 55 × Y 53 × Z 54.32**。后背平面 Z=−30，最前端 Z=24.32；壳底 Y=−28.2，前顶面 Y=24.8。此尺寸不含底座。
- 前盖单件外包围盒：55 × 53 × 7.2；后壳单件约 55 × 53 × 47.12。两个零件在 Z=17.12 处衔接。
- 低矮底座装配坐标包围盒：36 × 4.95 × 30.5。圆形 20° 底座：48 × 25.29 × 46.47；三脚 20° 底座：61 × 28.72 × 52.67。后两项为倾斜放置后的轴向包围盒，不是水平占地尺寸。
- 单斜切肩部设计面：`Y = (5/3)Z + 21.4667`；内侧平行偏移 2.2。前肩设计半径 R18、后肩 R12、后周边 R2.5。这些是造型设计值，并非 Sony 原机测量值。

## 模块接口与公差

| 项目 | v50 规格 | 数据状态 |
|---|---|---|
| 原显示模块面板 | 46 × 46 × 5 | 外形参考图；厚度为使用者实测 |
| 显示玻璃 / 有效显示区 | 43.30 × 43.30 / 38.99 × 38.99 | [Waveshare 尺寸资料](https://github.com/waveshareteam/ESP32-S3-Touch-AMOLED-2.16/tree/main/dimensions) |
| PCB 外形 / 厚度 | 42 × 39 / 1.6 | 外形来自拆解标注；厚度暂定 |
| 四孔中心 | X=±18.5、Y=±17；孔距 37 × 34 | 模块尺寸标注与 CAD 基准 |
| PCB 与原面板背面间距 | 5.0；四个间隔件 Ø5 × 5、通孔约 Ø2.35 | v50 CAD 设计 |
| 螺丝 / 后壳通孔 / 螺丝头入口 | M2×14 / Ø2.35 / Ø4.9 | 使用者螺丝规格与 v50 CAD 设计 |
| 原面板下部螺母座 | 两处 Ø4.8、深 2.6，X=±18.5、Y=−17 | **仅参考模型中的拟加工尺寸**；原面板实物未核对 |
| 下部螺丝名义啮合 | 约 2.48 | CAD 计算；未计真实螺纹起始与螺丝头尺寸 |
| 前盖摩擦筋 / 名义直边间隙 | 左右各凸出 0.2 / 0.1 | v50 CAD 设计；名义每侧过盈约 0.1 |
| 前盖内唇至玻璃最小距离 | 0.23 | CAD 距离，未计打印收缩 |
| 电池 | 34 × 31 × 11；在模型中占 X 34、Y 11、Z 31 | 使用者提供外形；包膜与导线需实测 |
| 喇叭 | 20 × 15 × 8；发声面朝顶部栅栏 | **暂定占位尺寸** |
| 后置 Type-C 母口法兰 / 孔距 | 20 × 6.7 / 16 | 使用者配件图 |
| 后置 Type-C 固定孔 | Ø2.4 | CAD 设计，供约 Ø2 mm 螺丝留余量 |
| 板上 Type-C 母口轴线 | X=0、Z=13.9；口沿约 Y=−22.8 | **暂定定位**，需实物核对 |
| 向后 90° 弯头下方空间 | 至少 3 高；向后走线 | CAD 预留；实际插头和线缆包络未测 |
| 顶部三按钮孔 | Ø5.3；中心距 10 | 模块尺寸标注 |

后壳内顶面有喇叭卡座，电池托盘朝屏幕端开放。侧面栅栏每侧 2 列×4 行，顶面栅栏为 2 组×4 列。后壳以背面贴打印平台、前开口朝上为设计打印方向；实际支撑需求应以切片和试打确认。

**装配边界：**下部螺母需安装到原显示面板；该面板不是这里提供的打印零件。热熔螺母的真实底孔、原面板可加工壁厚、Type-C 插头外形、电池包膜、喇叭卡紧力及整体实物装配尚未验证。
