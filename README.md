#include<stdio.h>
#include<stdlib.h>
#include<string.h>
#include<time.h>
void input();
void display();
struct student{
char name[50];
int sem;
long int id;
float fee_paid;
float bal;

};
struct student s;
FILE *fp;
long sz = sizeof(s);

int main()
{
    int ch;
    while(1)
    {
        system("cls");
        printf("<== College Fee Management ==> \n");
        printf("1.  Addition \n");
        printf("2. Searching \n");
        printf("3. Sorting \n");
        printf("4. Deletion \n");

        printf("5. Generate report \n");
        printf("Enter your choice\n");
        scanf("%d",&ch);
 while(getchar() != '\n');
        switch(ch)
        {

            case 0: exit(0);
            break;

            case 1: input();
                    break;

            case 2: display();
                    break;
        }
printf("Enter any key to continue");

getchar();
getchar();

    }
    return(0);
}

void input()
{
  fp = fopen("stud.txt","a");
  memset(&s, 0, sizeof(s));

    printf("Enter student name: ");
    fgets(s.name, sizeof(s.name), stdin);
    s.name[strcspn(s.name, "\n")] = 0;


  printf("Enter Student Id ");
  scanf("%ld",&s.id);
  printf("Enter Semester");
  scanf("%d",&s.sem);
  printf("Enter fee paid");
  scanf("%f",&s.fee_paid);
  printf("Enter balance");
  scanf("%f",&s.bal);
   fprintf(fp, "%s|   %ld|    %d  |  %.2f |   %.2f\n",
            s.name, s.id, s.sem, s.fee_paid, s.bal);
  printf("Record Saved Successfully\n");
    fclose(fp);

}
void display()
{

}

