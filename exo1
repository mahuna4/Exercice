#include <stdio.h>
#include <string.h>
#include <stdlib.h>
#include <unistd.h>
#include <sys/types.h>
#include <sys/wait.h>

int main(int argc, char *argv[])
{
 int status;
   pid_t pid1,pid2,pid3;
   pid1=fork();
 if(pid1<0)
{
   printf("Erreure,le premier fils n'est pas créer\n");
   exit(EXIT_FAILURE);
}

if(pid1==0)

{
	printf("Pid du premier est: %d \n",getpid());

}

else

{
    pid2=fork();
    if(pid2<0)
    {
	printf("Erreure,le second fils n'est pas créer\n");
	exit(EXIT_FAILURE);
    }
    if(pid2==0)
    {
      printf("pid du seconde est : %d \n",getpid());
   }
   else
  {
   pid3=fork();
    if(pid3<0)
    {
	printf("Erreure,le troisieme fils n'est pas créer\n");
	exit(EXIT_FAILURE);
    }
    if(pid3==0)
     {
        printf("pid du troisieme est : %d \n",getpid());
        printf("\n");
     }
     else
     {
	        pid1 = wait(&status);
                printf("Status de l'arret du fils %d %d\n", status, pid1);
                pid2 = wait(&status);
                printf("Status de l'arret du fils %d %d\n", status, pid2);
                pid3 = wait(&status);
                printf("Status de l'arret du fils %d %d\n", status, pid3);
            
     }

  }

}





}
