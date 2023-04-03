?> [返回 SimpleSaveManager](md/scripts/Simple/SimpleSaveManager.md?id=runtime)

> 在存档中，向指定key，加载，存储值

--------------------------------

## SetBool :id=set

> 存储

```csharp
bool saveSuccess = SimpleSaveManager.SetBool("test", false);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 存储的键
value | bool | 存储的值

--------------------------------

## GetBool :id=get

> 加载

```csharp
bool loadValue = SimpleSaveManager.GetBool("test", false);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 加载的键
defaultValue | bool | 加载的默认值

