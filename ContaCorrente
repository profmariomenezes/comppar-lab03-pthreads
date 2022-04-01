#include <pthread.h>   
#include <stdio.h>
#include <stdlib.h>         

void * deposito(int *id);
void * saque(int *id);

int i = 0, j = 0;

double saldo = 1000;

int main()
{
  pthread_t t1, t2;

  pthread_create(&t1, NULL, (void *)deposito, NULL);
  pthread_join(t1, NULL);
  pthread_create(&t2, NULL, (void *)saque, NULL);
  pthread_join(t2, NULL);

  printf("Saldo: %.2f",saldo);
}

void * deposito(int *id)
{
  double dep;

  while(j < 10)
    {
      dep = (double)(5);

      saldo += dep;
      printf("Depositado: %.2f\n", dep);
      
      j ++;
    }
};

void * saque(int *id)
{
  double debt;

  while (i < 10)
    {
      debt = (double)(2);  
      if (saldo - debt < 50)
	printf("Saldo insuficiente\n");
      else
	{
	  saldo -= debt;
	  printf("Saque: %.2f\n", debt);
	}
      i ++;
    }
}
