# Boolean Rules and Branching

*Boolean expressions define the conditions used to select a program branch.*

## Learning Sequence

| Stage | Ordered Material |
| --- | --- |
| 1. Concepts | Boolean Rules and Branching → Collections and Iteration → Functions and Object State |
| 2. Guided Examples | Booleans and Comparisons → Lists → Dictionaries → Conditionals → Loops → Functions |
| 3. Integrated Practice | Weekly Study Summary Problem → Practice Notebook → Result Analysis |
| 4. Next Session | Paths and Filesystem State |

Optional extensions follow the core route: Tuples, Sets, Comprehensions, and Classes.

## Purpose

A comparison produces `True` or `False`. Boolean operators combine those results, and a conditional chooses one code path from an ordered set of alternatives.

```text
observed value -> comparison -> Boolean rule -> selected branch
```

This pattern later defines analytical cohorts: the rule must be inspectable before its selected rows or actions can be interpreted.

## Theory

Comparisons express boundaries such as equal to, less than, or at least. `and` requires both conditions, `or` requires at least one, and `not` reverses a truth value. In an `if`/`elif`/`else` chain, Python selects the first true branch, so ordering is part of the rule rather than a cosmetic choice.

## Example Coverage

- Booleans and Comparisons shows named simple and compound truth values.
- Conditionals compares valid, boundary, and invalid paths under an ordered rule.
- The Weekly Study Summary applies a declared condition to a compact week of observations.

## Assumptions and Limits

A branch implements a chosen rule rather than an objective truth. Changing a boundary or the order of overlapping conditions can change the output. The examples keep each condition small enough to read directly and do not use abbreviated expressions that would hide the decision.

## References

- [Python 3.12 Tutorial: More on Conditions](https://docs.python.org/3.12/tutorial/datastructures.html#more-on-conditions)
- [Python 3.12 Tutorial: if Statements](https://docs.python.org/3.12/tutorial/controlflow.html#if-statements)


# Collections and Iteration

*Select a collection that represents the required value relationship, then apply an operation to each element.*

## Purpose

Lists preserve sequence and permit change. Dictionaries attach keys to values. A loop visits collection elements in an explicit order and can accumulate a result without repeating nearly identical code.

```text
related values -> list or dictionary -> ordered visits -> accumulated result
```

## Theory

A list is appropriate when position and order matter; a dictionary is appropriate when a stable key identifies a field or record. Copying separates later mutations from the source collection. During iteration, the loop variable names the current element and an accumulator records the partial result after each visit.

Optional structures refine those relationships without becoming prerequisites. A tuple fixes a short positional record, a set emphasizes uniqueness and membership, and a comprehension compresses a simple transformation only after its expanded loop is understood.

## Example Coverage

- Lists shows selection, mutation, copying, sorting, and nesting.
- Dictionaries shows key-based retrieval, updates, and missing-key handling.
- Loops displays ordered visits, running totals, and stopping conditions.
- Optional extensions include Tuples, Sets, and Comprehensions.
- The Weekly Study Summary organizes and summarizes a compact synthetic log.

## Assumptions and Limits

The examples fit in memory and favor direct loops over compact syntax that has not yet been introduced. Collection choice should follow the relationship that must be preserved, not convenience alone. The optional structures can be skipped because later core lessons use lists and dictionaries explicitly.

## References

- [Python 3.12 Tutorial: Data Structures](https://docs.python.org/3.12/tutorial/datastructures.html)
- [Python 3.12 Tutorial: for Statements](https://docs.python.org/3.12/tutorial/controlflow.html#for-statements)



# Functions and Object State

*A stable interface separates a reusable operation from the values supplied on one particular call.*

## Purpose

A function gives a calculation a name, receives inputs through parameters, and returns a result to the caller. This boundary makes repeated work easier to test because the same operation can be applied to several explicit inputs.

## Theory

Parameters are local names defined by the function, arguments are the values supplied by a call, and `return` sends a result back without relying on printed text. A focused function should make its expected input and returned structure evident.

The optional class lesson extends this boundary by attaching state and behavior to a new kind of object. Use a class when several operations share the same state; later core lessons do not require a student-defined class.

## Example Coverage

- Functions returns a labeled dictionary from a reusable numeric summary.
- The optional Classes keeps related state and behavior together.
- The Weekly Study Summary packages a repeated weekly calculation behind one function interface.

Continue with the first guided notebook, Booleans and Comparisons.

## Assumptions and Limits

A function is reusable only while its input expectations and return meaning remain stable. Printed output is for inspection and cannot substitute for a returned value. The class example introduces organization rather than inheritance or large object-oriented designs.

## References

- [Python 3.12 Tutorial: Defining Functions](https://docs.python.org/3.12/tutorial/controlflow.html#defining-functions)
- [Python 3.12 Tutorial: Classes](https://docs.python.org/3.12/tutorial/classes.html)
