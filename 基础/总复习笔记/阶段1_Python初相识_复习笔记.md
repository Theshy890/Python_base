# 阶段1 Python初相识 完整复习笔记

> 阶段目标：能独立写出Python程序，理解变量、数据类型、输入输出
> 在AI应用开发中的作用：所有代码的"识字课"，调用AI接口、处理数据都离不开这些基础元素

---

## 一、本阶段核心知识点清单

### 🟢 必背知识点（必须熟练掌握）

| 编号 | 知识点 | 核心记忆点 |
|------|--------|-----------|
| 1.1 | print() 打印输出 | `print()` 让程序"说话"；文字加引号，数字不加引号；多内容用逗号分隔 |
| 1.2 | 注释 | `#` 单行注释；`"""` 多行注释；注释是给"人"看的，Python会忽略 |
| 1.3 | 变量 | `变量名 = 值`；变量名只能由字母、数字、下划线组成，不能以数字开头，不能是关键字 |
| 1.4 | 四大基本数据类型 | `int` 整数、`float` 浮点数、`str` 字符串、`bool` 布尔值（True/False） |
| 1.5 | 输入 input() | `input()` 获取用户输入，得到的是字符串；需要用类型转换才能当数字用 |
| 1.6 | 类型转换 | `int()`、`float()`、`str()`、`bool()`；转换失败会报错 |
| 1.7 | 基础运算符 | `+ - * / // % **`；注意 `//` 整除、`%` 取余、`**` 乘方 |
| 1.8 | f-string 格式化字符串 | `f"文字{变量}文字"`，把变量嵌入字符串中 |
| 1.9 | 字符串基础方法 | `split()` 拆分、`join()` 拼接、`replace()` 替换、`strip()` 去空白、`upper()`/`lower()` 大小写 |

### 🟡 拓展知识点（补充理解，提升代码质量）

| 编号 | 知识点 | 核心记忆点 |
|------|--------|-----------|
| 1.10 | PEP8 代码规范 | 变量名小写加下划线、运算符两边加空格、每行不超过79字符 |
| 1.11 | 完整运算符体系 | 算术运算符、比较运算符（`== != > < >= <=`）、赋值运算符（`+= -=`）、逻辑运算符（`and or not`） |
| 1.12 | 字符串完整体系 | 索引 `s[0]`、切片 `s[1:4]`、字符串判断方法（`isdigit()`、`startswith()` 等） |
| 1.13 | 报错基础理论 | `SyntaxError` 语法错误、`NameError` 名字未定义、`TypeError` 类型错误、`ValueError` 值错误 |
| 1.14 | 浮点数精度 | `0.1 + 0.2 != 0.3`；用 `round()`、`math.isclose()` 或 `Decimal` 解决 |
| 1.15 | 编码基础 | 计算机用二进制存储信息；`UTF-8` 是常用中文编码；乱码通常是编码不一致导致 |

---

## 二、核心代码示例（仅本阶段语法，无超纲内容）

### 1. print() 打印输出
```python
# 打印文字
print("Hello, Python!")

# 打印多个内容，自动用空格分隔
name = "小明"
age = 20
print("姓名：", name, "年龄：", age)

# 打印日志（AI调试常用）
print("[2026-07-18] 任务：文本清洗 | 状态：开始执行")
```

### 2. 变量与数据类型
```python
# 变量赋值
article_title = "AI入门指南"    # 字符串 str
word_count = 1500                # 整数 int
price = 0.002                    # 浮点数 float
is_published = True              # 布尔值 bool

# 查看类型
print(type(article_title))       # <class 'str'>
print(type(word_count))          # <class 'int'>
```

### 3. 输入与类型转换
```python
# 获取用户输入（都是字符串）
user_input = input("请输入一段文字：")

# 统计字数
print("您输入了", len(user_input), "个字符")

# 如果需要数字，要转换
calls = input("请输入调用次数：")
calls = int(calls)               # 字符串转整数
cost = calls * 0.002
print("预计费用：", cost, "元")
```

### 4. 基础运算符
```python
a = 17
b = 5

print(a + b)    # 22
print(a - b)    # 12
print(a * b)    # 85
print(a / b)    # 3.4
print(a // b)   # 3  整除
print(a % b)    # 2  取余
print(a ** b)   # 1419857  乘方
```

### 5. f-string 格式化字符串
```python
task_name = "文本摘要"
confidence = 0.95

# 把变量嵌入字符串
result = f"任务：{task_name} | 置信度：{confidence}"
print(result)

# AI场景：输出处理结果
article_count = 100
print(f"已处理 {article_count} 篇文章")
```

### 6. 字符串基础方法
```python
article = "Python is great. Python is easy to learn."

# split：按指定内容拆分
words = article.split(" ")
print(words)

# join：用指定内容拼接列表（字符串）
sentence = " ".join(words)
print(sentence)

# replace：替换内容
cleaned = article.replace("Python", "AI")
print(cleaned)

# strip：去掉首尾空白
text = "  hello world  "
print(text.strip())

# upper/lower：大小写转换
print("hello".upper())    # HELLO
print("WORLD".lower())    # world
```

### 7. 字符串索引与切片
```python
text = "Python"

print(text[0])     # P，第一个字符
print(text[-1])    # n，最后一个字符
print(text[0:3])   # Pyt，从0开始取3个字符
print(text[2:])    # thon，从2取到末尾
```

### 8. 字符串判断方法
```python
print("123".isdigit())            # True
print("abc".isalpha())            # True
print("abc123".isalnum())         # True
print("Hello".startswith("He"))   # True
print("Hello".endswith("lo"))     # True
```

### 9. 浮点数精度与 Decimal
```python
# 普通浮点数有精度问题
print(0.1 + 0.2)        # 0.30000000000000004

# 方案1：round四舍五入
print(round(0.1 + 0.2, 2))   # 0.3

# 方案2：Decimal精确计算
from decimal import Decimal
fee1 = Decimal("0.1")
fee2 = Decimal("0.2")
print(fee1 + fee2)      # 0.3
```

---

## 三、高频易错点 & 踩坑总结

| 易错点 | 错误示例 | 正确写法 | 知识点 |
|--------|---------|---------|--------|
| 文字没加引号 | `print(你好)` | `print("你好")` | print |
| 变量名以数字开头 | `1name = "a"` | `name1 = "a"` | 变量命名 |
| 用中文括号/引号 | `print（"你好"）` | `print("你好")` | 语法规范 |
| input得到的是字符串 | `age = input() + 5` | `age = int(input()) + 5` | 类型转换 |
| `//` 和 `/` 混淆 | `5 / 2` 以为是 2 | `5 // 2` 才是 2 | 运算符 |
| 字符串拼接数字报错 | `"费用" + 100` | `"费用" + str(100)` | 类型转换 |
| split找不到分隔符 | `"abc".split(",")` | 返回 `["abc"]` | split方法 |
| join语法写反 | `words.join(" ")` | `" ".join(words)` | join方法 |
| 浮点数直接比较 | `0.1 + 0.2 == 0.3` | `round(0.1+0.2, 2) == 0.3` | 浮点精度 |
| Decimal传浮点数 | `Decimal(0.1)` | `Decimal("0.1")` | Decimal |
| 索引越界 | `"abc"[5]` | `"abc"[2]` 才是最后一个 | 字符串索引 |

---

## 四、配套练习题（自测用）

### 练习 1：变量与输出
写出代码，定义变量 `user_name = "张三"`，`score = 85`，并用 f-string 输出 `"张三的得分是85分"`。

<details>
<summary>答案</summary>

```python
user_name = "张三"
score = 85
print(f"{user_name}的得分是{score}分")
```
</details>

### 练习 2：类型转换
用户输入一个数字字符串，输出它的平方。

<details>
<summary>答案</summary>

```python
num = input("请输入一个数字：")
num = float(num)
print("平方是：", num * num)
```
</details>

### 练习 3：字符串处理
给定文本 `"AI 正在改变 世界"`，请去掉所有空格后输出。

<details>
<summary>答案</summary>

```python
text = "AI 正在改变 世界"
cleaned = text.replace(" ", "")
print(cleaned)
```
</details>

### 练习 4：浮点数精度
计算 `0.1 + 0.2 + 0.15` 的总和，并保留 2 位小数输出。

<details>
<summary>答案</summary>

```python
from decimal import Decimal
a = Decimal("0.1")
b = Decimal("0.2")
c = Decimal("0.15")
total = a + b + c
print(round(total, 2))
```
</details>

### 练习 5：综合应用
用户输入一段文字，输出这段文字的字数、第一个字和最后一个字。

<details>
<summary>答案</summary>

```python
text = input("请输入一段文字：")
print("字数：", len(text))
print("第一个字：", text[0])
print("最后一个字：", text[-1])
```
</details>

---

## 五、AI开发实战应用场景

### 场景 1：处理 AI 返回的文本
调用大模型后，返回的是一段字符串。阶段1的知识让你能：
- 用 `len()` 统计回复长度
- 用 `split()` 按句号/换行拆分句子
- 用 `replace()` 清理特殊符号
- 用 `strip()` 去掉多余空白

### 场景 2：计算 API 调用费用
AI接口通常按调用次数或 Token 数计费：
- 用 `input()` 获取调用次数
- 用 `int()` 转换类型
- 用 `Decimal` 精确计算总费用，避免浮点误差

### 场景 3：格式化输出结果
- 用 f-string 把模型名称、置信度、处理时间组合成可读报告
- 用 `print()` 输出调试日志，追踪程序执行流程

### 场景 4：数据清洗前置检查
- 用 `isdigit()` 判断用户输入是否为纯数字
- 用 `startswith()`/`endswith()` 判断文件名后缀、URL协议等
- 用大小写转换统一文本格式

---

**复习建议**：把本笔记中的代码示例全部手敲一遍，尤其是 `split/join` 和 `Decimal` 部分，这两块最容易在后续 AI 项目实战中用到。
