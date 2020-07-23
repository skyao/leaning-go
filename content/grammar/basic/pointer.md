---
date: 2018-12-04T23:50:00+08:00
title: 指针
weight: 415
menu:
  main:
    parent: "grammar-basic"
description : "go语言中的指针"
---

Go 具有指针。 指针保存了变量的内存地址。

## 基本语法

定义：类型 `*T` 是指向类型 `T` 的值的指针。其零值是 `nil`。

```go
var p *int
```

生成：`&` 符号会生成一个指向其作用对象的指针。

```go
i := 42
p = &i
```

取值：`*` 符号表示指针指向的底层的值。

```go
fmt.Println(*p) // 通过指针 p 读取 i
*p = 21         // 通过指针 p 设置 i
```

注意：与 C 不同，**Go 没有指针运算**。