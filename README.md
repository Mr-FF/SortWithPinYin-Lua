# SortWithPinYin-Lua
可用来实现lua中汉字字符串根据拼音排序

使用方法：
PinYinToWordStrTable仅作为字典配置，Word_Pin_Table表只需要在引入的时候生成一次，后续直接在Word_Pin_Table中取值。

比较单个字符：
通过word在转换出来的Word_Pin_Table表中取对应的拼音字母和在该读音中的index值，例如Word_Pin_Table["啊"]的值为"a3"，再根据获得的值进行字符串比较。

比较字符串：
使用getWords方法获取两个字符串的字符表，再逐个对应比较。

ps:拼音表中的文字整合了unicode和gbk的中文编码，做了一些剔除，还包含了一些日文或者韩文字符（考虑到玩家注册昵称时可能会使用该类文字= =）
