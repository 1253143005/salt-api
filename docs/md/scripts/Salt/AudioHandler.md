
?> [返回 Salt](md/scripts/salt.md)

> 关卡声音控制器。

## 属性 :id=param

类 | 类型 | 赋值/获取 |  说明
-------- |  ----- |  -----|  -----
<small>isInGame</small>  | <small>bool</small> | <small>get</small> | <small>关卡数据</small>
<small>play</small>  | <small>bool</small> | <small>set/get</small> | <small>关卡正在播放中</small>
<small>pause</small>  | <small>bool</small> | <small>set/get</small> | <small>关卡暂停</small>
<small>time</small>  | <small>float</small> | <small>set/get</small> | <small>关卡运行时间(秒)</small>
<small>allTracks</small>  | <small>List<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) ></small> | <small>get</small> | <small>所有音轨</small>

## 按键回调 :id=keyCallback

类 | 类型 | 参数说明 | 说明
-------- |  ----- |   ----- | -----
<small>onKeyboardDown</small>  | <small>UnityEvent<[AudioKeyboardKeyType](md/scripts/Salt/AudioHandler/AudioKeyboardKeyType.md) ></small> | <small>按下的按键类型</small> | <small>按键按下回调</small>
<small>onKeyboardHold</small>  | <small>UnityEvent<[AudioKeyboardKeyType](md/scripts/Salt/AudioHandler/AudioKeyboardKeyType.md) ></small> | <small>持续按下的按键类型</small>  | <small>按键持续按下回调</small>
<small>onKeyboardUp</small>  | <small>UnityEvent<[AudioKeyboardKeyType](md/scripts/Salt/AudioHandler/AudioKeyboardKeyType.md) ></small> | <small>抬起的按键类型</small>  | <small>按键抬起回调</small>

## 检测回调 :id=DetermineCallback

类 | 类型 | 参数说明 | 说明
-------- |  ----- | -----| -----
<small>onDetermineMiss</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>触发miss回调</small>
<small>onDeterminePerfect</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>触发perfect回调</small>
<small>onDetermineGood</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>触发good回调</small>
<small>onDetermineAlways</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>触发always回调</small>

## 音轨回调 :id=TrackCallback

类 | 类型 | 参数说明 | 说明
-------- |  ----- | -----| -----
<small>onUpdateTrack</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>刷新音轨回调</small>
<small>onUpdateLinkTrack</small>  | <small>UnityEvent<[TrackDetail](md/scripts/Salt/AudioHandler/TrackDetail.md) , int></small> | <small>音轨，触发音节</small> | <small>刷新链接音轨回调</small>

## 方法 :id=func

类 |  说明
-------- |  -----
<small>[GetInstance](md/scripts/Salt/AudioHandler.md?id=GetInstance)</small>  | <small>获取单例，此类只可以使用此方法来实例化</small>
<small>[Play](md/scripts/Salt/AudioHandler.md?id=Play)</small>  | <small>播放当前关卡</small>
<small>[Pause](md/scripts/Salt/AudioHandler.md?id=Pause)</small>  | <small>暂停关卡播放状态</small>
<small>[Resume](md/scripts/Salt/AudioHandler.md?id=Resume)</small>  | <small>恢复关卡播放状态</small>
<small>[Stop](md/scripts/Salt/AudioHandler.md?id=Stop)</small>  | <small>终止关卡播放状态</small>
<small>[Update](md/scripts/Salt/AudioHandler.md?id=Update)</small>  | <small>刷新关卡数据</small>
<small>[Init](md/scripts/Salt/AudioHandler.md?id=Init)</small>  | <small>初始化播放数据</small>
<small>[RemoveLoopMusic](md/scripts/Salt/AudioHandler.md?id=RemoveLoopMusic)</small>  | <small>移除音效，和弦音效的循环列表</small>
<small>[ParseAudioPropertyData](md/scripts/Salt/AudioHandler.md?id=ParseAudioPropertyData)</small>  | <small>处理音乐数据</small>

## 方法展示

### GetInstance() :id=GetInstance

> 获取单例，此类只可以使用此方法来实例化

***例子***
``` csharp
AudioHandler handler = AudioHandler.GetInstance();
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Update(float time) :id=Update

> 刷新关卡数据。根据给定的时间，刷新当前的关卡应该触发的状态

!> 注：声音文件并不是按照stream方式播放。 

***参数***

类 |  类型 | 说明
-------- |  ----- |  -----
<small>time</small>|<small>float</small>|<small>当前关卡执行的时间</small>

***例子***

``` csharp
float runTime = 5f;
AudioHandler.GetInstance().Update(runTime);
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Stop() :id=Stop

> 终止关卡播放状态

***例子***

``` csharp
AudioHandler.GetInstance().Stop();
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Play(AudioProperty audioProperty = null, string soundCategroy = null, string chordSoundCategroy = null, string musicCategroy = null) :id=Play

> 播放当前关卡，如果设置参数的值，会对当前的关卡数据进行初始化并覆盖之前设置的值

***参数***

类 |  类型 | 默认值|说明
-------- |  ----- |  ----- |  -----
<small>audioProperty</small>|<small>[AudioProperty](md/scripts/Salt/AudioHandler/AudioProperty.md)</small>|<small>null</small>|<small>关卡数据</small>
<small>soundCategroy</small>|<small>string</small>|<small>null</small>|<small>音效目录名称</small>
<small>chordSoundCategroy</small>|<small>string</small>|<small>null</small>|<small>和弦音效目录名称</small>
<small>musicCategroy</small>|<small>string</small>|<small>null</small>|<small>音乐目录名称</small>

***例子***

``` csharp
AudioHandler.GetInstance().Play();
```

``` csharp
AudioProperty audioProperty; //从别处加载
var soundCategroy = "音效目录";
var chordSoundCategroy = "和弦音效目录";
var musicCategroy = "音乐目录";
AudioHandler.GetInstance().Play(audioProperty, soundCategroy, chordSoundCategroy, musicCategroy);
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Pause() :id=Pause

> 暂停关卡播放状态

***例子***

``` csharp
AudioHandler.GetInstance().Pause();
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Resume() :id=Resume

> 恢复关卡播放状态

***例子***

``` csharp
AudioHandler.GetInstance().Resume();
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### Init(AudioProperty audioProperty, string soundCategroy, string chordSoundCategroy, string musicCategroy) :id=Init

> 初始化播放数据

***参数***

类 |  类型 |说明
-------- |  ----- |   -----
<small>audioProperty</small>|<small>[AudioProperty](md/scripts/Salt/AudioHandler/AudioProperty.md)</small>|<small>关卡数据</small>
<small>soundCategroy</small>|<small>string</small>|<small>音效目录名称</small>
<small>chordSoundCategroy</small>|<small>string</small>|<small>和弦音效目录名称</small>
<small>musicCategroy</small>|<small>string</small>|<small>音乐目录名称</small>

***例子***

``` csharp
AudioProperty audioProperty; //从别处加载
var soundCategroy = "音效目录";
var chordSoundCategroy = "和弦音效目录";
var musicCategroy = "音乐目录";
AudioHandler.GetInstance().Init(audioProperty, soundCategroy, chordSoundCategroy, musicCategroy);
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### RemoveLoopMusic() :id=RemoveLoopMusic

> 移除音效，和弦音效的循环列表

***例子***

``` csharp
AudioHandler.GetInstance().RemoveLoopMusic();
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

### ParseAudioPropertyData(string data) :id=ParseAudioPropertyData

> 处理音乐数据

***例子***

``` csharp
string data; //音乐关卡数据
AudioProperty audioProperty = AudioHandler.GetInstance().ParseAudioPropertyData(data);
```

``` csharp
JSONObject dataJson; //音乐关卡Json数据
AudioProperty audioProperty = AudioHandler.GetInstance().ParseAudioPropertyData(dataJson);
```
<small>[- 返回 -](md/scripts/Salt/AudioHandler.md?id=func)</small>

