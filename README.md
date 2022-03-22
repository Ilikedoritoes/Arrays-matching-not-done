#include <stdlib.h>
#include <stdio.h>
#define row 3
#define colume 3
#define _CRT_SECURE_NO_WARNINGS

int main()
{
	int x, y, one = 1;
	int sum;
	printf("please enter %d x %d numbers.\n", row, colume);
	int mtrx[row][colume];
	int mtrx2[row][colume];


	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			scanf_s("%d", &mtrx[x][y]);
		}
	}

	printf("please enter the second one!\n");

	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			scanf_s("%d", &mtrx2[x][y]);
		}
	}


	for (x = 0; x < row; x++)
	{
		for (y = 0; y < colume; y++)
		{
			
			if (mtrx[x][y] != mtrx2[x][y])
			{
				one = 0;
				break; // <----- stops the "for" Y loop 
			}
			
		}
		if (one == 0)
		break; //<--- stops a block of a loop from happening again (only the first one)
	}

	if (one == 1)
		printf("The two arrays match.");
	else
		printf("The arrays dont match.");



	system("pause");

}

//משימות:
// יש לקלוט 2 מטריצות ולהוכיח האם המטריצות זהות
// להדפיס האם המטריצות מכילות את אותם המספרים ( לא בהכרח אותו הסדר) <-- NOT DONE YET
