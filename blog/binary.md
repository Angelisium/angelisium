# Bitwise manipulation

Memo of bitwise manipulation.   
The examples below will be done with uint8, for readability, the empty left bits
will be explicitly noted 0.   
For simplicity,  when I talk about a signed number,  I am talking about a signed
number in the [two's complement][u2c] representation.

```js
// Bitwise AND : &
// for any bit `a` and `b` equal to 1, the resulting bit will be 1 else 0.
1010 1010 & 0011 0011 = 0010 0010 // decimal : 170 & 51 = 34 (unsigned)

// vertical representation :
A: 1010 1010
B: 0011 0011
R: 0010 0010
```

```js
// Bitwise OR : |
// for any bit `a` or `b` equal to 1, the resulting bit will be 1 else 0.
1010 1010 | 0011 0011 = 1011 1011 // decimal : 170 | 51 = 187 (unsigned)

// vertical representation :
A: 1010 1010
B: 0011 0011
R: 1011 1011
```

```js
// Bitwise XOR : ^
// for any bit `a` equal to 1 but not equal to `b` and vice versa, the resulting
// bit will be 1 else 0.
1010 1010 ^ 0011 0011 = 1001 1001 // decimal : 170 & 51 = 153 (unsigned)

// vertical representation :
A: 1010 1010
B: 0011 0011
R: 1001 1001
```

```js
// Bitwise NOT : ~
// for any bit `a` equal to 1, the resulting bit will be 0 else 1.
~ 0101 0101 = 1010 1010 // decimal : ~ 85 = 170 = 85 (unsigned)
~ 0101 0101 = 1010 1010 // decimal : ~ 85 = -86 = 85 (signed)

// vertical representation :
A: 0101 0101
R: 1010 1010
```

```js
// Left shift : <<
// the resulting will be a `a` left shift of `b` 0 bits.
// excess bits shifted off are discarded.
1010 1010 << 0000 0011 = 0101 0000 // decimal : 170 << 3 =  80 (unsigned)
0000 1100 << 0000 0010 = 0011 0000 // decimal :  12 << 2 =  48 (unsigned)
```

```js
// Unsigned right shift : >>
// the resulting will be a `a` right shift of `b` 0 bits.
1010 1010 >> 0000 0001 = 0101 0101 // decimal : 170 >> 1 = 85 (unsigned)

// Signed right shift : >>
// the resulting will be a `a` right shift of `b` bits.
// the new bits take the value of the leftmost bit (the sign).
1111 1110 >> 0000 0001 = 1111 1111 // decimal :  -2 >> 1 = -1 (signed)
0111 1111 >> 0000 0110 = 0000 0001 // decimal : 127 >> 6 =  1 (signed)
```

```js
// Weakly typed languages use signed integers to represent all positive or
// negative integers. But sometimes it may be necessary to make a right shift by
// inserting some 0 independently to the sign.

// This is why these languages provide an "Unsigned right shift" operator.
// Unsigned right shift : >>>
1111 1110 >>> 0000 0001 = 0111 1111 // decimal :  -2 >>> 1 = 127 (signed)
0111 1111 >>> 0000 0110 = 0000 0001 // decimal : 127 >>> 6 =   1 (signed)

// PS: in my example, the result is 127 because I use int8 for readability.
// For example, in javascript the numbers are represented by int32 and you would
// have 2 147 483 647.
// For example, in powershell the numbers are represented by int64 and you would
// have 9 223 372 036 854 775 807.
```

[u2c]: https://en.wikipedia.org/wiki/Signed_number_representations#Two's_complement
