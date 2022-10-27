# Guide to setup prettier with eslint and airbnb style

- Create package.json file using

```
npm init
```

It will ask about
project name
version
description
entry point
etc
You may configure as you want

setup eslint using

```
npx eslint --init
```

Select 'To check syntax and find problems, and enforce code style' in How would you like to use ESLint? Option

then javascript modules

select options according to your project

however select 'use a popular style guide' when asked about 'How would you like to define a style for your project?'
then airbnb
select config file to be json

then install prettier

```
npm install eslint-config-prettier eslint-plugin-prettier prettier --save-dev
```

add the following to your prettier

```json
{
  "singleQuotes": true
}
```

.eslintrc.json file should look something like this

```json
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": ["airbnb-base", "prettier"],
  "overrides": [],
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["prettier"],
  "rules": {
    "prettier/prettier": "error",
    "quotes": ["error", "single"]
  }
}
```
