# 内容  

- [内容](#内容)
  - [1. 综述](#1-综述)
    - [1.1 范围](#11-范围)
    - [1.2 目的](#12-目的)
    - [1.3 内容简介](#13-内容简介)
    - [1.4 特定术语](#14-特定术语)
    - [1.5 此标准中的约定用法](#15-此标准中的约定用法)
    - [1.6 语法描述](#16-语法描述)
    - [1.7 此标准中使用的颜色](#17-此标准中使用的颜色)
    - [1.8 此标准的内容](#18-此标准的内容)
    - [1.9 弃用的 clause](#19-弃用的-clause)
    - [1.10 例子](#110-例子)
    - [预备知识](#预备知识)
  - [2. Normative references](#2-normative-references)
  - [3. 设计和验证的构造块](#3-设计和验证的构造块)
    - [3.1 概述](#31-概述)
    - [3.2 设计元素](#32-设计元素)
    - [3.3 Modules](#33-modules)
    - [3.4 Programs](#34-programs)
    - [3.5 Interfaces](#35-interfaces)
    - [3.6 Checkers](#36-checkers)
    - [3.7 Primitives](#37-primitives)
    - [3.8 Subroutines](#38-subroutines)
    - [3.9 Packages](#39-packages)
    - [3.10 Configurations](#310-configurations)
    - [3.11 Overview of hierarchy](#311-overview-of-hierarchy)
    - [3.12 Compilation and elaboration](#312-compilation-and-elaboration)
    - [3.13 Name spaces](#313-name-spaces)
    - [3.14 Simulation time units and precison](#314-simulation-time-units-and-precison)
  - [4. 调度语义](#4-调度语义)
  - [5. 词法约定](#5-词法约定)
  - [6. 数据类型](#6-数据类型)
  - [7. 聚合数据类型](#7-聚合数据类型)
    - [7.1 概述](#71-概述)
    - [7.2 结构体](#72-结构体)
      - [7.2.1 Packed 结构体](#721-packed-结构体)
    - [7.2.2 结构体赋值](#722-结构体赋值)
    - [7.3 联合体(Union)](#73-联合体union)
      - [7.3.1 Packed 联合体](#731-packed-联合体)
      - [7.3.1 Tagged 联合体](#731-tagged-联合体)
  - [8. 类](#8-类)
  - [9. Processes](#9-processes)
  - [10. Assignment statement](#10-assignment-statement)
  - [11. 操作符和表达式](#11-操作符和表达式)
  - [12. Procedual programming statements](#12-procedual-programming-statements)
  - [13. 任务和函数(子任务)](#13-任务和函数子任务)
  - [14. 时钟块](#14-时钟块)
  - [15. 跨 Process 的同步和通信](#15-跨-process-的同步和通信)
  - [16. Assertions](#16-assertions)
  - [17. Checkers](#17-checkers)
  - [18. 产生受约束的随机值](#18-产生受约束的随机值)
  - [19. 功能覆盖率](#19-功能覆盖率)
  - [20. Utility 系统任务和系统函数](#20-utility-系统任务和系统函数)
  - [21. 输入/输出系统任务和函数](#21-输入输出系统任务和函数)
  - [22. Compiler directives](#22-compiler-directives)
  - [23. 模块和层级结构](#23-模块和层级结构)
  - [24. Programs](#24-programs)
  - [25. Interfaces](#25-interfaces)
  - [26. Packages](#26-packages)
  - [27. Generate 结构](#27-generate-结构)
  - [28. 门级和开关级建模](#28-门级和开关级建模)
  - [29. 用户原语定义](#29-用户原语定义)
  - [30. Specify blocks](#30-specify-blocks)
  - [31. Timing checks](#31-timing-checks)
  - [32. 使用 Standard delay format 进行反标](#32-使用-standard-delay-format-进行反标)
  - [33. 配置一个设计的内容](#33-配置一个设计的内容)
  - [34. 受保护的 Envelopes](#34-受保护的-envelopes)
  - [35. DPI](#35-dpi)
  - [36. PLI](#36-pli)
  - [37. VPI](#37-vpi)
  - [38. VPI 调用定义](#38-vpi-调用定义)
  - [39. 断言 API](#39-断言-api)
  - [40. 代码覆盖率控制和 API](#40-代码覆盖率控制和-api)
  - [41. 数据读取 API](#41-数据读取-api)
  - [B4](#b4)
  - [Annex A (正式的) 形式化语法](#annex-a-正式的-形式化语法)
  - [Annex B (正式的) 关键字](#annex-b-正式的-关键字)
  - [Annex C (正式的) 已弃用的 clause](#annex-c-正式的-已弃用的-clause)
  - [Annex D (非正式的) 可选的系统任务和系统函数](#annex-d-非正式的-可选的系统任务和系统函数)
  - [Annex E (非正式的) 可选的 compiler directives](#annex-e-非正式的-可选的-compiler-directives)
  - [Annex F (正式的) 并发断言的形式化语义](#annex-f-正式的-并发断言的形式化语义)
  - [Annex G (正式的) Std package](#annex-g-正式的-std-package)
  - [Annex H (正式的) DPI C layer](#annex-h-正式的-dpi-c-layer)
  - [Annex I (正式的) svdpi.h](#annex-i-正式的-svdpih)
  - [Annex J (正式的) Inclusion of foreign language code](#annex-j-正式的-inclusion-of-foreign-language-code)
  - [Annex K (正式的) vpi\_user.h](#annex-k-正式的-vpi_userh)
  - [Annex L (正式的) sv\_compatibility.h](#annex-l-正式的-sv_compatibilityh)
  - [Annex M (正式的) sv\_vpi\_user.h](#annex-m-正式的-sv_vpi_userh)
  - [Annex N (正式的) 概率分布函数的算法](#annex-n-正式的-概率分布函数的算法)
  - [Annex O (非正式的) 加密/解密 flow](#annex-o-非正式的-加密解密-flow)
  - [Annex P (非正式的) 术语表](#annex-p-非正式的-术语表)
  - [Annex Q (非正式的) 参考书籍](#annex-q-非正式的-参考书籍)


## 1. 综述  

### 1.1 范围  

此标准提供 IEEE 1800 SystemVerilog 语言的语法和语义的定义, 此语言是统一的硬件设计,规范和验证的语言. 此标准包括了对行为级(behavioral),寄存器传输级(RTL) 和门级(gate-level)硬件描述的支持; 支持 testbench, coverage, assertion, 面向对象(object-oriendted) 和随机约束结构; 以及为其他编程语言提供 API(application programming interfaces).  

### 1.2 目的  

此标准旨在满足日益增长的硬件规范, 设计, 验证语言使用需求. 此版本修复了 IEEE Std 1800-2012 中的语言定义的错误. 此版提供了更强的特性以易于设计, 验证, 跨编程语言交互.  

### 1.3 内容简介  

该标准为 SystemVerilog 语言的完整标准. 此标准包含以下内容:  

- 所有 SystemVerilog 结构的形式化语法和语义.  
- 用于仿真的系统 task 和 function, 比如文本输出命令.  
- 编译器指令, 如文本替换宏和仿真时间刻度.
- 编程语言接口(Programming Language Interface, PLI)机制
- SystemVerilog 的 Verification Procedual Interface(VPI) 的形式化语法和语义.
- 不包含在 VPI 内的一个 Application Programming Interface(API), 用于覆盖率(coverage)访问.
- Direct programming interface(DPI), 用于与 C 语言互动.  
- VPI, API, DPI 的头文件
- concurrent assertion 的形式化语义  
- standard delay format(SDF)结构的形式化语法和语义
- 非正式的用例

### 1.4 特定术语

以下术语贯穿此文档:  

- SystemVerilog 3.1a 指 Accellera SystemVerilog 3.1a Language Reference Manual[B4](#b4)  
- Verilog 指 IEEE Std 1364-2005
- Language Reference Manual (LRM) 指 Verilog 或 SystemVerilog 的标准文档
- Tool 指读取 SystemVerilog 源码的软件实现, 如逻辑仿真器(Logic Simulator)

### 1.5 此标准中的约定用法

此标准组织成 clause, 每个 clause 关注此语言的一个特定方面. 在 clause 中还有 subclause 用于讨论各个 construct 和 concept. 

以下为贯穿此标准的措辞约定:  

- "Shall" 用于表示强制要求, 必须严格遵循此标准, 不能有偏差.
- "Should" 用于表示在多个可能的选项中某个选项更为合适, 但是并不排除其他选项; 或表示某个行为更合适但不强制要求; 或表示不期望出现某个行为, 但并不禁止出现此类行为.
- "May" 用于表示可以在标准允许的范围内的行为.
- "can" 用于陈述.

```text
译者注: 使用"必须"替代"Shall", 使用"可以"替代"Can", 另外两个直接使用英文表示.
```

### 1.6 语法描述

正文使用以下约定:  

- 定义一个术语的时候使用*斜体*  
- ***斜体加粗***用于举例, 文件名再, 常量引用, 特别是 0, 1, x, z 值.  
- 当指代真正的 SystemVerilog 关键字时使用 **加粗** 字体表示.

```text
译者注: "斜体加粗"在原文中是 constant-width, "加粗" 在原文中是 boldface constant-width. 译者使用 Markdown 无法打出这些字体.
```

使用巴克斯范式(Backus-Naur Form,BNF) 描述 SystemVerilog 的语法. 约定如下:  

- 小写单词, 单词间可能有下划线"\_", 表示 syntactic category. 例如: module_declaration  
- 使用`红色`字符表示语法中所需的关键词, 操作符, 标点符号,例如: `module => ;`

- 使用垂线 "|"分割不同的可选择的 `items`,例如: unary_operator::=  `+` | `-` | `!` | `~` | `&` | `|` | `~|` | `^` | `~^` | `^~` |
- 使用不加粗的中括号"[]"括住可选的 item. 例如: function_declaration::=`function` [lifetime] [function_body_declaration]
- 使用不加粗的大括号"{}"括住一个重复的 item. 此 item 可以出现 0 次或2多次; 与 equivalent left-recursive 规则一样, 从左向右开始重复. 因此, 以下两条规则等价:  
  - list_of_param_assignments ::= param_assignment { `,` param_assignment}
  - list_of_param_assignments ::= param_asignment | list_of_param_assignments `,` param_asignment

语法中的*限定性术语*是一个术语, 如 *array_identifier*, 在此术语中, "array" 表示了语义内容, "identifier" 术语表示此限定性术语归约为了此语法中的术语 "identifier", 即 array_identifier 是 identifier. 此语法并没有完整的定义此类限定性术语的语义; 比如通过声明语句可以将一个 identifier 语义上地限定为 array_identifier, 但在使用 array_identifier 的语法中并未显式地描述声明的格式.  

### 1.7 此标准中使用的颜色  

此标准中只使用少量颜色以增强阅读性. 颜色并非必要的, 也不影响阅读黑白版本的标准文档. 在以下情况使用颜色:  

- 超链接到此标准的其他部分使用${\color{blue}{蓝色}}$, 如 [B4](#b4)  
- 在形式化语言定义中的语法关键字和 token 使用`红色`  
- 某些图片使用了少量的颜色以增强阅读性

### 1.8 此标准的内容  

略略略略略略略略

### 1.9 弃用的 clause

[Annex C](#annex-c) 中列出了之前版本的 IEEE Std 1364 或 IEEE Std 1800 中存在但现已弃用的 construct. [Annex C](#annex-c) 也列出了此标准中出现了的 construct, 但是这些 construct 在此标准的未来版本中可能弃用.

### 1.10 例子

此标准中有少量的 SV 代码例子. 这些是非正式的例子. 它们用于展示 SV construct 在一个简单的上下文中的用法, 而非定义完整的语法.  

### 预备知识

此标准中的部分 clause 假定您有一定的 C 语言编程经验.  

## 2. Normative references

略略略略略略略略

## 3. 设计和验证的构造块

### 3.1 概述

此 clause 讨论以下内容:  

- module, programs, interface, checkers, primitives 的用途
- subroutine 概述
- packages 概述
- configurations 概述
- 设计的层级结构 概述
- compilation 和 elaboration 的定义
- Declaration name spaces
- 仿真时刻, 仿真单位和仿真精度

此 clause 定义了 SV 中许多重要的术语和概念, 且贯穿此文档. 此 clause 提供了用于硬件设计和仿真环境的建模块的用途和用法.  

### 3.2 设计元素  

一个*设计元素*是一个 SV module, program, interface, checker, package, primitive 或 configuration. 使用以下关键字引用上述结构: **module**, **program**, **interface**, **checker**, **package**, **primitive**, 和 **config**.  

设计元素是用于建模和构建一个设计和验证环节的基本构造块. 这些构造块可以包含声明和 procedual 代码.

此 clause 描述了这些构造块的用途. 它们的完整语法和语义定义在后文给出.

### 3.3 Modules

SV 中的基本构造块是 module, 使用关键字 **module** 和 **endmodule**包围. modules 主要用于表示设计块, 但是也可以包含验证代码以及在验证块和设计块之间通信. module 可以包含以下结构:  

- port
- 数据声明, 如 nets, variable, structure 和 union
- 常量(constant)声明
- 用户自定义类型定义
- Class 定义
- 从 package 中引入声明
- 定义 subroutine
- 例化其他 module, program, interface, checker, primitive
- 例化 class 对象
- continuous assignment
- procedual 块
- generate 块
- specify 块

在此标准的后文中陆续讨论上述结构.  

注意--上述并未列出所有结构. module 可以包含其他的结构, 这些结构也会在后文中讨论.  

下述是一个使用 module 表示 2 选 1 多选器 (multiplexer) 的简单例子:  

```verilog
  module mux2to1 (
    input wire a, b, sel,
    output logic y
  );
  always_comb begin 
    if(sel) y = a;
    else    y = b;
  end
  endmodule: mux2to1
```

关于 module 的更多细节见[23. 模块和层级结构](#23-模块和层级结构) 以及 3.11 节.  

### 3.4 Programs  

program 构造块使用关键字 **program** .. **endprogram** 包围. 此结构用于建模 testbench 环境. 尽管 module 可以很好的描述硬件, 但是对于 testbench 来说, 重点并不是硬件级的细节, 比如 wire, 结构层级, 互联, 而是在于建模完整的用于验证设计的环境.  

program 快服务于以下三个目的:  

- 提供 testbench 的执行入口点
- 创建一个 scope, 在此 scope 中封装 program-wide data, task 和 function.  
- 提供一个语法上下文, 用于指定 Reaction 区域中的调度.  

program 结构是 testbench 和设计之间明确的分界线, 更重要的是其指定了专门的仿真执行语义. 协同[14. 时钟块](#14-时钟块)(**clocking**) 为设计和 testbench 之间提供了不会产生竞争的互动方式, 且可以使用 cycle 和 transaction 级的抽象.  

program 块可以包含数据声明, 类定义, subroutine 定义, 对象实例, 一个或多个 initial 或 final procedure. program 不可以包含 always procedure, primitive 实例, module 实例, interface 实例, 其他 program 实例.

SV 中的抽象和建模结构简化了 testbench 的创建和维护. 实例化和单独地连接不同 program 实例的能力使得它们能够用作通用模型.  

声明 program 的例子:  

```verilog
  program test (input clk, input [16:1] addr, inout [7:0] data);
    initial begin 
      ...
  endprogram
```

在 [24. Programs](#24-programs) 对其进行更细致的讨论.

### 3.5 Interfaces  

使用关键字 **interface**...**endinterface** 包围 interface 结构. interface 封装了用于设计块之间, 设计块和验证块之间的通信, 允许从抽象的系统级设计通过连续的细化以平滑的迁移到低级别的寄存器传输和设计的结构视图上. 通过封装块之间的通信, 有助于设计重用.  

在最低级, interface 是一组命名的 net 和 variable, 在设计中例化的 interface 可以连接其他例化了的 module, interface, program. 可以通过端口访问 interface, 可以在需要的时候引用 interface 中的 net 和 variable. 设计中经常包含端口列表和端口连接列表, 这些列表只是不断重复的名字. 使用单个名字替换掉一组名字的能力可以极大的降低设计描述的大小以及增强可维护性.  

interface 的另外一个能力是封装功能, 使得在一个接口更像一个类模板.  interface 可以有参数, 常量, 变量, 函数和任务. 可以声明 interface 中元素的类型, 或者是通过参数传递元素的类型. 使用 interface 实例的名字对成员变量和函数进行引用. 因此, 通过 interface 连接的 module 可以简单地调用 interface 的 subroutine 成员驱动通信. 因此, 可以通过替换拥有相同成员的不同接口(接口的实现的抽象级别冉)以改变通信的抽象级别和/或通信协议的粒度. 而通过此接口连接的 module 无需做出任何改变.  

为给 module 的端口提供方向信息以及控制特定模块使用的 subroutine, 提供了 **modport** 结构. 就像其名字, 从 module 的视角定义方向信息.  

除了 subroutine, interface 可以包含 process (例, nitial 或 always procedure) 以及 continuous assignment (对 testbench 和 系统级建模很有用). 这样, interface 就可以包含自己的协议检查器, 以自动地验证通过 interface 连接的所有模块是否符合指定协议. 还能实现 functional coverage 记录和报告, 协议检查, 断言.  

interface 定义和使用的一个例子:  

```verilog
  interface simple_bus(input logic clk); // 定义 interface
    logic req,gnt;
    logic [7:0] addr, data;
    logic [1:0] mode;
    logic start, rdy;
  endinterface

  module memMode(simple_bus a); // simple_bus interface 端口
    logic avail;
    // 当在顶层模块实例化 memMod时, a.req 是"simple_bus" interface 的
    // 实例 sb_intf 的 req 信号
    always @(posedge a.clk) a.gnt <= a.req & avail;
  endmodule

  module cpuMod(simple_bus b);
    ...
  endmodule

  module top;
    logic clk = 0;
    
    simple_bus sb_intf(.clk(clk)); // 实例化 interface
    
    memMod mem(.a(sb_intf)); // 连接 interface 到 module 实例
    cpuMod cpu(.b(sb_intf)); // 连接 interface 到 module 实例
  endmodule
```

[25. Interfaces](#25-interfaces)给出了 interface 的完整描述.  

### 3.6 Checkers  

略

### 3.7 Primitives  

略

### 3.8 Subroutines  

略

### 3.9 Packages  

略

### 3.10 Configurations  

略

### 3.11 Overview of hierarchy

略

### 3.12 Compilation and elaboration  

略

### 3.13 Name spaces

略

### 3.14 Simulation time units and precison


## 4. 调度语义  

## 5. 词法约定

## 6. 数据类型

## 7. 聚合数据类型  

### 7.1 概述  

此章描述了以下内容:  

- 结构体的定义和使用
- 联合体的定义和使用
- Packed 数组, unpacked 数组, 动态数组, 关联数组和队列  
- 数组的查询和操作

### 7.2 结构体

**结构体**是一组数据类型的集合且可以作为一个整体进行引用, 或者使用名字单独引用构成结构体的数据类型. 默认情况下, 结构体是 unpacked 的, 这意味着如何打包这组数据类型取决于编译器的实现. unpacked 结构体可以包含任意数据类型.  

结构体的定义遵循 C 语法, 不过没有可选在 "\{" 之前没有可选的 tag.  结构体声明的语法如 Syntax 7-1 所示:  

![I](./img/syntax%207-1.png)  

```text
13) 如果使用 struct 或 union 关键字时使用了 packed_dimension, 则必须使用 packed 关键字.  
16) 只有在 tagged 的 union 中才可以使用 void 数据类型. 仅在 unpacked 的结构体内才可以使用 random_qualifier.  
```

(Syntax 7-1 -- 结构体声明和语法)  

声明结构体的例子:  

```verilog  
  struct { bit [7:0] opcode; bit [23:0] addr;} IR; // 使用匿名结构体定义变量 IR

  IR.opcode = 1; // 设置 IR 中的域

  typedef struct {
    bit [7:0]   opcode;
    bit [23:0]  addr  ;
  } instruction;  // 命名的结构体类型
  instruction IR; // 定义变量
```

#### 7.2.1 Packed 结构体  

packed 结构体可以将一个 vector 分为子域, 可以方便地访问成员. packed 结构体有连续的 bit 域, 在内存中无间隙的存放. unpacked 结构体的 packing 取决于编译器实现, 通常来说符合符合 C 编译器的实现. 当一个 packed 结构体作为 primary 出现, 其应当被视作单个向量.  

一个 packed 结构体也可以在算数和逻辑运算中当做整体使用, 其行为取决于其符号, 默认为无符号数. 结构体中指定的第一个成员是最高有效位.  

```verilog
  struct packed signed {
    int       a;
    shortint  b;
    byte      c;
    bit [7:0] d;
  } pack1; // 有符号, 2 - state
  
  struct packed unsigned {
    time          a;
    integer       b;
    logic [31:0]  c;
  } pack2; // 无符号, 4 - state
```

  不允许将 unpacked 结构体声明为有符号数. 下述为非法用例:  

```verilog
  typedef struct signed {
    int   f1;
    logic f2;
  } SIllegalSignedUnpackedStructType;  // 非法声明

```

如果一个 packed 结构体内的数据类型都是 2 - state 的, 则此结构体整体视为 2-state 向量

如果一个 packed 结构体内的数据类型都是 4 - state, 则此结构体整体视为 4 - state 向量. 如果混用 4 - state 和 2 - state 类型, 则读取成员时隐式地将 4 - state 转换为 2 - state , 在写入时将 2 - state 转换为 4 - state.  

可以使用位选方式选择 packed 结构体内的位, 就像此结构体是一个 packed 数组, 数组范围为 [n-1:0]:  

``` verilog  
  pack1 [15:8] // c
```

只有表 6-8 (见 6.11 节) 中总结的 packed 数据类型和整数数据类型为 packed 结构体中的合法数据类型.  

packed 结构体可以和 typedef 一起使用:  

```verilog
  typedef struct packed {
    bit [3:0]   GFC; 
    bit [7:0]   VPI; 
    bit [11:0]  VCI; 
    bit         CLP; 
    bit [3:0]   PT ; 
    bit [7:0]   HEC; 
    bit [47:0] [7:0] Payload; 
    bit [2:0]   filler; 
  } s_atmcell;
```

### 7.2.2 结构体赋值  

结构体可以作为整体赋值, 可以作为整体传递入/出 subroutine.  

在声明成员时使用初始化赋值语句可以为构体的数据类型赋予默认成员值. 被赋值的表达式必须为常量表达式.  

例子如下:  

```verilog
  typedef struct {
    int addr = 1 + constant;
    int crc;
    byte data [4] = '{4{1}}; 
  } packet1;
```  

实例化此结构体.  

```verilog  
  packet p1; // typedef 定义了初始化值. p1.crc 将使用 int 的默认值.  
```

如果在变量声明的同时显式地使用了初始值, 则忽略结构体数据类型内部的初始赋值表达式. 5.10 讨论了如何将初始值赋值给结构体. 如:  

```verilog
  packet1 pi = '{1,2,'{2,3,4,5}}; 
```

成员变量中含有 union 的 unpacked 结构体和 packed 结构体不得为成员变量设置单独的默认值.  

```
不知如何翻译
The initial assignment expression within a data type shall be ignored when using a data type to declare a net
that does not have a user-defined nettype (see 6.7.1).
```

### 7.3 联合体(Union)

联合体是一种数据类型, 可以通过命名的成员数据类型的名字访问单个存储区域中的值. 在同一时刻, 只能使用 union 中的一个数据类型. 默认情况下 union 是unpacked, 这意味着并不强制要求 union 所表示的值如何存储. 动态类型和 chandle 类型只能用于 tagged 联合体.  

联合体声明语法如 Syntax 7-2 所示:  

![I](./img/Syntax%207-2-1.png)  
![I](./img/Syntax%207-2-2.png)  

```text
13) 如果使用 struct 或 union 关键字时使用了 packed_dimension, 则必须使用 packed 关键字.  
16) 只有在 tagged 的 union 中才可以使用 void 数据类型. 仅在 unpacked 的结构体内才可以使用 random_qualifier.  
```  

Syntax 7-2 -- 联合体声明语法  

*例子*:  

```verilog  
typedef union { int i; shortreal f; } num; // 命名的联合体类型
num n; 
n.f = 0.0; // 将 n 设置为浮点类型
typedef struct { 
bit isfloat; 
union { int i; shortreal f; } n; // 匿名联合体类型 
} tagged_st; // 命名的结构体
```

如果 unpacked 联合体类的的变量未被指定初始值, 则联合体被初始化为联合体内第一个成员的初始值.  

```text
不知如何翻译
One special provision exists in order to simplify the use of unpacked unions: if an unpacked union contains
several unpacked structures that share a common initial sequence and if the unpacked union object currently
contains one of these structures, it is permitted to inspect the common initial part of any of them anywhere
that a declaration of the complete type of the union is visible. Two structures share a common initial
sequence if corresponding members have equivalent types for a sequence of one or more initial members. 
```

#### 7.3.1 Packed 联合体

packed 联合体内只能包含整数数据类型成员变量. 一个 packed untagged 联合体的成员必须大小相等(不同意 unpacked 联合体或 packed tagged联合体, 它们的成员可以为不同大小). 因此, 一个联合体成员被写入后可以通过另外一个成员读取. packed 联合体不同于 unpacked 联合体, 当其作为 primary 出现时, 应当被视作单个向量.  

packed 联合体可以在算数和逻辑操作中当做整体使用, 其行为取决于其符号, 默认为无符号数. 可以使用位选选择 packed 联合体中的位, 就像范围为 [n-1:0] 的packed 数组一样.  

只有表 6-8(见 6.11) 中总结的整数数据类型和 packed 数据类型可以在 packed 联合体中使用.  

如果 packed 联合体包含 2-state 和 4-state 成员, 则整个联合体为 4-state的. 读取时会隐式地将 4-state 转换为 2-state, 写入时会隐式地将 2-state 转换为 4-state.

可以使用不同的位宽访问联合体, 如:  

```verilog
  typedef union packed { // 默认无符号
    s_atmcell acell; 
    bit [423:0] bit_slice; 
    bit [52:0][7:0] byte_slice; 
  } u_atmcell;
  u_atmcell u1;
  byte b; bit [3:0] nib;
  b = u1.bit_slice[415:408]; // 同 b = u1.byte_slice[51];
  nib = u1.bit_slice [423:420]; // 同 nib = u1.acell.GFC; 
```

对于 packed 联合体, 读写一个成员不受机器字节序的影响, 不像 unpacked 结构体的 unpacked 联合体为 C-compatible 的, 且成员地址降序排列.  

#### 7.3.1 Tagged 联合体

## 8. 类

## 9. Processes

## 10. Assignment statement

## 11. 操作符和表达式

## 12. Procedual programming statements

## 13. 任务和函数(子任务)

## 14. 时钟块

## 15. 跨 Process 的同步和通信

## 16. Assertions

## 17. Checkers

## 18. 产生受约束的随机值

## 19. 功能覆盖率

## 20. Utility 系统任务和系统函数

## 21. 输入/输出系统任务和函数

## 22. Compiler directives

## 23. 模块和层级结构

## 24. Programs

## 25. Interfaces

## 26. Packages

## 27. Generate 结构

## 28. 门级和开关级建模

## 29. 用户原语定义

## 30. Specify blocks

## 31. Timing checks

## 32. 使用 Standard delay format 进行反标

## 33. 配置一个设计的内容

## 34. 受保护的 Envelopes

## 35. DPI

## 36. PLI

## 37. VPI

## 38. VPI 调用定义

## 39. 断言 API

## 40. 代码覆盖率控制和 API

## 41. 数据读取 API

## B4

## Annex A (正式的) 形式化语法

## Annex B (正式的) 关键字

## Annex C (正式的) 已弃用的 clause

## Annex D (非正式的) 可选的系统任务和系统函数

## Annex E (非正式的) 可选的 compiler directives

## Annex F (正式的) 并发断言的形式化语义

## Annex G (正式的) Std package

## Annex H (正式的) DPI C layer

## Annex I (正式的) svdpi.h

## Annex J (正式的) Inclusion of foreign language code

## Annex K (正式的) vpi_user.h

## Annex L (正式的) sv_compatibility.h

## Annex M (正式的) sv_vpi_user.h

## Annex N (正式的) 概率分布函数的算法

## Annex O (非正式的) 加密/解密 flow

## Annex P (非正式的) 术语表

## Annex Q (非正式的) 参考书籍
