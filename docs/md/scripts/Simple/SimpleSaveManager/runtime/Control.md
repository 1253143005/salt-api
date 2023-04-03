?> [返回 SimpleSaveManager](md/scripts/Simple/SimpleSaveManager.md?id=runtime)

> 在存档中，向指定key，加载，存储值

--------------------------------

## Has :id=has

>在存档中是否存在指定键

```csharp
bool hasKey = SimpleSaveManager.Has("test");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 查询的键

--------------------------------

## Delete :id=delete

> 在存档中删除指定键的存档

```csharp
bool hasSuccess = SimpleSaveManager.Delete("test");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 删除的键

--------------------------------

## Save :id=save

> 将存档的缓存修改确实写入存储中

```csharp
SimpleSaveManager.Save();
```

--------------------------------

## Backup :id=backup

!> 将存档备份到指定文件中 **<font size=1 color=#D26264>[ 此方法目前可能存在bug，暂不建议使用 ]</font>**

```csharp
SimpleSaveManager.Backup("backup 1");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 备份的键

--------------------------------

## Restore :id=restore 

!> 将指定存档恢复 **<font size=1 color=#D26264>[ 此方法目前可能存在bug，暂不建议使用 ]</font>**

```csharp
bool hasSuccess = SimpleSaveManager.Backup("backup 1");
```

名称 | 类型 | 说明
-------- | -----| -----
key | string | 恢复的键


