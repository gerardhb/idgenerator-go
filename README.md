#  ❄️ idenerator-go

#### 介绍
这是 https://github.com/yitter/idgenerator 的 Go 专项引用库
更多使用说明，请参考前述项目。

## Go环境

1.SDK，go1.14

2.启用 Go-Modules

```
go env -w GO111MODULE=on
go env -w GOPROXY=https://goproxy.cn,https://goproxy.io,direct
```

3. 安装方式
```
    go get -u -v github.com/yitter/idgenerator-go
```

## Go代码示例
```
var yid = gen.IDHelperInit()
fmt.Println(yid.NextID())

// 方法二：自定义参数
var options = contract.NewIdGeneratorOptions(1)
//options.WorkerIdBitLength = 6
//options.SeqBitLength = 6
//options.TopOverCostCount = 2000
//options.BaseTime = time.Date(2020, 2, 20, 2, 20, 2, 20, time.UTC).UnixNano() / 1e6
yid.SetIdGenerator(options)

```