# 第二课：Anaconda 环境搭建与 VSCode Python 编程基础完整教程

## 📖 目录
- [课程定位](#课程定位)
- [课前准备](#课前准备)
- [模块一Anaconda-Python环境搭建](#模块一anaconda-python环境搭建)
- [模块二VSCode-Python编程基础教学](#模块二vscode-python编程基础教学)
- [模块三综合实操与成果验收](#模块三综合实操与成果验收)
- [截图清单建议](#截图清单建议)
- [常见问题](#常见问题)

---

## 课程定位

本课是面向初学者的 Python 入门实践课，重点解决三个问题：

1. 如何在 Windows 上正确安装并管理 Python 环境
2. 如何使用 VSCode 进行 Python 编写、调试与代码管理
3. 如何通过一组渐进式练习，完成从“能运行代码”到“能独立完成小任务”的过渡

**本课学习目标：**
- 能在 Windows 上完成 Anaconda 安装与验证
- 能创建并切换独立的 Python 虚拟环境
- 能在 VSCode 中配置 Python 开发环境
- 能完成基础 Python 练习并验证运行结果
- 能提交一份完整的第二课学习成果

---

## 课前准备

### 软件清单

| 软件 | 用途 | 建议版本 |
|------|------|----------|
| Anaconda | Python 环境与包管理 | 最新稳定版 |
| VSCode | 代码编辑与调试 | 最新稳定版 |
| Windows 10/11 | 操作系统 | 64 位 |

### 建议目录

建议在电脑中创建统一学习目录：

```text
D:\PythonCourse\
├── lesson2\
├── lesson2_project\
└── screenshots\
```

### 课堂命名规范

本课统一使用以下环境名和目录名，便于老师批改：

- conda 环境名：`py-ai-lesson2`
- 项目目录名：`lesson2_project`

### 截图说明

本教程中用如下格式提示截图位置，授课时请按提示截图并插入文档或课件：

- `[截图 M1-01]` 表示模块一第 1 张截图
- `[截图 M2-03]` 表示模块二第 3 张截图

---

## 模块一：Anaconda Python环境搭建

## 1.1 什么是 Anaconda

Anaconda 是一个面向数据分析与科学计算的 Python 发行版，它自带：

- Python 解释器
- conda 包管理工具
- 虚拟环境管理能力
- 常见科学计算库安装能力
- 图形化管理工具 Anaconda Navigator

对于初学者来说，它的优势是：

- 安装简单
- 环境隔离清晰
- 常见包安装稳定
- 同时支持命令行和图形界面

---

## 1.2 下载 Anaconda

### 操作步骤

1. 打开浏览器，访问 Anaconda 官网  
   `https://www.anaconda.com/download`
2. 选择 **Windows**
3. 选择 **64-Bit Graphical Installer**
4. 点击下载

### 截图演示

- `[截图 M1-01]` Anaconda 官网下载页
- `[截图 M1-02]` Windows 下载按钮位置

### 操作验证检查点

- 下载到本地的安装文件扩展名应为 `.exe`
- 文件名中通常包含 `Anaconda3`

---

## 1.3 安装 Anaconda

### 安装步骤

1. 双击下载好的安装程序
2. 点击 `Next`
3. 阅读协议后点击 `I Agree`
4. 选择安装范围：推荐 `Just Me`
5. 选择安装路径，建议保持默认，或安装到：

```text
D:\Anaconda3
```

6. 安装选项建议：
   - `Add Anaconda to my PATH environment variable`：**不要勾选**
   - `Register Anaconda as my default Python 3.x`：**建议勾选**
7. 点击 `Install`
8. 安装完成后点击 `Finish`

### 关键配置参数说明

| 选项 | 建议 | 原因 |
|------|------|------|
| Just Me | 推荐 | 避免系统范围权限问题 |
| 安装路径 | 英文目录 | 避免中文路径兼容问题 |
| Add to PATH | 不勾选 | 防止污染系统环境变量 |
| Register as default Python | 可勾选 | 让 VSCode 更容易识别 Python |

### 截图演示

- `[截图 M1-03]` 安装协议界面
- `[截图 M1-04]` 安装路径选择界面
- `[截图 M1-05]` 高级安装选项界面
- `[截图 M1-06]` 安装完成界面

### 操作验证检查点

安装完成后，在开始菜单应该能看到以下应用：

- Anaconda Navigator
- Anaconda Prompt

---

## 1.4 验证 Anaconda 是否安装成功

### 方法一：使用 Anaconda Prompt

1. 打开开始菜单
2. 搜索并打开 `Anaconda Prompt`
3. 输入以下命令：

```bash
conda --version
python --version
```

### 预期结果

你应该能看到类似输出：

```bash
conda 24.x.x
Python 3.11.x
```

### 截图演示

- `[截图 M1-07]` Anaconda Prompt 中版本验证结果

### 操作验证检查点

- `conda --version` 能正常显示版本号
- `python --version` 能正常显示版本号

---

## 1.5 使用 conda 创建虚拟环境

### 为什么要创建虚拟环境

虚拟环境可以让不同课程、不同项目使用不同版本的 Python 和依赖包，互不影响。

### 创建环境命令

在 `Anaconda Prompt` 中执行：

```bash
conda create -n py-ai-lesson2 python=3.11 -y
```

### 激活环境

```bash
conda activate py-ai-lesson2
```

### 查看已有环境

```bash
conda env list
```

### 预期结果

激活成功后，命令行前面会出现环境名：

```bash
(py-ai-lesson2) C:\Users\你的用户名>
```

### 关键配置参数说明

| 参数 | 含义 |
|------|------|
| `conda create` | 创建新环境 |
| `-n py-ai-lesson2` | 指定环境名称 |
| `python=3.11` | 指定 Python 版本 |
| `-y` | 自动确认安装 |
| `conda activate` | 激活环境 |

### 截图演示

- `[截图 M1-08]` 创建环境命令执行过程
- `[截图 M1-09]` 激活环境后的终端状态

### 操作验证检查点

- `conda env list` 中能看到 `py-ai-lesson2`
- 当前终端前缀显示 `(py-ai-lesson2)`

---

## 1.6 管理 Python 版本

### 查看当前 Python 版本

```bash
python --version
```

### 创建其他 Python 版本环境

如果你需要额外测试 Python 3.10，可以执行：

```bash
conda create -n py310-demo python=3.10 -y
```

### 删除不再使用的环境

```bash
conda remove -n py310-demo --all -y
```

### 操作验证检查点

- 能说清楚“系统 Python”和“虚拟环境 Python”的区别
- 能独立完成环境创建、切换、删除

---

## 1.7 安装常用科学计算包

在激活 `py-ai-lesson2` 环境后执行：

```bash
conda install numpy pandas matplotlib -y
```

### 分包说明

| 包名 | 用途 |
|------|------|
| `numpy` | 数值计算 |
| `pandas` | 表格与数据分析 |
| `matplotlib` | 绘图 |

### 验证安装

```bash
python
```

进入 Python 解释器后输入：

```python
import numpy
import pandas
import matplotlib
print("安装成功")
```

退出解释器：

```python
exit()
```

### 截图演示

- `[截图 M1-10]` conda 安装科学计算包
- `[截图 M1-11]` import 验证成功

### 操作验证检查点

- 三个核心包都能成功导入
- 不出现 `ModuleNotFoundError`

---

## 1.8 使用 Anaconda Navigator 管理环境

### 打开 Navigator

从开始菜单打开 `Anaconda Navigator`

### 图形化操作

1. 点击左侧 `Environments`
2. 点击 `Create`
3. 环境名填写：`py-ai-lesson2-gui`
4. 选择 Python 版本
5. 点击 `Create`

### 图形化安装包

1. 选择刚创建的环境
2. 搜索 `numpy`
3. 勾选后点击 `Apply`

### 截图演示

- `[截图 M1-12]` Navigator 主界面
- `[截图 M1-13]` Environments 页面
- `[截图 M1-14]` 图形化安装 numpy

### 操作验证检查点

- 能通过 Navigator 新建环境
- 能通过 Navigator 安装至少一个包

---

## 1.9 使用 conda 命令行管理环境

### 常用命令总表

```bash
conda env list
conda activate py-ai-lesson2
conda deactivate
conda list
conda install numpy pandas matplotlib -y
conda remove 包名
conda remove -n 环境名 --all -y
```

### 推荐课堂说明

- Navigator 适合第一次上手
- conda 命令行适合长期开发
- 以后大部分技术文档默认使用命令行方式

---

## 模块二：VSCode Python编程基础教学

## 2.1 安装 VSCode

### 操作步骤

1. 打开浏览器，访问  
   `https://code.visualstudio.com/`
2. 下载 Windows 版本
3. 双击安装
4. 建议勾选以下选项：
   - `Add "Open with Code" action to Windows Explorer file context menu`
   - `Add to PATH`
   - `Register Code as an editor for supported file types`

### 截图演示

- `[截图 M2-01]` VSCode 官网下载页
- `[截图 M2-02]` VSCode 安装选项页

### 操作验证检查点

- 开始菜单能找到 VSCode
- 双击文件夹时可选择用 VSCode 打开

---

## 2.2 安装 Python 开发扩展

### 必装扩展

在 VSCode 左侧 `Extensions` 中搜索并安装：

1. `Python`（Microsoft）
2. `Pylance`

### 扩展作用说明

| 扩展 | 作用 |
|------|------|
| Python | Python 语言支持、运行、调试 |
| Pylance | 智能提示、类型分析 |

### 截图演示

- `[截图 M2-03]` 扩展市场安装 Python
- `[截图 M2-04]` 扩展市场安装 Pylance

### 操作验证检查点

- 扩展界面显示 `Installed`
- 新建 `.py` 文件后能看到 Python 语言高亮

---

## 2.3 在 VSCode 中选择 Python 解释器

### 操作步骤

1. 打开 VSCode
2. 选择 `File -> Open Folder`
3. 打开你的课程目录 `lesson2_project`
4. 按 `Ctrl + Shift + P`
5. 搜索 `Python: Select Interpreter`
6. 选择 `py-ai-lesson2` 对应的解释器

### 验证方法

新建 `check_env.py` 文件，输入：

```python
import sys
print(sys.executable)
print(sys.version)
```

运行后，应显示 Anaconda 环境中的 Python 路径。

### 截图演示

- `[截图 M2-06]` 选择解释器界面
- `[截图 M2-07]` 运行 check_env.py 结果

### 操作验证检查点

- 能正确选中 `py-ai-lesson2`
- 输出路径中包含 `Anaconda` 或环境名

---

## 2.4 安装代码格式化和 Linting 工具

在激活环境后执行：

```bash
conda activate py-ai-lesson2
pip install black pylint
```

### 推荐 VSCode 设置

打开 `settings.json`，加入以下配置：

```json
{
  "editor.formatOnSave": true,
  "editor.tabSize": 4,
  "python.defaultInterpreterPath": "",
  "python.formatting.provider": "none",
  "[python]": {
    "editor.defaultFormatter": "ms-python.black-formatter"
  },
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.analysis.autoImportCompletions": true,
  "python.analysis.typeCheckingMode": "basic"
}
```

### 配置说明

| 配置项 | 说明 |
|--------|------|
| `editor.formatOnSave` | 保存时自动格式化 |
| `editor.defaultFormatter` | 指定 Python 默认格式化器 |
| `python.linting.enabled` | 启用语法与规范检查 |
| `python.linting.pylintEnabled` | 启用 pylint |
| `python.analysis.autoImportCompletions` | 自动导入提示 |

### 截图演示

- `[截图 M2-08]` settings.json 配置界面
- `[截图 M2-09]` 保存自动格式化效果

### 操作验证检查点

- 保存 Python 文件后自动整理缩进
- 错误代码行出现波浪线提示

---

## 2.5 智能提示配置与使用

### 演示代码

新建 `autocomplete_demo.py`：

```python
import pandas as pd

data = {
    "name": ["Alice", "Bob", "Cindy"],
    "score": [88, 92, 95]
}

df = pd.DataFrame(data)
print(df.head())
```

当你输入 `df.` 时，VSCode 应出现属性和方法提示。

### 截图演示

- `[截图 M2-10]` `df.` 智能提示下拉框

### 操作验证检查点

- 出现 `head`、`describe`、`columns` 等提示项

---

## 2.6 Python 代码调试技巧

### 调试示例代码

新建 `debug_demo.py`：

```python
numbers = [2, 4, 6, 8]
total = 0

for number in numbers:
    total += number

average = total / len(numbers)
print("平均值是：", average)
```

### 调试步骤

1. 在 `total += number` 行左侧单击，设置断点
2. 点击左侧 `Run and Debug`
3. 选择 `Python File`
4. 点击开始调试或按 `F5`
5. 观察：
   - Variables 面板
   - Call Stack
   - Debug Console

### 建议讲解的调试技巧

- `F5`：开始调试
- `F10`：单步跳过
- `F11`：单步进入
- `Shift + F5`：停止调试

### 截图演示

- `[截图 M2-11]` 设置断点
- `[截图 M2-12]` 调试变量面板

### 操作验证检查点

- 能成功停在断点
- 能看到 `total` 的值逐步变化

---

## 2.7 渐进式编程练习

## 练习1：变量与数据类型

### 目标

认识字符串、整数、浮点数、布尔值。

### 代码

```python
name = "Zhangsan"
age = 23
height = 172.5
is_student = True

print("姓名：", name)
print("年龄：", age)
print("身高：", height)
print("是否是学生：", is_student)
print(type(name))
print(type(age))
```

### 预期结果

```text
姓名： Zhangsan
年龄： 23
身高： 172.5
是否是学生： True
<class 'str'>
<class 'int'>
```

### 验证检查点

- 学生能修改自己的姓名和年龄
- 运行结果与变量类型一致

---

## 练习2：控制流程

### 目标

掌握 `if`、`elif`、`else`。

### 代码

```python
score = 86

if score >= 90:
    level = "优秀"
elif score >= 75:
    level = "良好"
elif score >= 60:
    level = "及格"
else:
    level = "需要努力"

print("分数：", score)
print("评价：", level)
```

### 预期结果

```text
分数： 86
评价： 良好
```

### 验证检查点

- 学生能将 `score` 改成不同值测试不同分支
- 能解释程序为何输出不同评价

---

## 练习3：函数定义

### 目标

掌握函数定义、参数、返回值。

### 代码

```python
def calculate_total(price, count):
    total = price * count
    return total


book_price = 39.8
book_count = 3
result = calculate_total(book_price, book_count)

print("总金额：", result)
```

### 预期结果

```text
总金额： 119.4
```

### 验证检查点

- 学生能自己更改 `price` 和 `count`
- 学生能说出 `return` 的作用

---

## 练习4：文件操作

### 目标

掌握最基本的文件写入与读取。

### 代码

```python
file_name = "student_note.txt"

with open(file_name, "w", encoding="utf-8") as file:
    file.write("姓名：张三\n")
    file.write("学号：2023001\n")
    file.write("课程：Python 第二课\n")

with open(file_name, "r", encoding="utf-8") as file:
    content = file.read()

print(content)
```

### 预期结果

```text
姓名：张三
学号：2023001
课程：Python 第二课
```

### 验证检查点

- 当前目录中能生成 `student_note.txt`
- 文件内容和终端输出一致

---

## 模块三：综合实操与成果验收

## 3.1 综合实操作业

请学生独立完成以下任务：

### 任务A：完成环境搭建

- 安装 Anaconda
- 创建 `py-ai-lesson2` 环境
- 安装 `numpy`、`pandas`、`matplotlib`

### 任务B：完成 VSCode 配置

- 安装 Python、Pylance 扩展
- 选择正确解释器
- 完成格式化与 Linting 配置

### 任务C：完成 4 个基础练习

- 变量与数据类型
- 控制流程
- 函数定义
- 文件操作

### 任务D：完成调试与运行验证

- 至少完成 1 次断点调试
- 至少完成 1 次程序运行结果截图
- 能向老师解释 1 个 Python 文件的运行结果

---

## 3.2 学生成果目录建议

```text
lesson2_project/
├── check_env.py
├── autocomplete_demo.py
├── debug_demo.py
├── exercise1_variables.py
├── exercise2_if.py
├── exercise3_function.py
├── exercise4_file.py
└── student_note.txt
```

---

## 3.3 操作验证总检查点

### 环境检查

- [ ] 能打开 Anaconda Prompt
- [ ] `conda --version` 正常
- [ ] `conda env list` 中有 `py-ai-lesson2`
- [ ] `import numpy` 不报错
- [ ] `import pandas` 不报错
- [ ] `import matplotlib` 不报错

### VSCode 检查

- [ ] 已安装 Python 扩展
- [ ] 已安装 Pylance 扩展
- [ ] 已正确选择 `py-ai-lesson2` 解释器
- [ ] 保存 Python 文件时能自动格式化
- [ ] 调试时能命中断点

### 编程练习检查

- [ ] 4 个练习都能运行
- [ ] 能看懂输出结果
- [ ] 文件操作练习能成功生成文本文件

---

## 3.4 成果验收标准

### 合格标准

满足以下条件即可判定为“完成本课”：

1. 成功创建并激活 `py-ai-lesson2` 环境
2. 成功安装 numpy、pandas、matplotlib
3. 在 VSCode 中完成解释器选择
4. 能运行 4 个练习文件
5. 能完成一次断点调试
6. 能清晰说明至少 1 个练习文件的运行结果

### 优秀标准

除合格标准外，再额外满足以下任意 3 条：

- 能解释 conda 环境的作用
- 能独立安装一个新 Python 包
- 能自己编写一个函数并调用
- 能读懂 pylint 提示并修复问题
- 能用 matplotlib 修改图表标题、颜色或标签

---

## 截图清单建议

| 编号 | 截图内容 | 建议文件名 |
|------|----------|------------|
| M1-01 | Anaconda 下载页 | `m1_01_anaconda_download.png` |
| M1-05 | 安装高级选项 | `m1_05_install_options.png` |
| M1-09 | 激活 conda 环境 | `m1_09_activate_env.png` |
| M1-11 | 科学计算包导入成功 | `m1_11_import_success.png` |
| M2-03 | Python 扩展安装 | `m2_03_python_extension.png` |
| M2-06 | VSCode 选择解释器 | `m2_06_select_interpreter.png` |
| M2-11 | 断点调试界面 | `m2_11_debug.png` |
| M2-12 | 运行结果验证 | `m2_12_run_result.png` |

建议统一保存在：

```text
documents/screenshots/lesson2/
```

---

## 常见问题

### Q1：为什么我输入 `conda` 提示不是内部命令？

A：通常是因为没有通过 `Anaconda Prompt` 打开，或者安装未成功。请先使用开始菜单中的 `Anaconda Prompt`。

### Q2：为什么 VSCode 找不到我创建的环境？

A：通常是因为环境未激活或 VSCode 尚未刷新。可先关闭 VSCode，再重新打开并执行 `Python: Select Interpreter`。

### Q3：为什么 `import pandas` 报错？

A：说明当前解释器不是 `py-ai-lesson2`，或者该环境里还没安装 pandas。

### Q4：为什么代码可以运行，但 VSCode 没有智能提示？

A：通常是因为没有安装 Pylance，或者当前没有正确选择 Python 解释器。请先检查扩展安装状态，再重新执行 `Python: Select Interpreter`。

---

## 教师使用建议

- 第一轮演示只讲操作，不讲太多底层原理
- 第二轮再解释环境、解释器、扩展、调试的概念
- 课堂上优先保障所有学生先把环境跑通
- 编程练习按“看老师演示 → 自己修改参数 → 独立重写”三步推进

---

祝大家顺利完成第二课学习任务。
