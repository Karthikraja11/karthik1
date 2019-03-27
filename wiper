#include <stdio.h>
#include <stdlib.h>
int manual(int);
void autom(int);
int battery=90;
//enum level {LOW=35,MED=45,HIGH=50};
int main()
{
    int manualbutton,sensorvalue;
    printf("Enter Manual/Auto mode\n");
    scanf("%d",&manualbutton);
    if(manualbutton==1)
    {
    printf("beforecall %d\n",battery);
       battery=manual(battery);
        printf("aftercall %d\n",battery);

       if(battery<=25)
        printf("Low battery,,,,,Kindly Recharge it\n");
    }
    else
    {
     printf("Enter the sensor value 0-1024");
     scanf("%d",&sensorvalue);
     autom(sensorvalue);
    }

    return 0;
}
int manual(int bat)
{
    int inputlevel;
    printf("Enter the level as 35 R 45 R 60");
    scanf("%d",&inputlevel);
    if(bat>=90)
    {
        printf("High wiper can be done\n");
    if(inputlevel==35)
        {printf("1");
        bat=bat-25;}
    else if(inputlevel==45)
        {printf("2");
        bat=bat-50;}
    else if(inputlevel==60){
        printf("3");
        bat=bat-75;}
    }
    else if (bat>75&&bat<90)
    {
    printf("medium wiper can be done\n");
        if(inputlevel==35)
        bat=bat-25;
        else if(inputlevel==45)
        bat=bat-50;
    }
    else
    {
        printf("Low wiper can be done\n");
        if(inputlevel==35)
        bat=bat-25;
    }

return bat;
}
void autom(int sensorvalue)
{
    if(sensorvalue<=50)
            printf("Duty cycle=0%\n");
     else if(sensorvalue>50&&sensorvalue<=250)
            printf("Duty cycle=25%\n");
    else if(sensorvalue>250&&sensorvalue<=1000)
            printf("Duty cycle=50%\n");
    else if(sensorvalue>1000&&sensorvalue<=1024)
            printf("Duty cycle=75%\n");
}
