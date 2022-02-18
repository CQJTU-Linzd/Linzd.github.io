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

下学期跟着代码随想录学算法。
