# 位与位运算
## 位
众所周知，在常见的计算机结构中，数据均以「位(bit)」存储。为了便于管理，每 8 位组成 1 个「字节(byte)」。使用前置修饰符，如 `K` —— 组成 `KB` 表示 $2^10$ byte 等。在硬件中，数据存储可能存在分区、分块等措施，此处不进行阐述。

利用 `bitstring` 函数，你可以方便地列出数字的各位数据
```jl
julia> bitstring(31)
"0000000000000000000000000000000000000000000000000000000000011111"
```

## 无符号整数
无符号整数的存储方式是最容易理解的：即二进制数。
以 $22=(10110)_2$ 为例：
| 单位数值 | 权值 | 结果 |
| --- | --- | --- |
| 0 | 1 | 0 |
| 1 | 2 | 2 |
| 1 | 4 | 4 |
| 0 | 8 | 0 |
| 1 | 16 | 16 |

## 带符号整数
参阅[此文](https://www.luogu.com.cn/blog/cdcq/ExplainationOnComplement)

## 浮点数
浮点数的实现较为复杂，你将会在对应章节读到部分内容

## 位运算
在阅读[布尔逻辑](bool_logic.md)后，你应该可以推断出：形如“按位与”的运算，就是对于每一位，分别进行与运算
```insert-fill
content = "17&5 = ?"
ans = "1"
```

## 杂项
关于硬件上的具体实现，请参阅[模拟电路](https://www.bilibili.com/video/BV1774114798)、[数字电路](https://www.bilibili.com/video/BV1Hi4y1t7zY)与[《从0到1设计一台计算机》](https://www.bilibili.com/video/BV1wi4y157D3)，也可以学习微电子。

你或许已经意识到，形如加法的运算可以使用位运算*模拟*。你可以尝试[此题](https://hydro.ac/p/H1087)
