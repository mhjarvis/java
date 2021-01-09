# ELEMENTARY PROGRAMMING

### THE MAIN METHOD:

```
1	public class HelloWorld {
2		public static void main(String[] args) {
3			...;
4		}
5	}
```

### SCANNER CLASS:

```
Scanner input = new Scanner(System.in);
int number = input.nextInt();
double doub = input.nextDouble();

next()							//reads a string that ends with a whitespace character
NextLine()						//read the entire line of text

nextByte(), nextShort(), nextInt(), nextLong(), nextFloat(), nextDouble(), next()		//token inputs
nextLine()											//line-based input

### CONSTANTS:

```
final datatype CONSTANTNAME = value;
```

casting:

```
int x = (int)6.32;		//x = 7
```

### OPERATORS:

==, !=, <, >, <=, >=, &&, ||, !<,!>, etc.

### INCREMENT/DECREMENT:

```
int x = 10;
int y = x++;			//x = 11, y = 10
x = 10;
int y = ++x;			//x = 11, y = 11
```

### CONTROL STATEMENTS:

The if-then statement:

```
if(test) {
  while(test) {
    for(initialize; test; increment) {
	  ...;
    ...;
    }
  }
}
```

The switch statement:

```
switch(expression) {
	case value1:
		statements;
	case value2:
		statements;
	default:			//default statement is optional
		statements;
}
```

OUTPUT STATEMENTS:

```
System.out.print(item);
System.out.println(item);		//prints appending a new line (\n)
```

### COMPILING/RUNNING:

```
javac ClassName.java		//compile code
java ClassName			//run code; calls the main() method from the file
```

### STRING METHODS:

```
char charAt(int i);				//character at position i
int indexOf(String s);				//index of first offurrence of s in the string; -1 means not found
int indexOf(String s, int start);		//index of first occurence of s at index start; -1 means not found	
int length();					//number of characters in string
String substring(int i);			//substring starting at index i
String substring(int i, int j);			//substring from index i to j - 1
String toLowerCase();				//returns copy in lowercase
String toUpperCase();				//returns copy in all uppercase
String trim();					//returns copy with whitespace removed from each end
```

### COMPARING STRINGS:

```
int compareTo(String s);			/*returns negative if string comes alphabetically before s, zero
                       			    if equal, and positive if alphabetically after*/
int compareToIgnoreCase(String s);		//ignores upper/lowercase
boolean equals(Object o);			//true if o is a string with the same contents as this string
boolean equalsIgnoreCase(String s)		//returns true if s has the same contents as this string, ignoring case

**							//use equals to test whether two strings have the same contents
**							//use compareTo() to compare string and test for alphabetical order
```

### ENHANCED FOR-LOOP:

```
for(type variable : collection) {...;}		//loops over each item in collection;

for(int item : data) {
	System.out.println(item);
}
```

### MATH OPERATIONS:

```
Math.pow(2, 3);					//2 to the power of 3
50 + (int)(Math.random() * 50)			//returns random int between 50 and 99
Math.random();					//random double between 0.0 and 1.0 (excluding 1.0);
System.currentTimeMillis() % 10			//generate random number
Math.abs(number);				//return the absolute value of number
```

Reversing a number:

```
n = 13
reverse = 0;
	
while(n != 0) {
	reverse = reverse * 10;
	reverse = reverse + n % 10;
	n = n / 10;
}
```

### MATH METHODS:

```
exp(x);						//return e raised to the power of x
log(x);						//return the natural logarigm of x
log10(x);					//return the base 10 logarithm of x
pow(a, b);					//returns a raised to the power of b
sqrt(x);					//returns the square root of x
```

Rounding:

```
ceil(x);					//x is rounded up to its nearest integer (returns a double)
floor(x);					//x is rounded down to its nearest integer (returns a double)
rint(x);					//x is rounded to its nearest integer
round(x);					//returns (int)Math.floor(x + 0.5) if x is float
                  //returns (long)Math.floor(x + 0.5) if x is a double
min/max/abs:						//works for int, long, float, double
max(4.4, 5.0);					//returns 5.0
min(3, 2);					//returns 2
abs(-2);					//returns 2
```

### ASCII

```
'0' to '9'						//code value 48 - 57; unicode value \u0030 - \u0039
'A' to 'Z'						//code value 65 - 90; unicode value \u0041 - \u005A
'a' to 'z'						//code value 97 - 122; unicode value \u0061 - \u007A
```

### HEXIDECIMAL:

```
Decimal	Hexidecimal
0	0
1	1
2	2
3	3
4	4
5	5
6	6
7	7
8	8
9	9
10	A
11	B
12	C
13	D
14	E
15	F
```

Converting hex to numbers:

```
int decimalValue = 0;
for(int i = 0; i < hex.length(); i++) {
  char hexChar = hex.charAt(i);
  decimalValue = decimalValue * 16 + hexCharToDecimal(hexChar);
}
```

### ESCAPE SEQUENCES:

```
\b							//backspace
\t							//tab
\n							//linefeed
\f							//formfeed
\r							//carriage return
\\							//backslash
\"							//double quote
```

### TESTING CHARACTERS:

```
if(ch >= 'A' && ch <= 'Z')			//test for upper case letter
if(ch >= 'a' && ch <= 'z')			//test for lower case letter
if(ch >= '0' && ch <= '9')			//test for numeric character

isDigit(ch);					//returns true if character is a digit
isLetter(ch);					//returns true if character is a letter
isLetterOrDigit(ch);				//letter or digit
isLowerCase(ch);				//test lower case
isUpperCase(ch);
toLowerCase(ch);				//returns lower case of character
toUpperCase(ch);				//returns upper case of character
```

string methods:

1	length();					//Returns the number of characters in this string.
2	charAt(index);					//Returns the character at the specified index from this string.
3	concat(s1);					//Returns a new string that concatenates this string with string s1.
4	toUpperCase();					//Returns a new string with all letters in uppercase.
5	toLowerCase();					//Returns a new string with all letters in lowercase.
6	trim(); 					//Returns a new string with whitespace characters trimmed on both sides.

comparing strings:

1	equals(s1);					//true if this string is equal to string s1
2	equalsIgnoreCase(s1);				//true if string is equal to s1; case sensitive
3	compareTo(s1);					//returns int greater than 0, equal to 0, less than 0 indicating whether
							//the string is greater than, equal to, or less than s1
4	compareToIgnoreCase(s1);			//comparison is case sensitive
5	startsWith(prefix);				//true if string starts with prefix
6	endsWith(suffix);				//""
7	contains(s1);					//true if s1 is a substring in this string

1	string == string1;				//only checks if both strings refer to the same object, not same contents
2	string.equals(string1);				//prefered method

substrings:

1	String message = "Welcome to Java";
2	String message = message.substring(0, 11);
3	//string now is "Welcome to ";

1	substring(beginIndex);
2	substring(beginIndex, endIndex);

finding character strings:

1	indexOf(ch);					//returns index of first occurence of ch; -1 if no math
2	indexOf(ch, fromIndex);				//finds occurence starting at fromIndex
3	indexOf(s);					//"" but for strings
4	indexOf(s, fromIndex);				//"" but for strings
5	lastIndexOf(ch);				//last occurence of character ch
6	lastIndexOf(ch, fromIndex);			//""
7	lastIndexOf(s);					
8	lastIndexOf(s, fromIndex);

convert string to number:

1	intValue = Integer.parseInt(intString);		//string into int
2	//example
3	String x = "23";
4	int y = Integer.parseInt(x);			
5	double dV = Double.parseDouble(doubleString);

formated printing:

1	printf();					

	%b						//boolean value
	%c						//character
	%d						//decimal integer
	%f						//floating-point number
	%e						//number in standard scientific notation
	%s						//string

1	int count = 5;
2	double amount = 45.56;
3	System.out.printf("count is %d and amount is %f", count, amount);

while loops:

1	while(...) {					//off-by-one error, use n - 1
2 		...;
3		System.out.println(...);
4	}

do-while loop:

1	do {						//loop executes at least ones before checking conditions
2		...;
3		...;
4	} while(...);

for loop:

1	for(int i = 0; i < n; i++) {
2		...;
3	};

BREAK / CONTINUE:
Using break immediately terminates a loop, while continue ends the current iteration and program control goes to the end of the loop body (i.e. continue breaks out of an iteration while the break keyword breaks out of a loop). 

while(num < 20) {
  number++;
  sum += number;
  if(sum >= 100) {
    break;						//exit loop and move to System.out statement
  }
}
System.out.println("The number is " + num);


while(num < 20) {
  number++;
  if(num == 10 || num == 11) {				//skip ensures 10 and 11 are not summed into the total
    continue;						//skip sum += num statement and return to while statement
  }
  sum += num;
}
System.out.println("The sum is " + sum);



*************************************************************************************************************************************
Chapter 6: Methods

DEFINING A METHOD:

modifier returnValueType methodName(list of parameters) {
  ...;
}

Example:

public static int addOne(int n) {
  n += 1;
  return n;
}

You can also envoke a methode (if public class) from other classes using the following syntax:

ClassName.methodName;

When a method is envoked, the system creates an activation record that stores parameters and variables for the method an dplaces the activation record in an area of memory known as a call stack (e.g. execution stack, runtime stack, machine stack, the stack). Once the method finishes, it returns to caller and the activation record is removed from the stack. Stored as a last-in, first out fashion. 

VOID METHOD:

The void method does not return a value. A 'return' statement is not needed, but it can be used to terminate the method and return to the method's caller. Example:

public static void printGrade(double score) {
  if(score < 0 || score > 100) {
    System.out.println("Invalid Score");
    return;
  }
}

OVERLOADING METHODS:

This allows you to name methods the same as long as the parameter lists are different. For example, instead of having a max method that accepts ints, you could have one that accepts doubles. The compiler will search out the method that is best fitting for the input. Generally, this makes reading a program easier. 

VARIABLE SCOPES:

The scope of a variable refers to the part of the program where the variable can be referenced. A variable defined inside a method is a local variable; it ends when the block that contains that variable ends. As long as variables are not nested in the same block, it can be declared multiple times. 

ABSTRACTION: 

This is achieved by seperating the use of a method from its implementation. Thus, a user can use a method without knowing how it is implemented. 
