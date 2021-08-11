---
layout: post
title:  Esoteric Hello World
categories: [Python,Esoteric,Snippet]
excerpt: First attempt at writing some "esoteric" Python. Gathered some tips from the folks over in the Python Discord server. `lambda`, `__import__`, `getattr`, `__call__` are all very useful for creating code like this.
---

## Hello World
![](/images/eso.png)
```python
    (lambda _0x : getattr(getattr(__import__(_0x), '__import__')(_0x), 'getattr')(__import__('os'), ''.join(getattr(__import__(_0x), 'chr')(__________) for __________ in [101, 116, 105, 114, 119][::-1]))(1, bytes(''.join([str(chr(int(getattr(getattr(__import__(_0x), str(getattr(getattr(__import__(_0x), str(getattr(getattr(__import__(_0x), ''.join([getattr(__import__(_0x), 'chr')(_) for _ in [getattr(__import__(_0x), 'int')('0x68', 16), getattr(__import__(_0x), 'int')('0x65', 16), getattr(__import__(_0x), 'int')('0x78', 16)]])), '__name__'))), '__name__'))), '__call__')(ord(__)), 16))) for __ in [chr(100 + ___) for ___ in [int(_____) for ____, _____ in getattr({str(______ + getattr(__import__(''.join([getattr(__import__(_0x), 'chr')(_______) for _______ in [109, 111, 100, 110, 97, 114][::-1]])), ''.join([getattr(__import__(_0x), 'chr')(________) for ________ in [116, 110, 105, 100, 110, 97, 114][::-1]]))(0, 100000)): ______ for ______ in [-list(zip([90]))[0][0], list(zip([0]))[0][0], list(zip([8]))[0][0], list(zip([14]))[0][0], list(zip([11]))[0][0], list(zip([19]))[0][0], -list(zip([68]))[0][0], list(zip([11]))[0][0], list(zip([8]))[0][0], list(zip([8]))[0][0], list(zip([1]))[0][0], list(zip([4]))[0][0]]}, ''.join([getattr(__import__(_0x), 'chr')(_________) for _________ in [115, 109, 101, 116, 105][::-1]]))()][::-1]]]), encoding=getattr('', 'join')([___________[0] for ___________ in [____________ for ____________ in list(chr(105)) + list(chr(105)) + list(chr(99)) + list(chr(115)) + list(chr(97))][::-1]]))))(getattr('', 'join')([getattr(chr, '__call__')(getattr(int, '__call__')(_____________[0], 16)) for _____________ in sorted(list(zip(['0x62', '0x73', '0x75', '0x6e', '0x69', '0x74', '0x69', '0x6c'], ['0', '7', '1', '6', '2', '4', '5', '3'])), key = lambda ______________: ______________[1])]))
```

## Result
Believe it or not, the output is
```shell
hello world
```

## Notable Bits
Combining `getattr` and `__import__` can be a powerful way to quickly get the attribute of some module or class that hasn't been explicitly imported at the top.
```python
path = getattr(__import__('sys'), 'path')
```

Using `getattr` to get a reference to `__call__` is one method for assigning functions to variables or even lambdas.
```python
c = getattr(int, '__call__')
c('42')
```
