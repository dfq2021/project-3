# project-3
implement length extension attack for SM3, SHA256, etc.
# 实验原理

长度扩展攻击是利用了SM3、SHA256、MD4、MD5、SHA-1、SHA-2这些hash算法的MD结构，在知晓信息的长度之下，可以在后续追加自定义信息来伪造有效hash值的一种攻击。

MD结构如图所示：
![pppp2](https://github.com/dfq2021/project-3/assets/129512207/0609ecf3-a62b-45db-83f5-ed7f9ecdfe92)


# 实验步骤
在知晓待hash的信息长度前提之下，在信息之后填充一定数量的零，直达信息长度为分组长度的整数倍，然后再添加自定义的信息，根据MD结构，这样操作之后的信息的hash值可以由以原先信息的hash值作为IV，新自定义信息作为待hash信息得到。我们将这样操作之后得到的hash值与plaintext||000...000||data_append的hash值做对比，若相同，则说明正确。

# 实验结果
![DACU{}%UD8CZ$GKFA77FA5B](https://github.com/jlwdfq/project-3/assets/129512207/950f2b37-02be-4ec6-96d1-bc00ea3912ee)
运行速度0.003s

# 实验环境
| 语言  | 系统      | 平台   | 处理器                     |
|-------|-----------|--------|----------------------------|
| Cpp   | Windows10 | VS2022 | Intel(R) Core(TM)i7-11800H |
# 小组分工
戴方奇 202100460092 单人组完成project3
