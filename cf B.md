
# B. Equations of Mathematical Magic
## 题目大意
- 就是解一个方程：a−(a⊕x)−x=0
## 解题思路 
- a−(a⊕x)−x=0 <==> a−(a^x)−x=0  <==>  x^a = x-a
- 如果运算符  ‘^’与 ‘-’起到相同的效果的话就是一个解
- 分析四种比较;
- 1^1=0   1-1=0
- 1^0=1   1-0=1
- 0^0=0   0-0=0，
- 0^1=1   0-1=-1
- 当a的二进制表示，如果这个位是1，则x对应的二进制对应的位数是0或者1都行；如果这个位是0，则x对应的二进制对应的位数只能是0。
- 所以，a的二进制表示有几个1就有2的几次方的情况。

## AC代码
```cpp
- #include <iostream>
- #include <cstdio>
- #include <cmath>
- using namespace std;

- int T;
- int main(){
- 	int a;
- 	int b;
- 	cin>>T;
- 	while(T--){
- 		int ans=1;
- 		scanf("%d",&a);
- 		int di=0;
- 		while(a){
- 			if(a&1){
- 				a/=2;
- 				di++;
- 			}
- 			else {
- 				a/=2;
- 			}
- 		}
- 	    ans=pow(2,di);
- 		printf("%d\n",ans);
- 	}
- } 
```

 
