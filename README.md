#include<stdio.h>
#include<stdlib.h>
#include<time.h>
struct student{
char name[50];
int sem;
long int id;
long int fee_paid;
long int bal;

}s;
FILE *fp;
long sz = sizeof(s);

int main()
{
    int ch;
    while(1)
    {
        system("cls");
        printf("<== College Fee Management ==> ");
        printf("1.  Addition ");
        printf("2. Searching ");
        printf("3. Sorting ");
        printf("4. Deletion ");
        
        printf("5. Generate report ");
        printf("Enter your choice\n");
        scanf("%d",&ch);
        
        switch(ch)
        {
            
            case 0: exit(0);
            
            case 1: input();
                    break;
                    
            case 2: display();
                    break;     
        }
        

getchar();

    }
    return(0);
}

void input()
{
  fp = fopen("stud.txt","ab"); 
  printf("Enter student name\n");
  fgets(s.na,50,stdin);
  printf("Enter Student Id ) 
    
}
