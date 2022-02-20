### 鸟随鸾凤飞腾远  人伴贤良品自高

## 2022.2.18  
在Github创建个人网站  
感谢苏秉楷，感谢Carl  

## 2022.2.18
这两天跟着Carl学了回溯算法。
回溯算法本质上就是暴力搜索，即仍为遍历，适用于解决排列、组合、子集一类的问题，其使用离不开递归调用。
for循环表示横向遍历，递归表示纵向遍历，直到遍历到叶子节点为止。  
  
回溯算法模板如下：  

void backtracking(vector<int>& v,vector<int>& vpath, int startIndex...)  
{  
  if(终止条件，例如vpath的大小达到题目要求，或者vpath中元素之和符合条件)  
  {  
     for(int i = 0; i < vpath.size(); i++)  
     {  
        cout << vpath[i]<< " ";  
     }  
     cout << endl;  
     return;  
  }  
  
  for(int i = startIndex; i < v.size(); i++)  
  {  
    //处理节点，例如vpath.pushback(v[i])，sum+=v[i]等  
  
    //递归  
    backtracking(v,vpath,startIndex...)//注意传入i还是i+1  
  
    //回溯  
    vpath.pop_back();  
    sum-=v[i];  
  }  
}  

2022.2.19  
在B站学会了怎么在overleaf打印出生僻字，并尝试写出一篇论文(材料是抄的)。  
问题: 1.摘要的Abstract怎么打印成中文;  
      2.小标题下怎么分点；  
      
2022.2.20
花了大半个晚上琢磨链表，还算满意。  
参考代码随想录的写法，独自写出了leetcode交换链表相邻两节点那道题。但是代码应该仍有改进的地方：对末尾几个节点的处理能否统一，即不根据链表的size就实现末尾节点的交换(偶数个就要把最后两个交换，奇数个就把倒数第二第三交换，最后一个不换)。  
     
2022.2.20晚23：09  
  简单看了一下哈希表，主要用来判断一个元素是否存在于集合中，其中unordered_set容器既可以排序，又可以去重。  
  注意包含头文件#include<unordered_set>;  
  构造函数：unordered_set<int> set(v.begin(), v.end());  
  
  还学会了一种for循环条件写法：  
  for(int i : set)//i表示set容器中的具体元素  
  {  
    if(set1.find(i)!=set1.end())//判断set中的元素是否出现在set1容器中，如果存在，返回当前元素的迭代器，否则返回.end()  
    {  
      
    }  
  }  
  
  
