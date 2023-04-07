
?> [返回 AudioHandler](md/scripts/Salt/AudioHandler.md)

> 关卡声音控制器。

!> 此控制类一个关卡只允许存在一个 

## 方法 :id=func

类 |  说明
-------- |  -----
<small>Remove</small>  | <small>移除数据`OnDestroy时会自动调用`</small>

## 属性 :id=param

类 | 类型 | 赋值/获取 |  说明
-------- |  ----- |  -----|  -----
<small>isInGame</small>  | <small>bool</small> | <small>`get`</small> | <small>关卡数据</small>
<small>play</small>  | <small>bool</small> | <small>`set/get`</small> | <small>关卡正在播放中</small>
<small>pause</small>  | <small>bool</small> | <small>`set/get`</small> | <small>关卡暂停</small>
<small>time</small>  | <small>float</small> | <small>`set/get`</small> | <small>关卡运行时间(秒)</small>
<small>allTracks</small>  | <small>List< TrackDetail ></small> | <small>`get`</small> | <small>所有音轨</small>

## 按键回调 :id=keyCallback

类 | 类型 | 参数说明 | 说明
-------- |  ----- |   ----- | -----
<small>onKeyboardDown</small>  | <small>UnityEvent<AudioKeyboardKeyType></small> | <small>按下的按键类型</small> | <small>按键按下回调</small>
<small>onKeyboardHold</small>  | <small>UnityEvent<AudioKeyboardKeyType></small> | <small>持续按下的按键类型</small>  | <small>按键持续按下回调</small>
<small>onKeyboardUp</small>  | <small>UnityEvent<AudioKeyboardKeyType></small> | <small>抬起的按键类型</small>  | <small>按键抬起回调</small>

## 检测回调 :id=DetermineCallback

类 | 类型 | 参数说明 | 说明
-------- |  ----- | -----| -----
<small>onDetermineMiss</small>  | <small>UnityEvent<TrackDetail, int></small> | <small>音轨，触发音节</small> | <small>触发miss回调</small>
<small>onDeterminePerfect</small>  | <small>UnityEvent<TrackDetail, int></small> | <small>音轨，触发音节</small> | <small>触发perfect回调</small>
<small>onDetermineGood</small>  | <small>UnityEvent<TrackDetail, int></small> | <small>音轨，触发音节</small> | <small>触发good回调</small>
<small>onDetermineAlways</small>  | <small>UnityEvent<TrackDetail, int></small> | <small>音轨，触发音节</small> | <small>触发always回调</small>



## CustomAudioProperty :id=CustomAudioProperty 
> 音乐属性

类 | 类型 | 说明
-------- |  ----- |  -----
<small>categroy</small>  | string | <small>声音类别</small>
<small>audioClips</small>  | AudioClip[] | <small>此类别声音中的声音文件</small>


## Editor

### 创建

在`Hierarchy`窗口点击鼠标右键，选择

`猫熊 > Salt > 关卡资源(LevelResource)`

会自动创建对应的GameObject

### 关卡查看

![](LevelResource_md_files/234e3d40-d50b-11ed-add9-63b3093e49b1.jpeg?v=1&type=image
 ':size=315x279'
)

点击设置可以打开关卡设置界面

![](LevelResource_md_files/b6427a80-d50b-11ed-add9-63b3093e49b1.jpeg?v=1&type=image ':size=901x620')

设置及内容如图所示。

音轨有对应的音轨序列按钮，点击可以显示选择查看的具体音轨内容

![](LevelResource_md_files/31efdb00-d50c-11ed-add9-63b3093e49b1.jpeg?v=1&type=image ':size=300x240')
