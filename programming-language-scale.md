Proposed scale for categorising programming languages, based on how mutch they abstract away the machine/machines it is executed on.


| Abstraction level | Characteristics | Examples |
| -  | - | - |
| 0| Direct or nearly direct mapping of language to native CPU instructions, no structured control flow, CPU architecture specific | Machine code, Assembly languages |
| 1  | Compiled, manual memory management, basic control flow (if, while, for), portable between CPU architectures | C|
| 2  | Compiled, manual memory management, with language/library support for automatic memory management. Language support for dynamic dispatch| C++, Rust, D, Ada|
| 2.5| Garbage collected, compiled to native code | Go, Haskell |
| 3  | Garbage collected, compiled to intermediate code, independent of CPU architecture, ahead of time and interpreted/just in time compiled at runtime | C#, Java
| 4  | Interpreted at runtime | Python, Javascript
| 5  | Directly integrated high level operations (email communication, database storage, building user interface), visual as oposed to text-based programming, executed on infrastructure inaccessible to the user |No-code/low-code platforms
