
?> [返回 AudioHandler](md/scripts/Salt/AudioHandler.md?id=connected)

> 音乐属性。

## 方法 :id=func

类 |  说明
-------- |  -----
<small>[GetVolume](md/scripts/Salt/AudioHandler/AudioProperty.md?id=GetVolume)</small>  | <small>获取指定声音的音量</small>
<small>[Copy](md/scripts/Salt/AudioHandler/AudioProperty.md?id=Copy)</small>  | <small>克隆当前属性</small>

## 属性 :id=param

类 | 类型 |  说明
-------- |  ----- |  -----
<small>musicID</small>  | <small>string</small> | <small>选择的音乐文件ID</small>
<small>latency</small>  | <small>float</small> | <small>音轨的偏移值</small>
<small>trackProperties</small>  | <small>List< [AudioTrackProperty](md/scripts/Salt/AudioHandler/AudioTrackProperty.md) ></small> | <small>音轨列表</small>
<small>audioSettings</small>  | <small>List< [AudioFileSetting](md/scripts/Salt/AudioHandler/AudioFileSetting.md) ></small> | <small>声音文件的设置</small>

## 方法实现

### GetVolume(string audioID) :id=GetVolume

> 获取指定声音的音量

***例子***

``` csharp
AudioProperty property; //已经定义的音乐属性
string audioID = "test";
float volume = property.GetVolume(audioID);
```

### Copy() :id=Copy

> 克隆当前属性

***例子***

``` csharp
AudioProperty oldProperty; //已经定义的音乐属性
AudioProperty newProperty = oldProperty.Clone();
```

