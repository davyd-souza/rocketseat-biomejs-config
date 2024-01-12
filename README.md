## Base configs

- typescript-eslint /recommended
  - [ ] await-thenable
  - [ ] ban-ts-comment
  - [x] ban-types
  - [ ] no-duplicate-enum-values
  - [x] no-empty-interface
  - [x] no-explicit-any
  - [x] no-extra-non-null-assertion
  - [ ] no-floating-promises
  - [ ] no-for-in-array
  - [ ] no-import-type-side-effects
  - [x] no-misused-new
  - [x] no-namespace
  - [ ] no-non-null-asserted-optional-chain
  - [x] no-non-null-assertion
  - [ ] no-redundant-type-constituents
  - [x] no-this-alias
  - [x] no-unnecessary-type-arguments
  - [ ] no-unsafe-arguments
  - [ ] no-unsafe-assignment
  - [ ] no-unsafe-call
  - [x] no-unsafe-declaration-merging
  - [ ] no-unsafe-enum-comparison
  - [ ] no-unsafe-member-access
  - [ ] no-unsafe-return
  - [x] prefer-as-const
  - [ ] prefer-enum-initializers
  - [ ] restrict-plus-operands
  - [ ] restrict-template-expressions
- react/ recommended
  - [ ] display-name
  - [ ] jsx-key
  - [x] jsx-no-comment-textnodes
  - [x] jsx-no-duplicate-props
  - [x] jsx-no-target-blank
  - [x] jsx-no-undef
  - [x] no-children-prop
  - [x] no-danger-with-children
  - [ ] no-deprecated
  - [ ] no-direct-mutation-state
  - [ ] no-find-dom-node
  - [ ] no-is-mounted
  - [ ] no-render-return-value
  - [ ] no-string-refs
  - [ ] no-unescaped-entities
  - [ ] no-unknown-property
  - [ ] no-unsafe
  - [ ] prop-types
  - [ ] require-render-return
- react-hooks/recommended
  - [x] exhaustive-deps
  - [x] rules-of-hooks

## Environments

### Next

These are the configurations found on [eslint-config-rocketseat/next](https://github.com/Rocketseat/eslint-config-rocketseat/blob/main/next.js).

Currently there's no support for Next linting on Biome, but there's an [issue open](https://github.com/vercel/next.js/discussions/59347) regarding this problem.

- extends
  - [x] typescript-eslint /recommended
  - prettier /recommended
- rules
  - error
    - [x] prettier/ printWidth: 80
    - [x] prettier/ tabWidth: 2
    - [x] prettier/ singleQuote: true
    - [x] prettier/ trailingComma: all
    - [x] prettier/ arrowParens: always
    - [x] prettier/ semi: false
    - [x] prettier/ endOfLine: auto
    - [ ] react/ no-unkown-property
  - warn
    - [x] jsx-a11y/ alt-text /img
    - [x] jsx-a11y/ aria-props
    - [x] jsx-a11y/ aria-proptypes
    - [x] jsx-a11y/ aria-unsupported-elements
    - [x] jsx-a11y/ role-has-required-aria-props
    - [ ] jsx-a11y/ role-supports-aria-props

### Additional rules:

- noUselessFragments
- noUndeclaredVariables
- useHookAtTopLevel
- noDangerouslySetInnerHtml

### React

- extends
  - [x] react/ recommended
  - [x] react-hooks/recommended
  - [ ] standard
  - [x] typescript-eslint/recommended
  - [x] prettier/recommended
- rules
  - error
    - [x] prettier/ printWidth: 80
    - [x] prettier/ tabWidth: 2
    - [x] prettier/ singleQuote: true
    - [x] prettier/ trailingComma: all
    - [x] prettier/ arrowParens: always
    - [x] prettier/ semi: false
    - [x] prettier/ endOfLine: auto
    - [ ] react/ no-unkown-property
    - [ ] react/ self-closing-comp
    - [ ] react/ prop-types: off
    - [ ] react/ react-in-jsx-scope: off
  - warn
    - [x] jsx-a11y/ alt-text /img
    - [x] jsx-a11y/ aria-props
    - [x] jsx-a11y/ aria-proptypes
    - [x] jsx-a11y/ aria-unsupported-elements
    - [x] jsx-a11y/ role-has-required-aria-props
    - [ ] jsx-a11y/ role-supports-aria-props

### Node

- extends
  - [ ] standard
  - [x] typescript-eslint/recommended
  - [x] prettier/recommended
- rules
  - error
    - [x] prettier/ printWidth: 80
    - [x] prettier/ tabWidth: 2
    - [x] prettier/ singleQuote: true
    - [x] prettier/ trailingComma: all
    - [x] prettier/ arrowParens: always
    - [x] prettier/ semi: false

## Reference

[Linter rules from other sources](https://github.com/biomejs/biome/discussions/3#eslint-plugin-jsx-a11y)
