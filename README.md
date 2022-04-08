# Comparative Programming Languages - CM30318

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

## Interpreted and Compiled

90. Read about the Java and Python bytecode systems, find out how they are generated and then executed
91. Any language can be interpreted/bytecoded/compiled. Why don't people use C interpreters?
92. Read about Cambridge Common Lisp, which compiles to C (mixed with bytecode)
93. The original C++ was actually a C transpiler, read about this
94. Read about Clojure, which compiles to Java, JavaScript and .NET
95. Read about Scala, the functional language that compiles to Java bytecode, JavaScript and machine code
96. Read about Kotlin, a static and implicitly typed, object-oriented, language that compiles to Java bytecode (for Android development)
97. Real about GraalVM that compiles Python, JavaScript, Ruby, R, LLVM and more to that Java VM
98. Look at a few languages and determine their usual method of execution
99. Considers the positives and negatives of doing this in each way (Java to machine code, C to bytecode etc...)
100. Many people think C is a simpler language, look at [this link](https://www.nayuki.io/page/summary-of-c-cpp-integer-rules)
101. Look at how C (and similar other languages) treats undefined behaviour
102. Look at how C (and similar other languages) treats implementation-defined behaviour

## Other Language Features

104. Think about what ```x = 42``` should return
105. What is the difference between returning two values, and one value which is a pair
106. Read about IEEE Not a Number (NaN)
107. Read about unchecked exceptions, such as RuntimeException in Java
108. How does Python handle errors
109. Look at thread local values, a concept related to dynamic scope
110. Look into the optimisations that modern JavaScript uses
111. How deep does Python allow function calls:

```python
def a(n):
    print(n)
    a(n + 1)
```

112. Why does Python not support tail-call optimisation
113. Read about tail-call optimisation in your favourite language
114. Why can't we do tail-call optimisation by hand for sibling calls
115. Read about the problems of TCO when a language has destructors
116. Read about the problems of TCO when a language has dynamic method calls
117. Read about how people have implemented TCO in Python, Java, etc...
118. Read about the Y-combinator in the lambda calculus
119. Read about which languages support first-class continuations in languages
120. Read about the *continuation passing* style of programming
121. Read about coroutines, functions that can return more than once
122. Read about the COMEFROM flow control construct

## Object Oriented Languages

123. Read about the categorisation: Single Responsibility Principle, Encapsulation, Abstraction, Minimal Coupling
124. Read about the SOLID principles
125. Compare SEAM, SOLID, and 'Encapsulation, Abstraction, Polymorhphism and Inheritance'
126. Look at java.lang.reflect
127. Think about the relationships between set theory, classes and objects, members and instances, subsets and subclasses
128. Determine the initial class hierarchy for your favourite languages
129. Compare multimethods with pair (and more generally), product types
130. Compare adding properties and behaviours dynamically to duck typing
131. Read about how ECMA 6 versions of JavaScript have classes, but they are just compiled into prototypes and closures
132. Read about C++20's concepts to constrain templates
133. Read about common lisp mixins
134. Read about how Rust uses traits extensively, with inheritance in it's traits, and no parent links in the instances
135. In a static single-inheritance language, dynamic lookup can be very fast. Read about dispatch tables/virtual method tables/vtables
136. Read about if your favourite language has support for choosing static and dynamic dispatch
137. Think about:

```java
Animal spot;
if (wombat() > 0) {
    spot = new Cat();
} else {
    spot = new Dog();
}
if (spot.hasTail()) {
    ...
}
```
should .hasTail() use the method from Cat, Dog, or Animal, and can this be done by the compiler or at runtime only?

138. Read about the problem that garbage collected languages have with destructors
139. Read about the Resource Acquisition Is Initialisation programming idiom to prevent resource leaks
140. Look up the CLOS algorithm and find some non-monotonic examples
141. Think about:
<img width="416" alt="Screenshot 2022-04-08 at 17 02 48" src="https://user-images.githubusercontent.com/75232368/162479778-a0e33da0-b84b-4625-8683-bc8f7ee5e6e4.png">

142. Read about C3 linearisation
143. Find out about how C++ addresses the diamond problem
144. Find out about how Eiffel addresses the diamond problem
145. What happens if you derive from two interfaces and they ask for different signatures for the same method name
146. Java 8 allows for default methods in interfaces, thus reintroducing the diamond problem. Find out how Java addresses this
147. Compare traits and mixins
148. **(Game developers):** Read about the entity-component system design pattern that favours composition over inheritance, used for at least two-decades in game engines
149. Look at ```type()```, ```dir()```, ```getattr()```, in Python
150. Think about the bootstrap problem of a MetaObject Protocol
151. Investigate the Metaobject class in Java
152. Investigate the metaobject system in Python
153. Investigate Joose, the JavaScript metaobject system
154. Investigate Moose, the Perl metaobject system

## The End

155. Read ["Energy Efficiency across Programming Languages"](https://doi.org/10.1145/3136014.3136031) 
156. Add languages to this chart:

<img width="294" alt="Screenshot 2022-04-08 at 17 10 13" src="https://user-images.githubusercontent.com/75232368/162480942-e110b368-a34b-49ef-803e-ff92cbd747d8.png">




