# COMP3411-9814-A3-Nine-Board-Tic-Tac-Toe
# COMP3411/9814 A3 Nine Board Tic Tac Toe 1v1 远程辅导、讲题和VIP定制服务 保证原创 严厉拒绝一份多售
# 源头导师 科班出身 非中介甩单！
# VX: csprojhelp 备注：github

【重点解析】：

九宫格版的 Tic Tac Toe：当上一个人在 cell 处落子后，下一个人会被传送到大棋盘里对应 cell 的小棋盘上，然后在那个小棋盘里找地方落下一子。获胜者为在任意小棋盘中首先连到 3 子的人，3行+3列+2对角线一共有 8 种连子方式。

starter code 框架提供了游戏服务器 servt ，游戏AI lookt，你需要编写自己的AI agent 。servt 在指定 port 开启游戏，lookt 和 agent 连接上相同 port 后开始对弈。

算法大框架没啥好说的，经典 minmax algorithm + alpha beta pruning。难点在于选择合适的 heuristic function 为 leaf nodes 估值，好的估值函数才能使 minmax 做出高质量的下一步选择。

注意到游戏思考时间规则为：初始每人 30 秒，之后每一步增加 2 秒，时间是累积使用的。当某人时间用完而游戏还未结束时，timeout 的人被判失败。一个提高算法性能的 trick 是：为游戏划分阶段，然后为不同阶段分配不同的合理时间而不是傻傻地均匀分配。

================================================

欢迎有需要辅导的同学dd～
