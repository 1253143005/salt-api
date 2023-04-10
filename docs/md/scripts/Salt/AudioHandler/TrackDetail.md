
?> [返回 AudioHandler](md/scripts/Salt/AudioHandler.md?id=connected)

> 音轨属性。

## 属性 :id=param

类 | 类型 | 默认值 |  说明
-------- |  ----- |  -----|  -----
<small>name</small>  | <small>string</small> | <small>`null`</small> | <small>音轨名称</small>
<small>id</small>  | <small>int</small> | <small>`-1`</small> | <small>音轨ID</small>
<small>playSyllableIndex</small>  | <small>int</small> | <small>`-1`</small> | <small>播放到的音节的序列号</small>
<small>mute</small>  | <small>bool</small> | <small>`false`</small> | <small>是否静音</small>
<small>isChord</small>  | <small>bool</small> | <small>`false`</small> | <small>是否和弦</small>
<small>isHold</small>  | <small>bool</small> | <small>`false`</small> | <small>是否按下激活</small>
<small>isAlways</small>  | <small>bool</small> | <small>`false`</small> | <small>是否always音轨</small>
<small>isPerfect</small>  | <small>bool</small> | <small>`false`</small> | <small>是否完美响应</small>
<small>keyboardKeyType</small>  | <small>[AudioKeyboardKeyType](md/scripts/Salt/AudioHandler/AudioKeyboardKeyType.md)</small> | <small>`AudioKeyboardKeyType.nil`</small> | <small>触发按键</small>
<small>syllables</small>  | <small>List< [SyllableDetail](md/scripts/Salt/AudioHandler/SyllableDetail.md) ></small> | <small>`new List<SyllableDetail>()`</small> | <small>音节列表</small>
<small>trackProperty</small>  | <small>[AudioTrackProperty](md/scripts/Salt/AudioHandler/AudioTrackProperty.md)</small> | <small>`null`</small> | <small>音轨数据</small>

