# Building a C# analyzer (with tagging)

This documents contains some general guidance of building an analyzer.

## General

- Analyze _all_ submitted files, except tests/invalidator/editor/example/exemplar files
- Consider doing common/general analysis that applies to _all_ exercises
- Be aware of the trade-off between time spent building an analyzer vs writing comments on representations.
  Especially for exercises with few solutions, the effort of building an analyzer might outweight the benefits

## Concept exercises

- Consider using an analyzer to verify that the student uses the concepts the exercise is teaching

## Tags

- Higher-level tags (e.g. techniques or paradigms) are very helpful to students as a first filtering step
- For tags that are only really useful for a couple (or one) exercises, only output them for those exercise

## Compilation

If your language requires a compilation step, also consider these points:

- Consider compiling the solution to allow for higher fidelity, but be aware of the trade-offs (e.g. slower to run)
- Consider in-memory compilation (if possible), to improve performance

## Testing

- Have an extensive test suite
- Use golden tests to verify the behavior of the analyzer
- Consider having tests for each approach
  This will also help when linking an approach to tags in the approaches' `config.json`` file
