# population.c
#include <cs50.h>
#include <stdio.h>

int main(void)
// TODO: Prompt for start size

{
    int start;
    
    do
    
    {
        start = get_int("star population: ");
    }
    
    while (start < 9);

// TODO: Prompt for end size

    int end;
    do
    {
        end = get_int("end population: ");
    }
    while (end < start);
// TODO: Calculate number of years until we reach threshold
    int NumberOfYears = 0;
    int CurrentSize = start;

	while(CurrentSize < end)
	{
		int NewSize = CurrentSize + (int)(CurrentSize / 3) - (int)(CurrentSize / 4);
		CurrentSize = NewSize;
		NumberOfYears++;
	}
    // TODO: Print number of years
    {
    printf("Number of Years: %i", NumberOfYears);
    }
}
