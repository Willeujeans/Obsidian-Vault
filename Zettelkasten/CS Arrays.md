Arrays are a simple storage type used in every language.

## Declaration
	int[] myArray;
	int[] myArray = {1,2,3};
	int[] myArray = new int[5];
	int[] myArray = new int[]{1,2,3};

## Finding Size
	myArray.Length;
## Passing Into arguments
	void PrintArray(int[] myArray){}
	PrintArray(yourArray);

## Looping
	ForEach:
	foreach(int element in numbers){
		Console.Write(element);
	}