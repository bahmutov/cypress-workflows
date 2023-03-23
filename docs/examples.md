# Examples

## Standard workflow

### End-to-end tests with an app start

```yml
name: ci
on: [push]
jobs:
  e2e:
    # https://github.com/bahmutov/cypress-workflows
    uses: bahmutov/cypress-workflows/.github/workflows/standard.yml@v1
    with:
      start: npm start
      wait-on: 'http://127.0.0.1:3000'
```

### End-to-end tests with a build and start steps

```yml
name: ci
on: [push]
jobs:
  e2e:
    # https://github.com/bahmutov/cypress-workflows
    uses: bahmutov/cypress-workflows/.github/workflows/standard.yml@v1
    with:
      build: npm run build
      start: npm start
      wait-on: 'http://127.0.0.1:3000'
```

### Component tests

```yml
name: ci
on: [push]
jobs:
  components:
    # https://github.com/bahmutov/cypress-workflows
    uses: bahmutov/cypress-workflows/.github/workflows/standard.yml@v1
    with:
      component: true
```
