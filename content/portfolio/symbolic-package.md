+++
draft = false
image = ""
showonlyimage = false
date = "2021-11-05T19:50:47+05:30"
title = "Symbolic Algebra Package for OCaml"
weight = 4
+++

•  Symbolic expression representation
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
•  Expression LATEX output option
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
•  Binding and evaluation of a symbolic expression
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
•  Expression simplification according to some basic heuristics
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
•  Single and multi-variable derivatives
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}
•  Basic vector calculus

<!--more-->
{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}

As of when this project was created, there is not a smooth package for working with symbolic expressions in OCaml as Sympy handles symbolic algebra in Python. A team and I created data structures to keep track of symbolic variables and symbolic expressions. A lexer and parser are used to parse PEMDAS operations and recognize possible symbol tokens, facilitate the ability to print a symbolic expression, combine two symbolic expressions to form a new expression, and simplification by removing common factors. The symbol engine could simplify an expression by trying to gather like terms and then factor the resulting expression.

A basic parser and lexer were implemented using OCamlyacc, Menhir, OCamllex. We developed the beginnings of an AST and coupled it with the parser and lexer. We made the tool more convenient to use and test by rebinding familiar infix operators in the Engine namespace. As apart of this project a REPL was developed to help with user experience. The functions created factor expressions, do numerical operations, remove redundant zeros, and add like terms. We developed test cases for the aforementioned functions and created example cases.

Symbolic expression representation (referred to as expressions) are represented unambiguously with the option of a LATEX output option. There's an example toplevel for others to build onto. The engine can collect like terms in expressions, which is also useful with respect to simplification. There is support for differentiation and the functions sin, cos, tan, exp, and ln. The LATEX option is able to remove unneeded parenthesis generated in th calculation process since both a textual representation of expressions and LATEX output exists. Redundant zeros are also removed, and like terms are added to remove bugs and improve readability.