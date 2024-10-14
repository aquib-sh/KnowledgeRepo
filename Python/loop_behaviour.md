## Contrast in behaviour of Python for loops as compared to other languages


## Traditional `For` loop
Consider a traditional programming language like C, C++, Java

```c
#include <stdio.h>

int main() {
    for(int i = 0; i < 10; i++) {
        printf("%d", i);
        while (i < 5){
            i++;
        }
    }
    return 0;
}
// Outputs: 06789
```
When you write the above for loop and increment the variable with while, 
it would actually modify it in the next iteration of for.
Like on the next iteration the for loop will assign it 6 and not 1


## Python `For` Loops
```python
for i in range(0, 10):
    print(i)
    while (i < 5):
        i += 1

# Outputs: 0123456789
```
The for i in range syntax of Python essentially reassigns the i value on each iteration. 
So it takes the value from range and assigns to i instead of incrementing the value by comparing it to existing one.
