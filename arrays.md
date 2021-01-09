# ARRAYS

### CREATING ARRAYS:

Once an array is created, its size is fixed. You must declare a variable to reference the array and specify the array's element type. Example:

```
elementType[] arrayRefVar;							//preferred
```
or

```
elementType arrayRefVar[];							//not preferred
```

Declaring an array variable, creating an array, and assigning the reference of the array to the variable can be all done at once:

elementType[] arrayRefVar = new elementType[arraySize];
double[] myList = new double[10];						//example

myList[0] = 4.53;
myList[1] = 23.3;
myList[2] = 23.1;
...etc...

int length = myList.length;							//get the length (size) of an array

INITIALIZING ARRAYS:

double[] myList = {1.4, 13.4, 12.4, 95.3};
System.out.println(myList.length);						//prints 4
System.out.println(myList[1]);							//prints 13.4


