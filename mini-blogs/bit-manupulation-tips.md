---
layout: post
title: Bit manipulation
---

# Get a bit value from a specific position

We have this binary number `0b101011`, and we want to extract the bit value from
the 3rd position from the right side.


| Binary number         | 1   | 0   | 1   | 0   | 1   | 1   |
|-----------------------|-----|-----|-----|-----|-----|-----|
| Position from right   | 5   | 4   | 3   | 2   | 1   | 0   |


```text
  0b101011;
      ^ Bit to extract
```

The first thing we need is a mask. For position `3`, the mask would be
`0b001000`. We can generate the value using the left shift (`<<`).

```java
int bitMask = 1 << 3; // This will generate the number 0b001000
```

Using the Bitwise AND operator (`&`), we will get `0b001000` or `0b000000`,
which depends on the value of the bit. In the current example at position `3` 
for the number `0b101011`, we will get `0b001000`.

```text
  0b101011
& 0b001000
  ________
  0b001000
```

After we get the value from the AND operation, we only need to use the right
shift (`>>`) to bring the bit to the zeroth position.

```text
  0b001000 >> 3 = 0b000001
```

Sample code,

```java
int number = 0b101011;
int position = 3;

int bitMask = 1 << position;

int masked = number & bitMask;

// The result will have a value of 1 or 0 based on the bit value from the number
// at the specific position
int result = masked >> position;
```

# Set a bit value to a specific position

The steps we will follow to set a bit to a specific position,

 1. Set zero to the position in the number using AND operator with the bitmask
    complement
 2. And then set the desired bit value to the position using OR operator

Let's say our number is `0b100100`, and we will set bit `0` at position `2` from
the right.

```text
 0b100101
      ^ 2nd position to set 1
```

Generating mask,

```java
int bitMask = 1 << 2; // This will generate the number 0b000100
int bitMaskCompliment = ~bitMask; // This will generate number 0b...111011
```

Setting zero to the specific position of the number,

```text
  0b100101
& 0b111011
  ________
  0b100001
```

And then, we can just use the OR operator to set the desired bit value.

```text
  0b100001
| 0b000000 // We can get it by: bitValue<<2
  ________
  0b100001
```

Sample code,

```java
int position = 2;
int bit = 0;
int number = 0b100101;

int bitMask = 1 << position;
int bitMaskCompliment = ~bitMask;

int numberWith0AtThePosition = number & bitMaskCompliment;

int result = numberWith0AtThePosition | bit << position;
```
