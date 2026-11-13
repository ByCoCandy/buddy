# Pergola Walkway 4K HDRI 环境光贴图说明

为减小 Git 仓库克隆体积，Blender 渲染场景所使用的 `4K` 环境光贴图 **`pergola_walkway_4k.exr`**（约 `84 MB`）未直接包含在仓库中。

> 💡 **提示**：如果你只是查看结构、修改模型尺寸或导出 3D 打印文件，**无需下载此文件**；只有需要在 Blender 中完整还原渲染图光影材质时，才需要按下方步骤补齐。

---

## 📥 下载与放置步骤

1. 打开 Poly Haven 资源页面：**[Pergola Walkway HDRI • Poly Haven](https://polyhaven.com/zh/a/pergola_walkway)**
2. 选择规格 **`4K`** + 格式 **`EXR`** 点击下载（也可直接使用官方直链下载）：
   - 直链下载：<https://dl.polyhaven.org/file/ph-assets/HDRIs/exr/4k/pergola_walkway_4k.exr>
3. 将下载好的文件放入当前 `Model/textures/` 目录下，确保文件名保持为：

```text
Model/
├── model-blender-res.blend
└── textures/
    ├── 8d1633a87402a765b459fc35e493106d.png
    ├── ArmsTexD.jpg
    ├── pergola_walkway.md
    └── pergola_walkway_4k.exr   <-- 放在这里
```

放入后再用 Blender 打开 [model-blender-res.blend](../model-blender-res.blend)，软件会自动关联该环境贴图（如果已经打开了工程，可在菜单栏依次点击 `File -> External Data -> Find Missing Files` 并选中当前 `textures` 文件夹即可）。

---

## 📄 授权说明

- **资源名称**：Pergola Walkway HDRI
- **来源**：[Poly Haven](https://polyhaven.com/zh/a/pergola_walkway)
- **开源协议**：[CC0 1.0 Universal (Public Domain)](https://polyhaven.com/license)
