# Game-of-50-
This is a small number based game in C !!!

#include<stdio.h>
#include<conio.h>
void main()
{
	int opt,num,i,input=0;
	clrscr();

	restart:
	clrscr();
	printf("\nStart -> 1\nRules -> 2\nExit -> 3\n\nEnter : ");
	scanf("%d",&opt);


	switch(opt)
	{
		case 1 : goto start;
		case 2 : goto rules;
		case 3 : goto end;
		default : printf("\nInvalid Input !!");
	}


	start:

		num=0;
		printf("\nOkay Let's Start.");
		printf("\n\nI have to choose between %d - %d :-",num+1,num+10);

		num=6;
		printf("\nI choose -> %d",num);

		for(i=1;i<=4;i++)
		{

				printf("\n\nIt's your turn");
				printf("\nChoose a number between %d - %d -> ",num+1,num+10);
				scanf("%d",&input);

				if(input>=num+1 && input<=num+10)
				{
					printf("\n\nI have to choose between %d - %d :-",input+1,input+10);
					printf("\nI choose -> %d",num+11);
				}
				else
				{
					printf("\n\nInvalid Input!!");
					getch();
					goto restart;
				}
		      num=num+11;
		}


		printf("\n\nI choose 50 and I won !!");
		getch();
		goto restart;


	rules:
		printf("\nIt's too simple :- ");
		printf("\n\n1] This is a number based game.");
		printf("\n2] First the computer chooses a number [say : 8]");
		printf("\n3] Then it's the user's turn to choose a number but the condition is :- ");
		printf("\n4] The number must be in the range of :- \n\t (number choosen by me + 1 - number choosen by me + 10)");
		printf("\n5] Eg : I chose 8 => The number you choose must lie between 9 (8+1) - 18 (8+10)");
		printf("\n6] Then comes my turn and then yours and so onnn......");
		printf("\n7] One who gets the change to chose 50 and if he/she chooses 50 wins the game.");
		printf("\n\nSo lets start.......");

		getch();
		goto restart;

	end:

}
