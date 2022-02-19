#include <stdio.h>
#include <stdlib.h>


void checkWin(char a[3][3],char x_o,int* count);
void affichTable(char a[3][3]);

int main() {
    char choose;
    int check,count=0;
    char x_o;
    char a[3][3]={ {'1','2','3'} , {'4','5','6'} , {'7','8','9'} };
    //show the table
    int i,n;
    do{
    	system("cls");
    	affichTable(a);
		printf("\n  Choose X or O : ");
    	x_o=getche();
    	fflush(stdin);
	}while(x_o!='O' && x_o!='X');
	
	do{
		system("cls");
    	affichTable(a);
	  	printf("\n  --- '%c' it's Your Turn----",x_o);
     	printf("\n\n   Choose Place : ");
     	choose=getche();
     	fflush(stdin);
    	
    	switch ( choose ) {
    	case '1':
    		if(a[0][0]!='1') continue;
    		a[0][0]=x_o;
    		break;
    	case '2':
    		if(a[0][1]!='2') continue;
    		a[0][1]=x_o;
    		break;
    	case '3':
    		if(a[0][2]!='3') continue;
    		a[0][2]=x_o;
    		break;
    	case '4':
    		if(a[1][0]!='4') continue;
    		a[1][0]=x_o;
    		break;
    	case '5':
    		if(a[1][1]!='5') continue;
    		a[1][1]=x_o;
    		break;
    	case '6':
    		if(a[1][2]!='6') continue;
    		a[1][2]=x_o;
    		break;
    	case '7':
    		if(a[2][0]!='7') continue;
    		a[2][0]=x_o;
    		break;
    	case '8':
    		if(a[2][1]!='8') continue;
    		a[2][1]=x_o;
    		break;
    	case '9':
    		if(a[2][2]!='9') continue;
    		a[2][2]=x_o;
    		break;
    	default:
    		printf("\n\n   Attention!! Choose A Number From the Table...5(Press Any key)");
    		getch();
    		continue;
		} 
		system("cls");
		
		checkWin(a,x_o,&count);
		if(x_o=='O')
			x_o='X';
		else if(x_o=='X')
			x_o='O';
		
	}while(1);
 
 	system("pause");
	return 0;
} 


void checkWin(char a[3][3],char x_o,int* count){

	int r;
	affichTable(a);
		char win[]="Congratulation!\n\nthe winer is ";
	  	for( r=0;r<3;r++ ) 
	  	{
	  	
      		if( a[r][0]==x_o && a[r][1]==x_o && a[r][2]==x_o ) 
		  	{
      			printf("%s%c\n",win,x_o);
      			system("pause");
      			exit(0);
		  	}
	  	}
	  
	    for( r=0;r<3;r++ ) 
		{
	  	
      		if( a[0][r]==x_o && a[1][r]==x_o && a[2][r]==x_o ) 
			{
      			printf("%s%c\n",win,x_o);
      			system("pause");
      			exit(0);
		  	}
	  	}
	  
	  	if( a[0][0]==x_o && a[1][1]==x_o && a[2][2]==x_o ) 
	  	{
      		printf("%s%c\n",win,x_o);
      		system("pause");
      		exit(0);
		}
		  
		if( a[0][2]==x_o && a[1][1]==x_o && a[2][0]==x_o ) 
		{
      		printf("%s%c\n",win,x_o);
      		system("pause");
      		exit(0);
		}

		*count+=1;
		if(*count>8)
		{
			printf("  Finale! \n\n No One Was Win\n");
			system("pause");
			exit(1);
		}
}


void affichTable(char a[3][3]){
	int i,n;
	printf("\n");
	for(i=0;i<3;i++ ) 
		{	
    		printf("\t\t");
      		for(n=0;n<3;n++ ) 
			{
      			printf("%c\t",a[i][n]);
	  		}
	  		printf("\n\n");
		}
}
 
