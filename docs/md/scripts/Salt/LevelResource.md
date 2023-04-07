
?> [返回 Salt](md/scripts/salt.md)

> 当前关卡数据的加载查看类。

!> 此控制类一个关卡只允许存在一个 

## 方法 :id=func

类 |  说明
-------- |  -----
<small>Remove</small>  | <small>移除数据`OnDestroy时会自动调用`</small>

## 属性 :id=param

类 | 类型 | 说明
-------- |  ----- |  -----
<small>levelData</small>  | TextAsset | <small>关卡数据</small>
<small>musicAudioClips</small>  | AudioClip[] | <small>默认声音列表中的声音文件</small>
<small>sfxAudioClips</small>  | AudioClip[] | <small>默认音效列表中的声音文件</small>
<small>soundCategroy</small>  | [CustomAudioProperty](md/scripts/Salt/LevelResource.md?id=CustomAudioProperty ) | <small>自定义音效文件</small>
<small>chordSoundCategroy</small>  | [CustomAudioProperty](md/scripts/Salt/LevelResource.md?id=CustomAudioProperty ) | <small>自定义和弦音效文件</small>
<small>musicCategroy</small>  | [CustomAudioProperty](md/scripts/Salt/LevelResource.md?id=CustomAudioProperty ) | <small>自定义音乐声音文件</small>
<small>id</small>  | int | <small>关卡ID</small>
<small>audioProperty</small>  | AudioProperty | <small>关卡数据</small>

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
