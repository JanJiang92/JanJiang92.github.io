---
title: interview_huawei
date: 2020-12-28 20:25:33
tags:
---

getline(cin, str)
1. sorting ASCII from small to large 
   1.1. violence, like the method "sort".
   1.2. hashmap + ASCII tablle
2. sorting string acorrding to dictionary order
   2.1 container: with the help of vector
3. the last word's length in a string 
   str.substr(position_begin, substr_len); when substr_len>str.size() output is just self.
   str.length();
4. counting the times of a character appearing
    {% codeblock %} isalpha()  tolower() islower() isupper() toupper() {% endcodeblock %}
5. 接受一个十六进制的数，输出该数值的十进制表示。
    #include<cmath>
    pow(16,bit++)
    str[i]-'A'+10
6. 图片整理(ASCII码值从小到大)常见ASCII码的大小顺序的规则是：0~9＜A~Z＜a~z
  sort(str.begin(),str.end());
7. 	蛇形矩阵
8. 生羊(dynamic programming(a kind of iteration))
9. 迷宫问题(backstepping(from top start, with a little recursive feeling in terms of data store),dynamic pro)
  backstepping:
      flag assign to 1
      push_back
      handling diff cases
      pop_back
      flag assign to 0

  2-dimensional assignment
       maze = vector<vector<int>>(N, vector<int>(M, 0));
       path_temp.clear();
       path_best.clear();
       for (auto &i : maze)
           for (auto &j : i)
               cin >> j;   

10.int型数据在内存中存储时1的个数
    m>>=1;; m&1

11. 数字颠倒
    #include<bits/stdc++.h> or #include<algorithm>
    s = to_string(num);
    reverse(s.begin(), s.end());

12. perfect_num 
   perfect_num= {6, 28, 496, 8128};

13. 杨辉三角的变形第一个偶数，找规律
14. 表达式求值
     {% codeblock %} isdigit {% endcodeblock %}
15.检查是否是闰年
   	{% codeblock %} if ((year % 4 == 0 && year % 100 != 0) || year % 400 == 0)
		return true;
    int a[] = { 31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31 };
    是闰年就多加1 {% endcodeblock %}
16.走方格的方案数
   dynamic or recursive

17. 最长回文子串或Redrainment走法
    dynamic pro
    attention:rightprt from 0 begin, and leftptr from 0 to rightprt
18.  质数因子
    加速方法: 	{% codeblock %} #include <math.h>     for(int i=2;i*i<=sqrt(num);) 
    {% endcodeblock %}
19  提取不重复的整数
    {% codeblock %}  if(mySet.count(aim) == 1) or s.find(a) == s.end()
      mySet.insert(aim);{% endcodeblock %}
20.  简单密码
     定义数组》{% codeblock %} //const string dict1="ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz";  {% endcodeblock %}
             //const string dict2="bcdefghijklmnopqrstuvwxyza22233344455566677778889999";
21. 迷宫问题
    #include <limits.h>  for INT_MAX
    vect.push_back( make_pair(arr[i],arr1[i]) );
    vector<vector<int>> tabVec(row,vector<int>(col,0));
        for(int i=0;i<row;i++)
            for(int j=0;j<col;j++){
                cin>>tabVec[i][j];
            }
22. 名字的漂亮度
    int n = sizeof(arr) / sizeof(arr[0]);
 
    /*Here we take two parameters, the beginning of the
    array and the length n upto which we want the array to
    be sorted*/
    sort(arr, arr + n);
    sort(countArr,countArr+26,[](int a,int b){return a>b;});

    map<int, int,greater <int>> gquiz1; Descending

23.  扑克牌大小
        (str.find("joker JOKER") != string::npos)
        size_t pos = str.find('-');
        string s1 = str.substr(0, pos);
        string s2 = str.substr(pos + 1);
24. 去重
    unique(ret.begin(), ret.end() 去重对相邻数据
    ret.erase(unique(ret.begin(), ret.end()), ret.end()); 去除后面无意义的部分

25.输入参数的立方根。保留一位小数。        printf("%.1lf",mid);

exprience:
    myvector.erase(it,it1); delete[it,it1)
    iterator used to iterate through the elements in the container
    问题出在 输出的第一个数也需要转十六进制

