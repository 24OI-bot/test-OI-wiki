从状态图上起点和终点同时开始进行宽度/深度优先搜索，如果发现相遇了，那么可以认为是获得了可行解。

双向广搜的步骤

```text
开始结点 和 目标结点 入队列 q
标记开始结点为 1
标记目标结点为 2
while(队列q不为空)
{
  从 q.front() 扩展出新的s个结点
  
  如果 新扩展出的结点已经被其他数字标记过
    那么 表示搜索的两端碰撞
    那么 循环结束
  
  如果 新的s个结点是从开始结点扩展来的
    那么 将这个s个结点标记为1 并且入队q 
    
  如果 新的s个结点是从目标结点扩展来的
    那么 将这个s个结点标记为2 并且入队q
}
```
