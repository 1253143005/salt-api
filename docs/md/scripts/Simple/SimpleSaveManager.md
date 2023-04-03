

> 存储管理器，进行存档的存储，获取，备份等操作。

## 1. Runtime

### 方法

#### Create [Static]
> Create
```csharp
//初始化存档管理器，在使用前需要调用
SimpleSaveManager.Create();
```
#### SetInt [Static]
> SetInt 
```csharp
//存储int值
SimpleSaveManager.SetInt("test", 1);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 存储的键
value | int | 存储的值

#### SetString [Static]
> SetString
```csharp
//存储string值
SimpleSaveManager.SetString ("test", "1");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 存储的键
value | string | 存储的值


### 属性

## Editor

[打开设置](md/installation.md?id=工具tab)

![](SimpleSaveManager_md_files/f31d4300-d1f4-11ed-afb0-c340f1571a81.jpeg?v=1&type=image)

***注：存档文件名可以填入路径：save/file，则表示在存储路径下创建SAVE/file文件***
