# libcst Codemods

Variety of codemods for [libcst](https://github.com/Instagram/LibCST), that are helpful for automated refactoring/moderanization of Python code.

### Codemods

- ConstantToFinal: Add `Final` as an annotation to all constant variables (`UPPER_UNDERSCORE`).
  - Input:
    ```python
    FOO = 1
    BAR: int = 2
    ```
  - Output:
      ```python
      FOO: Final = 1
      BAR: Final[int] = 2
      ```
  - Flags: `-c` to include class constants, `-s` to run the codemod on stubs only.

  
