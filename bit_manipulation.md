## 1. Get the right most set bit:-

```javascript
n & -n;
```

#### How :-

**let check for 12**

```
             n = 00000000 00000000 00000000 00001100
            ~n = 11111111 11111111 11111111 11110011
    -n == ~n+1 = 11111111 11111111 11111111 11110100
        n & -n = 00000000 00000000 00000000 00000100
```

#### Conclusions :-

- if **n = 2<sup>x</sup>** then <span style="color:green">**n&-n == n**</span>
- <span style="color:green">n&-n</span> gives the maximum A such that
  - A = 2<sup>x</sup> or x Exponent of 2
  - n % A == 0

## 2. Check if number is a power of 2 :-

```javascript
x && !(x & (x - 1));
```

## 3. Fastest way to swap 2 numbers :-

```javascript
a ^= b;
b ^= a;
a ^= b;
// one liner
x = x ^ y ^ (y = x);
```

## 4. Check if a number has bits in an alternate pattern :-

```javascript
const allBitShouldBeSet = n ^ (n >> 1);
const allBitAreSet = (num) => (num & (num + 1)) == 0;
allBitAreSet(allBitShouldBeSet);
```

## 5. Check if a number is divisible by 3 :-

1. count the number of set bits at even positions. `even`
2. count the number of set bits at odd positions. `odd`
3. if `abs(even - odd) % 3 == 0` then number is divisible by 3.

## 7. Check the kth bit of number `num` :-

```javascript
(1 << k) | num;
```

## 6. Set the kth bit of number `num` :-

```javascript
(num >> k) & 1;
```
