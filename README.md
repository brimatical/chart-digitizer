# Chart Digitizer - 图表数据提取工具

A browser-based tool for extracting numerical data from chart images (bar charts, line charts, etc.) captured from scientific literature. Inspired by [WebPlotDigitizer](https://automeris.io/WebPlotDigitizer/).

一个基于浏览器的图表数据提取工具，可从文献截图中精准提取柱状图、折线图等图表的数据。

**Live Demo / 在线使用：[https://brimatical.github.io/chart-digitizer/](https://brimatical.github.io/chart-digitizer/)**

---

## Features / 功能特点

- **Image Input** — Upload, drag-and-drop, or paste (Ctrl+V) chart screenshots directly  
  支持上传、拖拽、Ctrl+V 粘贴图表截图

- **4-Point Axis Calibration** — Click 4 known points on the axes (X₁, X₂, Y₁, Y₂) and enter their values to establish a pixel-to-value mapping  
  4 点标定法：点击坐标轴上 4 个已知刻度点并输入数值，建立像素→数值的精确映射

- **Precision Picking** — Use arrow keys for pixel-by-pixel cursor adjustment; Shift+Arrow for 5px fast move  
  逐像素精确采点：方向键微调，Shift+方向键快移

- **Real-time Magnifier** — 2x–32x zoom magnifier panel with customizable crosshair color and opacity  
  实时放大镜：2x~32x 可调，十字准线颜色和透明度可自定义

- **Extended Crosshair** — Full-width/height crosshair overlay on the main canvas, toggleable with `C` key  
  全幅十字准线：覆盖整张图，按 `C` 键开关

- **Data Export** — Export collected data points as CSV  
  数据导出：一键导出 CSV

- **Privacy** — 100% client-side. No image is uploaded to any server. Everything runs in your browser.  
  隐私安全：纯前端运行，图片不会上传到任何服务器

## How to Use / 使用方法

### Step 1: Upload Image / 上传图片

Upload a chart screenshot via file picker, drag-and-drop, or clipboard paste (Ctrl+V).

### Step 2: Calibrate Axes / 标定坐标轴

Click **"开始标定"** (Start Calibration) and follow the 4-step guided process:

| Point | Description |
|-------|-------------|
| **X₁** | A known point on the X-axis (e.g., left tick mark). Enter its X value. |
| **X₂** | Another known point on the X-axis (e.g., right tick mark). Enter its X value. |
| **Y₁** | A known point on the Y-axis (e.g., bottom tick mark). Enter its Y value. |
| **Y₂** | Another known point on the Y-axis (e.g., top tick mark). Enter its Y value. |

For each point:
1. **Click** to place the marker on the chart
2. Use **Arrow Keys** to fine-tune position (pixel-by-pixel precision)
3. Press **Enter** to confirm position
4. Type the axis value in the right panel, press **Enter**

After all 4 points, click **"确认标定"** (Confirm Calibration).

### Step 3: Collect Data Points / 采集数据点

Click on data points in the chart. The real-world coordinates are calculated automatically based on your calibration.

### Step 4: Export / 导出

Click **"导出 CSV"** to download your data.

## Keyboard Shortcuts / 快捷键

| Key | Action |
|-----|--------|
| `Click` | Place calibration point / Collect data point |
| `↑ ↓ ← →` | Move cursor by 1 pixel |
| `Shift + Arrow` | Move cursor by 5 pixels |
| `Enter` | Confirm calibration point position |
| `Space` | Collect data point at keyboard cursor |
| `Delete` | Remove last data point |
| `C` | Toggle extended crosshair |
| `+` / `-` | Zoom magnifier in / out |

## Tech Stack / 技术栈

- Pure HTML + CSS + JavaScript (single file, no dependencies)
- Canvas API for image rendering and annotation
- Runs entirely in the browser

## License

MIT

## Acknowledgements

Inspired by [WebPlotDigitizer](https://automeris.io/WebPlotDigitizer/) by Ankit Rohatgi.
