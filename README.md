# mathematica2julia

This is a source to source translator for converting Mathematica expressions into callable Julia code, adapted from the original Mathematica-to-Python translator at https://juanjose.garciaripoll.com/blog/converting-mathematica-to-python/ .

## Quick Start
Open `Export to Julia.nb` and evaluate the entire notebook. In the last section titled `Export to Julia (not Python)`, there are example translations of an expression using the optimized translator `OptimizeExpressionToPython[]` and the non-optimized translator `ToPython[]`. Note that, although many of the code internals use the word "Python", the output is of course actually Julia code.

## Changes from Python version

- More optimal parentheses (much smaller code)
- Use ``Experimental`OptimizeExpression`` to "compile" the Mathematica expressions before conversion (repeated subexpressions are expressed in intermediate variables and order of operations is optimized) -- this results in much faster Julia code, especially for big expressions
- Many small adaptations for Julia syntax, function names, etc
- Default maximum line width increased
