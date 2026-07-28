# Values, Names, and Numeric Types

*Define each value by name, data type, and unit before calculating and reporting a result.*

## Learning Sequence

| Stage | Ordered Material |
| --- | --- |
| 1. Concepts | Values, Names, and Numeric Types → String Structure and Transformation |
| 2. Guided Examples | Printing Strings with Variables → Numeric Types and Math → Strings |
| 3. Integrated Practice | Campus Event Budget Problem → Practice Notebook → Result Analysis |
| 4. Next Session | Boolean Rules and Branching |

## Purpose

Python evaluates an expression and produces a value. A literal supplies a value directly, a variable gives that value a reusable name, and an arithmetic expression combines named values. `print()` then displays the calculated value.

```text
literal value -> variable name -> arithmetic expression -> labeled output
```

This sequence is the smallest version of a later data workflow: obtain values, name them, transform them, and communicate the result.

## Theory

Integers represent whole counts, while floating-point values represent finite approximations to real numbers. An operator should match the quantity being computed: addition combines amounts, multiplication applies a rate, division forms a quotient, and the remainder operator records what is left after whole groups are removed. Reassignment attaches a name to a new value; it does not revise values printed before the reassignment.

## Example Coverage

- Printing Strings with Variables shows literals, names, reassignment, and output order.
- Numeric Types and Math displays types, quotients, remainders, and rounded displays.
- The Campus Event Budget applies named numeric values to income, cost, and balance calculations.

## Assumptions and Limits

The guided values are small enough to inspect directly. Floating-point display is rounded for communication, but later calculations should retain the unrounded value. A descriptive variable name records meaning and units, but Python does not verify that the supplied real-world meaning is correct.

## References

- [Python 3.12 Tutorial: Numbers](https://docs.python.org/3.12/tutorial/introduction.html#numbers)
- [Python 3.12 Tutorial: Floating-Point Arithmetic](https://docs.python.org/3.12/tutorial/floatingpoint.html)


# String Structure and Transformation

*Inspect string order and boundaries, then compare the source string with each transformed result.*

## Purpose

A string is an ordered sequence of characters. Position-based selection shows its structure, string methods create cleaned or searched versions, and a formatted string places computed values beside labels.

## Theory

Indexing selects one character, while slicing selects a range without changing the original string. Cleaning methods return new strings, so preserving the source beside the transformed value makes the effect inspectable. A formatted string evaluates expressions inside braces and inserts their evaluated values into a larger string.

The distinction between source text and derived text matters later when table columns are cleaned: a transformation should produce a reproducible result without modifying the source value.

## Example Coverage

- Strings demonstrates indexing, slicing, cleaning, search, and formatting with printed source-and-result pairs.
- The Campus Event Budget combines an event name with numeric results in one concise report.

Continue with the first guided notebook, Printing Strings with Variables.

## Assumptions and Limits

Character positions describe Python's sequence representation, not the linguistic structure of every writing system. The examples use compact English text and do not address locale-aware sorting, normalization, or natural-language interpretation. Formatting improves communication but does not validate the underlying values.

## References

- [Python 3.12 Tutorial: Text](https://docs.python.org/3.12/tutorial/introduction.html#text)
- [Python 3.12 Tutorial: Formatted String Literals](https://docs.python.org/3.12/tutorial/inputoutput.html#formatted-string-literals)
