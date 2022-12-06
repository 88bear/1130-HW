# 1130-HW

## [C_AR022-易] 字母出現的頻率

```c
#include <stdio.h>  
#include <stdlib.h>  
  
int main(){  
    int result[26] = {0};  
    char ch;  
    int temp;  
    while(1){  
        ch = getchar();  
        if(ch >= 'A' && ch <= 'Z' ){  
            temp = ch - 'A';  
            result[temp]++;  
        }  
        if(ch >= 'a' && ch <= 'z'){  
            temp = ch - 'a';  
            result[temp]++;  
        }  
        if(ch == '\n' || ch == EOF)  
            break;  
    }  
    printf("%d",result[0]);  
    for(int i = 1; i<26; i++){  
        printf(" %d",result[i]);  
    }  
    printf("\n");  
    return 0;  
}  
```
----------
## [C_AR76-易] 提款機程式

```c
#include <stdio.h>  
#include <stdlib.h>

int main(){
    int data[6][3] = {  
        {123, 456, 9000},  
        {456, 789, 5000},  
        {789, 888, 6000},  
        {336, 558, 10000},  
        {775, 666, 12000},  
        {566, 221, 7000}  
    };
    int n;
    int acc[10],pw[10];
    scanf("%d",&n);
    for(int i = 0; i < n; ++i){
        scanf("%d %d",&acc[i],&pw[i]);
    }
    for(int j = 0; j < n; ++j){
        int f = 0;
        for(int k = 0; k < 6; ++k){
            if(acc[j] == data[k][0] && pw[j] == data[k][1]){
                printf("%d\n",data[k][2]);
            }  
            else{  
                f++;  
            }  
        }
        if(f == 6){  
            printf("error\n");
        }
    }
    return 0;
}
```
------------
## [C_AR20-易] 檢查數值是否有重複

```c
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
  
int main(int argc, char *argv[]){  
   int n,cnt;
   scanf("%d",&n);  
   int str[130];
   for(int s=0; s<n; s++){  
      scanf("%d",&str[s]);  
   }
   for(int i=0; i<n; i++){  
      for(int j=0; j<n; j++){    
         if(str[i] == str[j])  
            cnt++;  
      }  
   }  
   if( (cnt-n) >= 1)  
      printf("0\n");  
   else  
      printf("1\n");  
}
```

```c
#include <stdio.h>   
#include <stdlib.h> 
 
int main(){ 
    int n; 
    scanf("%d",&n); 
    int num[n];   
    int count[2000000];   
    int cou = 0;   
    for(int i = 0; i < 2000000; i++){ 
        count[i] = 0;   
    } 
    for(int i = 0; i < n; ++i){   
        scanf("%d",&num[i]); 
        if(count[num[i]] == 0){ 
            count[num[i]]++;   
        } 
    } 
    for(int i = 0; i < 2000000; i++){ 
        if(count[i] == 1){ 
            cou++; 
        } 
    } 
    if(cou == n){   
        printf("1\n"); 
    }   
    else{   
        printf("0\n");   
    }       
    return 0;   
}  
```
