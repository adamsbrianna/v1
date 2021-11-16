+++
draft = false
image = ""
showonlyimage = false
date = "2021-11-05T19:50:47+05:30"
title = "Symbolic Algebra Package for OCaml"
weight = 4
+++

•  Symbolic expression representation (Referred to as Expressions)
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

As of when this project was created of right now there isn’t a smooth package for working
with symbolic expressions in OCaml as Sympy handles symbolic algebra in Python. We created data structures to keep track of symbolic variables and symbolic expressions, a lexer and parser to parse PEMDAS operations and recognize possible symbol tokens, the ability to print a symbolic expression, combine two symbolic expressions to form a new expression, and simplification
by removing common factors. In our demo, we demonstrated that a user could create symbols and expressions and that the symbol
engine could simplify an expression by trying to gather like terms and then factor the resulting expression.

Develop the beginnings of formatting and evaluating expressions and operations to strings. Write the beginnings of progress report. Develop additional test cases. Implement a basic parser and lexer using OCamlyacc, Menhir, OCamllex, and examples given
as part of the course. Develop the beginnings of the AST and couple it with the parser and lexer. Make the tool more convenient to use and test by rebinding familiar infix operators in the Engine namespace. Copy and adapt scaffolding from previous assignments (i.e. the Makefile and configurations). Inspect all code (including code from other members), write failing test cases, and make the tests pass. Develop the beginnings of the REPL (which admittedly got seriously refactored). Develop functions to factor expressions, do numerical operations, remove redundant zeros,
and add like terms. Develop test cases for above functions. Write script for the demo and help develop example cases

Symbolic expression representation (Referred to as Expressions). Unambiguous representation of an expression. Possibly ambiguous LATEX output option (pretty-printing). Binding and evaluation of a symbolic expression. Expression simplification according to some basic heuristics. Partial derivatives. An example toplevel for others to build onto. This project is particularly useful because as of right now there isn’t a smooth package for working. with symbolic expressions in OCaml as Sympy handles symbolic algebra in Python.

The engine can collect like terms in expressions, which is also useful with respect to simplification. We added some support for differentiation
and the functions sin, cos, tan, exp, and ln. Pretty-printing doesn’t print as many unneeded parenthesis. Both textual representation of expressions and LATEX output exists. Develop additional test cases. Improve the basic parser and lexer using OCamlyacc, Menhir, OCamllex, and examples given as part of the course. Confirm that the parser and lexer work for simple and intermediate cases. Implement and test differentiation code. Implement and test new unops such as sin, cos, tan, exp, and ln. Overhaul functions to do numerical operations, remove redundant zeros, and add like terms to remove bugs and improve readability. Develop functions to determine what variables a function is dependent upon. Develop test cases for above functions. Write script for the demo and help develop example cases