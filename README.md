# multi-value-return-from-funcation 

#include <stdio.h>

#include <stdlib.h>

int math (int ,int ,int*,int*,int*);


int main()

{

int a =5;

int b=10;

int sum ;

int sub ;

int multi;

int status ;

status = math(a,b,&sum,&sub,&multi);


if (status = 0){


    printf("something wrong");
    

}

else{

printf("addtion= %d \nsubtraction= %d\nmultiplication= %d",sum,sub,multi);

}

return 0;

}
int math (int x,int y,int* sum ,int* sub ,int* multi ){


if(sum == NULL || sub == NULL|| multi == NULL){


    return 0;
    
}

else{

*sum = x+y;

*sub = x-y;

*multi = x*y;

}

return 1;


}

