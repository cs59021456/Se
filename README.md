# Se
#include<stdio.h>
#include<time.h>
  
int main()
{
    time_t timer;
    struct tm* tm_info;
    char day[3];
    char month[3];
    char year[5];
      
    time(&timer);
    tm_info = localtime(&timer);
    strftime(day, 3, "%d", tm_info);
    strftime(month, 3, "%m", tm_info);
    strftime(year, 5, "%Y", tm_info);
      
    printf("\n\tToday is  %s/%s/%s\n", day, month, year);
    printf("\n Good luck\n");
    printf("May this day be a good day.");
      
    return 0;
}
