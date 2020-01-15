#include <stdio.h>

void findUnion(int arr[][10], int q, int z, int x,int barr[20]);
void shiftSets(int arr[10][10],int q);
void findIntersection(int arr[10][10], int q, int carr[10],int w,int e);
void swapSets(int arr[10][10],int barr[10][10],int q, int w, int e);
void inputSets (int arr[10][10]);
int main (void)
{
	int q,i,a,count=1;
	int arr[10][10];
	int barr[10][10];
	
	while(count=1)
	{
		printf("\n");
	printf("***********\n0. Input sets\n1. Swap sets\n2. Find intersection\n3. Shift sets\n4. Find Union\n5. Quit\nEnter your choice (0,1,2,3,4,5):");
	scanf("%d",&q);
	

	if(q==0)
	{
		
		inputSets(arr);
	}
    else if(q==1)
	{
		int w,e;
		printf("Input set columns to swap: ");
	scanf("%d%d",&w,&e);
	  swapSets(arr,barr,10,w,e);
	
 
	
	}
	else if(q==2)
	{
		int carr[10],w,e;
		printf("Input set columns to compare: ");
	scanf("%d%d",&w,&e);

	  findIntersection(arr,10,carr,w,e);

	  for(a=0;a<10;a++)
	  {
	  if(carr[a]!=0)
		  printf("%d",carr[a]);
	  }
	}

	else if(q==3)
	{
	  shiftSets(arr,10);
	
	}

	else if(q==4)
	{
		int z,x;
		int barr[20];

		printf("Input 2 integers: ");
		scanf("%d%d",&z,&x);

	   findUnion(arr,10,z,x,barr);
	 
	
	}

	 


	else if(q==5)
	{
		count=0;
	printf("Bye!\n");
	break;
	
	}
	
	}
	return(0);	
}



void inputSets (int barr[10][10])
{
 int i,a;
 for(i=0;i<10;i++)
 {
	 printf("Enter 10 integers for set %d: ",i+1);
	 printf("\n");
 for(a=0;a<10;a++)
 {
 
 scanf("%d",&barr[a][i]);
}
  }

 for(i=0;i<10;i++)
 {
	 printf("\n");
 for(a=0;a<10;a++)
 {
 
 printf("%d ",barr[i][a]);
}
  }

 
}

void swapSets(int arr[10][10],int barr[10][10],int q, int w, int e)
{
	int i,a,c;
	
	printf("\n");
	for(i=0;i<q;i++)
	{
	 c = arr[i][w-1];
        arr[i][w-1] = arr[i][e-1];
        arr[i][e-1] = c;
}
	 
 
	

	  printf("Set %d and set %d swapped.\n",w,e);	
}


void findIntersection(int arr[10][10], int q, int carr[10],int w,int e)
{
	int a,i,c,count=0,k=0,ana=0;
	
	for(i=0;i<10;i++)
		carr[i]=0;
	

   for(i=0;i<10;i++)
   {
	   for(a=0;a<10;a++)
	   {
      if(arr[i][w]==arr[a][e])
	  {
	    carr[k]=arr[a][e];
		
	  }
	   
		  
   }
	   k++;
   }
   
   
		   printf("Intersection array: ");

   for(a=0;a<10;a++)
   {
   if(carr[a]==0 && carr[a+1]==0)
   {
	   printf("There is no intersection.\n");
	   break;
   }

   else 
   {
	   
   for(i=0;i<count;i++)
	printf("%d ",carr[i]);
   }
   }
   
   

}


void shiftSets(int arr[10][10],int q)
{
	int w,i,a,e;

  printf("Input a number: ");
  scanf("%d",&w);

  for(e=w;e>0;e--)
  {
  for(i=0;i<10;i++)
	{
	w=arr[i][9];
	for(a=9;a>=0;a--)
	{
		
		arr[i][a]=arr[i][a-1];
		
	}
	arr[i][0]=w;
	}

   
  }
  

  

  for(i=0;i<10;i++)
		{
			printf("\n");
			for(a=0;a<10;a++)
  printf("%d ",arr[i][a]);

}

  }


void findUnion(int arr[][10], int q, int z, int x,int barr[20])
{
	int i,a,k=0;
  
	
	for(a=0;a<q;a++)
	{
	   barr[k]=arr[a][z];
	k++;
	}
	
	
	
	
	k=10;

	for(i=0;i<q;i++)
	{
	barr[k]=arr[i][x];
	k++;
	}
	
	printf("Union of two sets: ");
	for(i=0;i<20;i++)
	printf("%d ",barr[i]);

	printf("\n");

}
