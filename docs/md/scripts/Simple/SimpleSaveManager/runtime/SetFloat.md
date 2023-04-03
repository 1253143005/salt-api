?> [返回 SimpleSaveManager](md/scripts/Simple/SimpleSaveManager.md?id=setget)

> 在存档中，向指定key，加载，存储值

--------------------------------

## SetFloat :id=set

> 存储

```csharp
bool saveSuccess = SimpleSaveManager.SetFloat("test", 1f);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 存储的键
value | float | 存储的值

--------------------------------

## GetFloat :id=get

> 加载

```csharp
float loadValue = SimpleSaveManager.GetFloat("test", 0f);
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 加载的键
defaultValue | float | 加载的默认值

