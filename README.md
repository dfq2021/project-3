# project-3
implement length extension attack for SM3, SHA256, etc.

# 实验步骤
1.在得到信息的长度和信息的hash值之后，我们先用零填充至分组的整数倍，再加入我们自定义的数据，根据MD结构，这样操作之后的hash值为以之前信息的hash值为IV，以自定义数据为信息的hash值

2.然后我们将第一步被填充和添加数据后的消息hash值与我们长度扩展攻击得到的hash值做对比，验证理论的正确性。

# 实验结果
![DACU{}%UD8CZ$GKFA77FA5B](https://github.com/jlwdfq/project-3/assets/129512207/950f2b37-02be-4ec6-96d1-bc00ea3912ee)
运行速度0.003s

# 实验环境
Windows10  

visual studio 2022

 CPU：11th Gen Intel(R) Core(TM) i7-11800H @ 2.30GHz
