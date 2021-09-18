// Stone-Paper-Scissor-Game-C-PROJECTS
//Stone Paper Scissor Game C PROJECTS  with source code in only c language.
#include<stdio.h>
#include<stdlib.h>
#include<time.h>
#include<math.h>

int spcgame();

	
int main()
{
	char result;
	printf("\n******************************************\n\t||WELCOME IN SPCGAME||\n\n//*****/ STONE PAPER SCISSOR GAME /*****//\n\n\t\t    \n\nLets start!!\n\n******************************************\n");
	result=spcgame();
	if(result==0)
	{
		printf("\nplay again");
		/*printf("\nplease reply ✓ for play again \t else type . ");
		char k;
		scanf("%c",&k);
		if(k=='y')
		result=spcgame();
		else
		return 0;*/
	}
	else 
		printf("\n\n\t||** YEHH !! YOU WIN !! **||");
	return 0;
	
}
int spcgame()
{
	
	char user;
	printf("\nenter your choice -");
	printf("\nTips:-\nEnter s for STONE,\np for PAPER,\nc for SCISSOR-\t");
 
	
	scanf("%c",&user);
	//printf("\n%c",user);
	printf("\n\n\n");
	if(user=='s')
	printf("your choice =\tStone");
	else if(user=='p')
	printf("your choice =\tPaper");
	else if(user=='c')
	printf("your choice =\tScissor");
	else
	{
		printf("You entered wrong choice!!");
		return 0;
	}
	char* gt[3];
	gt[0]="s";
	gt[1]="p";
	gt[2]="c";
	char cpu;
    srand(time(NULL));
    cpu = *gt[rand() % 3];
   // printf("%c",random);
	printf("\n\n");
	if(cpu=='s')
	printf("computer's choice = Stone");
	else if(cpu=='p')
	printf("computer's choice = Paper");
	else 
	printf("computer's choice = Scissor");
	if(user==cpu)
	{
	printf("\n\nIt's Draw");
	return 0;
	}
	else if(user=='p'&&cpu=='s')
	{
		
		return 1;
	}
	else if(user=='c'&&cpu=='p')
	{
		
		return 1;
	}
	else if(user=='s'&&cpu=='c')
	{
		
		return 1;
	}
	else if(user=='s'&&cpu=='p')
	{
		printf("\n\nSorry you lose...");
		return 0;
	}
	else if(user=='c'&&cpu=='s')
	{
		printf("\n\nSorry you lose...");
		return 0;
	}
	else if(user=='p'&&cpu=='c')
	{
		printf("\n\nSorry you lose...");
		return 0;
	}
}
