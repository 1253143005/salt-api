
?> [返回 Simple](md/scripts/simple.md)

> 存储管理器，进行存档的存储，获取，备份等操作。

## 控制方法 :id=static

> 控制方法

类 |  说明
-------- |  -----
<small>[Create](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=Create)</small>  | <small>初始化存档管理器，需要在所有的应用之前调用</small>
<small>[Has](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=has)</small>  | <small>在存档中是否存在指定键</small>
<small>[Delete](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=delete)</small>  | <small>在存档中删除指定键的存档</small>
<small>[Save](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=save)</small>  | <small>将存档的缓存修改确实写入存储中</small>
<small>[Backup](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=backup)</small>  | <small>将存档备份到指定文件中</small>
<small>[Restore](md/scripts/Simple/SimpleSaveManager/runtime/Control.md?id=restore)</small>  | <small>将指定存档恢复</small>

## 存储加载方法 :id=setget

> 控制方法

类 |  说明
-------- |  -----
<small>[SetInt](md/scripts/Simple/SimpleSaveManager/runtime/SetInt.md?id=set)</small>  | <small>将int值存储到key下</small>
<small>[GetInt](md/scripts/Simple/SimpleSaveManager/runtime/SetInt.md?id=get)</small>  | <small>从key下加载int值</small>
<small>[SetString](md/scripts/Simple/SimpleSaveManager/runtime/SetString.md?id=set)</small>  | <small>将string值存储到key下</small>
<small>[GetString](md/scripts/Simple/SimpleSaveManager/runtime/SetString.md?id=get)</small>  | <small>从key下加载string值</small>
<small>[SetBool](md/scripts/Simple/SimpleSaveManager/runtime/SetBool.md?id=set)</small>  | <small>将bool值存储到key下</small>
<small>[GetBool](md/scripts/Simple/SimpleSaveManager/runtime/SetBool.md?id=get)</small>  | <small>从key下加载bool值</small>
<small>[SetFloat](md/scripts/Simple/SimpleSaveManager/runtime/SetFloat.md?id=set)</small>  | <small>将float值存储到key下</small>
<small>[GetFloat](md/scripts/Simple/SimpleSaveManager/runtime/SetFloat.md?id=get)</small>  | <small>从key下加载float值</small>

## Editor

?> [打开 设置](md/installation.md?id=工具tab)

![](SimpleSaveManager_md_files/f31d4300-d1f4-11ed-afb0-c340f1571a81.jpeg?v=1&type=image)

***注：存档文件名可以填入路径：save/file，则表示在存储路径下创建SAVE/file文件***
