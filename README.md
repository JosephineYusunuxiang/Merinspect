# Merinspect 观察助手_classic_era_附魔全修复版
    
# 请将压缩包里的MerInspect和InstanceLockeddownTimer两个文件夹放入World of Warcraft\_classic_era_\Interface\AddOns一并加载。  

# 有任何附魔错误欢迎在github留言、论坛回复或给我发邮件，期待您的意见！   
  
  重大喜讯！我修好了毒性软泥--(bushi)  
  MerInspect_classic_era_版附魔显示已完全修复。  
  本版插件只适配1.14.3版本游戏！其他大版本游戏数据库没有整理添加。 
  
  目前这版插件生效必须配合加载以下任意一款网易插件： 
  !!!163UI!!!网易有爱控制台、 
  alaChat_Classic聊天插件（旧版）、  
  alaTrade拍卖行插件、  
  alaMisc实用小功能、 
  InstanceLockeddownTimer 有爱爆本计时器。  
  
  有爱离线包地址https://wowui.w.163.com/163ui/   
  仅需要离线压缩包里任意一款即可。   
  
  玉素奴香@哈霍兰CN  
  个人仓库https://github.com/JosephineYusunuxiang/MerInspect  
  
  -------------------------------------------------------  
  
  --tips--1--2023--03--17--  
  --本版Merinspect插件为适配_classic_era_1.14.3版本游戏而修复  
  --修了几条数值相同位置对应错误的附魔技能&物品ID，发现是同一附魔ID对应多个部位附魔技能。  
  --数据对应结构是这样的：附魔ID(enchant)--附魔技能ID(spell)--附魔道具ID(item)--学习附魔技能ID(spell)--附魔技能书物品ID(item)   
  --后三个不一定每种附魔都有，比如很多附魔是训练师直接教的，没有最后一步；而_classic_era_版本没有附魔羊皮纸，基本不会有附魔道具；头腿肩NPC卖的附魔没后两步。  
  --个人猜测这个类似于暗黑2属性词条，至少在_classic_era_版本，同一数值属性是个唯一性光环（enchant，类似于aura）,被多个部位引用。  
  --怪不得这插件十几年过了这么多大佬的手还是这个鸟样。真是个天坑。  
  
    
  --tips--2--  
  --via 暧昧的呓语@https://bbs.nga.cn/read.php?tid=33886174 大佬的帖子里学习到了处理分支的方法。  
  --利用了大佬v1.2版本的\MerInspect\libs\LibItemEnchant.lua数据库文件。  
  --重新整理排序了_era_版本的附魔相关内容  
  --所以本插件仅适用于_era_版本游戏  
  
    
  --tips--3--  
  --游戏主lua套件使用的是 Qcat@http://wowcat.net/bbs/new/topic/1631-1 猫站长大佬的版本，似乎19年在那里下载这个后我这里一直就没有被更新覆盖过，原站网盘链接都无了哈哈……  
  --因为我找到的所有后续版本C面板角色属性统计中，都有很多条目不显示了，比如法术命中、物理命中等。  
  --而且这些版本似乎脱依赖库都没弄干净，也一样需要诸如有爱控制台、大脚控制台所带的依赖库。否则1.14.3版本游戏单独测试插件，可以载入，但不能显示装备统计和属性统计面板。  
  --现在其他面板插件、WA字符串，法术命中、物理命中、治疗强度等面板统计都不能反馈出数值，GetSpellHitModifier()\GetHitModifier()\GetSpellBonusHealing()这几个API都失效了。  
  --我手里这版本插件能统计出这几项数值，本人研究插件刚起步水平很差，没有能力寻么它是咋实现的，和其他版本插件区别在哪。  
  --所以插件能用能正常显示就不再继续深入脱库了。而且设置生效似乎也不太灵光，这个也没能力深入研究了。  
  
    
  --tips--4--  
  --本版Merinspect需要配合配合加载以下任意一款网易插件，才能正常工作，否则单独Merinspect插件在1.14.3版本游戏不能显示统计面板：  
  --!!!163UI!!!网易有爱控制台、  
  --alaChat_Classic聊天插件（旧版）、  
  --alaTrade拍卖行插件、  
  --alaMisc实用小功能、  
  --InstanceLockeddownTimer 有爱爆本计时器。  
  --有爱离线包地址@https://wowui.w.163.com/163ui/   
  --大脚控制台我试过了不能行。  
  --似乎是这几款网易插件里的\ala\fix.lua脚本起了作用。不过单独在Merinspect.toc里加载这个lua并不能完全正常工作，这样C面板装备统计可以显示，但属性统计不行。还是要正常使用任意一款。  
  --不按此条说明使用，插件不生效概不负责！！（因为没有盘代码函数的能力）！！除非您有能力自己处理代码。  
  
    
  --tip--5--  
  --再次感谢 暧昧的呓语@NGA大佬修复的后续大版本适配版。我这里其实就是吃了他现成的思路，把这个数据库缝合到另外一版插件里。各位如果需要下载woltk版Merinspect可以到上面他的帖子中下载。   --欢迎各位观众姥爷二次开发，望有兴趣的大佬可以继续整理把主lua处理干净~  
  --万分感谢前人的研究整理。  
