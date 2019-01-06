本代码仅用于个人学习

go的基本类型
    bool
    string
    int  int8  int16  int32  int64
    uint uint8 uint16 uint32 uint64 uintptr
    byte // uint8 的别名
    rune // int32 的别名
        // 表示一个 Unicode 码点
    float32 float64
    complex64 complex128
    int, uint 和 uintptr 在 32 位系统上通常为 32 位宽，在 64 位系统上则为 64 位宽。

变量
    var 语句用于声明一个变量列表，跟函数的参数列表一样，类型在最后
    example:
        var c, python, java bool
        var i, j int = 1, 2
        var c, python, java = true, false, "no!"

函数
    函数可以没有参数或接受多个参数
    add 接受两个 int 类型的参数。（注意类型在变量名 之后）
    example:
        func add(x int, y int) int

    函数可以返回任意数量的返回值
    example:
        func swap(x, y string) (string, string) {
            return y, x
        }

    在函数中，简洁赋值语句 := 可在类型明确的地方代替 var 声明
    example:
        var i, j int = 1, 2
        k := 3
        c, python, java := true, false, "no!"

输出
    println and printf的区别
    print就是一般的标准输出，但是不换行
    Println :可以打印出字符串，和变量，换行
    Printf : 只可以打印出格式化的字符串,可以输出字符串类型的变量，不可以输出整形变量和整形，换行
    example:
        fmt.Print("hello world")
        fmt.Println("hello world", variable)
        fmt.Printf("%v %v %v %q\n", i, f, b, s)