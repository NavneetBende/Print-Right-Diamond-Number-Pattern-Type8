PRINTING PATTERN:
2

34

567

891011

891011

567

34

2

PREREQUISITE:
Basic knowledge of C language and use of loops.

ALGORITHM:
Take the number of rows as input from the user and store it in any variable.(‘r‘ in this case).
Run a loop ‘r’ number of times to iterate through each of the rows. From i=0 to i<r. The loop should be structured as for( i=0 ; i<r : i++).
Use an if condition to to print the top half of the pyramid. if (i<=r/2). Then intialise count1=count+1 and Then run a loop from j=0 to j<=i. The loop should be structured as for(j=0 ; j<=i ; j++)
Inside this loop increment count and print it.
Outside this loop print a newline.
Else initialise count=count1;
Run a different loop from j=i to j<r-i. The loop should be structured as for( j=i ; j<r-i ; j++).
Inside this loop print count and increment it
outside the loop modify the value of count1 as count1=count1-(r-i)+1
then print a newline
CODE IN C:
#include<stdio.h>
int main()
{
int i,j,r,count,count1;                        //declaring integer variables i,j for loops , r for number of rows and count for increment in value
count=1; //initialising count
printf("Enter the number of rows(even) :\n");  //Asking user for input
scanf("%d",&r);                                //taking number of rows and saving it in variable r
for(i=0;i<r;i++)                               // loop for number of rows
  {
    if(i<r/2)  
     {
       count1=count+1;
       for(j=0;j<=i;j++)                       // loop for digits per each row
         {
           count++;                             //incrementing count
           printf("%d",count);                  //printing digits
         }
       printf("\n");                           // printing newline after each row
     }    
    else                                       //else condition for bottom half
     {
       count=count1;                           //copying value
       for(j=0;j<r-i;j++)                      //loop to print digits 
         {
           printf("%d",count);                 //printing digits
           count++;                            //incrementing count
         }
       count1=count1-(r-i)+1;                  //copying value
       printf("\n");                           //printing newline
     }

  } 

}
TAKING INPUT:


DISPLAYING OUTPUT:
