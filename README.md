# Rocketseat biomejs config

I use [@rocketseat/eslint-config](https://github.com/Rocketseat/eslint-config-rocketseat) a lot, so I decided to create a [Biome](https://biomejs.dev/) version since I'm planning to migrate to it.

There are still a few features missing. You can find the rules I was able to implement and those that Biome currently supports in the [rules list below](#rules-list)

I'll try to keep this updated as much as possible, but I might miss something occasionally, so feel free to open an issue - it would really help a lot!

# Summary
- [Introduction](#rocketseat-biomejs-config)
- [Summary](#summary)
- [How to use](#how-to-use)
- [Rules list](#rules-list)
  - [Uses](#uses)
    - [Node](#node)
    - [React](#react)
    - [Next](#next)
  - [Legend](#legend)
  - [standard/](#standard)
  - [typescript-eslint/](#typescript-eslint)
  - [react](#react-1)
  - [react-hooks](#react-hooks)
  - [jsx-a11y](#jsx-a11y)
  - [eslint-plugin-next](#eslint-plugin-next)
- [Reference](#reference)


# How to use

First download the package as a dev dependency:

```
$ npm i -D rocketseat-biomejs-config

$ pnpm i -D rocketseat-biomejs-config

$ yarn add -D rocketseat-biomejs-config

$ bun add -d rocketseat-biomejs-config
```

Then create the file `biome.json` and add the following:

```
{
  "extends": ["rocketseat-biomejs-config/react|node|next.json"]
}
```


# Rules list
Below you can see the rules I found that Rocketseat uses.
It's mostly the plugin's recommended settings, with only a few exceptions.

## Uses
Which configuration each technology uses:

### Node:
- standard
- typescript-eslint/recommended

### React:
- react/recommended
- react-hooks/recommended
- standard
- typescript-eslint/recommended

### Next:
- eslint-plugin-next
- standard
- typescript-eslint/recommended

## Legend
- ❌: if it should be an error
- ⚠️: if it should be a warning
- ⚫: if it should be off

## standard/
- [x] no-var [⚠️]
- [ ] object-shorthand [❌, 'properties']
- [ ] accessor-pairs [❌]
  - setWithoutGet: true
  - enforceForClassMembers: true
- [ ] array-bracket-spacing [❌, 'never']
- [ ] array-callback-return [❌]
  - allowImplicit: false
  - checkForEach: false
- [ ] arrow-spacing [❌]
  - before: true
  - after: true
- [ ] block-spacing [❌, 'always']
- [ ] brace-style [❌, '1tbs']
  - allowSingleLine: true
- [ ] camelcase [❌]
  - allow: ^UNSAFE_
  - properties: never
  - ignoreGlobals: true
- [ ] comma-dangle [❌]
  - arrays: never
  - objects: never
  - imports: never
  - exports: never
  - functions: never
- [ ] comma-spacing [❌]
  - before: false
  - after: true
- [ ] comma-style [❌, 'last']
- [ ] computed-property-spacing [❌, 'never']
  - enforceForClassMembers: true
- [x] constructor-super [❌]
- [x] curly [❌, 'multi-line']
- [x] default-case-last [❌]
- [ ] dot-location [❌, 'property']
- [x] dot-notation [❌]
  - allowKeywords: true
- [ ] eol-last [❌]
- [x] eqeqeq [❌, 'always']
  - null: 'ignore'
- [ ] func-call-spacing [❌, 'never']
- [ ] generator-star-spacing [❌]
  - before: true
  - after: true
- [ ] indent [❌, 2]
  - SwitchCase: 1,
  - VariableDeclarator: 1
  - outerIIFEBody: 1
  - MemberExpression: 1
  - FunctionDeclaration: {}
    - parameters: 1
    - body: 1
  - FunctionExpression: {}
    - parameters: 1
    - body: 1 
  - CallExpression: {}
    - arguments: 1 
  - ArrayExpression: 1
  - ObjectExpression: 1
  - ImportDeclaration: 1
  - flatTernaryExpressions: false
  - ignoreComments: false
  - ignoredNodes: []
    - 'TemplateLiteral *'
    - 'JSXElement'
    - 'JSXElement > *'
    - 'JSXAttribute'
    - 'JSXIdentifier'
    - 'JSXNamespacedName'
    - 'JSXMemberExpression'
    - 'JSXSpreadAttribute'
    - 'JSXExpressionContainer'
    - 'JSXOpeningElement'
    - 'JSXClosingElement'
    - 'JSXFragment'
    - 'JSXOpeningFragment'
    - 'JSXClosingFragment'
    - 'JSXText'
    - 'JSXEmptyExpression'
    - 'JSXSpreadChild'
  - offsetTernaryExpressions: true
- [ ] key-spacing [❌]
  - beforeColon: false
  - afterColon: true
- [ ] keyword-spacing [❌]
  - before: true
  - after: true
- [ ] lines-between-class-members [❌, 'always']
  - exceptAfterSingleLine: true
- [ ] multiline-ternary [❌, 'always-multiline']
- [ ] new-cap [❌]
  - newIsCap: true
  - capIsNew: false
  - properties: true
- [ ] new-parens [❌]
- [x] no-array-constructor [❌]
- [x] no-async-promise-executor [❌]
- [ ] no-caller [❌]
- [x] no-case-declarations [❌]
- [x] no-class-assign [❌]
- [x] no-compare-neg-zero [❌]
- [x] no-cond-assign [❌]
- [x] no-const-assign [❌]
- [x] no-constant-condition [❌]
  - checkLoops: false
- [x] no-control-regex [❌]
- [x] no-debugger [❌]
- [ ] no-delete-var [❌]
- [x] no-dupe-args [❌]
- [x] no-dupe-class-members [❌]
- [x] no-dupe-keys [❌]
- [x] no-duplicate-case [❌]
- [ ] no-useless-backreference [❌]
- [x] no-empty [❌]
  - allowEmptyCatch: true
- [x] no-empty-character-class [❌]
- [x] no-empty-pattern [❌]
- [x] no-eval [❌]
- [x] no-ex-assign [❌]
- [ ] no-extend-native [❌]
- [ ] no-extra-bind [❌]
- [x] no-extra-boolean-cast [❌]
- [ ] no-extra-parens [❌, 'functions']
- [x] no-fallthrough [❌]
- [ ] no-floating-decimal [❌]
- [x] no-func-assign [❌]
- [x] no-global-assign [❌]
- [ ] no-implied-eval [❌]
- [x] no-import-assign [❌]
- [ ] no-invalid-regexp [❌]
- [x] no-irregular-whitespace [❌]
- [ ] no-iterator [❌]
- [x] no-labels [❌]
  - # [allow only on loops](https://biomejs.dev/linter/rules/no-confusing-labels/)
  - allowLoop: false
  - allowSwitch: false
- [x] no-lone-blocks [❌]
- [x] no-loss-of-precision [❌]
- [x] no-misleading-character-class [❌]
- [x] no-prototype-builtins [❌]
- [x] no-useless-catch [❌]
- [ ] no-mixed-operators [❌]
  - groups: []
    - ['==', '!=', '===', '!==', '>', '>=', '<', '<='],
    - ['&&', '||'],
    - ['in', 'instanceof']
  - allowSamePrecedence: true
- [ ] no-mixed-spaces-and-tabs [❌]
- [ ] no-multi-spaces [❌]
- [ ] no-multi-str [❌]
- [ ] no-multiple-empty-lines [❌]
  - max: 1
  - maxBOF: 0
  - maxEOF: 0
- [ ] no-new [❌]
- [ ] no-new-func [❌]
- [ ] no-new-object [❌]
- [x] no-new-symbol [❌]
- [x] no-new-wrappers [❌]
- [x] no-obj-calls [❌]
- [ ] no-octal [❌]
- [x] no-octal-escape [❌]
- [ ] no-proto [❌]
- [x] no-redeclare [❌]
  - builtinGlobals: false
- [x] no-regex-spaces [❌]
- [ ] no-return-assign [❌, 'except-parens']
- [x] no-self-assign [❌]
  - props: true
- [x] no-self-compare [❌]
- [x] no-sequences [❌]
- [x] no-shadow-restricted-names [❌]
- [x] no-sparse-arrays [❌]
- [ ] no-tabs [❌]
- [x] no-template-curly-in-string [❌]
- [x] no-this-before-super [❌]
- [x] no-throw-literal [❌]
- [ ] no-trailing-spaces [❌]
- [x] no-undef [❌]
- [x] no-undef-init [❌]
- [ ] no-unexpected-multiline [❌]
- [ ] no-unmodified-loop-condition [❌]
- [x] no-unneeded-ternary [❌]
  - defaultAssignment: false
- [x] no-unreachable [❌]
- [ ] no-unreachable-loop [❌]
- [x] no-unsafe-finally [❌]
- [x] no-unsafe-negation [❌]
- [ ] no-unused-expressions [❌]
  - allowShortCircuit: true
  - allowTernary: true
  - allowTaggedTemplates: true
- [x] no-unused-vars [❌]
  - args: 'none'
  - caughtErrors: 'none'
  - ignoreRestSiblings: true
  - vars: 'all'
- [x] no-use-before-define [❌]
  - functions: false
  - classes: false
  - variables: false
- [ ] no-useless-call [❌]
- [ ] no-useless-computed-key [❌]
- [x] no-useless-constructor [❌]
- [x] no-useless-escape [❌]
- [x] no-useless-rename [❌]
- [ ] no-useless-return [❌]
- [x] no-void [❌]
- [ ] no-whitespace-before-property [❌]
- [x] no-with [❌]
- [ ] object-curly-newline [❌]
  - multiline: true
  - consistent: true
- [ ] object-curly-spacing [❌, 'always']
- [ ] object-property-newline [❌]
  - allowMultiplePropertiesPerLine: true
- [x] one-var [❌]
  - initialized: 'never'
- [ ] operator-linebreak [❌, 'after']
  - overrides: {}
    - '?': 'before'
    - ':': 'before'
    - '|>': 'before' 
- [ ] padded-blocks [❌]
  - blocks: 'never'
  - switches: 'never'
  - classes: 'never'
- [x] prefer-const [❌]
  - destructuring: 'all'
- [ ] prefer-promise-reject-errors [❌]
- [x] prefer-regex-literals [❌]
  - disallowRedundantWrapping: true
- [ ] quote-props [❌, 'as-needed']
- [ ] quotes [❌, 'single']
  - avoidEscape: true
  - allowTemplateLiterals: false
- [ ] rest-spread-spacing [❌, 'never']
- [ ] semi [❌, 'never']
- [ ] semi-spacing [❌]
  - before: false
  - after: true
- [ ] space-before-blocks [❌, 'always']
- [ ] space-before-function-paren [❌, 'always']
- [ ] space-in-parens [❌, 'never']
- [ ] space-infix-ops [❌]
- [ ] space-unary-ops [❌]
  - words: true
  - nonwords: false
- [ ] spaced-comment [❌, 'always']
  - line: {}
    - markers: []
      - '*package'
      - '!'
      - '/'
      - ','
      - '='
  - block: {}
  - balanced: true
  - markers: []
    - '*package'
    - '!'
    - ','
    - ':'
    - '::'
    - 'flow-include'
  - exceptions: []
    - '*' 
- [ ] symbol-description [❌]
- [ ] template-curly-spacing [❌, 'never']
- [ ] template-tag-spacing [❌, 'never']
- [ ] unicode-bom [❌, 'never']
- [x] use-isnan [❌]
  - enforceForSwitchCase: true
  - enforceForIndexOf: true
- [x] valid-typeof [❌]
  - requireStringLiterals: true
- [ ] wrap-iife [❌, 'any']
  - functionPrototypeMethods: true
- [ ] yield-star-spacing [❌, 'both']
- [x] yoda [❌, 'never']
- [ ] import/export [❌]
- [ ] import/first [❌]
- [ ] import/no-absolute-path [❌]
  - esmodule: true
  - commonjs: true
  - amd: false
- [ ] import/no-duplicates [❌]
- [ ] import/no-named-default [❌]
- [ ] import/no-webpack-loader-syntax [❌]
- [ ] n/handle-callback-err [❌, '^(err|error)$']
- [ ] n/no-callback-literal [❌]
- [ ] n/no-deprecated-api [❌]
- [ ] n/no-exports-assign [❌]
- [ ] n/no-new-require [❌]
- [ ] n/no-path-concat [❌]
- [ ] n/process-exit-as-throw [❌]
- [ ] promise/param-names [❌]

## typescript-eslint/
- [ ] ban-ts-comment [❌]
- [x] no-array-constructor [❌]
- [ ] no-duplicate-enum-values [❌]
- [ ] no-empty-object-type [❌]
- [x] no-explicit-any [❌]
- [x] no-extra-non-null-assertion [❌]
- [x] no-misused-new [❌]
- [x] no-namespace [❌]
- [ ] no-non-null-asserted-optional-chain [❌]
- [x] no-require-imports [❌]
- [x] no-this-alias [❌]
- [x] no-unnecessary-type-constraint [❌]
- [x] no-unsafe-declaration-merging [❌]
- [ ] no-unsafe-function-type [❌]
- [ ] no-unused-expressions [❌]
- [x] no-unused-vars [❌]
- [ ] no-wrapper-object-types [❌]
- [x] prefer-as-const [❌]
- [x] prefer-namespace-keyword [❌]
- [ ] triple-slash-reference [❌]

## react/
- [ ] display-name [❌]?
- [x] jsx-key [❌]?
- [x] jsx-no-comment-textnodes [❌]?
- [x] jsx-no-duplicate-props [❌]?
- [x] jsx-no-target-blank [❌]?
- [ ] jsx-no-undef [❌]?
- [ ] jsx-uses-react [❌]?
- [ ] jsx-uses-vars [❌]?
- [x] no-children-prop [❌]?
- [x] no-danger-with-children [❌]?
- [ ] no-deprecated [❌]?
- [ ] no-direct-mutation-state [❌]?
- [ ] no-find-dom-node [❌]?
- [ ] no-is-mounted [❌]?
- [ ] no-render-return-value [❌]?
- [ ] no-string-refs [❌]?
- [ ] no-unescaped-entities [❌]?
- [ ] no-unknown-property [❌]
- [ ] prop-types [⚫]
- [ ] react-in-jsx-scope [⚫]
- [ ] require-render-return [❌]?
- [ ] self-closing-comp [❌]

## react-hooks/
- [x] rules-of-hooks [❌]
- [x] exhaustive-deps [❌]

## jsx-a11y/
- [x] alt-text [⚠️]
  - elements: []
    - img
  - img: []
    - 'Image'
- [x] aria-props [⚠️]
- [x] aria-proptypes [⚠️]
- [x] aria-unsupported-elements [⚠️]
- [x] role-has-required-aria-props [⚠️]
- [x] role-supports-aria-props [⚠️]

## eslint-plugin-next/
- [x] google-font-display [❌]
- [ ] google-font-preconnect [❌]
- [ ] inline-script-id [❌]
- [ ] next-script-ga [❌]
- [ ] no-assign-module-variable [❌]
- [ ] no-async-client-component [❌]
- [ ] no-before-interactive-script-outside-document [❌]
- [ ] no-css-tags [❌]
- [x] no-document-import-in-page [❌]
- [ ] no-duplicate-head [❌]
- [x] no-head-element [❌]
- [x] no-head-import-in-document [❌]
- [ ] no-html-link-for-pages [❌]
- [x] no-img-element [❌]
- [ ] no-page-custom-font [❌]
- [ ] no-script-component-in-head [❌]
- [ ] no-styled-jsx-in-document [❌]
- [ ] no-sync-scripts [❌]
- [ ] no-title-in-document-head [❌]
- [ ] no-typos [❌]
- [ ] no-unwanted-polyfillio [❌]

# Reference
[standard](https://github.com/standard/eslint-config-standard/blob/master/src/index.ts)
[typescript-eslint/recommended](https://github.com/typescript-eslint/typescript-eslint/blob/main/packages/eslint-plugin/src/configs/recommended.ts)
[eslint-plugin-react/recommended](https://www.npmjs.com/package/eslint-plugin-react)
[eslint-plugin-react-hooks](https://www.npmjs.com/package/eslint-plugin-react-hooks)
[eslint-plugin-jsx-a11y](https://www.npmjs.com/package/eslint-plugin-jsx-a11y)
[eslint-plugin-next](https://nextjs.org/docs/pages/building-your-application/configuring/eslint#eslint-plugin)
[Rules sources](https://biomejs.dev/linter/rules-sources/)
