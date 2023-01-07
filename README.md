# tree-sitter-perl-better

This is Yet Another perl tree-sitter module.

## Getting Started Developing

To get started, install the dependencies for this repo

```bash
npm i
```

That should get you set up with tree-sitter's cli locally.

### Generating the Bindings

In this project, the generated C source code (stored in the `src` directory) is
.gitignored. In order to generate it, run

```bash
npx tree-sitter generate 
```

You'll need to do this after any changes to the grammar.

### Running the tests

Tests are stored in the `/test/corpus` directory, as txt files. A little reference on the
syntax can be found [here](https://tree-sitter.github.io/tree-sitter/creating-parsers#command-test).

You can run the tests with 

```bash
npx tree-sitter test
```

See the help output (`-h`) for that command for some more details on using the test
runner.

## Contributing

If you'd like to contribute, Pull Requests are welcome! The plan is to build the grammar
from the bottom up, from simple statements with solid code coverage, eventually building
up to full, complex syntax.

You can see a reference of the grammar's DSL [here](https://tree-sitter.github.io/tree-sitter/creating-parsers#the-grammar-dsl). It's fairly straigthforward, and makes for pleasant reading. It is stored in `grammar.js` at the root of this repo.

For subtle points in the grammar implementation, PLEASE leave comments. The extra bytes
spent on the comments in dev will go a long way in the big picture.
