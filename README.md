# ts-express
A ts-based express generator

# How to use ts-node in Express

### step 1: use express generator to make a new project

```
$ npm install express-generator -g
$ express --view=pug myapp
$ cd myapp && npm install

```

the project seems like:
```
├─bin
├─public
│  ├─images
│  ├─javascripts
│  └─stylesheets
├─routes
└─views
```

### step 2: install typescript in this project

```
$ npm install typescript --save
$ npm install ts-node --save
$ npm install @types/node --save
```

### step 3: set typescript configuration

```
$ npm install typescript -g
$ tsc --init
```

then you will see there is a new file named tsconfig.json.
here are my settings

```
{
  "compilerOptions": {
    "target": "es6",
    "module": "commonjs",
    "outDir": "dist",
    "declaration": true,
    "sourceMap": true,
    "noEmitOnError": true,
    "noUnusedLocals": false,
    "noImplicitReturns": true,
    "noFallthroughCasesInSwitch": true,
    "strictNullChecks": true,
    "noImplicitAny": false,
    "noUnusedParameters": false,
    "noImplicitThis": false,
    "allowUnusedLabels": true,
    "allowJs": true
  }
}
```

except tsconfig.json, in order to lint your ts code,you should create another file named tslint.json

```
{
  "rules": {
    "align": [
      true,
      "parameters",
      "arguments",
      "statements"
    ],
    "ban": false,
    "class-name": true,
    "comment-format": [
      true,
      "check-space"
    ],
    "curly": false,
    "eofline": false,
    "forin": false,
    "indent": [
      true,
      "spaces"
    ],
    "interface-name": false,
    "jsdoc-format": false,
    "label-position": true,
    "max-line-length": [
      false,
      180
    ],
    "member-access": false,
    "member-ordering": [
      true
    ],
    "no-any": false,
    "no-arg": true,
    "no-bitwise": true,
    "no-conditional-assignment": true,
    "no-consecutive-blank-lines": true,
    "no-console": [
      false
    ],
    "no-construct": false,
    "no-debugger": true,
    "no-duplicate-variable": true,
    "no-empty": false,
    "no-eval": true,
    "no-inferrable-types": false,
    "no-internal-module": true,
    "no-require-imports": false,
    "no-shadowed-variable": true,
    "no-string-literal": false,
    "no-switch-case-fall-through": true,
    "no-trailing-whitespace": false,
    "no-unused-expression": true,
    "no-use-before-declare": true,
    "no-var-keyword": true,
    "no-var-requires": false,
    "object-literal-sort-keys": false,
    "one-line": [
      true,
      "check-open-brace",
      "check-whitespace"
    ],
    "quotemark": [
      false
    ],
    "radix": false,
    "semicolon": false,
    "switch-default": false,
    "trailing-comma": [
      false,
      {
        "multiline": "never",
        "singleline": "never"
      }
    ],
    "triple-equals": [
      true
    ],
    "typedef": [
      true
    ],
    "typedef-whitespace": [
      true,
      {
        "call-signature": "nospace",
        "index-signature": "nospace",
        "parameter": "nospace",
        "property-declaration": "nospace",
        "variable-declaration": "nospace"
      }
    ],
    "variable-name": [
      true,
      "allow-leading-underscore",
      "ban-keywords"
    ],
    "whitespace": [
      true,
      "check-branch",
      "check-decl",
      "check-operator",
      "check-separator",
      "check-type"
    ]
  }
}
```

### step 4: it's time to change file ext to 'ts'

* change file ext of `app.js` and all js file below `routes/` to js

emm...
A picture with all types of error


### step 5: delete bin/www and move listen to app.ts
