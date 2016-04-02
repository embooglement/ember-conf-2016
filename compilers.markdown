# Compilers

### James Kyle
- Worked on [Babel](https://babeljs.io/)
- Thinks the only reason compilers are scary is because people don't teach them in an approachable way

### Compilers
- Transforms one (easily readable) language into a different (easily executed) language
- Source code doesn't directly map to a binary like assembly does
- Consists of three steps
  1. Parsing: abstract the code
  2. Transform: manipulates it
  3. Code Generation: converts to low level language

### Parsing
- Lexical and Syntactical analysis
- Breaks code into tokens and reformats them into an abstract syntax tree (AST)

### Transformation
- Manipulates the AST
- All nodes have defined values (strings, call expressions, numbers, etc.)
- This stage modifies the AST or creates a copy of it based on the target language
- Uses visitors
  - A visitor is a function that executes based on the type of node it interacts with
  - For instance, if it's a call expression it looks at its subtree to interpret the function

### Code Generation
- Takes the modified AST and stringifies it

### Example
https://github.com/thejameskyle/the-super-tiny-compiler
