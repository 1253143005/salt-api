
?> [返回 AudioHandler](md/scripts/Salt/AudioHandler.md?id=connected)

> 音轨属性。

## 方法 :id=func

类 |  说明
-------- |  -----
<small>[CheckIsActive](md/scripts/Salt/AudioHandler/AudioProperty.md?id=CheckIsActive)</small>  | <small>判断当前的音轨是否激活</small>
<small>[Copy](md/scripts/Salt/AudioHandler/AudioProperty.md?id=Copy)</small>  | <small>克隆当前属性</small>

## 属性 :id=param

类 | 类型 |  音乐编辑器专用 |  说明
-------- |  ----- |  -----|  -----
<small>id</small>  | <small>string</small>| <small>false</small> | <small>ID</small>
<small>name</small>  | <small>string</small>| <small>false</small> | <small>音轨名称</small>
<small>color</small>  | <small>int</small>| <small>true</small> | <small>音轨颜色</small>
<small>mute</small>  | <small>bool</small>| <small>true</small> | <small>是否静音</small>
<small>perfect</small>  | <small>bool</small>| <small>true</small> | <small>是否完美</small>
<small>active</small>  | <small>bool</small>| <small>true</small> | <small>是否激活</small>
<small>activeChordSound</small>  | <small>bool</small> | <small>true</small>| <small>是否激活和弦音乐</small>
<small>chordSoundIDList</small>  | <small>List< string ></small> | <small>false</small>| <small>和弦音乐ID列表</small>
<small>isAlwaysDetermined</small>  | <small>bool</small> | <small>false</small>| <small>是永久触发</small>
<small>forwardTime</small>  | <small>float</small> | <small>false</small>| <small>提前值</small>
<small>determineKeyType</small>  | <small>[AudioDetermineKeyType](md/scripts/Salt/AudioHandler/AudioDetermineKeyType.md)</small>| <small>false</small> | <small>判定按键类型</small>
<small>keyboardKeyType</small>  | <small>[AudioKeyboardKeyType](md/scripts/Salt/AudioHandler/AudioKeyboardKeyType.md)</small> | <small>false</small>| <small>按键</small>
<small>tempoProperties</small>  | <small>List< [AudioTempoProperty](md/scripts/Salt/AudioHandler/AudioTempoProperty.md) ></small> | <small>false</small>| <small>节奏</small>
<small>determinProperties</small>  | <small>[AudioDeterminProperty](md/scripts/Salt/AudioHandler/AudioDeterminProperty.md) []</small> | <small>false</small>| <small>音节判定属性</small>
<small>chordDeterminCopyProperties</small>  | <small>[AudioDeterminChordSoundProperty](md/scripts/Salt/AudioHandler/AudioDeterminChordSoundProperty.md) []</small> | <small>false</small>| <small>和弦音乐ID的索引列表-拷贝副本</small>

## 方法实现

### CheckIsActive() :id=CheckIsActive

> 判断当前的音轨是否激活

***例子***

``` csharp
AudioTrackProperty property; //已经定义的音轨属性
bool isActive= property.CheckIsActive();
```

### Copy() :id=Copy

> 克隆当前属性

***例子***

``` csharp
AudioTrackProperty oldProperty; //已经定义的音轨属性
AudioTrackProperty newProperty = oldProperty.Copy();
```
