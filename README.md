# graphql-ts-mode

This is a major mode based on the built in support for [tree-sitter][ts] in
Emacs, for editing [GraphQL][gql] documents.

[ts]: https://tree-sitter.github.io/tree-sitter/
[gql]: https://graphql.org/

## Installation

You will currently have to install from source. Clone this repository to
`~/.emacs.d/lisp/graphql-ts-mode/`, then configure it like this:

```elisp
(use-package graphql-ts-mode
  :ensure nil
  :load-path "lisp/graphql-ts-mode/"
  :mode ("\\.graphql\\'" "\\.gql\\'")
  :init
  (with-eval-after-load 'treesit
    (add-to-list 'treesit-language-source-alist
                 '(graphql "https://github.com/bkegley/tree-sitter-graphql"))))
```

Install the grammar using `treesit-install-language-grammar`.
