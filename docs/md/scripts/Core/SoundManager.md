
?> [返回 Core](md/scripts/core.md)

> 声音管理器。

## 属性 :id=param

> 静态引用

类 | 类型 | 赋值/获取 |  说明
-------- |  ----- |  -----|  -----
<small>activeSave</small>  | <small>bool</small> | <small>set/get</small> | <small>激活存储</small>
<small>showLog</small>  | <small>bool</small> | <small>set/get</small> | <small>设置是否显示log</small>
<small>globalUIButtonClickSoundID</small>  | <small>string</small> | <small>set/get</small> | <small>点击按钮的全局音效ID</small>
<small>defaultClickSoundID</small>  | <small>string</small> | <small>get</small> | <small>默认点击音效</small>
<small>mute</small>  | <small>bool</small> | <small>set/get</small> | <small>静音</small>
<small>backgroundMute</small>  | <small>bool</small> | <small>set/get</small> | <small>失去焦点的时候是否静音</small>
<small>volumeAll</small>  | <small>float</small> | <small>set/get</small> | <small>总声音音量</small>
<small>volumeMusic</small>  | <small>float</small> | <small>set/get</small> | <small>音乐音量</small>
<small>volumeSFX</small>  | <small>float</small> | <small>set/get</small> | <small>音效音量</small>

## 方法 :id=func

类 |  说明
-------- |  -----
<small>[GetInstance](md/scripts/Core/SoundManager.md?id=GetInstance)</small>  | <small>获取单例，此类只可以使用此方法来实例化</small>
<small>[HasMusic](md/scripts/Core/SoundManager.md?id=HasMusic)</small>  | <small>音乐是否存在</small>
<small>[GetMusic](md/scripts/Core/SoundManager.md?id=GetMusic)</small>  | <small>获取音乐</small>
<small>[AddMusic](md/scripts/Core/SoundManager.md?id=AddMusic)</small>  | <small>将音乐增加在声音管理器上</small>
<small>[PlayMusic](md/scripts/Core/SoundManager.md?id=PlayMusic)</small>  | <small>播放音乐</small>
<small>[StopMusic](md/scripts/Core/SoundManager.md?id=StopMusic)</small>  | <small>停止音乐播放</small>
<small>[RemoveMusic](md/scripts/Core/SoundManager.md?id=RemoveMusic)</small>  | <small>移除音乐</small>
<small>[RemoveMusices](md/scripts/Core/SoundManager.md?id=RemoveMusices)</small>  | <small>移除音乐</small>
<small>[RemoveAllMusic](md/scripts/Core/SoundManager.md?id=RemoveAllMusic)</small>  | <small>移除所有音乐</small>
<small>[HasSFX](md/scripts/Core/SoundManager.md?id=HasSFX)</small>  | <small>音效是否存在</small>
<small>[GetSFX](md/scripts/Core/SoundManager.md?id=GetSFX)</small>  | <small>获取音效</small>
<small>[AddSFX](md/scripts/Core/SoundManager.md?id=AddSFX)</small>  | <small>将音效增加在声音管理器上</small>
<small>[PlaySFX](md/scripts/Core/SoundManager.md?id=PlaySFX)</small>  | <small>播放音效</small>
<small>[RemoveSFX](md/scripts/Core/SoundManager.md?id=RemoveSFX)</small>  | <small>移除音效</small>
<small>[RemoveSFXes](md/scripts/Core/SoundManager.md?id=RemoveSFXes)</small>  | <small>移除音效</small>
<small>[RemoveAllSFX](md/scripts/Core/SoundManager.md?id=RemoveAllSFX)</small>  | <small>移除所有音效</small>
<small>[HasSound](md/scripts/Core/SoundManager.md?id=HasSound)</small>  | <small>声音是否存在</small>
<small>[GetSound](md/scripts/Core/SoundManager.md?id=GetSound)</small>  | <small>获取音音</small>
<small>[AddSound](md/scripts/Core/SoundManager.md?id=AddSound)</small>  | <small>将音音增加在声音管理器上</small>
<small>[SetCategoryVolume](md/scripts/Core/SoundManager.md?id=SetCategoryVolume)</small>  | <small>设置指定目录的音量</small>
<small>[GetCategoryVolume](md/scripts/Core/SoundManager.md?id=GetCategoryVolume)</small>  | <small>获取指定目录的音量</small>
<small>[PlaySound](md/scripts/Core/SoundManager.md?id=PlaySound)</small>  | <small>播放声音</small>
<small>[RemoveSound](md/scripts/Core/SoundManager.md?id=RemoveSound)</small>  | <small>移除声音</small>
<small>[RemoveSounds](md/scripts/Core/SoundManager.md?id=RemoveSounds)</small>  | <small>移除声音</small>
<small>[RemoveCategory](md/scripts/Core/SoundManager.md?id=RemoveCategory)</small>  | <small>移除声音列表</small>
<small>[GetSoundVolumes](md/scripts/Core/SoundManager.md?id=GetSoundVolumes)</small>  | <small>获取对应列表的声音音量</small>
<small>[Play3DSound](md/scripts/Core/SoundManager.md?id=Play3DSound)</small>  | <small>播放3D音效</small>
<small>[PauseSound](md/scripts/Core/SoundManager.md?id=PauseSound)</small>  | <small>暂停声音</small>
<small>[PauseAll](md/scripts/Core/SoundManager.md?id=PauseAll)</small>  | <small>暂停所有声音</small>
<small>[ResumeAll](md/scripts/Core/SoundManager.md?id=ResumeAll)</small>  | <small>恢复所有声音</small>
<small>[StopAll](md/scripts/Core/SoundManager.md?id=StopAll)</small>  | <small>停止所有声音</small>
<small>[ClearAllSaves](md/scripts/Core/SoundManager.md?id=ClearAllSaves)</small>  | <small>清空所有声音存档</small>

## 方法展示

### GetInstance() :id=GetInstance

> 获取单例，此类只可以使用此方法来实例化

***例子***
``` csharp
SoundManager manager = SoundManager.GetInstance();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### HasMusic(string name) :id=HasMusic

> 音乐是否存在

***例子***
``` csharp
string musicID = "test";
bool musicIsExist = SoundManager.HasMusic(musicID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### GetMusic(string name) :id=GetMusic

> 获取音乐

***例子***
``` csharp
string musicID = "test";
AudioClip musicAudioClip = SoundManager.GetMusic(musicID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### AddMusic(string name, AudioClip audioClip) :id=AddMusic

> 将音乐增加在声音管理器上

***例子***
``` csharp
string musicID = "test";
AudioClip musicAudioClip; //增加的音乐的数据流
SoundManager.AddMusic(musicID, musicAudioClip);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### PlayMusic(string id) :id=PlayMusic

> 播放音乐

***例子***
``` csharp
string musicID = "test";
AudioClip playedMusic = SoundManager.PlayMusic(musicID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### StopMusic() :id=StopMusic

> 停止音乐播放

***例子***
``` csharp
SoundManager.StopMusic();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveMusic(string soundID) :id=RemoveMusic

> 移除音乐

***例子***
``` csharp
string musicID = "test";
bool isSuccessRemoved = SoundManager.RemoveMusic(musicID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveMusices(string[] soundIDs) :id=RemoveMusices

> 移除音乐

***例子***
``` csharp
string[] musicIDs = new string[] {"test"};
bool isSuccessRemoved = SoundManager.RemoveMusices(musicIDs);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveMusices(List< string > soundIDs) :id=RemoveMusices

> 移除音乐

***例子***
``` csharp
List<string> musicIDs = new List<string>() {"test"};
bool isSuccessRemoved = SoundManager.RemoveMusices(musicIDs);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveAllMusic() :id=RemoveAllMusic

> 移除所有音乐

***例子***
``` csharp
SoundManager.RemoveAllMusic();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### HasSFX(string name) :id=HasSFX

> 音效是否存在

***例子***
``` csharp
string sfxID = "test";
bool sfxIsExist = SoundManager.HasSFX(sfxID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### GetSFX(string name) :id=GetSFX

> 获取音效

***例子***
``` csharp
string sfxID = "test";
AudioClip sfxAudioClip = SoundManager.GetSFX(sfxID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### AddSFX(string name, AudioClip audioClip) :id=AddSFX

> 将音效增加在声音管理器上

***例子***
``` csharp
string sfxID = "test";
AudioClip sfxAudioClip; //增加的音乐的数据流
SoundManager.AddSFX(sfxID, sfxAudioClip);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### PlaySFX(string id, float spatialBlend = 0) :id=PlaySFX

> 播放音效

***例子***
``` csharp
string sfxID = "test";
float spatialBlend = 0; //3D效果 [0, 1]越接近1越有3D效果
AudioClip playedSFX = SoundManager.PlaySFX(sfxID, spatialBlend);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSFX(string soundID) :id=RemoveSFX

> 移除音效

***例子***
``` csharp
string sfxID = "test";
bool isSuccessRemoved = SoundManager.RemoveSFX(sfxID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSFXes(string[] soundIDs) :id=RemoveSFXes

> 移除音效

***例子***
``` csharp
string[] sfxIDs = new string[] {"test"};
bool isSuccessRemoved = SoundManager.RemoveSFXes(sfxIDs);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSFXes(List< string > soundIDs) :id=RemoveSFXes

> 移除音效

***例子***
``` csharp
List<string> sfxIDs = new List<string>() {"test"};
bool isSuccessRemoved = SoundManager.RemoveSFXes(sfxIDs);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveAllSFX() :id=RemoveAllSFX

> 移除所有音效

***例子***
``` csharp
SoundManager.RemoveAllSFX();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### HasSound(string name, string categoryName) :id=HasSound

> 声音是否存在

***例子***
``` csharp
string soundID = "test";
string categoryName = "category"; //声音所在的列表
bool soundIsExist = SoundManager.HasSound(soundID, categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### GetSound(string name, string categoryName) :id=GetSound

> 获取声音

***例子***
``` csharp
string soundID = "test";
string categoryName = "category"; //声音所在的列表
AudioClip soundAudioClip = SoundManager.GetSound(soundID, categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### AddSound(string name, AudioClip audioClip, string categoryName, bool isLoop, float MinTimeBetweenPlayCalls = 0.05f) :id=AddSound

> 将声音增加到指定声音列表上

***例子***
``` csharp
string soundID = "test";
AudioClip soundAudioClip; //声音的数据流
string categoryName = "category"; //声音所在的列表
bool isLoop = false; //是否循环
float MinTimeBetweenPlayCalls = 0.05f; //相同audioclip最短播放时间间隔
SoundManager.AddSound(soundID, soundAudioClip, categoryName, isLoop, MinTimeBetweenPlayCalls);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### SetCategoryVolume(string categoryName, float volume) :id=SetCategoryVolume

> 设置指定目录的音量

***例子***
``` csharp
string categoryName = "category"; //声音所在的列表
float volume = 1f; //音量
SoundManager.SetCategoryVolume(categoryName, volume);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### GetCategoryVolume(string categoryName) :id=GetCategoryVolume

> 获取指定目录的音量

***例子***
``` csharp
string categoryName = "category"; //声音所在的列表
float categoryVolume = SoundManager.GetCategoryVolume(categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### PlaySound(string id, string categoryName, float spatialBlend = 0) :id=PlaySound

> 播放声音

***例子***
``` csharp
string soundID = "test";
string categoryName = "category"; //声音所在的列表
float spatialBlend = 0f; //3D效果 [0, 1]越接近1越有3D效果
AudioObject playedSoundAudioClip = SoundManager.PlaySound(soundID, categoryName, spatialBlend);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSound(string soundID, string categoryName) :id=RemoveSound

> 移除声音

***例子***
``` csharp
string soundID = "test";
string categoryName = "category"; //声音所在的列表
bool isSuccessRemoved = SoundManager.RemoveSound(soundID, categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSounds(string[] soundIDs, string categoryName) :id=RemoveSounds

> 移除声音

***例子***
``` csharp
string[] soundIDs = new string[] {"test"};
string categoryName = "category"; //声音所在的列表
bool isSuccessRemoved = SoundManager.RemoveSounds(soundIDs, categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveSounds(List<string> soundIDs, string categoryName) :id=RemoveSounds

> 移除声音

***例子***
``` csharp
List<string> soundIDs = new List<string>() {"test"};
string categoryName = "category"; //声音所在的列表
bool isSuccessRemoved = SoundManager.RemoveSounds(soundIDs, categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### RemoveCategory(string categoryName) :id=RemoveCategory

> 移除声音列表

***例子***
``` csharp
string categoryName = "category"; //声音所在的列表
bool isSuccessRemoved = SoundManager.RemoveCategory(categoryName);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>

### GetSoundVolumes() :id=GetSoundVolumes

> 获取对应列表的声音音量

***例子***
``` csharp
Dictionary<string, float> categorySounds = new Dictionary<string, float>(); //声音列表的音量
categorySounds  = SoundManager.GetSoundVolumes();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### Play3DSound(string id, Transform parent, Vector3 position, float range, string categoryName = SFX, float spatialBlend = 1) :id=Play3DSound

> 播放3D音效

***例子***
``` csharp
string soundID = "test";
Transform parent; //声音的父节点容器
Vector3 position; //声音播放位置
float range; //响应半径
string categoryName = "SFX"; //声音所在的列表
float spatialBlend = 0f; //3D效果 [0, 1]越接近1越有3D效果
AudioObject playedSoundAudioClip = SoundManager.Play3DSound(soundID, parent, position, range, categoryName, spatialBlend);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### PauseSound(string id) :id=PauseSound

> 暂停声音

***例子***
``` csharp
string soundID = "test";
List<AudioObject> pausedAudioClips = SoundManager.PauseSound(soundID);
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### PauseAll() :id=PauseAll

> 暂停所有声音

***例子***
``` csharp
SoundManager.PauseAll();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### ResumeAll() :id=ResumeAll

> 恢复所有声音

***例子***
``` csharp
SoundManager.ResumeAll();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### StopAll() :id=StopAll

> 停止所有声音

***例子***
``` csharp
SoundManager.StopAll();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>


### ClearAllSaves() :id=ClearAllSaves

> 清空所有声音存档

***例子***
``` csharp
SoundManager.ClearAllSaves();
```
<small>[- 返回 -](md/scripts/Core/SoundManager.md?id=func)</small>



