# ARRAYS

### CREATING ARRAYS AND ACCESS:

Once an array is created, its size is fixed. Arrays should have the same type of elements contained within them. You must declare a variable to reference the array and specify the array's element type. Example:

```
elementType[] arrayRefVar;							//preferred
```
or

```
elementType arrayRefVar[];							//not preferred
```

Declaring an array variable, creating an array, and assigning the reference of the array to the variable can be all done at once:

```
elementType[] arrayRefVar = new elementType[arraySize];
double[] myList = new double[10];						//example

myList[0] = 4.53;
myList[1] = 23.3;
myList[2] = 23.1;
...etc...

int length = myList.length;							//get the length (size) of an array
```

### INITIALIZING ARRAYS:

```
double[] myList = {1.4, 13.4, 12.4, 95.3};
System.out.println(myList.length);						//prints 4
System.out.println(myList[1]);							//prints 13.4
```

Initilization with random variables can be achieved as follows:

```
for(int i = 0; i < arr.length; i++) {
  arr[i] = Math.random() * 100;
}
```

Random shuffling of elements can be achieved by:

```
for(int i = 0; i < arr.length; i++) {
  int j = (int)(Math.random() * arr.length);
  double temp = arr[i];
  arr[i] = arr[j];
  arr[j] = temp;
}
```

### FOR-EACH LOOPS:

Foreach loops enables you to traverse the array sequentially wihtout having to use a index variable. To display all the elements of an array, we could for example:

```
for(int i: myArray) {
  System.out.println(i);
}
```


