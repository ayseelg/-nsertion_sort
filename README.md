# -nsertion_sort
// insertion_sort //insertionsort algoritması kullanılarak c dilinde 1 ile 100 arasındaki sayıları küçükten büyüğe doğru sıralayan kod bloğu
#include <stdio.h>
#include <stdlib.h>
#include <conio.h>
#include <time.h>

void insertionsort(int array[], int boyut)
{
	int i,j;
	int eleman;
	
	for (i=1; i<boyut; i++)
	{
		eleman = array[i];
		j = i-1;
		
		while (i>0 && array[j]>eleman)
		{
			array[j+1] = array[j];
			j--;
		}
		array[j+1] = eleman;
	}
	for(i=0;i<boyut;i++){
		printf("%d",array[i]);
	}
}

int main() {
	
	srand(time(NULL));
	int dizi_indeksi=100;
	int dizi[dizi_indeksi]={0};
	int i;
	int index = 0; 
	
	while(index < girilen_sayi_adedi)
	{
		int rastsayi = rand()%dizi_indeksi+1;
		int varmi = 0;
		
		for ( i=0; i<index; i++)
		{
			if(dizi[i] == rastsayi)
			{
				varmi = 1;
				break;
			}
		} 
		
		if(!varmi)
		{
			dizi[index] = rastsayi;
			index++;
		}
	}	
	
	for(i=0;i<dizi_indeksi;i++)
	{
		printf("%d - ",dizi[i]);
	}
	
	printf("\n");
	printf("\n");

	insertionsort(dizi,dizi_indeksi);

	return 0;
}
