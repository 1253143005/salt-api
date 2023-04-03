
?> [返回 Simple](md/scripts/simple.md)

> 缓冲池，初始化，缓冲，移除等操作。

## 控制方法 :id=static

> 控制方法

类 |  说明
-------- |  -----
<small>[Spawn](md/scripts/Simple/SimplePool.md?id=Spawn)</small>  | <small>从缓冲池中获取已缓冲的GameObject</small>
<small>[Remove](md/scripts/Simple/SimplePool.md?id=Remove)</small>  | <small>将GameObject放置回缓冲池中</small>
<small>[RemovePool](md/scripts/Simple/SimplePool.md?id=RemovePool)</small>  | <small>将指定缓冲池的已经缓冲的内容全部回收</small>
<small>[CreatePool](md/scripts/Simple/SimplePool.md?id=CreatePool)</small>  | <small>代码创建缓冲池</small>

## Editor

>挂载方法

![](SimplePool_md_files/7db36820-d211-11ed-be64-0b27884aa10a.jpeg?v=1&type=image)

如图所示，在GameObject上使用Add Component挂载SimplePoolContainer组件。
其中属性：
- **isGlobal** ：表示此缓冲池是否是全局缓冲池，如果是全局缓冲池，则不会因为切换场景而卸载
- **Pool ID** ：表示此缓冲池的ID，生成，回收都需要使用到缓冲池ID
- **Pool Items** ： 表示缓冲Item列表
	- **item** ： 为缓冲的预制体prefab
	- **Preload Num** ： 为预缓冲数量，缓冲池初始化时，会预先缓冲此数量的GameObject，**但是需要注意，此数值越大会造成越多的初始创建开销。**
	- **Pool Max** ： 为缓冲池最大容量，如果超过此容量，缓冲池会在合适的时间移除多余的的GameObject

---------------------------

## 控制方法（详细）

### Spawn :id=Spawn

> 从缓冲池中获取已缓冲的GameObject

```csharp
GameObject go = SimplePool.Spawn("poolID", "itemID", parentTransform);
```

名称 | 类型 | 说明
-------- | -----| -----
poolID | string | 缓冲池的ID
itemID | string | 缓冲预制体的ID
transform | Transform | 实例化的父节点位置

--------------------------------

### Remove :id=Remove

> 将GameObject放置回缓冲池中

?> 如果此GameObject并不在指定的回收池中，会直接destroy

```csharp
SimplePool.Remove("poolID", removeGameObject);
```

名称 | 类型 | 说明
-------- | -----| -----
poolID | string | 缓冲池的ID
gameObject | GameObject | 回收的GO

--------------------------------

### RemovePool :id=RemovePool

> 将指定缓冲池的已经缓冲的内容全部回收

?> 并不会销毁当前缓冲池

```csharp
SimplePool.RemovePool("poolID");
```

名称 | 类型 | 说明
-------- | -----| -----
poolID | string | 缓冲池的ID

--------------------------------

### CreatePool :id=CreatePool

> 代码创建缓冲池

```csharp
var poolItems = new SimplePoolItemProperty[0];
SimplePool.CreatePool("poolID", poolItems, false)
```

名称 | 类型 | 说明
-------- | -----| -----
poolID | string | 缓冲池的ID
poolItems | SimplePoolItemProperty[] | 缓冲物体列表
isGlobal | bool | 是否是全局缓冲池

