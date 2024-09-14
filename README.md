# mathematica2julia

This is a source to source translator for converting Mathematica expressions into callable Julia code, adapted from the original Mathematica-to-Python translator at https://juanjose.garciaripoll.com/blog/converting-mathematica-to-python/ .

## Quick Start
Open `Export to Julia.nb` and evaluate the entire notebook. In the last cell, you can adapt the output to suit your needs. The script 

## Changes from Python version

- More optimal parentheses (much smaller code)
- Use ``Experimental`OptimizeExpression`` to "compile" the Mathematica expressions before conversion (repeated subexpressions are expressed in intermediate variables and order of operations is optimized) -- this results in much faster Julia code
- Many small adaptations for Julia syntax, function names, etc
- Default maximum line width increased
