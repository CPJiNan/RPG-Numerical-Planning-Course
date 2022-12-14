# 0.了解各类属性及其原理
## 序言
### 关于属性插件
本文档配套使用的属性插件为 [源属性OriginAttribute](https://www.mcbbs.net/thread-1248537-1-1.html)
( [MCBBS](https://www.mcbbs.net/thread-1248537-1-1.html) |
[Gitee](https://gitee.com/amazing-ocean-origin/origin-attribute) |
[插件文档](https://mc-origin.gitbook.io/originattribute/)  )
## 认识属性标签
> 属性标签列表来自[插件文档](https://mc-origin.gitbook.io/originattribute/attribute/attribute-overview/shu-xing-biao-qian)
### 攻击类属性
    //单次攻击对敌人造成的伤害，类型为物理
    物理攻击  <范围值> 或 <固定值>
    //单次攻击对敌人造成的伤害，类型为魔法
    魔法攻击  <范围值> 或 <固定值> 
    //单次攻击对敌人造成的伤害，对象为玩家
    PVP攻击  <范围值> 或 <固定值>  
    //单次攻击对敌人造成的伤害，对象为怪物
    PVE攻击  <范围值> 或 <固定值>  
    //使单次攻击造成伤害额外增加 攻击力 * 攻击力加成
    攻击力加成  <百分比> 
    //单次攻击触发暴击的概率
    暴击几率  <百分比>  
    //触发暴击时，使单次攻击造成伤害额外增加 加成后攻击力 * 暴击几率 * 暴击伤害
    暴击伤害  <百分比>  
    //单次攻击触发吸血的概率
    吸血几率  <百分比>  
    //触发吸血时，使单次攻击造成伤害的同时额外为玩家回复 实际伤害 * 吸血几率 * 吸血倍率
    吸血倍率  <百分比>  
    //敌人触发闪避时，无视敌人闪避强制对敌人造成伤害的概率
    抓取  <百分比>
### 防御类属性
    //单次受到伤害直接减少的数值，类型为物理
    物理防御  <范围值> 或 <固定值>
    //单次受到伤害直接减少的数值，类型为魔法
    魔法防御  <范围值> 或 <固定值>
    //单次受到伤害直接减少的数值，对象为玩家
    PVP防御  <范围值> 或 <固定值>
    //单次受到伤害直接减少的数值，对象为怪物
    PVE防御  <范围值> 或 <固定值>
    //使单次受到伤害直接额外减少 防御力 * 防御力加成
    防御力加成  <百分比>
    //单次受到攻击触发免疫全额伤害的概率
    闪避  <百分比>
    //使敌人对自己造成的吸血数额直接减少 吸血抗性
    吸血抗性  <固定值>
    //单次受到攻击触发格挡的概率
    格挡几率  <百分比>
    //触发格挡时，使单次受到伤害直接减少 敌人总攻击力 * 格挡倍率
    格挡倍率  <百分比>
    //触发格挡时，使单次受到伤害直接减少 格挡伤害
    格挡伤害  <固定值>
### 其他类属性
    //使生命值额外增加 生命上限
    生命上限  <固定值>
    //使生命值额外增加 实际生命上限 * 生命提升
    生命提升  <百分比>
    //使获得的经验值额外增加 获得经验 * 经验加成
    经验加成  <百分比>
    //使移动速度额外增加 移动速度 * 移速加成
    移速加成  <百分比>
### 属性读取格式
固定值读取格式

    物理攻击: 9
    物理攻击 + 9
    + 9 物理攻击

范围值读取格式

    物理攻击：9 - 15

百分比读取格式

    闪避: 100%
    闪避 + 100%