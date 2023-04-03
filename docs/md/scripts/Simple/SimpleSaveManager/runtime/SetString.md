?> [返回 SimpleSaveManager](md/scripts/Simple/SimpleSaveManager.md?id=runtime)

> 在存档中，向指定key，加载，存储值

--------------------------------

## SetString :id=set

> 存储

```csharp
bool saveSuccess = SimpleSaveManager.SetString("test", "1");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 存储的键
value | string | 存储的值

--------------------------------

## GetString :id=get

> 加载

```csharp
int loadValue = SimpleSaveManager.GetString("test", null);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 加载的键
defaultValue | string | 加载的默认值

