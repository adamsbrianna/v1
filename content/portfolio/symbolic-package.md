+++
draft = false
image = ""
showonlyimage = false
date = "2016-11-05T19:50:47+05:30"
title = "Symbolic Algebra Package for OCaml"
weight = 4
+++

Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.
<!--more-->

* A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, 
*  in which roasted parts of sentences fly into your mouth.

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
2. Aliquam tincidunt mauris eu risus.

> The Big Oxmox advised her not to do so, because there were thousands of bad Commas, wild Question Marks and devious Semikoli, but the Little Blind Text didn't listen. She packed her seven versalia, put her initial into the belt and made herself on the way.

## Header Level 2

* Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
* Aliquam tincidunt mauris eu risus.

1. Vision
Our current vision for the system we’re building has remained fairly consistent with MS0. We still
want to build a useful symbolic algebra package for OCaml. The features we have in mind for this
system include:
•Symbolic expression representation (Referred to as Expressions)
•Expression LATEX output option
•Binding and evaluation of a symbolic expression
•Expression simplification according to some basic heuristics
•Single and multi-variable derivatives
•Basic vector calculus
•Maybe a toplevel, but the project is now evolving to something that just interfaces well with
OCaml and its toplevel.
This project is particularly useful because as of right now there isn’t a smooth package for working
with symbolic expressions in OCaml as Sympy handles symbolic algebra in Python.
2. Summary of progress
We created data structures to keep track of symbolic variables and symbolic expressions, a lexer and
parser to parse PEMDAS operations and recognize possible symbol tokens, the ability to print a
symbolic expression, combine two symbolic expressions to form a new expression, and simplification
by removing common factors.
In our demo, we demonstrated that a user could create symbols and expressions and that the symbol
engine could simplify an expression by trying to gather like terms and then factor the resulting
expression.
3. Activity breakdown
- Brianna Adams, bja49
•Develop the beginnings of formatting and evaluating expressions and operations to strings
•Write the beginnings of progress report
•Develop additional test cases
- Alex Coy, ac2456
•Implement a basic parser and lexer using OCamlyacc, Menhir, OCamllex, and examples given
as part of the course
•Develop the beginnings of the AST and couple it with the parser and lexer
•Make the tool more convenient to use and test by rebinding familiar infix operators in the
Engine namespace
1
Brianna Adams, bja49
Alex Coy, ac2456
Tito Maresca, tjm275
CS 3110 Final Project
MS1: Progress Report
Page 2 of 3
Spring 2020
•Copy and adapt scaffolding from previous assignments (i.e. the Makefile and configurations)
•Inspect all code (including code from other members), write failing test cases, and make the
tests pass.
- Tito Maresca, tjm275
•Develop the beginnings of the REPL (which admittedly got seriously refactored).
•Develop functions to factor expressions, do numerical operations, remove redundant zeros,
and add like terms
•Develop test cases for above functions.
•Write script for the demo and help develop example cases
__________________________________________________________

We still want to build a useful symbolic algebra package for OCaml. The features we have in mind
for this system include:
•Symbolic expression representation (Referred to as Expressions)
•Unambiguous representation of an expression
•Possibly ambiguous LATEX output option (pretty-printing)
•Binding and evaluation of a symbolic expression
•Expression simplification according to some basic heuristics
•Partial derivatives
•An example toplevel for others to build onto
This project is particularly useful because as of right now there isn’t a smooth package for working
with symbolic expressions in OCaml as Sympy handles symbolic algebra in Python.
2. Summary of progress
We refined our rudimentary simplification functions. The engine can collect like terms in expres-
sions, which is also useful with respect to simplification. We added some support for differentiation
and the functions sin, cos, tan, exp, and ln.
3. Activity breakdown
- Brianna Adams, bja49
•Pretty-printing doesn’t print as many unneeded parenthesis
•Both textual representation of expressions and LATEX output exists.
•Develop additional test cases
- Alex Coy, ac2456
•Improve the basic parser and lexer using OCamlyacc, Menhir, OCamllex, and examples given
as part of the course
•Confirm that the parser and lexer work for simple and intermediate cases
•Implement and test differentiation code
•Implement and test new unops such as sin, cos, tan, exp, and ln.
- Tito Maresca, tjm275
•Overhaul functions to do numerical operations, remove redundant zeros, and add like terms
to remove bugs and improve readability.
1
Brianna Adams, bja49
Alex Coy, ac2456
Tito Maresca, tjm275
CS 3110 Final Project
MS2: Progress Report
Page 2 of 2
Spring 2020
•Develop functions to determine what variables a function is dependent upon.
•Develop test cases for above functions.
•Write script for the demo and help develop example cases