The purpose of Ratio is to do exact basic arithmetic operations on non integers.  
 
For example Java has no data type that can store 1/3 exactly.  
Another simple example is to add 0.1 ten times. The sum should be 1 but that is not what we get: 
```java 
double d = 0d; 
for (int i = 0; i < 10; i++) { 
    d += 0.1d; 
} 
System.out.println(d); 
 
Output: 
0.9999999999999999 
``` 
If you work with statistics or another field with somewhat extensive calculations 
with non integer numbers the errors can accumulate and cause incorrect results and/or behavior. 
 
Sample usage: 
```java 
Ratio ratio = Ratio.create(1, 3) 
        .times(1, 3) 
        .plus(1, 3) 
        .dividedBy(2) 
        .minus(1, 6); 
System.out.println("Str: " + ratio.toString()); 
System.out.println("Big dec: " + ratio.getBigDec()); 
System.out.println("Double: " + ratio.getDouble()); 
 
Str: 1/18 
Big dec: 0.05555555555555555555555555555555556 
Double: 0.05555555555555555 
```