## Coding challenge - CodeWars - Multiples of 3 or 5

Source of the challenge: https://www.codewars.com/kata/514b92a657cdc65150000006

### Summary of challenge - Authored by ChatGPT

### Basic testcases

```c++
#include <gtest/gtest.h>
#include "../src/solution.h"

TEST(SolutionTest, DefaultCase) {
    EXPECT_EQ(solution(10), 23);
}
```

### Solution

solution.h

```c++
#ifndef SOLUTION_H
#define SOLUTION_H

#include <string>

int solution(int number);

#endif
```

solution.cpp

```c++
#include "solution.h"

using namespace std;

int solution(int number) {
    int result = 0;

    for (int i = 0; i < number; i++) {
        if (i % 3 == 0 || i % 5 == 0) {
            result += i;
        }
    }

    return result;
}
```
