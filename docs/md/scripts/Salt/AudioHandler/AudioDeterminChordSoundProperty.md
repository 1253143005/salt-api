
?> [返回 AudioHandler](md/scripts/Salt/AudioHandler.md?id=connected)

> 音节和弦判定属性。

## 方法 :id=func

类 |  说明
-------- |  -----
<small>[Copy](md/scripts/Salt/AudioHandler/AudioProperty.md?id=Copy)</small>  | <small>克隆当前属性</small>

## 属性 :id=param

类 | 类型 |  说明
-------- |  ----- |  -----
<small>type</small>  | <small>[AudioDetermineType](md/scripts/Salt/AudioHandler/AudioDetermineType.md)</small> | <small>判定类型</small>
<small>chordIndexes</small>  | <small>List< int ></small> | <small>和弦音乐ID的索引列表</small>
<small>holdReleaseChordIndexes</small>  | <small>List< int ></small> | <small>长按抬起触发-和弦音乐ID的索引列表</small>

## 方法实现

### Copy() :id=Copy

> 克隆当前属性

***例子***

``` csharp
AudioDeterminChordSoundProperty oldProperty; //已经定义的音节和弦判定属性
AudioDeterminChordSoundProperty newProperty = oldProperty.Clone();
```

