# Comparative Programming Languages - CM30319

# Excercises

## Language Families and Paradigms 

1. Read about Perl 6, and what made it such a large change to Perl 5 that they renamed the language to Raku
2. Compare:

```perl
$count = "99";
$count++;
```
and
```perl
$count = "cat";
$count++;
```

3. Read about PHP, a language derived from Perl for web pages
4. Look at asm.js, a small subset of JavaScript that limited the excess features of JavaScript
5. Is compiling from C++ to WebAssembly a good idea?
6. Why is Deep Learning called a dataflow approach?
7. Read about actors in multi-agent systems

## Memory Management

8. Find out how long it takes to create an object in Java
9. Find the overhead of calling ```malloc()``` and ```free()``` in C (or favourite language equivalent)
10. Read about concurrent garbage collection in Golang
11. Using Java for high-frequency trading in banks has problems due to garbage collection latency, read about this
12. Read about "GC coprocessor", an idea for hardware to support garbage collection
13. Look up ```sys.getrefcount()``` in Python
14. Python uses reference counting (runtime memory management), but also has a garbage collector, why?
15. **(Advanced)** The new M1 chip from Apple has special support in it's instruction set to support Swift's reference counting, read about this
16. A garbage collector can be added to C/C++ through libraries, is this the best of both worlds or the worst of both worlds?
17. Read about valgrind, Allinea, AddressSantizer and other runtime memory checking tools
18. Read about how clever compilers can use proofs to avoid the need for runtime checking
19. **(Advanced)** Read about affine and linear types
20. **(C+++ Specific)** Read about C++ move semantics vs compile-time tracking for memory management
21. **(Swift Specific)** Compare the idea of exclusivity enforcement on variables against compile-time tracking for memory management
22. How does Python handle scope and extent

## Types

23. Read about gradual typing that mixes static and dynamic types
24. Find out how much overhead have on each non-primitive value to encode its type
25. Compare ```sqrt(3/2)``` and ```sqrt(3.0/2.0)``` in C, then in Python2 and then in Python3
26. Consider the difference in converting int -> float a) preserving value, b) preserving bit pattern
27. **(Advanced)** Read about various types of casting in C++, ```reinterpret_cast```, ```static_cast``` etc...
28. Read the ECMA standard to discover the 10-step process required for addition
29. Consider the following with Python's duck typing:

```python
def two10(n):
    for i in range(10):
        n = 2*n
    return n
    
two10(1)
two10(1.0)
two10("1")
two10(two10)
```

30. Read about why Rust allows the compiler to infer types such as:

```rust
let vals: Vector<_> = something
```

31. Read about the extent of explicit vs implicit types in your favourite language
32. Why do static type checkers for Python (duckly typed) exist?
33. Read about Hindley-Milner type systems
34. Why is type inference being adopted in traditionally statically typed languages? (```auto``` in C++, ```var``` in Java, etc...)
35. Think about type inference in the presence of automatic type coercions (weak typing)
36. Read about generics in Java and Go
37. Understand why the negation of integers is fundamentally different to the negation of floats
38. Find out what overloading your favourite languages support
39. Valid Swift code:

```swift
func min<T: Comparable>(x: T, y: T) -> T {
    return y < x ? y : x
}
```
Read about generic specialization in Swift

40. Read about C#'s lazy monomorphisation
41. Read about how C supports polymorphism via ```void *```
42. Read about higher-kinded types and type classes
43. Read about early vs late binding for types
44. Read about how C++ uses templates to support a form of dependant types
45. Read about how Rust supports a simple kind of dependant types
46. Think about mixing higher-kind and dependant types, e.g. ```Vec<T, n>```
47. Read about sum and product types
48. Read about function types (lambdas)
49. Read about covariance and contravariance
50. Read about algebraic data types
51. Read about nominal and structural typing (determining type equalities)
52. Read about Curry-Howard Correspondance

## Variables & Evaluation

53. Why does the Haskell interpreter behave differently to the ghci compiler when given ```'x = x + 1'```
54. **(C)** Read about why C cannot support iterators
55. Look into Python iterators and enumerate
56. **(C++)** Read about how C++ has added support for iterators
57. Think about the code you need to write to add one to every element of a tree using a) for-loops, b) recursion and c) iterators
58. Read about maps, the functional version of iterators
59. **(Advanced)** Read about internal vs external iterators
60. Read about single-static assignment variables
61. Understand the difference between assignment and local variable binding
62. Look up *output parameter* and *inout parameter*s
63. Find a language where variables can be values
64. Fortran is call-by-reference, but allows ```func inc(2*m)```, find out what is happening here
65. **(Advanced)** Read about how lvalues are implicitly coerced/dereferenced/converted to rvalues on the right side of an assignment
66. **(Advanced)** Read about Algol 68
67. **(Advanced)** Read about rvalue references in C++
68. Compare call-by-name to inlining code
69. Read about alpha renaming
70. Compare call-by-name to variable capture in the lambda calculus
71. Read about Jensen's device
72. Read about fexprs in Lisp
73. Does call-by-reference need local variables to be renamed
74. Compare call-by-name with applicative order reduction and normal order reduction in the lambda calculus
75. Read about referential transparency (handling non-deterministic functions like Random in call-by-need languages)
76. Understand the difference between the & and && operators
77. What happens to the evaluation when you overload && in C++
78. Investigate extended boolean operators in Python and JavaScript
79. What is the difference between call-by-reference and using references in a call-by-value language
80. Is Java call-by-value or call-by-reference? Explain
81. What is Python's calling mechanism
82. C++ has native call-by-reference, read about using lambdas to mimic call-by-name
83. Read about generators and coroutines as a way languages can mimic lazy behaviour
84. Read about thunks as a way languages can mimic lazy behaviour
85. **(Advanced)** How do C++'s rvalue references differ from call-by-name
86. Read about how lazy evaluation allows you to describe infinite datastructures
87. Do you think that lazy evaluation is declarative
88. Do you think that lazy evaluation is dataflow
89. Go, Rust and Swift are new languages being developed, look at them and decide what is new and different (if anything)
