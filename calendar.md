```c
#include <stdio.h>
#include <conio.h>

    
int returnDay(int day,int month,int year)
{   

    int y,y1,r,r2,r3,r4,r5,S;
    int day1[]={0,1,2,3,4,5,6};
    int month1[]={0,3,3,6,1,4,6,2,5,0,3,5};
    int year1[]={6,4,2,0,6};
    y1=year/100;
    r=y1%16;
    r2=year1[r];
    printf("Year:%d",r2);
    r3=year%100;
    r4=r3/4;
    r5=month1[month-1];
    printf("\nMonth:%d",r5);
    S=(r3+r4+r5+r2+day)%7;
    printf("\nDay:=%d",S);
    return S;
    /*
    if (S == 0)
        printf("\n Sunday \n");
    else if (S == 1)
        printf("\n Monday \n");
    else if (S == 2)
        printf("\n Tuesday \n");
    else if (S== 3)
        printf("\n Wednesday \n");
    else if (S == 4)
        printf("\n THURSDAY \n");
    else if (S == 5)
        printf("\n Friday \n");
    else
        printf("\n Saturday \n");
        */
}
int main(){
    int dayInt,monthInt,yearInt;
    int dowInt;
    printf("\n Enter a valid day:");
    scanf("%d", &dayInt);
    printf("\n Enter a valid month:");
    scanf("%d", &monthInt);
    printf("\n Enter a valid year:");
    scanf("%d", &yearInt);
    printf("\nSun\tMon\tTue\tWed\tThu\tFri\tSat\n");
    
    printf("\n------------------------------------------------------");
    dowInt=returnDay(dayInt,monthInt,yearInt);

    for(int i=1;i<=dowInt;i++)
      printf("\t");
    printf("%d",dayInt)  ;
    
    printf("\n------------------------------------------------------");
}

##OUTPUT
Enter a valid day:28
 Enter a valid month:8

 Enter a valid year:1975
Year:0
Month:2
Day:=4
------------------------------------------------------
Sun     Mon     Tue     Wed     Thu     Fri     Sat
                                28
------------------------------------------------------

```
