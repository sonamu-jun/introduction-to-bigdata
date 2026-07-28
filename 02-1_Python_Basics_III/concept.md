# Paths and Filesystem State

*A path can describe a location without changing the filesystem, while an explicit file operation creates observable state.*

## Learning Sequence

| Stage | Ordered Material |
| --- | --- |
| 1. Concepts | Paths and Filesystem State → Text and Structured File Round Trips → Debugging, Imports, and Runtime Tools |
| 2. Guided Examples | Paths → Files and Directories → Text Files → CSV and JSON → Debugging → Modules and Packages |
| 3. Integrated Practice | Sensor Log File Problem → Practice Notebook → Result Analysis |
| 4. Next Session | Structure Selection and Growth |

Optional extensions follow the core route: Binary Files and Image Files.

## Purpose

Separating path construction from file effects makes a notebook safer to rerun and easier to diagnose.

```text
Path construction -- no filesystem change
        |
        v
explicit read or write -- file state changes
        |
        v
existence, contents, and structure -- observed filesystem state
```

## Theory

A relative path is interpreted from the current working directory, while a resolved path shows an absolute location. Joining path components constructs a location; methods such as creating a directory or writing text create state. A reproducible lesson uses one exact target, displays the resulting tree or contents, and avoids accumulating new artifacts on repeated runs.

## Example Coverage

- Paths compares working, relative, and resolved locations without creating the proposed file.
- Files and Directories creates and inspects one bounded directory tree.
- The Sensor Log File constructs a path and writes one exact output artifact.

## Assumptions and Limits

Relative paths depend on the process working directory. Permissions, case sensitivity, and path separators vary across systems, although `pathlib` provides a consistent object-oriented interface. The guided notebooks confine writes to lesson output directories and do not model concurrent file access.

## References

- [Python 3.12 pathlib Documentation](https://docs.python.org/3.12/library/pathlib.html)
- [Python 3.12 os.path Documentation](https://docs.python.org/3.12/library/os.path.html)


# Text and Structured File Round Trips

*A round trip is complete only when saved data can be restored and its expected structure can be inspected.*

## Purpose

Plain text preserves characters and lines, CSV represents a flat table, and JSON represents nested values. Each format supports a different structure, but the evidence chain is the same: write or load a compact source, restore it, and compare the observed representation with the contract.

## Theory

Text mode requires an encoding; UTF-8 makes that choice explicit. Write mode replaces a target, append mode adds content at the end, and a `with ... as` block closes the file when the block finishes. CSV rows require a stable field order, while JSON preserves lists, dictionaries, numbers, text, Boolean values, and null values.

Binary mode represents raw bytes rather than decoded text. The optional binary and image lessons extend the round-trip idea, but later core lessons do not depend on the `pickle` module or image annotation.

## Example Coverage

- Text Files writes, appends, and restores a three-line artifact.
- CSV and JSON compares compact records after two structured round trips; its source is documented in CSV and JSON Sources.
- Optional extensions include Binary Files and Image Files.
- The Sensor Log File validates content restored from the saved artifact rather than from a separate in-memory copy.

## Assumptions and Limits

A successful round trip verifies representation, not the truth of the source data. Newline conventions can vary by platform, and `pickle` files should never be loaded from an untrusted source. Image pixels preserve a raster representation but do not by themselves establish semantic meaning.

## References

- [Python 3.12 Tutorial: Reading and Writing Files](https://docs.python.org/3.12/tutorial/inputoutput.html#reading-and-writing-files)
- [Python 3.12 csv Documentation](https://docs.python.org/3.12/library/csv.html)
- [Python 3.12 json Documentation](https://docs.python.org/3.12/library/json.html)


# Debugging, Imports, and Runtime Tools

*Debug with the smallest relevant program state and import reusable library names explicitly.*

## Purpose

Debugging is a cycle of reproducing a problem, inspecting the smallest relevant state, correcting one cause, and checking normal, boundary, and invalid inputs. Imports complement that cycle by making established library tools available under explicit namespaces.

## Theory

A traceback identifies the failing operation and call sequence. Validation should reject an input before an unclear downstream failure, while exception handling should cover only the expected error. A module is one Python file; a package organizes modules. Qualified names such as `statistics.mean` preserve the origin of an imported operation.

## Example Coverage

- Debugging shows intermediate state, focused failures, and labeled test cases.
- Modules and Packages uses namespaced standard-library tools for paths and a compact summary.
- The Sensor Log File validates restored fields after a bounded file effect.

Continue with the first guided notebook, Paths.

## Assumptions and Limits

Exception handling should not hide unrelated defects. A passing compact example establishes only the behavior that was checked, and an import does not guarantee that a third-party package has the expected version. These lessons use Python 3.12 and the standard library unless a notebook declares another dependency.

## References

- [Python 3.12 Tutorial: Errors and Exceptions](https://docs.python.org/3.12/tutorial/errors.html)
- [Python 3.12 Tutorial: Modules](https://docs.python.org/3.12/tutorial/modules.html)
- [Python 3.12 importlib Documentation](https://docs.python.org/3.12/library/importlib.html)
